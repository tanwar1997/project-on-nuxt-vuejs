<template>
    <div> <h1>{{username}}</h1>
    <h1>{{password}}</h1>
         <div class="dummyForm">
            <div class="form-element">
              <input type="text" v-model="username" placeholder="Email / Username">
            </div>
            <div class="form-element">
              <input type="password" v-model="password" placeholder="Password">
            </div>
            <div class="form-element">
              <input type="checkbox" id="remember_me">
              <label for="remember_me">Remember me</label>
            </div>
            <div class="form-element">
              <button>Sign In</button>
            </div>
          </div> 
          <nuxt-link to="/">goToHOME</nuxt-link>
    </div>
</template>

<script>
export default {
    layout:'default',
  data: function(){
    return{
      username:undefined,
      password:undefined
    }
  },
  
  
}
</script>