<template>
  <div class="name">
    {{ name }}
  </div>
  <br>
  <button 
    class="btn btn-primary"
    v-on:click="updateName"
  >
    Click
  </button>
</template>

<script>
import { ref, reactive } from 'vue';

export default{
  setup(){
    // const name = ref('Kossie Coder1');
    const name = reactive({
      id: 1
    });

    // const greeting = (name) => {
    //   return 'Hello, ' + name;
    // };

    // const greet = greeting(name);

    const updateName = () =>{
      // name.value = 'Kossie Coder'; ref는 value.id
      name.id += 1; // reactive는 value 없이 사용
      console.log(name);
    };

    return {
      name,
      updateName
    };
  }
}
</script>

<style>
  .name {
    color: red;
  }
</style>