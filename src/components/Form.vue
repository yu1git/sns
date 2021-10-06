<template>
  <div class="alert alert-primary ">
    <input class="form-control" v-model="input"><br>
    <button class="btn btn-info mt-2 " v-on:click="update">ツイートする</button>
  </div>

</template>

<script>
export default {
  name: 'Form',
  
  emit:['update'],
  data(){
    return{
      input:'no input',
    }
  },
  methods: {
      update(){
          this.$emit('up-event',this.input)
      }
  },
}
</script>
<style>
div{
  text-align: center;
}
</style>