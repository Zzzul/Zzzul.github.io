<template>
  <div id="home">
    <desktop-navigation />

    <div class="container">
      <div class="row mt-5">
        <breadcrumb>
          <li class="breadcrumb-item active text-secondary" aria-current="page">
            Home
          </li>
        </breadcrumb>

        <!-- Global loading -->
        <div class="col-sm-12 mb-0" v-if="loading">
          <div class="ph-item bordered mb-0 py-5">
            <div class="ph-col-12">
              <div class="ph-row">
                <div class="ph-col-4 empty"></div>
                <div class="ph-col-4 big"></div>
                <div class="ph-col-4 empty"></div>
                <div class="ph-col-4 empty"></div>
                <div class="ph-col-4 big"></div>
                <div class="ph-col-4 empty"></div>

                <div class="ph-col-12 big"></div>
                <div class="ph-col-12 big"></div>

                <div class="ph-col-2 empty"></div>
                <div class="ph-col-8 big"></div>
                <div class="ph-col-2 empty"></div>
              </div>
            </div>

            <!-- Desktop loading -->
            <div class="d-none d-md-block">
              <div class="ph-col-12">
                <div class="ph-row">
                  <div class="ph-col-2 empty"></div>
                  <div
                    class="ph-picture ms-5 me-3"
                    style="
                      width: 50px;
                      height: 50px;
                      margin-left: 163px !important;
                    "
                  ></div>
                  <div
                    class="ph-picture me-3"
                    style="width: 50px; height: 50px"
                  ></div>
                  <div
                    class="ph-picture me-3"
                    style="width: 50px; height: 50px"
                  ></div>
                  <div
                    class="ph-picture me-3"
                    style="width: 50px; height: 50px"
                  ></div>
                  <div
                    class="ph-picture me-3"
                    style="width: 50px; height: 50px"
                  ></div>
                  <div
                    class="ph-picture me-3"
                    style="width: 50px; height: 50px"
                  ></div>
                </div>
              </div>
            </div>
            <!-- End of loading desktop -->

            <!-- Mobile loading -->
            <div class="d-sm-block d-md-none">
              <div class="ph-col-12">
                <div class="ph-row">
                  <div
                    class="ph-picture ms-5 me-2"
                    style="width: 50px; height: 50px; margin-left: 4px"
                  ></div>
                  <div
                    class="ph-picture me-2"
                    style="width: 50px; height: 50px"
                  ></div>
                  <div
                    class="ph-picture me-2"
                    style="width: 50px; height: 50px"
                  ></div>
                  <div
                    class="ph-picture me-2"
                    style="width: 50px; height: 50px"
                  ></div>

                  <div class="ph-col-4 empty"></div>
                  <div
                    class="ph-picture me-2"
                    style="width: 50px; height: 50px"
                  ></div>
                  <div
                    class="ph-picture me-2"
                    style="width: 50px; height: 50px"
                  ></div>
                </div>
              </div>
            </div>
            <!-- End of mobile loading -->
          </div>
          <!-- End of ph-item -->
        </div>
        <!-- End of global loading -->

        <!-- Card -->
        <div class="col-md-12" id="main-content" v-else>
          <div class="card bordered-hover">
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

        <div class="col-md-12 text-center my-5">~~~</div>
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
        content: "my Website portofolio",
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
