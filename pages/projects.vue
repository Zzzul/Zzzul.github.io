<template>
  <div id="home">
    <desktop-navigation />

    <div class="container">
      <div class="row mt-4 mb-4">
        <breadcrumb>
          <li class="breadcrumb-item">
            <nuxt-link to="/" class="text-decoration-none">Home</nuxt-link>
          </li>
          <li class="breadcrumb-item active" aria-current="page">Projects</li>
        </breadcrumb>

        <!-- Project card -->
        <div
          class="col-sm-12 col-md-6 col-lg-4 mb-4"
          v-for="project of projects"
          :key="project.slug"
        >
          <ProjectCard :project="project" />
        </div>

        <Footer />
      </div>
    </div>

    <mobile-navigation />
  </div>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const projects = await $content("projects", params.slug)
      .only(["title", "description", "color", "source", "demo", "tags"])
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
        content: "Projects open source & komersil yang sudah/sedang saya buat",
      },
    ],
  },
}
</script>
