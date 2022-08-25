<template>
  <div
    class="card bordered-hover p-0 animated"
    style="background-color: #F4F9F9"
  >
    <div class="card-body pb-3">
      <nuxt-link
        class="mb-1 mt-1"
        style="font-size: 13px"
        :to="'/blog/' + post.slug"
      >
        {{ post.title }}
        <br />
        <span style="font-size: 9px" class="text-dark">
          {{ post.description }}
        </span>
      </nuxt-link>

       <div v-if="post.tags" class="my-2">
        <div v-for="tag of post.tags" :key="tag" class="d-inline-flex">
          <small style="font-size: 8px" class="me-2 fw-light tags">
            #{{ tag }}
          </small>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["post"],
}
</script>
