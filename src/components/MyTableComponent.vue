<template>
  <div class="my-table-component">
    <table class="table">
      <thead>
        <tr>
          <th scope="col">#</th>
          <th scope="col">Texto digitado</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(item, index) in myItems" :key="index">
          <td>{{ index }}</td>
          <td>{{ item }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: "MyTableComponent",
  props: {
    myItems: {
      type: Array,
    },
  },
  data: () => ({
    // headers: [
    //     {}
    // ],
  }),
};
</script>

<style></style>
