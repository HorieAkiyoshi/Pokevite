<script setup></script>

<template>
  <nav class="navbar navbar-expand-lg navbar-dark bg-primary">
    <div class="container-fluid">
      <router-link class="navbar-brand" to="/">
        <img
          src="https://cdn-icons-png.flaticon.com/512/188/188987.png"
          alt="PokeVite Logo"
          width="30"
          height="24"
          class="d-inline-block align-text-top"
        />
        PokeVite
      </router-link>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNav"
        aria-controls="navbarNav"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item">
            <router-link class="nav-link" aria-current="page" to="/">Home</router-link>
          </li>
          <li class="nav-item">
            <router-link class="nav-link" to="/about">About</router-link>
          </li>
        </ul>
      </div>
    </div>
  </nav>

  <!-- Content -->
  <div class="main">
    <router-view></router-view>
  </div>

  <footer class="bg-primary text-light">
    <div>Design in {{ new Date().getFullYear() }}</div>
  </footer>
</template>

<style>
body {
  box-sizing: border-box;
  height: 100vh;
  background: #4e9bed;
  background: linear-gradient(0deg, rgba(78, 155, 237, 1) 0%, rgba(20, 26, 199, 1) 67%);
}

footer {
  position: fixed;
  bottom: 0;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 56px;
}
</style>
