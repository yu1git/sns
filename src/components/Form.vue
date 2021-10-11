<template>
  <div class="alert alert-primary form form-group">
    <input class="form-control" 
    placeholder="ユーザー名" v-model="input.user.user_name"><input class="form-control" 
    placeholder="ユーザーID" v-model="input.user.user_id">
    <textarea
      name="form"
      id=""
      class="form-control"
      cols="60"
      rows="5"
      placeholder="いまなにしてる？"
      v-model="input.body"
    ></textarea
    ><br>
    <button class="btn btn-info mt-2 text-white" v-on:click="update">
      ツイートする
    </button>
  </div>
</template>

<script>
export default {
  name: "Form",

  data() {
    return {
      input: {
        id: 0,
        body: "",
        user:{
          user_id: "",
          user_name: "",
        }
      },
    };
  },
  methods: {
    update() {
      this.input.id += 1;
      //値渡しするために、新しいオブジェクトを定義する
      const message = Object.assign({},this.input);
      this.$emit("up-event", message);
    },
  },
};
</script>
<style>
div {
  text-align: center;
}
</style>