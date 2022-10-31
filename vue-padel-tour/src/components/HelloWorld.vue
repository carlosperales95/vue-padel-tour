<template>
  <div class="splash">
    <div class="forelayer">
      <img id="ball" src="../assets/pade-ball.png">
    </div>
    <div class="backlayer">
      <img id="player" src="../assets/padel-smash.png">
      <ul class="titling">
        <li><h1 class="left-side">El</h1></li>
        <li><h1 class="right-side">mejor</h1></li>
        <li><h1>torneo</h1></li>
        <li><h1>de</h1></li>
      </ul>
    </div>
    <div class="last">
      <ul>
        <li><h1>padel</h1></li>
        <li><h1 class="under">para</h1></li>
        <li><h1>los</h1></li>
        <li><h1>que saben</h1></li>
      </ul>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'HelloWorld',
  props: {
    msg: String
  }
})
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

.splash {
  background-color: #9db7a9;
  min-height: 130vh;
  font-family: 'StrogConcrete';
}

@font-face {
    font-family: StrogConcrete;
    src: url("../assets/StrongConcrete-Bold.otf") format("opentype");
}

.backlayer {
  width: 100%;
  display: flex;
  position: absolute;
  align-items: center;
  justify-content: center;
  img {
    margin-top: 35vh;
    z-index: 9;
  }
  .titling {
    width: 60%;
    position: absolute;
    top:10vh;
    left: 40vh;
    display: flex;
    flex-direction: column;
    h1 {
      font-size: 15vh;
      margin:0;
    }
    .right-side {
      float: right !important;
      margin-right: 15vh
    }
  }
}

.last {
  position: absolute;
  z-index: 12;
  font-size: 8vh;
  width: 60%;
  top: 62vh;
  left: 40vh;

  h1 {
    margin:0;
  }
}

.forelayer {
  position: absolute;
  max-width: 100%;
  align-items: center;
  justify-content: center;
  margin-left: 60vh;
  z-index: 10;
}

#ball {
  height: 35vh;
}

#player {
  height: 80vh;
}
</style>
