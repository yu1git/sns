<template>
  <div class="alert alert-primary">
    <p>{{uptweet}}</p>
    <slot />
  </div>

</template>

<script>
export default {
  name: 'Tweet',
  props: {
    uptweet:Array,
  },
  data(){
    return{
    }
  }
}
</script>