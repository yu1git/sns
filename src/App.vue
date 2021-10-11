<template>
  <div id="app" class="mx-auto mt-4" style="width: 400px">
    <h2 class="text-info">Twitter_vue</h2>
    <div>
      <Form v-on:up-event="upmessage" />
      <div style="margin-top:20px">
        <Tweet v-bind:uptweet="input" v-for="input in tweet" v-bind:key="input.id" />
      </div>
    </div>
  </div>
</template>

<script>
import Form from "./components/Form.vue";
import Tweet from "./components/Tweet.vue";

export default {
  name: "App",
  components: {
    Form,
    Tweet,
  },

  data() {
    return {
      tweet: Array.of({
            id: 0,
            body: "まだツイートはありません",
            user: {
              user_id:"",
              user_name:"",
          },
        }),
    };
  },
  methods: {
    upmessage(uptweet) {
      this.tweet.push(uptweet);
    },
  },
};
</script>
