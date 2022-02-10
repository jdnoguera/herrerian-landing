<template>
  <v-app>
    <!-- app bar -->
    <v-app-bar app color="#728ca3" height="100" clipped-left elevation="0">
      <div class="container">
        <nuxt-link to="/">
          <v-img :src="logo" height="80" width="200" contain alt="Biggie"/>
        </nuxt-link>

        <nav>
          <nuxt-link class="nav-item" to="/" exact-active-class="focused">Inicio</nuxt-link>
          <nuxt-link class="nav-item" to="/products" exact-active-class="focused">Productos</nuxt-link>
          <nuxt-link class="nav-item" to="/contact" exact-active-class="focused">Contacto</nuxt-link>
        </nav>

        <div class="d-flex align-center">
          <v-btn icon>
            <v-icon>mdi-instagram</v-icon>
          </v-btn>

          <v-btn icon>
            <v-icon>mdi-facebook</v-icon>
          </v-btn>
        </div>
      </div>
    </v-app-bar>

    <!-- Content -->
    <v-main>
      <div>
        <Nuxt />
      </div>
    </v-main>

    <!-- footer -->

  </v-app>
</template>

<script>
export default {
  name: "default",
  data: () => ({
    logo: require("static/smith-logo.png")
  }),
}
</script>

<style scoped>
.container {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.nav-item {
  font-family: Alef,serif;
  text-decoration: none;
  margin-left: 10px;
  font-size: 20px;
  font-weight: bold;
  color: white;
  letter-spacing: 0.0rem;
}
</style>
