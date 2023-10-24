<template>
  <footer class="bg-black">
    <div class="footer-wrapper">
      <div class="first-col">
        <div class="col-span-1 row-span-1 max-h-[16px] md:mb-4">
          <TheLogo />
        </div>
        <nav
          class="socialmedia "
        >
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

      <div class="third-col">
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
.footer-wrapper {
  @apply mx-auto max-w-6xl grid md:grid-cols-2 lg:grid-cols-5 gap-8 px-4 py-16 lg:px-0;
}
.first-col {
  @apply grid lg:grid-cols-2 lg:col-span-3 md:auto-rows-auto md:gap-4;
}
.third-col {
  @apply flex flex-col justify-between items-end lg:col-span-2 md:justify-between;
}
.third-col a {
  @apply text-white hover:underline;
}
.links {
  @apply flex gap-4 lg:flex-col items-start lg:col-start-2 lg:row-start-1 lg:row-span-2 md:row-start-2 md:flex-row md:mb-20;
}
.socialmedia {
  @apply flex gap-4 gap-4 items-center lg:col-start-1 lg:row-start-2 max-h-[20px] self-end;
}
nav a {
  @apply text-white hover:text-gray-500 uppercase text-sm;
}
/* nav a:hover {
  color: #000;
} */
</style>
