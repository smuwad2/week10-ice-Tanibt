<script>
import BlogPost from './subcomponents/BlogPost.vue'

export default {
  components: { BlogPost },
  data() {
    return {
      posts: [
        { subject: 'My First Love', entry: 'A very handsome boy give me rose for vday', mood: 'Happy' },
        { subject: 'CNY Homework', entry: 'This crazy women give us CNY homework omg can she pliz go enjoy CNY and leave us alone', mood: 'Angry' },
        { subject: 'My puppy', entry: 'Mummy say she will give me away my dog because he pee everywhere', mood: 'Angry' }
      ]
    }
  }
}
</script>

<template>
  <div class="container mt-4">
    <h2 class="text-center mb-4">My Blog Posts</h2>
    <div class="d-flex flex-column align-items-center">
      <BlogPost
        v-for="(post, index) in posts"
        :key="index"
        :subject="post.subject"
        :entry="post.entry"
        :mood="post.mood"
      />
    </div>
  </div>
</template>