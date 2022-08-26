<template>
  <div id="home">
    <desktop-navigation />

    <div class="container">
      <div class="row">
        <breadcrumb>
          <li class="breadcrumb-item active text-secondary" aria-current="page">
            Home
          </li>
        </breadcrumb>

        <!-- Card -->
        <div class="col-md-12 mb-4" id="main-content">
          <div class="card bordered">
            <div class="card-body p-5 text-center">
              <h4 class="mb-3">Hai!</h4>
              <h2 class="mb-3">Saya Mohammad Zulfahmi</h2>

              <h2 class="mb-4">Web Developer</h2>

              <a href="#" class="text-decoration-none animated" target="blank">
                <img
                  src="~/assets/img/social-media/fb.webp"
                  class="mb-2 socmed-icon"
                  alt="facebook logo"
                />
              </a>

              <a
                href="https://www.instagram.com/zzzzzul/"
                class="text-decoration-none animated"
                target="blank"
              >
                <img
                  src="~/assets/img/social-media/ig.webp"
                  class="mb-2 socmed-icon"
                  alt="Instagram logo"
                />
              </a>

              <a
                href="https://github.com/Zzzul"
                class="text-decoration-none animated"
                target="blank"
              >
                <img
                  src="~/assets/img/social-media/github.webp"
                  class="mb-2 socmed-icon"
                  alt="github logo"
                />
              </a>

              <a
                href="https://zzzul.medium.com/"
                class="text-decoration-none animated"
                target="blank"
              >
                <img
                  src="~/assets/img/social-media/medium.webp"
                  class="mb-2 socmed-icon"
                  alt="medium logo"
                />
              </a>

              <a
                href="https://www.linkedin.com/in/muhammad-zulfahmi/"
                class="text-decoration-none animated"
                target="blank"
              >
                <img
                  src="~/assets/img/social-media/linkedin.webp"
                  class="mb-2 socmed-icon"
                  alt="linkedin logo"
                />
              </a>

              <a
                href="mailto:mzulfahmi807@gmail.com"
                class="text-decoration-none animated"
                target="blank"
              >
                <img
                  src="~/assets/img/social-media/gmail.webp"
                  class="mb-2 socmed-icon"
                  alt="gmail logo"
                  height="47px"
                  style="object-fit: cover"
                />
              </a>
            </div>
          </div>
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
    title: "Home",
    meta: [
      {
        hid: "description",
        name: "description",
        content: "Hai!, sekarang saya punya webiste portofolio loh..",
      },
    ],
  },
}
</script>

<style>
  body {
    color-scheme: light dark;

    font-synthesis: none;
    text-rendering: optimizeLegibility;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    -webkit-text-size-adjust: 100%;
  }

  @media (prefers-color-scheme: dark) {
    body, 
    html {
      color: rgba(255, 255, 255, 0.87);
      background-color: #191919;
    }

    .bordered,
    .bordered-hover {
        -webkit-transition-duration: 0.3s;
        transition-duration: 0.3s;
        -webkit-transition-property: transform;
        transition-property: transform;
        -webkit-transition-timing-function: ease-out;
        transition-timing-function: ease-out;
        -webkit-box-shadow: -5px 5px 0px 1px #DDDDDD !important;
        -moz-box-shadow: -5px 5px 0px 1px #DDDDDD !important;
        box-shadow: -5px 5px 0px 0px #DDDDDD !important;
        border-radius: 2px !important;
        border: 2px solid #DDDDDD;
        /* border: 2px solid #191919; */
    }

    .bordered-without-shadow{
        border: 2px solid #DDDDDD !important;
    }

    .card-body{
       background-color: #242424;
    }

    .bordered{
      color: #DDDDDD !important;
    }

    .breadcrumb{
      background-color: #242424;
    }

    .breadcrumb-item{
      color: #DDDDDD !important;
    }

    .text-primary{
      color: #81CACF !important;
    }

    .navbar-light, .btn-primary, .bg-primary{
      background-color: #243A73 !important;
    }

    .bordered-hover:hover,
    .bordered-hover:focus,
    .bordered-hover:active {
        -webkit-transform: translateY(7px);
        transform: translateY(7px);
        -webkit-box-shadow: -2px 2px 0px 1px rgb(255, 255, 255) !important;
        -moz-box-shadow: -2px 2px 0px 1px rgb(255, 255, 255) !important;
        box-shadow: -2px 2px 0px 0px rgb(255, 255, 255) !important;
        border: 2px solid #DDDDDD;
    }

    .tags{
      border: 1px dashed #DDDDDD;
      border-radius: 2px;
    }

    .active-uri{
      border-bottom: white solid 2px;
    }

    .text-dark{
      color: white !important;
    }

    .btn-close{
      border-radius: 2px !important;
      border: 1px solid white !important;
      font-size: 11px;
      padding: 10px !important;
      color: white !important;
      justify-content: center;
    }

    .btn-primary{
      border-radius: 2px !important;
      border: 2px solid white !important;
      font-size: 12px;
    }

    input,textarea{
      border: 1px solid white !important;
      background-color: #413F42 !important;
    }

    input::placeholder, textarea::placeholder{
      color: white !important;
    }

    input:active,
    input:focus,
    textarea:active,
    textarea:focus{
      -webkit-box-shadow: -3px 2px 0px 1px rgb(255, 255, 255) !important;
      -moz-box-shadow: -3px 2px 0px 1px rgb(255, 255, 255) !important;
      box-shadow: -3px 2px 0px 0px rgb(255, 255, 255) !important;
    }

    a.nuxt-link-exact-active {
      border-bottom: 2px solid white;
      border-bottom-width: 70% !important;
    }

    a {
      color: #81CACF;
      text-decoration: inherit;
    }
    a:hover {
      color: #4CACBC;
    }

    .nuxt-content-highlight{
      background-color: #413F42;
    }

    code{
      color: #711A75;
    }

    p, h1, h2, h3, h4, h5, h6, .navbar-brand, .nav-link{
      color: #DDDDDD !important;
    }
  }
</style>
