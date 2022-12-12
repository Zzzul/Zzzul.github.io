<template>
  <div>
    <div class="text-center mt-3" v-if="$colorMode.value === 'light'">
        <a
          href="https://www.instagram.com/zzzzzul/"
          class="text-decoration-none animated"
          target="_blank"
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
          target="_blank"
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
          target="_blank"
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
          target="_blank"
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
          target="_blank"
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

      <div class="text-center mt-3" v-if="$colorMode.value === 'dark'">
        <a
          href="https://www.instagram.com/zzzzzul/"
          class="text-decoration-none animated"
          target="_blank"
        >
          <img
            src="~/assets/img/social-media/dark/ig.webp"
            class="mb-2 socmed-icon"
            alt="Instagram logo"
          />
        </a>

        <a
          href="https://github.com/Zzzul"
          class="text-decoration-none animated"
          target="_blank"
        >
          <img
            src="~/assets/img/social-media/dark/github.webp"
            class="mb-2 socmed-icon"
            alt="github logo"
          />
        </a>

        <a
          href="https://zzzul.medium.com/"
          class="text-decoration-none animated"
          target="_blank"
        >
          <img
            src="~/assets/img/social-media/dark/medium.webp"
            class="mb-2 socmed-icon"
            alt="medium logo"
          />
        </a>

        <a
          href="https://www.linkedin.com/in/muhammad-zulfahmi/"
          class="text-decoration-none animated"
          target="_blank"
        >
          <img
            src="~/assets/img/social-media/dark/linkedin.webp"
            class="mb-2 socmed-icon"
            alt="linkedin logo"
          />
        </a>

        <a
          href="mailto:mzulfahmi807@gmail.com"
          class="text-decoration-none animated"
          target="_blank"
        >
          <img
            src="~/assets/img/social-media/dark/gmail.webp"
            class="mb-2 socmed-icon"
            alt="gmail logo"
            height="47px"
            style="object-fit: cover"
          />
        </a>
      </div>
  </div>
</template>
