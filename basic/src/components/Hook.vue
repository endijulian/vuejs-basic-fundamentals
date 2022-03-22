<template>
  <div class="hook">
    <h1>Post</h1>

  <input type="text" v-model="searchTrem" placeholder="Search....">

    <div v-for="post in filtersearch" :key="post.id">
      <h2>{{ post.title }}</h2>
      <p>{{ post.body | snippet }}</p>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "Hook",
  data() {
    return {
      posts:[],
      searchTrem: ''
    };
  },
  computed:{
    filtersearch(){
      return this.posts.filter(post => {
        return post.title.match(this.searchTrem)
      })
    }
  },
  methods: {},
  created() {
    axios
      .get("https://jsonplaceholder.typicode.com/posts")
      .then((response) => {
        this.posts = response.data
      })
      .catch(error =>{
        console.log(error);
      });
  },
};
</script>

<style scoped>
h1 {
  color: red;
  text-align: center;
}
</style>