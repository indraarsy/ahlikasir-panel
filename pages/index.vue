<template>
  <div></div>
</template>

<script>
export default {
  mounted() {
    this.$auth.loggedIn == true
      ? this.$router.push('/admin')
      : this.$router.push('/login')
  }
}
</script>

<style scoped></style>
