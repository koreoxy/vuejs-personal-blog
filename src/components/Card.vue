<script setup>
import { ref } from "vue";
import dataBlog from "../data/data.json";
import BentoGrid from "./bento-grid/BentoGrid.vue";
import BentoGridItem from "./bento-grid/BentoGridItem.vue";
import Skeleton from "./bento-grid/Skeleton.vue";
import { useRouter } from "vue-router";

const blogs = ref(dataBlog);
const router = useRouter();

function detailBlog(id) {
  router.push({ name: "blog", params: { id } });
}
</script>

<template>
  <BentoGrid class="max-w-4xl mx-auto">
    <BentoGridItem
      v-for="blog in blogs"
      :key="blog.id"
      :link="() => detailBlog(blog.id)"
      :title="blog.title"
      :description="blog.description"
      :class="i === 3 || i === 6 ? 'md:col-span-2' : ''"
    >
      <template #header>
        <Skeleton />
      </template>
      <!-- <template #icon>
        <component :is="item.img" class="h-4 w-4 text-neutral-500" />
      </template> -->
    </BentoGridItem>
  </BentoGrid>
</template>
