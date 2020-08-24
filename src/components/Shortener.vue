<template>
  <section class="container shortener-container">
    <div class="shortener rounded">
      <form class="shortener-form">
        <input type="text" placeholder="Shorten a link here..." class="rounded" />
        <p v-if="error">Please add a link</p>
        <button href="#" class="btn rounded btn-primary">Shorten it!</button>
      </form>
    </div>

    <div class="links-container" v-if="links !== null">
      <div class="link-card rounded">
        <p class="long-link">
          <a href="#">https://www.frontendmentor.io</a>
        </p>

        <div class="rel-content">
          <p class="rel-link">
            <a href="#">https://rel.ink/</a>
          </p>
          <button href="#" class="btn rounded btn-primary copy">Copy</button>
        </div>
      </div>
      <div class="link-card rounded">
        <p class="long-link">
          <a href="#">https://www.frontendmentor.io</a>
        </p>

        <div class="rel-content">
          <p class="rel-link">
            <a href="#">https://rel.ink/</a>
          </p>
          <button href="#" class="btn rounded btn-primary copy">Copy</button>
        </div>
      </div>
      <div class="link-card rounded">
        <p class="long-link">
          <a href="#">https://www.frontendmentor.io</a>
        </p>

        <div class="rel-content">
          <p class="rel-link">
            <a href="#">https://rel.ink/</a>
          </p>
          <button href="#" class="btn rounded btn-primary copy">Copy</button>
        </div>
      </div>
      <div class="link-card rounded">
        <p class="long-link">
          <a href="#">https://www.frontendmentor.io</a>
        </p>
        <div class="rel-content">
          <p class="rel-link">
            <a href="#">https://rel.ink/</a>
          </p>
          <button href="#" class="btn rounded btn-primary copy">Copy</button>
        </div>
      </div>
      <div class="link-card rounded">
        <p class="long-link">
          <a href="#">https://www.frontendmentor.io</a>
        </p>
        <div class="rel-content">
          <p class="rel-link">
            <a href="#">https://rel.ink/</a>
          </p>
          <button href="#" class="btn rounded btn-primary copy">Copy</button>
        </div>
      </div>
      <div class="link-card rounded">
        <p class="long-link">
          <a href="#">https://www.frontendmentor.io</a>
        </p>
        <div class="rel-content">
          <p class="rel-link">
            <a href="#">https://rel.ink/</a>
          </p>
          <button href="#" class="btn rounded btn-primary copy">Copy</button>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data: () => ({
    links: [],
  }),
  methods: {},
};
</script>

<style scoped>
/* shortener section */
.shortener-container {
  position: relative;
  top: -140px;
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


.link-card {
  padding: 0 2rem;
}

.link-card,
.rel-content {
  display: flex;
  background: white;
  align-items: center;
  justify-content: space-between;
  margin: 1rem 0;
}

.long-link a {
  color: var(--bg-dark-violet);
  font-weight: 700;
}

.rel-link a {
  color: var(--primary-color);
}

.copy {
  padding: 1rem 2rem;
}

@media (max-width: 768px) {
  /* shortener */
  .shortener {
    background-image: url("~@/assets/images/bg-shorten-mobile.svg");
    padding: 1.5rem;
  }

  .shortener-form,
  .link-card,
  .rel-content {
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

  .link-card {
    padding-top: 1rem;
  }

  .rel-content {
    width: 100%;
    align-items: flex-start;
  }

  .rel-link {
    margin-bottom: 0.5rem;
  }

  .copy{
    display: block;
    width: 100%;
    margin: 0;
  }
}
</style>