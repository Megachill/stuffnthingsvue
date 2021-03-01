<template>
  <div>

    <button
        :disabled="bDownloadingPosts"
        @click="getPosts"
    >Click to get posts</button>

    <hr>

    <ul v-for="post in posts" :key="post.id">
      <h4>({{ post.userId }}) {{ post.title }}</h4>
      <p>{{ post.body }}</p>
    </ul>


  </div>
</template>
<script>
export default {
  name: "post-index",
  data() {
    return {
      bDownloadingPosts: false,
      posts: [],
    }
  },
  created() {
  },
  mounted() {
    // stub
  },
  methods: {
    getPosts() {
      this.bDownloadingPosts = true

      this.axios.get('https://jsonplaceholder.typicode.com/posts')
        .then((response) => {
          console.log(response)
          this.posts = response.data

          this.bDownloadingPosts = false
        })
        .catch((err) => {
          console.warn(err.response)
          this.bDownloadingPosts = false
        })
    }
  },
}
</script>
