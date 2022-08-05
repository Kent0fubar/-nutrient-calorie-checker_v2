<template>
  <div class="header">
      <h3 style="height:100%; margin:0; padding-left:10px; padding-top:3px;"><router-link to="/">Nutrient & Calorie Checker ✓</router-link></h3>
      <button class="menuBtn" @click="isOpen = !isOpen" :class="{'open' : isOpen === true}" style="position: absolute; top:5px; right: 10px; height:30px; width:40px; margin:0 5px 0 auto; padding:0; border:0; border-radius:5px; background-color:#fff; z-index:500; cursor:pointer;">
          <span></span>
          <span style="margin:5.5px auto;"></span>
          <span></span>
      </button>
      <transition name="fade" mode="out-in" appear>
          <div v-if="isOpen === true" style="position:fixed; top:0; left:0; z-index:100; width:100%; height:120%; background-color: rgba(0, 0, 0, 0.6)">
              <ul  class="menuWindow" style="list-style:none; width:130px; position:absolute; top:40px; right:0%; padding:0; margin:0; border:0.5px solid #dedede; background-color:#333333; z-index:1;">
                  <li>Daily Record</li>
                  <li @click="isOpen = false"><router-link to="/login">Login</router-link></li>
                  <li>Sign Up</li>
                  <li>Contact Us</li>
              </ul>
          </div>
      </transition>
  </div>
  <router-view/>
  <div class="footer" style="background-color:#333333">
            <ul class="footerMenu" style="float:right; margin:0; padding-right:10px;">
                <li>Contact Us</li>
                <li>Terms of Use</li>
            </ul>
            <p style="padding-left:10px;">Nutrient</p>
            <p style="padding-left:10px;">& Calorie Checker</p>
        </div>
</template>

<script>

export default {
  setup() {
    
  },
  data() {
    return {
      isOpen: false
    }
  }
}
</script>


<style>

body {
  margin: 0;
}

a {
  color: #fff;
  text-decoration: none;
}

.header {
        height: 30px;
        width: 100%;
        padding: 5px 0px;
        background-color: #333333;
        color: #fff;
        display: flex;
    }

    .menuBtn span {
        display: block;
        position: relative;
        height: 3px;
        width: 20px;
        background-color: #333333;
        border-radius: 5px;
        margin: 0 auto;
        transition: all .5s;
    }

    .menuBtn.open span:nth-of-type(1) {
        top: 2.5px !important;
        background: #ff6666;
        transform: translateY(6px) rotate(-50deg);
    }

    .menuBtn.open span:nth-of-type(2) {
        opacity: 0;
    }

    .menuBtn.open span:nth-of-type(3) {
        top: -2px !important;
        background: #ff6666;
        transform: translateY(-6px) rotate(50deg);
    }

    .menuWindow li {
        text-align: center;
        padding: 15px;
        box-sizing: border-box;
        border: 1px solid #dedede;
    }

    .footer {
        height: 100px;
        width: 100%;
        padding: 10px 0px;
    }

    .footer p, li {
        color: #fff;
        margin: 0;
        list-style: none;
    }
</style>
