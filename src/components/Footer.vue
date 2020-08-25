<template>
  <footer>
    <div class="container">
      <div class="section-a">
        <h3 class="footer-logo">Shortly</h3>
      </div>

      <div class="section-b">
        <ul class="footer-nav">
          <li class="nav-heading">
            <a href="#" class="nav-link">Features</a>
          </li>
          <li class="nav-item">
            <a href="#" class="nav-link">Link Shortening</a>
          </li>
          <li class="nav-item">
            <a href="#" class="nav-link">Branded Links</a>
          </li>
          <li class="nav-item">
            <a href="#" class="nav-link">Analytics</a>
          </li>
        </ul>

        <ul class="footer-nav">
          <li class="nav-heading">
            <a href="#" class="nav-link">Resources</a>
          </li>
          <li class="nav-item">
            <a href="#" class="nav-link">Blog</a>
          </li>
          <li class="nav-item">
            <a href="#" class="nav-link">Developers</a>
          </li>
          <li class="nav-item">
            <a href="#" class="nav-link">Support</a>
          </li>
        </ul>

        <ul class="footer-nav">
          <li class="nav-heading">
            <a href="#" class="nav-link">Company</a>
          </li>
          <li class="nav-item">
            <a href="#" class="nav-link">About</a>
          </li>
          <li class="nav-item">
            <a href="#" class="nav-link">Our Team</a>
          </li>
          <li class="nav-item">
            <a href="#" class="nav-link">Careers</a>
          </li>
          <li class="nav-item">
            <a href="#" class="nav-link">Contact</a>
          </li>
        </ul>
      </div>

      <div class="section-c">
        <ul class="socials">
          <li class="social-icon">
            <a href="#">
              <img :src="require('@/assets/images/icon-facebook.svg')" alt />
            </a>
          </li>
          <li class="social-icon">
            <a href="#">
              <img :src="require('@/assets/images/icon-twitter.svg')" alt />
            </a>
          </li>
          <li class="social-icon">
            <a href="#">
              <img :src="require('@/assets/images/icon-pinterest.svg')" alt />
            </a>
          </li>
          <li class="social-icon">
            <a href="#">
              <img :src="require('@/assets/images/icon-instagram.svg')" alt />
            </a>
          </li>
        </ul>
      </div>
    </div>
  </footer>
</template>


<style scoped>
footer {
  background: var(--bg-dark-violet);
  color: white;
  padding: 2rem 0;
}

.footer-logo {
  font-size: 2rem;
}

.footer-nav {
  padding: 0 1rem;
}

footer > .container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 2rem;
}

.section-b {
  display: flex;
  justify-content: space-between;
}

.section-c > .socials {
  display: flex;
}

.section-c > .socials li {
  padding: 0 1rem;
}

.nav-link {
  color: white;
  font-weight: 500;
}

.nav-link:hover {
  color: var(--primary-color);
}

.nav-heading {
  margin-bottom: 1.3rem;
}

.nav-heading a {
  font-weight: 700;
}

.nav-item {
  padding-top: 0.8rem;
}

.nav-item a {
  color: var(--bg-gray);
}

/* Mobile screens */
@media (max-width: 768px) {
  footer > .container {
    text-align: center;
    grid-template-columns: 1fr;
  }

  .section-b {
    flex-direction: column;
  }

  .section-c > .socials {
    justify-content: center;
  }
  .footer-nav {
    padding: 1rem;
  }

  .nav-heading {
    margin-bottom: 0.7rem;
  }
  .nav-item {
    padding-top: 0.4rem;
  }
}

</style>