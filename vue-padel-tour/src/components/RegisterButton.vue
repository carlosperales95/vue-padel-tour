<template>
    <div class="undertitle">
        <a href="https://docs.google.com/forms/d/e/1FAIpQLScwWGUPVgSSKEO62GzD7y8m0qOtBX3z0gqt9ASCWYRFubctJw/viewform?usp=sharing">
          <button type="button">Register now</button>
        </a>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'RegisterButton',
  props: {
  }
})
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

  .undertitle {
    width: 100%;
    display: flex;
    // position: absolute;
    align-items: center;
    justify-content: center;
    margin-top: 0vh;
    transform: rotatex(10deg);
    animation: rotateAngle 6s linear infinite;
    a {
      text-decoration: none;
    }
  }

  button {
    display: block;
    position: relative;
    margin: 0.5em 0;
    padding: .8em 2.2em;
    cursor: pointer;
    color: red;

    background: #d1ebde;
    border: solid 2px red;
    border-radius: .4em;

    text-transform: uppercase;
    font-size: 1.4em;
    font-family: "Work Sans", sans-serif;
    font-weight: 500;
    letter-spacing: 0.04em;

    mix-blend-mode: color-dodge;
    perspective: 500px;
    transform-style: preserve-3d;

    animation: appear 3.5s ease-out;

    &:before, &:after {
      --z: 0px;
      position: absolute;
      top: 0;
      left: 0;
      display: block;
      content: '';
      width: 100%;
      height: 100%;
      opacity: 0;
      mix-blend-mode: inherit;
      border-radius: inherit;
      transform-style: preserve-3d;
      transform: translate3d(
        calc(var(--z) * 0px),
        calc(var(--z) * 0px),
        calc(var(--z) * 0px)
      );
    }
    span {
      mix-blend-mode: none;
      display: block;
    }
    &:after {
      background-color: #5D00FF;
    }
    &:before {
      background-color: #FF1731;
    }
    &:hover {
      background-color: #FFF65B;
      transition: background .3s 0.1s;
    }
    &:hover:before {
      --z: 0.04;
      animation: translateWobble 2.2s ease forwards;
    }
    &:hover:after {
      --z: -0.06;
      animation: translateWobble 2.2s ease forwards;
    }
  }

  @keyframes rotateAngle {
    0% {
      transform: rotateY(0deg) rotateX(10deg);
      animation-timing-function: cubic-bezier(0.61, 1, 0.88, 1);
    }
    25% {
      transform: rotateY(20deg) rotateX(10deg);
    }
    50% {
      transform: rotateY(0deg) rotateX(10deg);
      animation-timing-function: cubic-bezier(0.61, 1, 0.88, 1);
    }
    75% {
      transform: rotateY(-20deg) rotateX(10deg);
    }
    100% {
      transform: rotateY(0deg) rotateX(10deg);
    }
  }

  @keyframes translateWobble {
    0% {
      opacity: 0;
      transform: translate3d(
        calc(var(--z) * 0px),
        calc(var(--z) * 0px),
        calc(var(--z) * 0px)
      );
    }
    16% {
      transform: translate3d(
        calc(var(--z) * 160px),
        calc(var(--z) * 160px),
        calc(var(--z) * 160px)
      );
    }
    28% {
      opacity: 1;
      transform: translate3d(
        calc(var(--z) * 70px),
        calc(var(--z) * 70px),
        calc(var(--z) * 70px)
      );
    }
    44% {
      transform: translate3d(
        calc(var(--z) * 130px),
        calc(var(--z) * 130px),
        calc(var(--z) * 130px)
      );
    }
    59% {
      transform: translate3d(
        calc(var(--z) * 85px),
        calc(var(--z) * 85px),
        calc(var(--z) * 85px)
      );
    }
    73% {
      transform: translate3d(
        calc(var(--z) * 110px),
        calc(var(--z) * 110px),
        calc(var(--z) * 110px)
      );
    }
    88% {
      opacity: 1;
      transform: translate3d(
        calc(var(--z) * 90px),
        calc(var(--z) * 90px),
        calc(var(--z) * 90px)
      );
    }
    100% {
      opacity: 1;
      transform: translate3d(
        calc(var(--z) * 100px),
        calc(var(--z) * 100px),
        calc(var(--z) * 100px)
      );
    }
  }

  @keyframes appear{
    0%   {opacity: 0;}
    89%   {opacity: 0;}
    99%     {opacity:1;}
  }

</style>
