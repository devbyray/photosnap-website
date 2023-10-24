<template>
  <div class="mx-auto max-w-screen-2xl">
    <GridTextLeft classLeft="bg-black text-white" mobileReverse>
      <template v-slot:left>
        <h2
          class="text-[32px] leading-[40px] md:text-[40px] md:leading-[48px] uppercase font-semibold tracking-wide"
        >
          Create and share your photo stories.
        </h2>
        <p class="opacity-60 mb-6">
          Photosnap is a platform for photographers and visual storytellers. We
          make it easy to share photos, tell stories and connect with others.
        </p>
        <nuxt-link to="/" class="text-sm uppercase flex gap-4 items-center"
          ><span>Get an invite</span>
          <img
            src="/images/shared/desktop/arrow-white.svg"
            class="max-h-[12px]"
        /></nuxt-link>
      </template>
      <template v-slot:right>
        <picture>
          <source
            media="(min-width: 641px and max-width: 1024px)"
            srcset="/images/home/tablet/create-and-share.jpg"
          />
          <source
            media="(min-width: 1024px)"
            srcset="/images/home/desktop/create-and-share.jpg"
          />
          <img
            src="/images/home/mobile/create-and-share.jpg"
            alt="Create and share your photo stories."
            class="object-cover w-full h-full"
          />
        </picture>
      </template>
    </GridTextLeft>
    <GridTextRight>
      <template v-slot:left>
        <picture>
          <source
          media="(min-width: 641px and max-width: 1024px)"
            srcset="/images/home/tablet/beautiful-stories.jpg"
          />
          <source
            media="(min-width: 1025px)"
            srcset="/images/home/desktop/beautiful-stories.jpg"
          />
          <img
            src="/images/home/mobile/beautiful-stories.jpg"
            alt="Beautiful stories every time"
            class="object-cover w-full h-full overflow-hidden"
          />
        </picture>
      </template>
      <template v-slot:right>
        <h2
          class="text-[32px] leading-[40px] md:text-[40px] md:leading-[48px] uppercase font-semibold tracking-wide"
        >
          Beautiful stories <br />
          every time
        </h2>
        <p class="opacity-60 mb-6">
          We provide design templates to ensure your stories look terrific.
          Easily add photos, text, embed maps and media from other networks.
          Then share your story with everyone.
        </p>
        <nuxt-link to="/" class="text-sm uppercase flex gap-4 items-center"
          ><span>View the stories</span>
          <img src="/images/shared/desktop/arrow.svg" class="max-h-[12px]"
        /></nuxt-link>
      </template>
    </GridTextRight>
    <GridTextLeft mobileReverse>
      <template v-slot:left>
        <h2
          class="text-[32px] leading-[40px] md:text-[40px] md:leading-[48px] uppercase font-semibold tracking-wide"
        >
          designed for everyone
        </h2>
        <p class="opacity-60 mb-6">
          Photosnap can help you create stories that resonate with your
          audience. Our tool is designed for photographers of all levels,
          brands, businesses you name it.
        </p>
        <nuxt-link to="/" class="text-sm uppercase flex gap-4 items-center"
          ><span>View the stories</span>
          <img src="/images/shared/desktop/arrow.svg" class="max-h-[12px]"
        /></nuxt-link>
      </template>
      <template v-slot:right>
        <picture>
          <source
          media="(min-width: 641px and max-width: 1024px)"
            srcset="/images/home/tablet/designed-for-everyone.jpg"
          />
          <source
            media="(min-width: 1025px)"
            srcset="/images/home/desktop/designed-for-everyone.jpg"
          />
          <img
            src="/images/home/mobile/designed-for-everyone.jpg"
            alt="Designed for everyone"
            class="object-cover w-full h-full"
          />
        </picture>
      </template>
    </GridTextLeft>
  </div>
</template>
