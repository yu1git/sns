<template>
  <div id="app" class="continer mx-auto mt-4" style="width:400px">
    <Form v-on:up-event="upmessage"  />
    <Tweet v-bind:uptweet="tweet">

    </Tweet>
  </div>
</template>

<script>
import Form from './components/Form.vue'
import Tweet from './components/Tweet.vue'

export default {
  name: 'App',
  components: {
    Form,
    Tweet
  },
  
  data(){
    return{
      tweet:[{
        tweet_1:{
          id:1,
          m:'まだツイートはありません',
          user:{
            user_id:'test_user',
            user_name:'test'
          }
        }
      },],
      //数字分Tweetが増える→中の数も変わってしまうので、tweetを配列にする→slotでやる
      count:0
    }
  },
  methods: {
    upmessage(message){
      this.$set(this.tweet,message);
      this.count++;
      console.log(this.tweet)
    }
  },
}
</script>

<style>

</style>
