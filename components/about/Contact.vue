<template>
  <div class="card bordered">
    <div class="card-body py-5 px-4">
      <h5 class="mb-3 text-primary text-center">#Contact</h5>

      <div class="text-center mt-3">
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

      <p class="text-center mt-3">
        Jika punya pertanyaan, kritik, saran atau kolaborasi, kamu bisa
        menghubungi saya melalui sosial media diatas atau form dibawah ini.
      </p>

      <div
        v-if="message == 'success'"
        class="
          alert alert-success alert-dismissible
          fade
          show
          bordered-without-shadow
          pb-3
        "
        role="alert"
        style="font-size: 11px"
      >
        <strong>Terimakasih!</strong> Pesan kamu sudah saya terima.

        <button
          @click="removeMessage"
          type="button"
          class="btn-close mt-2 me-3"
          data-bs-dismiss="alert"
          aria-label="Close"
        ></button>
      </div>

      <div
        v-if="message == 'error'"
        class="
          alert alert-danger alert-dismissible
          fade
          show
          bordered-without-shadow
          pb-3
        "
        role="alert"
        style="font-size: 11px"
      >
        <strong>Maaf!</strong> Terjadi suatu kesalahan.

        <button
          @click="removeMessage"
          type="button"
          class="btn-close mt-2 me-3"
          data-bs-dismiss="alert"
          aria-label="Close"
        ></button>
      </div>

      <form @submit.prevent="sendMessage" name="contact-form">
        <div class="row">
          <div class="col-md-6 mt-2">
            <div class="form-group">
              <label for="nama">Nama</label>
              <input
                id="nama"
                type="text"
                class="form-control"
                placeholder="Nama"
                minlength="3"
                name="nama"
                :disabled="loading"
                required
              />
            </div>
          </div>

          <div class="col-md-6 mt-2">
            <div class="form-group">
              <label for="email">Email</label>
              <input
                id="email"
                type="email"
                class="form-control"
                placeholder="Email"
                min="5"
                name="email"
                :disabled="loading"
                required
              />
            </div>
          </div>

          <div class="col-md-12 mt-3">
            <div class="form-group">
              <label for="pesan">Pesan</label>
              <textarea
                id="pesan"
                class="form-control"
                placeholder="Pesan"
                rows="6"
                minlength="5"
                name="pesan"
                :disabled="loading"
                required
              ></textarea>
            </div>
          </div>
        </div>

        <button
          v-if="loading"
          type="submit"
          class="btn btn-primary mt-3 disabled"
          disabled
        >
          <!-- <img
            src="~/assets/img/loading.svg"
            class="img-fluid"
            style="width: 30px; color: white"
            alt="Loading"
          /> -->
          <!-- <span class="pt-5">Loading...</span> -->
          Loading...
        </button>

        <button v-else type="submit" class="btn btn-primary mt-3">Kirim</button>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      loading: false,
      message: "",
    }
  },
  methods: {
    removeMessage() {
      this.message = ""
    },
    async sendMessage() {
      this.loading = true

      await fetch(this.$config.scriptUrl, {
        method: "POST",
        body: new FormData(document.forms["contact-form"]),
      })
        .then((response) => {
          // console.log("Success!", response)
          console.log("Success!")

          document.forms["contact-form"].reset()

          this.message = "success"

          this.loading = false
        })
        .catch((error) => {
          // console.error("Error!", error.message)
          console.error("Error!")

          document.forms["contact-form"].reset()

          this.message = "error"

          this.loading = false
        })
    },
  },
}
</script>
