<template>
  <div class="my-list-component">
    <div class="mb-3">
      <label for="formInput1" class="form-label"> Digite alguma coisa </label>
      <input
        type="text"
        class="form-control"
        v-model="userInput"
        id="formInput1"
        placeholder="Alguma coisa ..."
      />
    </div>
    <div class="mb-3">
      <button
        @click="addToList"
        class="btn btn-primary"
        type="button">Enviar</button>
    </div>
    <div class="mb-4">
        <my-table-component
            :myItems="myItems"></my-table-component>
    </div>
  </div>
</template>

<script>
import MyTableComponent from './MyTableComponent.vue';
export default {
  components: { MyTableComponent },
  name: "MyListComponent",
  data:() => ({
    userInput: '',
    myItems:[
    ],
  }),
  methods:{
    addToList(){
        this.myItems.push(this.userInput);
        this.userInput = '';
        // this.myItems.push(Object.assign(this.userInput));
    },
  },
};
</script>

<style scoped>
.form-control {
  /* background-color: red !important; */
  width: 50% !important;
  margin-left: 25% !important;
}
/* .my-list-component {
  background-color: rgb(0, 0, 0) !important;
} */

/* .form-label {
  color: white !important;
} */
</style>
