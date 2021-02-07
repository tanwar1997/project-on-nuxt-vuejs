<template>
  <div class="container">
    
    <h1><strong>Home page</strong></h1>
     <p>
      This page is rendered on the <strong>{{ rendering }}</strong>
    </p>
     <p v-if="rendering === 'server'">
      First load or hard refresh is done on server side.
    </p>
    <p v-if="rendering === 'client'">Navigation is done on client side.</p>
   
  <b-nav>
    <b-nav-item active to="/login/sign-up">signUpTodo</b-nav-item>
    <b-nav-item to="/todoList">my-todo-list</b-nav-item>
    <b-nav-item to="/login/sign-in">sign in </b-nav-item>
    
  </b-nav>
</div>
</template>
<script>
export default {
  asyncData() {
    return {
      rendering: process.server ? 'server' : 'client'
    }
  }
  
}
</script>
<style  scoped>
.container {
  margin-top: 100px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
 background-color: aquamarine;
}


</style>