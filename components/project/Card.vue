<template>
  <div
    class="card bordered-hover p-0"
    :style="{ 'background-color': project.color }"
  >
    <div class="card-body p-3">
      <p class="mb-1 mt-1" style="font-size: 13px">
        {{ project.title }}
        <br />
        <span style="font-size: 9px">{{ project.description }}</span>
      </p>

      <div v-if="project.tags" class="mb-2">
        <div v-for="tag of project.tags" :key="tag" class="d-inline-flex">
          <small
            style="font-size: 8px"
            class="me-2 fw-light border border-1 border-dark tags"
          >
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
      <a :href="project.source" target="blank" style="font-size: 11px"
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

<style>
</style>
