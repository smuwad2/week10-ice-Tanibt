<script>
export default {
  props: ['subject', 'entry', 'mood'],
  computed: {
    imgSrc() {
      return `/assets/${this.mood.toLowerCase()}.png`
    }
  }
}
</script>

<template>
  <div class="card mb-3 text-center shadow-sm" style="width: 18rem;">
    <img :src="imgSrc" class="card-img-top" alt="Mood image" />
    <div class="card-body">
      <h5 class="card-title">{{ subject }}</h5>
      <p class="card-text">{{ entry }}</p>
    </div>
  </div>
</template>