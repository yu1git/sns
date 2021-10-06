<template>
  <div >
    <input v-model="tweet">
  </div>

</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
  },
  data(){
    return{
      tweet:"",
    }
  }
}
</script>

