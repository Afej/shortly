<template>
  <header class="container">
    <nav class="navbar">
      <h1 class="logo">Shortly</h1>

      <ul class="nav">
        <li class="nav-item">
          <a href="#" class="nav-link">Features</a>
        </li>
        <li class="nav-item">
          <a href="#" class="nav-link">Pricing</a>
        </li>
        <li class="nav-item">
          <a href="#" class="nav-link">Resources</a>
        </li>
      </ul>
    </nav>


    <ul class="nav">
      <li class="nav-item">
        <a href="#" class="nav-link">Login</a>
      </li>
      <li class="nav-item">
        <a href="#" class="btn btn-primary">Sign Up</a>
      </li>
    </ul>
  </header>
</template>

<script>
export default {};
</script>

<style scoped>
header {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.logo {
  color: var(--bg-dark-violet);
  font-size: 2.5rem;
}

.navbar {
  display: flex;
}

.nav {
  display: flex;
  align-items: center;
  justify-content: space-evenly;
  padding: 0 3rem;
}

a{
  font-weight: 700;
}

.nav-link:hover{
   color: var(--bg-dark-violet);
}
</style>