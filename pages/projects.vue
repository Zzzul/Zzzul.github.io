<template>
  <div id="home">
    <desktop-navigation />

    <div class="container">
      <div class="row mt-2 mb-4">
        <breadcrumb>
          <li class="breadcrumb-item">
            <nuxt-link to="/" class="text-decoration-none">Home</nuxt-link>
          </li>
          <li class="breadcrumb-item active" aria-current="page">Projects</li>
        </breadcrumb>

        <!-- Desktop -->
        <div v-if="loading" class="d-none d-md-block">
          <div class="row mb-4">
            <div class="col-md-4">
              <div class="card bordered p-0">
                <div class="card-body p-5">
                  <marquee
                    behavior="alternate"
                    onmouseover="this.stop()"
                    onmouseout="this.start()"
                    direction="right"
                    >Loading..
                  </marquee>
                </div>
              </div>
            </div>

            <div class="col-md-4">
              <div class="card bordered p-0">
                <div class="card-body p-5">
                  <marquee
                    behavior="alternate"
                    onmouseover="this.stop()"
                    onmouseout="this.start()"
                    direction="right"
                    >Loading..
                  </marquee>
                </div>
              </div>
            </div>

            <div class="col-md-4">
              <div class="card bordered p-0">
                <div class="card-body p-5">
                  <marquee
                    behavior="alternate"
                    onmouseover="this.stop()"
                    onmouseout="this.start()"
                    direction="right"
                    >Loading..
                  </marquee>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Mobile -->
        <div v-if="loading" class="d-sm-block d-md-none">
          <div class="col-md-12">
            <div class="card bordered p-0">
              <div class="card-body p-5">
                <marquee
                  behavior="alternate"
                  onmouseover="this.stop()"
                  onmouseout="this.start()"
                  direction="right"
                  >Loading..
                </marquee>
              </div>
            </div>
          </div>
        </div>

        <!-- Project card -->
        <div
          v-else
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
      projects: [],
    }
  },
  methods: {
    async getProjectsData() {
      const listProjects = await this.$content("projects")
        .only(["title", "description", "color", "source", "demo", "tags"])
        .sortBy("createdAt", "desc")
        .fetch()
        .catch((err) => console.log(err))

      setTimeout(() => {
        this.loading = false

        this.projects = listProjects
      }, 1500)
    },
  },
  created() {
    this.getProjectsData()
  },
}
</script>
