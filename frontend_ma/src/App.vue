<template>
    <div id="app">
        <div>
            <b-img center v-bind="mainProps"
            src="data:image/png;base64,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"
            alt="Center image"></b-img>
        </div>
        <nav class="navbar navbar-light bg-light">
            <div class="container-fluid">
              
                <h1 class="navbar-brand">Novedades</h1>
                <h1 class="navbar-brand">Promociones</h1>
                <a class="navbar-brand">Toallas</a>
                <a class="navbar-brand">Osos</a>
                <a class="navbar-brand">Calcetas</a>
                <a class="navbar-brand">Ropa interior</a>
                
                <form class="d-flex">
                    <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
                    <button class="btn btn-outline-success" type="submit">Search</button>
                </form>
              
            </div>
        </nav>
        <router-view/>
    </div>
</template>

<script>
  export default {
    data() {
      return {
        mainProps: {width: 150, height: 70, class: 'm1' }
      }
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

nav {
  padding: 30px;
}

nav a {
    /* font-weight: bold; */
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: left;
    color: #2c3e50;
}

nav h1 {
  font-weight: bold
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
