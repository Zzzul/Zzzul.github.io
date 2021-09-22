<template>
  <div id="home">
    <desktop-navigation />

    <div class="container">
      <div class="row mt-5">
        <breadcrumb>
          <li class="breadcrumb-item">
            <nuxt-link to="/" class="text-decoration-none">Home</nuxt-link>
          </li>
          <li class="breadcrumb-item active" aria-current="page">Projects</li>
        </breadcrumb>

        <!-- Card -->
        <div
          class="col-sm-12 col-md-6 col-lg-4 mb-4"
          v-for="project of projects"
          :key="project.slug"
        >
          <div
            class="card bordered-hover p-0"
            :style="{ 'background-color': project.color }"
          >
            <div class="card-body p-3">
              <p class="mb-1 mt-1" style="font-size: 13px">
                {{ project.title }}
                <br />
                <span style="font-size: 9px">{{ project.description }}</span>
              </p>
              <a
                :href="project.demo"
                target="blank"
                style="font-size: 11px"
                v-if="project.demo"
                >Demo</a
              >
              <a :href="project.source" target="blank" style="font-size: 11px"
                >Source</a
              >
            </div>
          </div>
        </div>

        <div class="col-md-12 text-center my-5">~~~</div>
      </div>
    </div>

    <mobile-navigation />
  </div>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const projects = await $content("projects", params.slug)
      .sortBy("createdAt", "desc")
      .fetch()
    return { projects }
  },
  head: {
    title: "Projects",
    meta: [
      {
        hid: "description",
        name: "description",
        content: "Projects Open Source yang saya buat",
      },
    ],
  },
  data() {
    return {
      loading: true,
    }
  },
  mounted() {
    setInterval(() => {
      this.loading = false
    }, 500)
  },
}
</script>
