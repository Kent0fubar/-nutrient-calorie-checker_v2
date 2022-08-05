<template>
  <div class="body" style="margin:0; width:100%; height:100%; min-width:320px; background:#eae7dc;">
    <div class="container">
      <div class="loginForm">
        <p>User Id</p>
        <input type="text" placeholder="Enter your Id" v-bind="userId">
        <p>Password</p>
        <input type="text" placeholder="Enter your password" v-bind="userPassword">
        <br>
        <button style="float:right; margin:5px 10px 15px 76.5%; padding:5px 8px; color:#fff; border:1.5px solid lightseagreen; border-radius:10px; background:dimgray; cursor:pointer;">Sign in</button>
        <hr>
        <p style="text-align:center; margin:0;">New to this web-site?</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      userId: null,
      userPassword: null
    }
  }
}
</script>

<style scoped>
  p {
    text-align: left;
    margin: 10px 0 0 50px;
    color: #fff;
  }

  button:hover {
    background: gray !important;
    transition: all .3s;
  }

  input {
    text-align: center;
    height: 30px;
    width: 80%;
    max-width: 200px;
    opacity: 0.8;
    box-sizing: border-box;
    border-radius: 10px;
    border: 2px solid gray;
    margin: 5px 10px;
  }

  .container {
    width: 80%;
    margin: 0 auto;
    padding: 3% 0;
  }

  .loginForm {
    text-align: center;
    margin: 0 auto;
    width: 70%;
    max-width: 300px;
    height: 400px;
    border-radius: 10px;
    background: #333333;
    border: 2px solid #dedede;
  }
</style>