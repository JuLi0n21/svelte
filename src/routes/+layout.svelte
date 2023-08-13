<script>
    import "../app.css";
    import Navbarlink from "./Navbarlink.svelte"
    let src = "favicon.png";
    let links = [
    {name: "About me", href:"/about" },
    {name: "Projects", href:"/Projects" }];

</script>
<nav class="flex justify-between bg-slate-900">
    <div class="basis-1/5 flex-row h-10">
        <a href="/">
            <img {src} alt="logo" class="h-20">
        </a>
    </div>

    <div class="basis-2/4 flex h-20 justify-evenly">
    {#each links as link}
        <Navbarlink name={link.name} href={link.href} />
    {/each}
    </div>

</nav>

<slot />

<style lang="postcss">

</style>
