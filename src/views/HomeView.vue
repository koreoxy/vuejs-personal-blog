<script setup>
import Card from "@/components/Card.vue";
</script>

<template>
  <main>
    <section
      class="flex flex-col md:flex-row gap-5 justify-between text-center items-center"
    >
      <div class="text-left basis-1/2">
        <h1>About Me</h1>
        <p>
          Hello! I',m Saifullah, but feel free to call me Iful or Ipul. I',m a
          22-year-old web development enthusiast from Meulaboh, West Aceh,
          Indonesia. With 3 years of academic background in Computer Science at
          Teuku Umar University,
        </p>
      </div>
      <div class="basis-1/4">
        <h1 class="font-bold text-5xl">Hello World Koreoxy</h1>
      </div>
      <div class="text-right basis-1/2">
        <div>
          <h1>Skills</h1>
          <p>
            my journey in programming began in 2020 with C++. Since then, my
            passion has evolved toward web development, where I now focus on
            building dynamic web applications using Next.js and Laravel.
          </p>
        </div>
      </div>
    </section>

    <section class="mt-10">
      <div>
        <h1>Latest Blog</h1>
        <hr class="mb-5" />
      </div>
      <Card />
    </section>
  </main>
</template>
