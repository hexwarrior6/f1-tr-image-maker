<template>
  <div class="team-logo">
    <img :src="require(`@/assets/${mercedes}`)" alt="Team Logo" />
  </div>
</template>

<script>
export default {
  name: 'TeamLogo',
  props: {
    mercedes: {
      type: String,
      required: true
    }
  }
}
</script>

<style scoped>
.team-logo img {
  width: auto;
  height: 20px;
}
</style>