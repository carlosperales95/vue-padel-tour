<template>
  <header>
    <router-link to="/">
      <img alt="Vue logo" src="../assets/logo.png" height="50">
    </router-link>
    <p>EspaÑish Padel Tournament</p>
    <nav>
      <ul>
        <li><router-link to="/info">El torneo</router-link></li>
        <li><router-link to="/register">Apuntate</router-link></li>
        <li><router-link to="/about">Sobre Nosotros</router-link></li>
      </ul>
    </nav>
  </header>
</template>

<style lang="scss">
  header {
    display: flex;
    border-bottom: 1px solid #ccc;
    padding: .5rem 1rem;

    p {
      margin-left: 1rem;
    }
  }

  a {
    color: #ccc;
    text-decoration: none;
    font-size: 1.5em;
    font-weight: 600;

    &:hover{

      color: aqua;

    }
  }

  nav {
    margin-left: auto;

    ul {
      list-style: none;
    }

    ul li {
      display: inline-flex;
      margin-left: 1rem;
    }
  }
</style>
