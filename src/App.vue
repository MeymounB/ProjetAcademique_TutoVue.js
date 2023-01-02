<template>
  <h1>Meymoun Boualaoui</h1>
  <p>Creative Developper</p>
  <nav>
    <router-link to="/">Accueil</router-link>
    <router-link to="/projets">Projets</router-link>
    <router-link to="/contact">Contact</router-link>
  </nav>
  <div class="trait"></div>
  <div class="mainContent">
    <p>Student in third year at Epsi, it has been now many years that I have interest in IT and
      partciluray in Web Development.</p>
    <p>For the moment, I prefer front-end (React/Vue) than back-end, but I'm
      open-minded.</p>
    <p>I'm actually looking for new experiences. Don't hesitate to contact me !</p>
  </div>
  <div class="trait"></div>
  <router-view />
  <br>
  <div class="trait"></div>
  <br>
  <footer>
    <nav>
      <div><router-link to="/">Accueil</router-link></div>
      <div><router-link to="/projets">Projets</router-link></div>
      <div><router-link to="/contact">Contact</router-link></div>
    </nav>
  </footer>
</template>

<style>
/* .disappear {
  display: none;
} */

#app {
  text-align: center;
  color: #2c3e50;
}

nav {
  display: flex;
  flex-direction: row;
  gap: 20px;
  justify-content: center;

  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}

.mainContent {
  margin: 0 100px;
}

p {
  font-size: large;
  text-align: center;
}

main>div>p:first-child {
  margin-bottom: 0;
}

p:nth-child(2) {
  margin: 0;
}

@media screen and (max-width: 1080px) {
  .mainContent {
    padding: 20px 60px 10px;
  }
}

.trait {
  margin: 0 100px;
  height: 1px;
  background-color: black;
}

footer {
  display: flex;
  flex-direction: row;
  justify-content: center;
  justify-items: center;
  align-items: center;
  align-content: center;
  flex-wrap: nowrap;
  gap: 20px;
}
</style>
