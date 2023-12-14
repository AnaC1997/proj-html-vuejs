<script>
import { store } from "../store.js"

export default {
  name: "PageHeader",
  props: ["info"],
  data() {
    return {
      store
    }
  },
  methods: {
    getImagePath: function (img) {
      return new URL(`../assets/svgs/${img}`, import.meta.url).href;
    }

  },
  mounted() {

  }
}
</script>

<template>

    <nav class="navbar navbar-expand-lg styleNav">
      <div class="container">
        <a class="navbar-brand" href="#"><img :src="getImagePath(info.img)" alt=""></a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavDropdown"
          aria-controls="navbarNavDropdown" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNavDropdown">
          <ul v-for="(options, key) in info.options" :key="key" class="navbar-nav">
            <li class="nav-item dropdown">
              <a class="nav-link dropdown-toggle overflow grey" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
                {{ options.title }}
              </a>
              <ul class="dropdown-menu grey">
                <li v-for="option in options.items" :key="option"><a class="dropdown-item" href="#">{{ option }}</a></li>
              </ul>
            </li>
          </ul>
        </div>
        <form class="d-flex" role="search">
          <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
          <button class="btn btn-outline-success" type="submit">BUY NEXGEN</button>
        </form>
      </div>
    </nav>
</template>

<style scoped lang="scss">
// importo variabili
@use '../styles/partials/variables' as *;

.styleNav {
  height: 10vh;
  background-color: #102638;

  img {
    width: 50%;
  }

  form{
    width: 25%;
    height: 2rem;
  }
  button{
    width: 100%;

  }

  .grey{
    color: #828D94;;
  }
 


}
</style>
