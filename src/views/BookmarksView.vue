<script>
import { RouterLink } from "vue-router";
import CirclesComponent from "@/components/CirclesComponent.vue";
import PostComponent from "@/components/PostComponent.vue";
import AccountComponent from "@/components/AccountComponent.vue";

export default {
  name: "HomeView",
  components: {
    AccountComponent,
    CirclesComponent,
    PostComponent
  },
  data() {
    return {
    }
  }
}
</script>

<template>
  <section class="home">

    <article class="middle">
      <section class="top-part-section">
        <RouterLink to="/" class="top-part">For you</RouterLink>
        <RouterLink to="/" class="top-part">Followed</RouterLink>
      </section>
      <PostComponent class="post"/>
      <PostComponent class="post"/>
      <PostComponent class="post"/>
    </article>

  </section>
</template>

<style scoped>
  .top-part-section {
    display: flex;
    gap: 20px;
    border-bottom: rgba(255, 255, 255, .15) solid 2px;
    padding: 10px 0;
    min-width: 100%;
  }
  .top-part {
    text-decoration: none;
    color: white;
    font-weight: bold;
    font-size: 1.2rem;
  }
  .middle {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  .post {
    max-width: 100%;
  }
  .home {
    display: flex;
    justify-content: center;
  }
  h2 {
    font-family: "Segoe UI", sans-serif;
    font-size: 1.2rem;
    color: rgba(255, 255, 255, .55);
    font-weight: normal;
  }
  p {
    margin-top: 3rem;
    color: rgba(255, 255, 255, .55);
  }

</style>