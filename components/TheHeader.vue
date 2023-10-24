<template>
  <header class="bg-white">
    <div class="header-wrapper">
      <div><TheLogo black /></div>
      <nav>
        <nuxt-link to="/stories">Stories</nuxt-link>
        <nuxt-link to="/features">Features</nuxt-link>
        <nuxt-link to="/pricing">Pricing</nuxt-link>
      </nav>
      <div>
        <Button>Get an invite</Button>
      </div>
    </div>
  </header>
</template>

<style scoped>
header {
  @apply py-4 h-[72px];
}
.header-wrapper {
  @apply mx-auto max-w-5xl flex justify-between items-center px-4 md:px-0;
}
nav {
  @apply flex gap-8 items-center;
}
nav a {
  @apply text-gray-500 uppercase text-sm;
}
nav a:hover {
  color: #000;
}
</style>
