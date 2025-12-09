<script>
  export let mobileMenuOpen = false;
</script>

<header class="fixed top-0 left-0 right-0 z-50 bg-white/80 backdrop-blur-md border-b border-gray-100">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="flex justify-between items-center h-16">
      <!-- Logo -->
      <div class="flex-shrink-0 flex items-center gap-2 cursor-pointer">
        <div class="w-8 h-8 bg-black rounded-lg flex items-center justify-center text-white">
          <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="3" stroke-linecap="round" stroke-linejoin="round">
            <path d="M20 6L9 17l-5-5"/>
          </svg>
        </div>
        <span class="font-bold text-xl tracking-tight">UserJot</span>
      </div>

      <!-- Desktop Navigation -->
      <nav class="hidden md:flex space-x-8">
        <a href="#pricing" class="text-sm font-medium text-gray-600 hover:text-gray-900">Pricing</a>
        <a href="#help" class="text-sm font-medium text-gray-600 hover:text-gray-900">Help</a>
        <a href="#blog" class="text-sm font-medium text-gray-600 hover:text-gray-900">Blog</a>
        <a href="#product" class="text-sm font-medium text-gray-600 hover:text-gray-900">Product</a>
      </nav>

      <!-- CTA Button -->
      <div class="hidden md:flex items-center">
        <a href="#signin" class="inline-flex items-center px-4 py-2 border border-transparent text-sm font-medium rounded-full text-white bg-black hover:bg-gray-800 transition-colors">
          Sign In
          <svg class="ml-2 -mr-1 w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
          </svg>
        </a>
      </div>

      <!-- Mobile menu button -->
      <div class="md:hidden flex items-center">
        <button on:click={() => mobileMenuOpen = !mobileMenuOpen} class="text-gray-500 hover:text-gray-900 focus:outline-none" aria-label="Toggle mobile menu">
          <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
          </svg>
        </button>
      </div>
    </div>
  </div>

  <!-- Mobile Menu -->
  {#if mobileMenuOpen}
    <div class="md:hidden bg-white border-b border-gray-100">
      <div class="px-2 pt-2 pb-3 space-y-1 sm:px-3">
        <a href="#pricing" class="block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:text-gray-900 hover:bg-gray-50">Pricing</a>
        <a href="#help" class="block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:text-gray-900 hover:bg-gray-50">Help</a>
        <a href="#blog" class="block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:text-gray-900 hover:bg-gray-50">Blog</a>
        <a href="#product" class="block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:text-gray-900 hover:bg-gray-50">Product</a>
        <a href="#signin" class="block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:text-gray-900 hover:bg-gray-50">Sign In</a>
      </div>
    </div>
  {/if}
</header>
