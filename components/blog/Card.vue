<template>
  <div
    class="card bordered-hover p-0"
    :style="{ 'background-color': post.color }"
  >
    <div class="card-body p-3">
      <nuxt-link
        class="mb-1 mt-1"
        style="font-size: 13px"
        :to="'/blog/' + post.slug"
      >
        {{ post.title }}
        <br />
        <span style="font-size: 9px" class="text-dark">{{
          post.description
        }}</span>
      </nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
  props: ["post"],
}
</script>
