<template>
  <div class="container-fluid">
    <div class="d-sm-flex align-items-center justify-content-between mb-4">
      <h1 class="h3 mb-0 text-gray-800">Users</h1>
    </div>
    <b-table-simple striped hover :items="items"></b-table-simple>
    <v2-table :data="list">
      <v2-table-column label="Name" prop="name"></v2-table-column>
      <v2-table-column label="Date" prop="date"></v2-table-column>
      <v2-table-column label="Address" prop="address"></v2-table-column>
    </v2-table>
  </div>
</template>

<script>
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
