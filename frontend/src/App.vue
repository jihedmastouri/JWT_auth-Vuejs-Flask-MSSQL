<template>
<div>
  <div class="d-flex align-items-center justify-content-center">
    <router-view />
  </div>
    <div class="d-flex align-items-center justify-content-center">
    <button class="btn btn-danger" @click="logout()" v-if="user.authenticated" >logout</button>
  </div>
</div>
</template>



<script>
import auth from './auth'

export default {
  data() {
    return {
      user: auth.user
    }
  },

  methods: {
    logout() {
      auth.logout()
    }
  }
}
</script>