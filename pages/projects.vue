<template>
  <div id="project">
    <desktop-navigation />

    <div class="container">
      <div class="row">
        <breadcrumb>
          <li class="breadcrumb-item">
            <nuxt-link to="/" class="text-decoration-none">Home</nuxt-link>
          </li>
          <li class="breadcrumb-item active" aria-current="page">Projects</li>
        </breadcrumb>

        <div class="col-md-12 text-start mb-2">
          <h4 class="text-primary">#Open Source</h4>
        </div>

        <ProjectLoading :loading="loading" />

        <!-- Open source project card -->
        <div
          :if="!loading"
          class="col-sm-12 col-md-6 col-lg-4 mb-4"
          v-for="project of openSourceProjects"
          :key="project.slug"
        >
          <ProjectCard :project="project" />
        </div>

        <div class="col-md-12 text-start mt-3 mb-2">
          <h4 class="text-primary">#Commercial</h4>
        </div>

        <ProjectLoading :loading="loading" />

        <!-- Commercial project card -->
        <div
          :if="!loading"
          class="col-sm-12 col-md-6 col-lg-4 mb-4"
          v-for="project of commercialProjects"
          :key="project.slug"
        >
          <ProjectCard :project="project" />
        </div>
      </div>
    </div>

    <Footer />

    <mobile-navigation />
  </div>
</template>

<script>
export default {
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
  data() {
    return {
      loading: true,
      openSourceProjects: [],
      commercialProjects: []
    }
  },
  methods: {
    async getProjectsData() {
      const listOpenSourceProjects = await this.$content("projects")
        .only(["title", "description", "color", "source", "demo", "tags","category"])
        .where({category: "open-source"})
        .sortBy("title", "asc")
        .fetch()
        .catch((err) => console.log(err))

      const listCommercialProjects = await this.$content("projects")
        .only(["title", "description", "color", "source", "demo", "tags","category"])
        .where({category: "commercial"})
        .sortBy("title", "asc")
        .fetch()
        .catch((err) => console.log(err))

        this.loading = false

        this.openSourceProjects = listOpenSourceProjects
        this.commercialProjects = listCommercialProjects
    },
  },
  created() {
    this.getProjectsData()
  },
}
</script>
