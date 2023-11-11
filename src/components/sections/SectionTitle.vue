<template>
    <div class="section-title">
        <p>{{ desc }}</p>
        <h2>{{ title }}</h2>
    </div>
</template>

<script>
export default {
  props: {
      title: String,
      desc: String
  }
}
</script>

<style lang="scss">
.section-title {
    text-align: center;
    h2 {
        font-size: 3rem;
        font-weight: bold;
    }
}
</style>