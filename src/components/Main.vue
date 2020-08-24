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

      <img
        :src="require('@/assets/images/illustration-working.svg')"
        alt
        class="illustration-image"
      />
    </main>

    <section class="container shortener-container">
      <div class="shortener rounded">
        <form class="shortener-form">
          <input type="text" placeholder="Shorten a link here..." class="rounded" />
          <button href="#" class="btn rounded btn-primary">Shorten it!</button>
        </form>
      </div>
    </section>

    <section class="statistics">
      <div class="container">
        <h3 class="statistics-title">Advanced Statistics</h3>
        <p class="statistics-text">
          Track how your links are performing across the web with
          <br />our advanced statistics dashboard
        </p>

        <div class="statistics-card-container">
          <div class="statistics-card card-a rounded">
            <div class="statistics-image-bg">
              <img
                :src="require('@/assets/images/icon-brand-recognition.svg')"
                alt="statistics image"
                class="statistics-image"
              />
            </div>
            <h4 class="statistics-card-heading">Brand Recognition</h4>
            <p
              class="statistics-card-text"
            >Boost your brand recognition with each click. Generic links don't mean a thing. Branded links helps instill confidence in your content.</p>
          </div>
          <div class="statistics-card card-b rounded">
            <div class="statistics-image-bg">
              <img
                :src="require('@/assets/images/icon-detailed-records.svg')"
                alt="statistics image"
                class="statistics-image"
              />
            </div>

            <h4 class="statistics-card-heading">Detailed Records</h4>
            <p
              class="statistics-card-text"
            >Gain insights into who is clicking your links. Knowing when and where people engage with your content helps inform better decisions.</p>
          </div>
          <div class="statistics-card card-c rounded">
            <div class="statistics-image-bg">
              <img
                :src="require('@/assets/images/icon-fully-customizable.svg')"
                alt="statistics image"
                class="statistics-image"
              />
            </div>

            <h4 class="statistics-card-heading">Fully Customizable</h4>
            <p
              class="statistics-card-text"
            >Improve brand awareness and content discoverability through customizable links, supercharging audience engagement.</p>
          </div>
        </div>
      </div>
    </section>

    <section class="boost">
      <div class="container boost-container">
        <h4 class="boost-heading">Boost your links today</h4>
        <button href="#" class="btn btn-primary">Get started</button>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  data: () => ({
    // shortenImage
  }),
};
</script>

<style scoped>
/* main section */
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
  padding: 1rem 0;
}

.lead-text {
  padding: 1rem 0;
}

a {
  margin: 1rem 0 0 0;
}

.illustration-image {
  position: relative;
  right: -230px;
  width: 60%;
}

/* shortener section */
.shortener-container {
  position: relative;
  top: 0px;
}

.shortener {
  background: var(--dark-violet) no-repeat;
  background-size: cover;
  background-image: url("~@/assets/images/bg-shorten-desktop.svg");
  padding: 3.5rem;
  margin: 2rem 0;
}

.shortener-form {
  display: flex;
  justify-content: center;
}

.shortener-form input {
  display: inline-block;
  width: 75%;
  padding: 0.7rem 1.5rem;
  outline: none;
  border: none;
  font-size: 18px;
}

button {
  font-weight: 700;
  font-size: 18px;
}

/* statistics section */
.statistics {
  background: var(--bg-gray);
  padding: 5rem 0;
  margin-top: -140px;
}

.statistics-title {
  color: var(--bg-dark-violet);
  font-weight: 700;
  font-size: 40px;
  text-align: center;
  margin-top: 3rem;
}

.statistics-text {
  text-align: center;
  padding: 1rem;
}

.statistics-card-container {
  display: flex;
  justify-content: space-evenly;
  padding: 3rem 0;
  margin: 4rem 0;
}

.statistics-card {
  position: relative;
  background: white;
  max-height: 450px;
  max-width: 500px;
  margin: 1rem;
  padding-bottom: 3rem;
}

.statistics-image-bg {
  position: absolute;
  background-color: var(--bg-dark-violet);
  border-radius: 50%;
  height: 100px;
  width: 100px;
  top: -15%;
}

.statistics-image {
  position: absolute;
  top: 25%;
  left: 29%;
}

.statistics-card-heading {
  color: var(--bg-dark-violet);
  padding: 4rem 0 1rem 0;
  font-size: 28px;
  font-weight: 700;
}

.statistics-card.card-a {
  position: relative;
  top: 0;
}

.statistics-card.card-b {
  position: relative;
  top: 40px;
}

/* lines */
.statistics-card.card-b::before {
  display: block;
  content: "";
  position: absolute;
  top: 40%;
  left: -31px;
  height: 10px;
  width: 30px;
  background: var(--primary-color);
  z-index: 1;
}

/* lines */
.statistics-card.card-b::after {
  display: block;
  content: "";
  position: absolute;
  top: 40%;
  right: -31px;
  height: 10px;
  width: 30px;
  background: var(--primary-color);
  z-index: 1;
}

.statistics-card.card-c {
  position: relative;
  top: 80px;
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

@media (max-width: 768px) {
  /* main */
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
    margin: 2rem 0 0 0;
  }

  .illustration-image {
    right: -100px;
    width: 100%;
  }

  /* shortener */
  .shortener-form {
    flex-direction: column;
  }

  .shortener-form input,
  .shortener-form button {
    margin: 1rem 0;
    width: 100%;
  }

  .shortener-form button {
    padding: 0.7rem 1.5rem;
  }

  /* statustics */
  .statistics-card-container {
    flex-direction: column;
    margin: 2rem 0;
    text-align: center;
    margin: 4rem 1rem;
    padding: 0 1rem;
  }

  .statistics-card {
    margin-bottom: 2.5rem;
  }

  .statistics-image-bg {
    left: 35%;
  }

  .statistics-card-heading {
    padding-top: 3rem;
    font-size: 20px;
    text-align: center;
  }

  .statistics-card-text {
    text-align: center;
  }

  /* lines */
  .statistics-card.card-b::before {
    top: -29%;
    left: 50%;
    height: 45px;
    width: 10px;
  }

  /* lines */
  .statistics-card.card-b::after {
    top: 100%;
    left: 50%;
    height: 48px;
    width: 10px;
  }

  /* boost */
  .boost-heading {
    font-size: 25px;
    padding: 1rem;
  }
}
</style>

