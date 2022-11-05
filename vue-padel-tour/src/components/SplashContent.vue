<template>
  <div class="splash">
    <div class="midcard">
      <div class="forelayer">
        <img id="ball" src="../assets/pade-ball.png">
      </div>
      <div class="backlayer">
        <img id="player" src="../assets/padel-smash.png">
        <div class="tittling">
          <ul class="titling-left">
            <li><h1>it's</h1></li>
            <li><h1>to</h1></li>
            <li><h1>your</h1></li>
          </ul>
          <ul class="titling-right">
            <li><h1>time</h1></li>
            <li><h1>prove</h1></li>
            <li><h1 class="over">padel</h1></li>
          </ul>
          <h1 class="over">skills</h1>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'SplashContent',
  props: {
  }
})
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

  ul {
    list-style-type: none;
    padding: 0;
  }

  li {
    display: inline-block;
    margin: 0 1vh;
  }

  .splash {
    background-color: #9db7a9;
    // min-height: 130vh;
    height: 90%;
    width: 100%;
    font-family: 'StrogConcrete';
    display: flex;
    align-items: center;
    flex-direction: column;
  }

  @font-face {
      font-family: StrogConcrete;
      src: url("../assets/StrongConcrete-Bold.otf") format("opentype");
  }

  .midcard {
    display: flex;
    flex-direction: column;
    max-width: inherit;
    max-height: inherit;
    width: 70%;
    height: 100%;
  }

  .backlayer {
    width: inherit;
    height: inherit;

    display: flex;
    position: absolute;
    align-items: center;
    justify-content: center;
    flex-wrap: wrap;
    top: -5%;
    img {
      margin-top: 35vh;
      z-index: 9;
    }
  }

  h1 {
    margin:0;
    font-size: 12vh;
    line-height: 15vh;
  }

  .tittling {
    position:absolute;
    width: 100%;
    height: 60%;
    display: flex;

    ul ~ h1{
      width: 100%;
      margin-top: calc(15vh * 3);
      text-align: center;
    }
  }

  .over {
    // margin-left: 3vh;
    position: absolute;
    z-index: 30;
    color: red;
    animation: push-appear 3s ease-out;
    // text-shadow: -2px 0 black, 0 2px black, 2px 0 black, 0 -2px black;
  }

  .titling-left {
    // max-width: 50%;
    max-height: 80%;
    width: 45%;
    height: auto;
    position: absolute;
    display: flex;
    flex-direction: column;
    h1 {
      float: right;
    }

  }

  .titling-right {
    max-width: 50%;
    max-height: 80%;
    margin-left: 48%;
    width: auto;
    height: auto;
    position: absolute;
    display: flex;
    flex-direction: column;
    float: right;

    .over {
      margin-left: 3vh;
    }

  }

  .forelayer {
    position: absolute;
    width: inherit;
    height: 30%;
    align-items: center;
    display: flex;
    flex-direction: column;
    z-index: 10;
  }

  #ball {
    max-width: 50%;
    max-height: 70%;
    width: auto;
    height: auto;
    margin-right: 15%;
  }

  #player {
    max-width: inherit;
    max-height: 60%;
    width: auto;
    height: auto;
  }

  @keyframes slide-left {
    from {
      margin-left: 100%;
      width: 300%;
    }

    to {
      margin-left: 48%;
      width: 100%;
    }
  }

  @keyframes push-appear{
    0%   {opacity: 0;}
    25%  {opacity: 0;}
    70%  {opacity: 0;}
    79%  {transform: scale(1.0);}
    80%  {transform: scale(1.1); opacity: 1;}
    95%  {transform: scale(1.5);}
  }

</style>
