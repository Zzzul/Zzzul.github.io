<template>
  <div id="home">
    <desktop-navigation />

    <div class="container">
      <div class="row mt-5">
        <breadcrumb>
          <li class="breadcrumb-item">
            <nuxt-link to="/" class="text-decoration-none">Home</nuxt-link>
          </li>
          <li class="breadcrumb-item active" aria-current="page">About</li>
        </breadcrumb>

        <!-- About -->
        <div class="col-md-12 mb-5">
          <div class="card bordered">
            <div class="card-body p-5 text-center">
              <h5 class="mb-4 text-primary">#Tentang Saya</h5>
              <p>
                Hai, saya Mohammad Zulfahmi. Saat ini saya adalah seorang
                mahasiswa semester akhir jurusan Teknik Informatika di
                <a href="https://binainsani.ac.id/" target="blank"
                  >Bina Insani University</a
                >
                dan sedang megikuti
                <a href="https://pmmb.fhcibumn.com/" target="blank"
                  >Program Magang Mahasiswa Bersertifikat(PMMB)</a
                >
                pada
                <a href="https://www.pertamina.com/" target="blank"
                  >PT. Pertamina (persero)</a
                >
                selama 6 bulan kedepan.
              </p>
              <p>
                Saya juga seorang Freelance Web Developer bersama dengan teman
                saya, biasanya menangani web yang menggunakan
                <a href="https://laravel.com/" target="blank">Laravel</a>.
              </p>
              <p>
                Untuk keahlian dan teknologi yang biasa saya gunakan kamu bisa
                lihat dibawah
                <a href="#skills">sini</a>.
              </p>
            </div>
          </div>
        </div>

        <!-- Skills -->
        <div class="col-md-12 mb-4" id="skills">
          <div class="card bordered">
            <div class="card-body px-5 pt-5 pb-4">
              <h5 class="text-primary text-center mb-4 font-weigth-bold">
                #Keahlian
              </h5>

              <!-- PHP & Javascript -->
              <div class="row mb-2">
                <!-- <div class="col-md-3 mb-2"></div> -->
                <div class="col-md-4 mb-2">
                  <h6>PHP</h6>
                  <ul>
                    <li class="mb-2">
                      <a
                        href="https://codeigniter.com/"
                        class="text-decoration-none"
                        target="blank"
                        data-bs-toggle="tooltip"
                        data-bs-placement="right"
                        title="Beberapa bulan"
                      >
                        <img
                          src="~/assets/img/skills/ci.png"
                          alt="Codeigniter Logo"
                          width="30px"
                        />
                        Codeigniter
                      </a>
                    </li>
                    <li class="mb-2">
                      <a
                        href="http://laravel.com/"
                        class="text-decoration-none"
                        target="blank"
                        data-bs-toggle="tooltip"
                        data-bs-placement="right"
                        title="± 1 tahun"
                      >
                        <img
                          src="~/assets/img/skills/laravel.png"
                          alt="Laravel Logo"
                          width="30px"
                        />
                        Laravel
                      </a>
                    </li>
                  </ul>
                </div>

                <div class="col-md-4 mb-2">
                  <h6>Javascript</h6>
                  <ul>
                    <li class="mb-2">
                      <a
                        href="https://jquery.com/"
                        target="blank"
                        data-bs-toggle="tooltip"
                        data-bs-placement="right"
                        title="± 1 tahun"
                      >
                        <img
                          src="~/assets/img/skills/jquery.png"
                          alt="Laravel Logo"
                          width="30px"
                        />
                        Jquery
                      </a>
                    </li>
                    <li class="mb-2">
                      <a
                        href="https://vuejs.org/"
                        target="blank"
                        data-bs-toggle="tooltip"
                        data-bs-placement="right"
                        title="Beberapa minggu"
                      >
                        <img
                          src="~/assets/img/skills/vue.png"
                          alt="Vue Logo"
                          width="30px"
                        />
                        Vue
                      </a>
                    </li>
                    <li class="mb-2">
                      <a
                        href="https://nuxtjs.org/"
                        target="blank"
                        data-bs-toggle="tooltip"
                        data-bs-placement="right"
                        title="Beberapa minggu"
                      >
                        <img
                          src="~/assets/img/skills/nuxt.png"
                          alt="Nuxt Logo"
                          width="30px"
                        />
                        Nuxt
                      </a>
                    </li>
                  </ul>
                </div>

                <div class="col-md-4 mb-2">
                  <h6>CSS</h6>
                  <ul>
                    <li class="mb-2">
                      <a
                        href="https://getbootstrap.com/"
                        target="blank"
                        data-bs-toggle="tooltip"
                        data-bs-placement="right"
                        title="± 2 tahun"
                      >
                        <img
                          src="~/assets/img/skills/bootstrap.png"
                          alt="Bootstrap Logo"
                          width="30px"
                        />
                        Bootstrap
                      </a>
                    </li>
                    <li class="mb-2">
                      <a
                        href="https://nostalgic-css.github.io/NES.css/"
                        target="blank"
                        data-bs-toggle="tooltip"
                        data-bs-placement="right"
                        title="Beberapa bulan"
                      >
                        <img
                          src="~/assets/img/skills/nes.png"
                          alt="NES CSS Logo"
                          width="30px"
                        />
                        NES CSS
                      </a>
                    </li>
                  </ul>
                </div>
              </div>

              <!-- Code editor & CSS -->
              <div class="row mb-2">
                <div class="col-md-4 mb-2">
                  <h6>Code Editor</h6>
                  <ul>
                    <li class="mb-2">
                      <a
                        href="https://code.visualstudio.com/"
                        target="blank"
                        data-bs-toggle="tooltip"
                        data-bs-placement="right"
                        title="± 1 tahun"
                      >
                        <img
                          src="~/assets/img/skills/vscode.png"
                          alt="VS Code Logo"
                          width="30px"
                        />
                        VS Code
                      </a>
                    </li>

                    <li class="mb-2">
                      <a
                        href="https://www.sublimetext.com/"
                        target="blank"
                        data-bs-toggle="tooltip"
                        data-bs-placement="right"
                        title="± 1 tahun"
                      >
                        <img
                          src="~/assets/img/skills/sublime.png"
                          alt="Sublime Text Logo"
                          width="30px"
                        />
                        Sublime Text
                      </a>
                    </li>
                  </ul>
                </div>

                <div class="col-md-4">
                  <h6>Database</h6>
                  <ul>
                    <li class="mb-2">
                      <a
                        href="https://www.mysql.com/"
                        target="blank"
                        data-bs-toggle="tooltip"
                        data-bs-placement="right"
                        title="± 1 tahun"
                      >
                        <img
                          src="~/assets/img/skills/mysql.png"
                          alt="My SQL Logo"
                          width="30px"
                        />
                        My SQL
                      </a>
                    </li>
                  </ul>
                </div>

                <div class="col-md-4 mb-2">
                  <h6>Tools</h6>

                  <ul>
                    <li class="mb-2">
                      <a
                        href="https://laragon.org/"
                        target="blank"
                        data-bs-toggle="tooltip"
                        data-bs-placement="right"
                        title="Beberapa bulan"
                      >
                        <img
                          src="~/assets/img/skills/laragon.png"
                          alt="Laragon Logo"
                          width="30px"
                        />
                        Laragon
                      </a>
                    </li>

                    <li class="mb-2">
                      <a
                        href="https://git-scm.com/"
                        target="blank"
                        data-bs-toggle="tooltip"
                        data-bs-placement="right"
                        title="± 1 tahun"
                      >
                        <img
                          src="~/assets/img/skills/git2.webp"
                          alt="Git Logo"
                          width="30px"
                        />
                        Git
                      </a>
                    </li>

                    <li class="mb-2">
                      <a
                        href="https://www.npmjs.com/"
                        target="blank"
                        data-bs-toggle="tooltip"
                        data-bs-placement="right"
                        title="Beberapa bulan"
                      >
                        <img
                          src="~/assets/img/skills/npm.png"
                          alt="NPM Logo"
                          width="30px"
                        />
                        NPM
                      </a>
                    </li>

                    <li class="mb-2">
                      <a
                        href="https://github.com/"
                        target="blank"
                        data-bs-toggle="tooltip"
                        data-bs-placement="right"
                        title="± 1 tahun"
                      >
                        <img
                          src="~/assets/img/skills/github.png"
                          alt="Github Logo"
                          width="30px"
                        />
                        Github
                      </a>
                    </li>
                  </ul>
                </div>
              </div>
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
    title: "Blog",
    meta: [
      {
        hid: "description",
        name: "description",
        content: "mengenal saya lebih dekat",
      },
    ],
  },
}
</script>
