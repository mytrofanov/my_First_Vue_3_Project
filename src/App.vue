<template>
  <div>
    <div>Likes: {{likes}}</div>
    <div>Dislikes: {{dislikes}}</div>
    <button @click="adLike">Like</button>
    <button @click="adDisLike">Dislike</button>
  </div>
</template>

<script>
export default {
  data () {
    return {
      likes: 0,
      dislikes: 0,
    }
  },
  methods: {
    adLike () {
      this.likes +=1
    },
    adDisLike () {
      this.dislikes +=1
    }
  }
}
</script>

<style lang="scss" scoped>

</style>
