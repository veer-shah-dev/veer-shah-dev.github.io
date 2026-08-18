---
layout: page
permalink: /repositories/
title: repositories
description: Live synced public GitHub repositories for veer-shah-dev.
nav: true
nav_order: 3
---

<div class="repositories">
  <div class="row row-cols-1 row-cols-md-2 g-4 mb-4">
    <div class="col">
      <img class="img-fluid rounded z-depth-1 w-100" src="https://github-readme-stats.vercel.app/api?username=veer-shah-dev&show_icons=true&theme=default" alt="Veer Shah GitHub Stats" />
    </div>
    <div class="col">
      <img class="img-fluid rounded z-depth-1 w-100" src="https://github-readme-stats.vercel.app/api/top-langs/?username=veer-shah-dev&layout=compact&theme=default" alt="Top Languages" />
    </div>
  </div>

  <h3 class="font-weight-bold mb-3">Public GitHub Repositories</h3>
  <div id="github-repos-container" class="row row-cols-1 row-cols-md-2 g-4">
    <div class="col-12 text-center py-4">
      <div class="spinner-border text-primary" role="status">
        <span class="sr-only">Loading repositories...</span>
      </div>
    </div>
  </div>
</div>

<script>
document.addEventListener("DOMContentLoaded", function () {
  const container = document.getElementById("github-repos-container");
  const username = "veer-shah-dev";

  fetch(`https://api.github.com/users/${username}/repos?sort=updated&per_page=100`)
    .then(response => response.json())
    .then(repos => {
      if (!Array.isArray(repos) || repos.length === 0) {
        container.innerHTML = `<p class="text-muted">No public repositories found.</p>`;
        return;
      }
      
      // Filter out forks if desired, or keep all public non-fork repos
      const publicRepos = repos.filter(repo => !repo.fork);

      if (publicRepos.length === 0) {
        container.innerHTML = `<p class="text-muted">No public repositories found.</p>`;
        return;
      }

      container.innerHTML = publicRepos.map(repo => `
        <div class="col mb-4">
          <div class="card h-100 hoverable shadow-sm">
            <div class="card-body d-flex flex-column justify-content-between">
              <div>
                <h5 class="card-title font-weight-bold mb-2">
                  <a href="${repo.html_url}" target="_blank" rel="noopener noreferrer" class="text-decoration-none">
                    <i class="fa-brands fa-github mr-2"></i>${repo.name}
                  </a>
                </h5>
                <p class="card-text text-muted small">${repo.description || "No description provided."}</p>
              </div>
              <div class="d-flex justify-content-between align-items-center mt-3 pt-2 border-top">
                <span class="badge badge-secondary">${repo.language || "Code"}</span>
                <div class="small text-muted">
                  <span class="mr-3"><i class="fa-regular fa-star mr-1"></i>${repo.stargazers_count}</span>
                  <span><i class="fa-solid fa-code-branch mr-1"></i>${repo.forks_count}</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      `).join('');
    })
    .catch(error => {
      console.error("Error fetching GitHub repos:", error);
      container.innerHTML = `<p class="text-danger">Failed to load repositories dynamically.</p>`;
    });
});
</script>
