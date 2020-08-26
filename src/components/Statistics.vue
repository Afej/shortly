<template>
  <section class="statistics">
    <Shortener />

    <div class="container statistics-container">
      <h2 class="statistics-title">Advanced Statistics</h2>
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
          <h3 class="statistics-card-heading">Brand Recognition</h3>
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

          <h3 class="statistics-card-heading">Detailed Records</h3>
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

          <h3 class="statistics-card-heading">Fully Customizable</h3>
          <p
            class="statistics-card-text"
          >Improve brand awareness and content discoverability through customizable links, supercharging audience engagement.</p>
        </div>
      </div>
    </div>
  </section>
</template>


<script>
import Shortener from "./Shortener";
export default {
  components: {
    Shortener,
  },
};
</script>

<style scoped>
/* statistics section */
.statistics {
  background: rgb(240,241,246);
  padding: 0 0 3rem 0;
  margin-top: 6rem;
  position: relative;
  top: 3rem;
}

.statistics-container {
  margin-top: -100px;
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
  margin: 2rem 0 4rem 0;
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

@media (max-width: 768px) {
  /* statustics */
  .statistics-card-container {
    flex-direction: column;
    margin: 2rem 0;
    text-align: center;
    align-items: center;
    margin: 4rem 0;
    padding: 0;
  }

  .statistics-card {
    margin-bottom: 2.5rem;
  }

  .statistics-image-bg {
    left: 40%;
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
    top: -38%;
    left: 49%;
    height: 57px;
    width: 10px;
  }

  /* lines */
  .statistics-card.card-b::after {
    top: 100%;
    left: 49%;
    height: 57px;
    width: 10px;
  }
}

@media (max-width: 500px) {
  .statistics-image-bg {
    left: 35%;
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
    height: 48.5px;
    width: 10px;
  }
}
</style>