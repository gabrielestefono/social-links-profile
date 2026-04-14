<script setup lang="ts">
import ButtonComponent from "./components/ButtonComponent.vue";
</script>

<template>
  <main>
    <article class="container">
      <header class="header">
        <figure>
          <img src="/public/profile-pic.png" alt="Jessica Randall" class="image" />
          <figcaption class="sr-only">Thumbnail of social media profile</figcaption>
        </figure>
        <div>
          <h1>Jessica Randall</h1>
          <address>London, United Kingdom</address>
        </div>
      </header>
      <section>
        <p>"Front-end developer and avid reader."</p>
      </section>
      <footer>
        <nav>
          <ul>
            <li>
              <ButtonComponent>GitHub</ButtonComponent>
            </li>
            <li>
              <ButtonComponent>FrontendMentor</ButtonComponent>
            </li>
            <li>
              <ButtonComponent>LinkedIn</ButtonComponent>
            </li>
            <li>
              <ButtonComponent>Twitter</ButtonComponent>
            </li>
            <li>
              <ButtonComponent>Instagram</ButtonComponent>
            </li>
          </ul>
        </nav>
      </footer>
    </article>
  </main>
</template>

<style scoped>
main {
  width: 100%;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

.container {
  background-color: var(--gray-800);
  width: 100%;
  height: fit-content;
  margin: var(--spacing-300);
  padding: var(--spacing-300);
  border-radius: var(--spacing-150);
  display: flex;
  flex-direction: column;
  max-width: 24rem;
}

.header {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: var(--spacing-300);
}

.header > figure {
  height: 5.5rem;
}

.image {
  width: 5.5rem;
  height: 5.5rem;
  border-radius: 50%;
}

.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  white-space: nowrap;
  border: 0;
  clip-path: inset(50%);
  clip: rect(0 0 0 0);
}

h1 {
  font: var(--preset-01);
  color: var(--white);
  margin-bottom: 4px;
}

address {
  font: var(--preset-02-bold);
  color: var(--green);
}

section {
  margin: var(--spacing-300) 0;
  text-align: center;
}

footer > nav > ul {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-200);
  list-style: none;
}

@media screen and (min-width: 600px) {
  .container {
    padding: var(--spacing-500);
  }
}
</style>
