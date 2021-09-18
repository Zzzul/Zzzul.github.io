<template>
  <div id="home">
    <!-- desktop -->
    <div class="d-none d-md-block mb-0">
      <div class="container">
        <div class="row justify-content-center pt-5">
          <div class="col-md-12 mb-4">
            <HeaderDesktop />
          </div>

          <Breadcrumb>
            <li class="breadcrumb-item" aria-current="page">Home</li>
          </Breadcrumb>

          <div class="col-md-12 pt-3">
            <div
              class="nes-container is-rounded with-title is-centered is-dark"
            >
              <p class="title">Hi</p>
              <h3 class="mt-4">I`m Muhammad Zulfahmi</h3>
              <h4>Web Developer</h4>

              <section class="icon-list mt-4">
                <!-- facebook -->
                <a href="#">
                  <i
                    class="
                      nes-icon
                      mx-4
                      mt-3
                      mb-5
                      facebook
                      is-medium
                      nes-pointer
                    "
                  ></i>
                </a>

                <!-- instagram -->
                <a href="#">
                  <i
                    class="
                      nes-icon
                      mx-4
                      mt-3
                      mb-5
                      instagram
                      is-medium
                      nes-pointer
                    "
                  ></i>
                </a>

                <!-- github -->
                <a href="https://github.com/Zzzul">
                  <i
                    class="nes-icon mx-4 mt-3 mb-5 github is-medium nes-pointer"
                  ></i>
                </a>

                <!-- medium -->
                <a href="#">
                  <i
                    class="nes-icon mx-4 mt-3 mb-5 medium is-medium nes-pointer"
                  ></i>
                </a>

                <!-- linkedin -->
                <a href="#">
                  <i
                    class="
                      nes-icon
                      mx-4
                      mt-3
                      mb-5
                      linkedin
                      is-medium
                      nes-pointer
                    "
                  ></i>
                </a>
              </section>
            </div>
          </div>

          <div class="col-md-12 mt-5 mb-3">
            <p class="text-center text-light">~~~</p>
          </div>
        </div>
      </div>
    </div>

    <!-- mobile -->
    <div class="d-sm-block d-md-none m-0 p-0">
      <div class="container mb-0 pb-0">
        <div class="row mt-2">
          <div class="col-md-12 mb-3">
            <nav
              style="--bs-breadcrumb-divider: '>'"
              aria-label="breadcrumb"
              class="nes-container is-rounded is-dark"
            >
              <ol class="breadcrumb text-light" style="font-size: 12px">
                <li class="breadcrumb-item" aria-current="page">Home</li>
              </ol>
            </nav>
          </div>

          <div class="col-md-12">
            <div
              class="
                nes-container
                is-rounded
                with-title
                is-centered is-dark
                with-title
              "
            >
              <p class="title title-bottom">Hi</p>
              <h5 class="mt-4 mb-2 name-bottom">I`m Muhammad Zulfahmi</h5>
              <h6 style="font-size: 10px">Web Developer</h6>

              <section class="icon-list mt-4">
                <!-- facebook -->
                <a href="#">
                  <i class="nes-icon mx-1 mb-4 facebook nes-pointer"></i>
                </a>

                <!-- instagram -->
                <a href="#">
                  <i class="nes-icon mx-1 mb-4 instagram nes-pointer"></i>
                </a>

                <!-- github -->
                <a href="https://github.com/Zzzul">
                  <i class="nes-icon mx-1 mb-4 github nes-pointer"></i>
                </a>

                <!-- medium -->
                <a href="#">
                  <i class="nes-icon mx-1 mb-4 medium nes-pointer"></i>
                </a>

                <!-- linkedin -->
                <a href="#">
                  <i class="nes-icon mx-1 mb-4 linkedin nes-pointer"></i>
                </a>
              </section>
            </div>
          </div>
        </div>

        <div class="row mt-5">
          <div class="col-md-12 mt-2">
            <p class="text-center text-light">~~~</p>
          </div>
        </div>

        <HeaderMobile />
      </div>
    </div>
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
}
</script>
