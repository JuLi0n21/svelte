<script>
  export let repository;

  const repoName = repository.name;
  const repoUrl = repository.html_url;
  const description = repository.description;
  const language = repository.language;
  const stargazersCount = repository.stargazers_count;
  const forksCount = repository.forks_count;
  const openIssuesCount = repository.open_issues_count;
  
</script>

<div class="github-project rounded-ld hover:border-fuchsia-400 border-4 border-gray-800 rounded-lg bg-gray-700 p-4 hover:-translate-y-1 hover:scale-105 inline-block relative">
  <a href="https://www.codefactor.io/repository/github/juli0n21/{repoName}" class="absolute top-2 right-0">
      <img src="https://www.codefactor.io/repository/github/juli0n21/{repoName}/badge" alt="CodeFactor" onerror="this.style.display='none'"/>
  </a>
  <a href={repoUrl} target="_blank" rel="noopener noreferrer" class="absolute top-0 left-4">{repoName}</a>

  {#if description != null}
  <p class="mt-4">{description}</p>
  {:else}
  <p class="mt-4">No description</p>
  {/if}
  {#if language != null}
      <p>Language: {language}</p>
  {:else}
      <p>Language: unknown</p>
  {/if}
  
  <p>Stars: {stargazersCount} | Forks: {forksCount} | Issues: {openIssuesCount}</p>
</div>


<style>
p {
  color: seashell;
}

a {
  color: limegreen;
}
</style>