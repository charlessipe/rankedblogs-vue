<template>

  <div class="navbar navbar-expand bg-primary navbar-dark">
    <div class="container-fluid">
      <router-link class="navbar-brand" 
      to="/">Ranked Blogs</router-link>
    </div>
    
    <div class="navbar-nav ml-auto">
    <router-link
      class="nav-item nav-link"
      to="/meetings"
      v-if="user"
    >Meetings</router-link>
    <router-link 
      class="nav-item nav-link" 
      to="/login"
      v-if="!user"
    >Login</router-link>
    <router-link 
      class="nav-item nav-link" 
      to="/login"
      v-if="!user"
    >Register</router-link>
    <button class="nav-item nav-link btn btn-link"
    @click="$emit('logout')"
    >
      logout
    </button>
    </div>
  </div>
</template>

<script>
  export default {
    name: "navigation",
    props: ["user"]	
}
</script>