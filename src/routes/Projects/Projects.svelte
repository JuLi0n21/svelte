<script>
import Githubrepo from './Githubrepo.svelte';

 const getrepos = async() => {
     const res = await fetch("https://api.github.com/users/JuLi0n21/repos");
  const data = await res.json();
  if(res.ok) {
    return data;
  }
  throw data;
 
 }

</script>

<div class="container mx-auto mt-8 ">
  <h2 class="text-3xl font-semibold mb-4">Projects</h2>
  <p>Some Projects i worked on, in my free time and for uni.</p>
  <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-4">
   {#await getrepos()}
    <p> ...Loading </p>
   {:then data} 
    {#each data as repository (repository.id)}
      <Githubrepo {repository}/>
    {/each}
    {:catch error}
	<p style="color: red">{error.message}</p>
   {/await}
  </div>
</div>
