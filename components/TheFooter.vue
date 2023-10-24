<template>
  <footer class="bg-black">
    <div class="mx-auto max-w-6xl py-16 px-4 flex flex-col items-center md:grid md:grid-cols-2 md:items-start">
      <div class="mb-12 md:mb-0 md:flex md:flex-col lg:grid lg:grid-cols-2">
        <div class="logo">
          <TheLogo />
        </div>
        <nav class="socialmedia">
          <nuxt-link class="inline-block" to="/"><IconsFacebook /></nuxt-link>
          <nuxt-link class="inline-block" to="/"><IconsYoutube /></nuxt-link>
          <nuxt-link class="inline-block" to="/"><IconsTwitter /></nuxt-link>
          <nuxt-link class="inline-block" to="/"><IconsPinterest /></nuxt-link>
          <nuxt-link class="inline-block" to="/"><IconsInstagram /></nuxt-link>
        </nav>
        <nav class="links">
          <nuxt-link to="/">Home</nuxt-link>
          <nuxt-link to="/">Stories</nuxt-link>
          <nuxt-link to="/features">Features</nuxt-link>
          <nuxt-link to="/pricing">Pricing</nuxt-link>
        </nav>
      </div>

      <div class="third-col flex flex-col gap-12 items-center md:justify-between h-full md:items-end">
        <div>
          <nuxt-link to="/" class="text-sm uppercase flex gap-4 items-center"
            ><span>Get an invite</span>
            <img
              src="/images/shared/desktop/arrow-white.svg"
              class="max-h-[12px]"
          /></nuxt-link>
        </div>
        <div class="text-gray-500">Copyright 2019. All Rights Reserved</div>
      </div>
    </div>
  </footer>
</template>

<style scoped>
.logo {
  @apply h-[16px] mb-6 md:mb-10;
}
.third-col a {
  @apply text-white hover:underline;
}
.socialmedia {
  @apply flex justify-center gap-4 mb-12 md:justify-start md:row-start-3 md:order-last md:mb-0;
}
.links {
  @apply flex flex-col items-center gap-4 mb-24 md:flex-row md:mb-16 lg:flex-col lg:items-start lg:mb-2 lg:row-span-3;
}
nav a {
  @apply text-white hover:text-gray-500 uppercase text-sm;
}
</style>
