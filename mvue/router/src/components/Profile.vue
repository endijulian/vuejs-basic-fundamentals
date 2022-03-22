<template>
  <div class="profile">
    <h2>Profile Page ( {{ userId }} )</h2>
  </div>
</template>

<script>
export default {
  name: 'Profile',
  data () {
    return {
        userId: this.$route.params.user_id
    }
  },
  methods:{
      updatedId(){
          this.userId = this.$route.params.user_id
      }
  },
  watch:{
      $route: 'updatedId'
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

    h2{
        color: green;
    }

</style>
