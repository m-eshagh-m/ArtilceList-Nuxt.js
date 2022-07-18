<template>
  <v-data-table
    :headers="headers"
    :items="products"
    :items-per-page="10"
    class="elevation-1"
  >
    <template #item="{ item }">
      <tr>
        <td>{{ item.id }}</td>
        <td><img :src="item.image" alt="" /></td>
        <td>{{ item.price }}</td>
        <td>{{ item.category }}</td>
      </tr>
    </template>
  </v-data-table>
</template>

<script>
export default {
  props: {
    products: {
      type: Array,
      required: true,
    },
  },

  data() {
    return {
      search: '',
      headers: [
        { text: 'Id', value: 'id' },
        { text: 'Image', value: 'image' },
        { text: 'Price', value: 'price' },
        { text: 'Category', value: 'category' },
      ],
    }
  },
}
</script>

<style lang="scss">
table {
  width: fit-content !important;

  img {
    width: 25px;
    height: 25px;
  }
}
</style>
