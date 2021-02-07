<template>
<div><h1 id="heading"> Welcome to  <span id="span">TODO list </span>  application</h1>
    <div class="form">
      <nuxt-link to="/"> home</nuxt-link>
        <div class="tab-header">
          <div class="active">Sign Up</div>
          <div>Sign In</div>
        </div>
        <div class="tab-content">
          <div class="tab-body active">
            <div class="form-element">
              <input  type="text" placeholder="Email" id="textone">
            </div>
            <div class="form-element">
              <input  type="text" placeholder="Username" id="texttwo">
            </div>
            <div class="form-element">
              <input type="password"  placeholder="Password" id="textthree">
            </div>
            <div class="form-element">
              <button to="/login/sign-in" type="submit" @click="isFromOpen= true">Sign Up</button>
              <span id="spanResult"> </span>
            </div>
          </div>  
          <a href=""></a>  
        </div>     
      </div>
    <div v-if="isFromOpen" class="dummyForm">
        <div class="tab-header">
          <div class="active">Sign Up</div>
          <div>Sign In</div>
        </div>
        <div class="tab-content">
          <div class="tab-body active">
            <div class="form-element">
              <input  type="text" placeholder="Username" id="texttwo">
            </div>
            <div class="form-element">
              <input type="password"  placeholder="Password" id="textthree">
            </div>
          </div>  
        </div>
       
      </div>
</div> 
</template>
<script>
export default {
  layout: 'default',
  data: function () {
    return {
      name: undefined,
      email: undefined,
      password: undefined,
      isFromOpen: false,
    }
  },
  methods: {
    testVariable() {
      this.$router.push({ path: '/sign-in' })
    },
  },
}
</script>

<style> 
* {
  box-sizing: border-box;
}
body {
  background: #ddd;
  font-family: sans-serif;
}
#heading {
  display: flex;
  text-align: center;
  justify-content: center;
  margin-top: 100px;
}
#span {
  color: lime;
}
.form {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 300px;
  background: #f5f5f5;
  box-shadow: 5px 5px 10px 5px #ccc;
}
.form .tab-header {
  height: 50px;
  line-height: 50px;
}
.form .tab-header > div {
  width: 50%;
  float: left;
  text-align: center;
  background: #ddd;
  color: #555;
  cursor: pointer;
}
.form .tab-header > div.active {
  background: #f5f5f5;
  color: #111;
}
.form .tab-content {
  padding: 20px;
}
.form .tab-content .form-element {
  margin: 10px 0;
}
.form .tab-content .form-element input {
  width: 100%;
  padding: 10px;
  border: 1px solid #aaa;
  font-size: 16px;
  background: #f5f5f5;
  border-radius: 5px;
  outline: none;
}
.form .tab-content .form-element input[type='checkbox'] {
  width: 30px;
  margin: 8px 0;
  margin-left: -5px;
}
.form .tab-content .form-element label {
  color: #111;
}
.form .tab-content .form-element button {
  margin-top: 5px;
  width: 100%;
  padding: 10px;
  border: none;
  outline: none;
  background: #00acee;
  color: #f5f5f5;
  font-size: 16px;
  text-transform: uppercase;
  cursor: pointer;
  border-radius: 5px;
}
.form .tab-content > div.active {
  display: block;
}
.form .tab-content > div {
  display: none;
}
</style>