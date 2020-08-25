<template>
  <section class="container shortener-container">
    <div class="shortener rounded">
      <div class="shortener-content">
        <form class="shortener-form" @submit.prevent="shortenUrl">
          <input
            type="text"
            placeholder="Shorten a link here..."
            class="rounded"
            v-model="linkUrl"
            :class="{error}"
          />
          <button class="btn rounded btn-primary">Shorten it!</button>
        </form>
        <p v-if="error" class="error-text">Please add a link</p>
      </div>
    </div>

    <div class="links-container" v-if="links">
      <div class="link-card rounded" v-for="link in links" :key="link.hashid">
        <p class="long-link">{{link.url}}</p>
        <div class="rel-content">
          <p class="rel-link">
            <a :href="link.relUrl">{{link.relUrl}}</a>
          </p>
          <button
            class="btn rounded btn-primary copy"
            ref="copy"
          >Copy</button>
          <!-- <button
            class="btn rounded btn-primary copy"
            v-clipboard="link.relUrl"
            v-clipboard:success="clipboardSuccessHandler"
            ref="copy"
          >Copy</button> -->
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import axios from "axios";

export default {
  data: () => ({
    links: [],
    linkUrl: "",
    error: false,
  }),
  mounted() {
    if (localStorage.getItem("links")) {
      this.links = JSON.parse(localStorage.getItem("links"));
    }
  },
  methods: {
    shortenUrl() {
      if (this.linkUrl !== "") {
        const url = this.linkUrl.trim();
        axios.post("https://rel.ink/api/links/", { url }).then((res) => {
          let data = {
            url: `${res.data.url.slice(0, 30)}...`,
            relUrl: `https://rel.ink/${res.data.hashid}`,
          };

          this.links.unshift(data);

          const ls = this.links;
          // console.log(ls)

          localStorage.setItem("links", JSON.stringify(ls));
        });

        this.error = false;
      } else {
        this.error = true;
      }

      this.linkUrl = "";
    },
    // clipboardSuccessHandler() {
    //   this.$refs.copy.innerHTML = "Copied!";
    //   this.$refs.copy.style.backgroundColor = "var(--dark-violet)";
    // },
  },
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

.shortener-form input.error {
  border: 3px solid var(--secondary-color);
}
.shortener-form input.error::placeholder {
  color: var(--secondary-color);
}

.error-text {
  color: var(--secondary-color);
  font-style: italic;
  margin: 0.5rem 0;
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

.long-link {
  color: var(--bg-dark-violet);
  font-weight: 700;
}

.rel-link a {
  color: var(--primary-color);
}

.copy {
  padding: 1rem 2rem;
}

/* ////////////// */
/* Media Queries */
/* //////////// */

@media (min-width: 1200px) {
  .shortener-form {
    justify-content: space-between;
  }
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
    align-items: flex-start;
  }

  .rel-content {
    width: 100%;
    align-items: flex-start;
  }

  .rel-link {
    margin-bottom: 0.5rem;
  }

  .copy {
    display: block;
    width: 100%;
    margin: 0;
  }
}
</style>