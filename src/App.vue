<template>
  <div id="app">
  	<h1>ユーザ一覧</h1>
    <div v-for="user in users" :key=user.id>
      {{ user.name }}
    </div>
  </div>
</template>

<script>
export default {
  name: 'app',
  computed : {
  	users : function(){
  		return this.$store.state.users
  	}
  },
  mounted(){
    this.$store.dispatch('getUsers')
  }
}
</script>

<style>
</style>
