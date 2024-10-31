<script>
export default {
  props: {
    className: {
      type: String,
      default: "",
    },
    title: {
      type: String,
    },
    description: {
      type: String,
    },
    link: {
      type: String,
    },
    type: Function,
    required: true,
  },
};
</script>

<template>
  <div
    :class="[
      'row-span-1 rounded-xl group/bento hover:shadow-xl transition duration-200 dark:shadow-none p-4 dark:bg-black dark:border-white/[0.2] bg-white border border-transparent justify-between flex flex-col space-y-4',
      className,
    ]"
    @click="link && link()"
  >
    <slot name="header"></slot>
    <div class="group-hover/bento:translate-x-2 transition duration-200">
      <div class="flex items-center">
        <slot name="icon"></slot>
      </div>
      <div class="font-bold text-neutral-200 mb-2 mt-2">
        {{ title }}
      </div>
      <div class="font-normal text-neutral-600 text-xs dark:text-neutral-300">
        {{ description }}
      </div>
    </div>
  </div>
</template>
