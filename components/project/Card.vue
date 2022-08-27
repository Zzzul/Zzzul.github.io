<template>
  <div
    class="card bordered-hover p-0 animated card-blog"
    style="background-color: #FDF6F0"
  >
    <div class="card-body p-3">
      <p class="mb-1 mt-1" style="font-size: 13px">
        {{ project.title }}
        <br />
        <span style="font-size: 9px">{{ project.description }}</span>
      </p>

      <div v-if="project.tags" class="mb-2">
        <div v-for="tag of project.tags" :key="tag" class="d-inline-flex">
          <small style="font-size: 8px" class="me-2 fw-light tags">
            #{{ tag }}
          </small>
        </div>
      </div>

      <a
        v-if="project.demo"
        :href="project.demo"
        target="blank"
        style="font-size: 11px"
      >
        Demo
      </a>
      <a  v-if="project.source" :href="project.source" target="blank" style="font-size: 11px"
        >Source</a
      >
    </div>
  </div>
</template>

<script>
export default {
  props: ["project"],
}
</script>
