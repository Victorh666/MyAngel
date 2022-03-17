<template>
    <div id="app">
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

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
