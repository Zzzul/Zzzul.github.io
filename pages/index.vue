<template>
  <div id="home">
    <desktop-navigation />

    <div class="container">
      <div class="row mt-4 mb-5">
        <breadcrumb>
          <li class="breadcrumb-item active text-secondary" aria-current="page">
            Home
          </li>
        </breadcrumb>

        <!-- Card -->
        <div class="col-md-12" id="main-content">
          <div class="card bordered">
            <div class="card-body p-5 text-center">
              <h5 class="mb-3">Hai,</h5>
              <h3 class="mb-3">Saya Mohammad Zulfahmi</h3>

              <h4 class="mb-4">Web Developer</h4>

              <a href="#" class="text-decoration-none" target="blank">
                <img
                  src="~/assets/img/social-media/fb.jpg"
                  class="mb-2 socmed-icon"
                  alt="facebook logo"
                />
              </a>

              <a
                href="https://www.instagram.com/zzzzzul/"
                class="text-decoration-none"
                target="blank"
              >
                <img
                  src="~/assets/img/social-media/ig.jpg"
                  class="mb-2 socmed-icon"
                  alt="Instagram logo"
                />
              </a>

              <a
                href="https://github.com/Zzzul"
                class="text-decoration-none"
                target="blank"
              >
                <img
                  src="~/assets/img/social-media/github.jpg"
                  class="mb-2 socmed-icon"
                  alt="github logo"
                />
              </a>

              <a href="#" class="text-decoration-none" target="blank">
                <img
                  src="~/assets/img/social-media/medium.jpg"
                  class="mb-2 socmed-icon"
                  alt="medium logo"
                />
              </a>

              <a
                href="https://www.linkedin.com/in/muhammad-zulfahmi/"
                class="text-decoration-none"
                target="blank"
              >
                <img
                  src="~/assets/img/social-media/linkedin.jpg"
                  class="mb-2 socmed-icon"
                  alt="linkedin logo"
                />
              </a>

              <a
                href="mailto:mzulfahmi807@gmail.com"
                class="text-decoration-none"
                target="blank"
              >
                <img
                  src="~/assets/img/social-media/gmail.jpg"
                  class="mb-2 socmed-icon"
                  alt="gmail logo"
                  width="60px"
                />
              </a>
            </div>
          </div>
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
    title: "Home",
    meta: [
      {
        hid: "description",
        name: "description",
        content: "Personal website saya",
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
