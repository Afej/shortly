<template>
  <div>
    <main class="container">
      <div class="main-content">
        <h2 class="lead-heading">More than just shorter links</h2>
        <p class="lead-text">
          Build your brand's recognition and get detailed
          insights on how your links are performing
        </p>
        <a href="#" class="btn btn-primary">Get Started</a>
      </div>
      <div class="bg-main">
        <img
          :src="require('@/assets/images/illustration-working.svg')"
          alt="illustration-image"
          class="illustration-image"
        />
      </div>
    </main>

    <Statistics />

    <section class="boost">
      <div class="container boost-container">
        <h2 class="boost-heading">Boost your links today</h2>
        <a href="#" class="btn btn-primary">Get started</a>
      </div>
    </section>
  </div>
</template>

<script>
import Statistics from "./Statistics";

export default {
  components: {
    Statistics,
  },
};
</script>

<style scoped>
/* main section */
main {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 2rem 0 2rem 1rem;
  margin-right: 0;
  margin-bottom: 2rem;
}

.main-content {
  margin-left: -70px;
  position: relative;
  left: -35px;
}

.lead-heading {
  color: var(--bg-dark-violet);
  font-weight: 700;
  font-size: 4.5rem;
  line-height: 1;
  padding: 1rem 0;
}

.lead-text {
  padding: 1rem 0;
}

a {
  margin: 1rem 0 0 0;
}

.bg-main {
  width: 100vw;
  overflow: hidden;
}

.illustration-image {
  position: relative;
  right: -80px;
  width: 100%;
}

/* boost section */
.boost {
  background: var(--dark-violet) no-repeat;
  background-size: cover;
  background-image: url("~@/assets/images/bg-boost-desktop.svg");
  padding: 2rem;
}

.boost-container {
  text-align: center;
}

.boost-heading {
  color: white;
  padding: 2rem;
  font-weight: 700;
  font-size: 35px;
}

/* media queries */

@media (max-width: 1024px) {
  .main-content {
    margin-left: -70px;
    position: relative;
    left: -10px;
  }
}

@media (max-width: 768px) {
  /* main */
  main {
    flex-direction: column;
    text-align: center;
    margin: 0 auto;
  }

  .main-content {
    order: 2;
    margin: 1rem 0;
  }

  .lead-heading {
    font-size: 2.5rem;
    margin: 0;
    padding-top: 2rem;
  }

  .bg-main {
    width: 100vw;
    overflow: hidden;
    padding: 5px 20px;
  }

  .illustration-image {
    right: -10px;
    width: 120%;
  }

  /* boost */
  .boost-heading {
    font-size: 25px;
    padding: 1rem;
  }
}

@media (max-width: 500px) {
  .illustration-image {
    right: 0;
    width: 140%;
  }
}
</style>

