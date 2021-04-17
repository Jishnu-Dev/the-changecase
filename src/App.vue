<template>

<nav class="navbar navbar-expand-md navbar-light bg-none">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">ChangeCase</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarText" aria-controls="navbarText" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarText">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="#">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Features</a>
        </li>
        <li class="nav-item dropdown">
          <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-bs-toggle="dropdown" aria-expanded="false">
            More Tools
          </a>
          <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
            <li><a class="dropdown-item" href="#">Action</a></li>
            <li><a class="dropdown-item" href="#">Another action</a></li>
            <li><hr class="dropdown-divider"></li>
            <li><a class="dropdown-item" href="#">Something else here</a></li>
          </ul>
        </li>
      </ul>
      <span class="navbar-text">
        <a class="nav-link" href="#">A project by <a href="https://github.com/Jishnu-Dev" target="_blank">Jishnu Raj ✔️</a></a>
      </span>
    </div>
  </div>
</nav>

  <img class="intro-img" alt="Vue logo" src="./assets/animated-intro.svg">
  <HelloWorld msg="The Changecase By Jishnu Raj"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.intro-img {
  width: 25vw !important;
  height: auto;
}
@media (max-width: 576px){
  .intro-img {
    width: 80vw !important;
    height: auto;
  }
}
@media (max-width: 768px){
  .intro-img {
    width: 48vw !important;
    height: auto;
  }
}
</style>
