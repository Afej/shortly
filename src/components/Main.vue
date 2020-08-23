<template>
  <main class="container">
    <div class="main-content">
      <h2 class="lead-heading">More than just shorter links</h2>
      <p class="lead-text">
        Build your brand's recognition and get detailed
        insights on how your links are performing
      </p>
      <a href="#" class="btn btn-primary">Get Started</a>
    </div>

    <img :src="require('@/assets/images/illustration-working.svg')" alt />
  </main>
</template>

<script>
export default {};
</script>

<style scoped>
main {
  display: flex;
  align-items: center;
  justify-content: space-between;
  position: relative;
  padding: 2rem 1rem;
}

.lead-heading {
  color: var(--bg-dark-violet);
  font-weight: 700;
  font-size: 3.6rem;
  line-height: 1.2;
}

.lead-text {
  padding: 1rem 0;
}

a {
  margin: 1rem 0 0 0;
}

img {
  position: relative;
  right: -230px;
  width: 60%;
}

@media (max-width: 768px) {
  main {
    flex-direction: column;
    text-align: center;
  }

  .main-content {
    order: 2;
    margin: 1rem 0;
  }

  .lead-heading {
    font-size: 2rem;
  }

  img {
    right: -100px;
    width: 100%;
  }
}
</style>

