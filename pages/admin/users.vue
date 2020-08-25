<template>
  <div class="container-fluid">
    <div class="d-sm-flex align-items-center justify-content-between mb-4">
      <h1 class="h3 mb-0 text-gray-800">Users</h1>
    </div>
    <b-table striped hover :items="items"></b-table>
  </div>
</template>

<script>
// import BootstrapVue from 'bootstrap-vue'
export default {
  data() {
    return {
      items: []
    }
  },
  mounted() {
    this.$axios.get('/api/users').then((res) => {
      this.items = res.data
      console.log(this.items)
    })
  }
}
</script>

<style scoped></style>
