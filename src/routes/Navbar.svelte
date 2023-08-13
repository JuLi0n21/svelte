<script>
  let isOpen = false;

  function toggleMenu() {
    isOpen = !isOpen;
  }
</script>

<nav class="bg-gray-800 p-4">
  <div class="flex items-center justify-between">
    <div class="flex items-center">
      <a href="#" class="text-white text-lg font-semibold">Logo</a>
    </div>
    <div class="md:hidden">
      <button class="text-white" on:click={toggleMenu}>
        <svg
          class="h-6 w-6 fill-current"
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 24 24"
        >
          <path
            fill-rule="evenodd"
            d="M3 5h18a1 1 0 0 1 0 2H3a1 1 0 0 1 0-2zm0 6h18a1 1 0 0 1 0 2H3a1 1 0 0 1 0-2zm0 6h18a1 1 0 0 1 0 2H3a1 1 0 0 1 0-2z"
          />
        </svg>
      </button>
    </div>
    <div class="hidden md:flex space-x-4">
      <a href="#" class="text-white">Home</a>
      <a href="#" class="text-white">About</a>
      <a href="#" class="text-white">Services</a>
      <a href="#" class="text-white">Contact</a>
    </div>
  </div>
  <div
    class="mt-2 md:hidden"
    class:visible={isOpen}
    class:hidden={!isOpen}
  >
    <a href="#" class="block text-white py-2">Home</a>
    <a href="#" class="block text-white py-2">About</a>
    <a href="#" class="block text-white py-2">Services</a>
    <a href="#" class="block text-white py-2">Contact</a>
  </div>
</nav>

<style>
  .visible {
    display: block;
  }

  .hidden {
    display: none;
  }
</style>
