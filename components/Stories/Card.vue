<script setup lang="ts">
const props = defineProps({
  image: {
    type: String,
    required: true,
  },
  title: {
    type: String,
    required: true,
  },
  date: {
    type: String,
    required: true,
  },
  author: {
    type: String,
    required: true,
  },
  async: {
    type: Boolean,
    default: false,
  },
});

const hover = ref(false);
function toggleHover() {
  hover.value = true;
}
function leaveHover() {
  hover.value = false;
}

const imageMobile = `/images/stories/mobile/${props.image}.jpg`;
const imageDesktop = `/images/stories/desktop/${props.image}.jpg`;
</script>

<template>
  <div
    class="relative md:hover:-translate-y-6 transition"
    @mouseover="toggleHover"
    @mouseleave="leaveHover"
  >
    <nuxt-link to="/">
      <picture>
        <source media="(max-width: 640px)" :srcset="imageMobile" />
        <source media="(min-width: 1024px)" :srcset="imageDesktop" />
        <img
          :src="imageDesktop"
          alt="Beautiful stories every time"
          class="object-cover w-full h-full overflow-hidden"
          :loading="props?.async ? 'lazy' : null"
        />
      </picture>
      <footer
        class="absolute bottom-0 left-0 flex flex-col justify-end pb-8 px-8 gap-1 text-white w-full h-[350px] bg-gradient-to-b from-white/0 to-black/75"
      >
        <div class="flex flex-col">
          <span>{{ props?.date }}</span>
          <h3 class="text-[24px] leading-[32px] font-semibold tracking-wide">
            {{ props?.title }}
          </h3>
          <p class="mb-4">by {{ props?.author }}</p>
          <div class="w-full border-t border-[#979797] pt-4">
            <div class="flex justify-between items-center">
              <span class="uppercase text-sm">Read story</span>
              <img
                src="/images/shared/desktop/arrow-white.svg"
                alt="arrow right"
                class="max-h-[12px]"
              />
            </div>
          </div>
        </div>
      </footer>
    </nuxt-link>
    <TheGradient
      :class="{ 'opacity-0': !hover, 'opacity-0 md:opacity-100': hover }"
      class="absolute left-0 bottom-0 transition"
    />
  </div>
</template>
