<script>
    import "../app.css";
    import Navbarlink from "./Navbarlink.svelte"
    let src = "favicon.png";
    let links = [
    {name: "Home" , href:"/" }, 
    {name: "Products", href:"/about" },
    {name: "About Us", href:"/contact" },
    {name: "Contact", href:"/profile" },
    {name: "Cart", href:"/cart" }];

</script>

<nav class="flex justify-between" >
<div class="basis-1/5 flex-row">
    <a href="/">
    <img {src} alt="logo">
    </a>
</div>

<div class="basis-2/4 flex justify-evenly h-30">

 
    {#each links as link}
        <Navbarlink name={link.name} href={link.href} />
    {/each}
    </div>
</nav>

<slot />

<style lang="postcss">

</style>
