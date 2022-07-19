<template>
  <div class="author">
    <h1 v-if="showTitle" class="author__site-title">
      {{ $static.metadata.siteName }}
    </h1>

    <p class="author__intro">
      A Eco friendly lifestyle, Travel, Foodie Blogger + Photographer &amp; Vlogger Portfolio
    </p>

    <p class="author__links">
      <a href="https://www.instagram.com/niicoe_co/">Instagram</a> ·
      <a href="https://twitter.com/niicoe_co">Twitter</a> ·
      <a href="https://www.youtube.com/channel/UCzV2BYxwNJlgc67Szapji0g"> YouTube </a> ·
      <a href="https://www.tiktok.com/@niicoe_co">TikTok</a>
    </p>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<script>
export default {
  props: ['showTitle'],
};
</script>

<style lang="scss">
.author {
  margin: 0 auto;
  max-width: 500px;
  text-align: center;
  padding-bottom: calc(var(--space) / 2);

  &__image {
    border-radius: 100%;
    width: 90px;
    height: 90px;
    margin-bottom: 1em;
  }

  &__intro {
    opacity: 0.8;
  }

  &__site-title {
    margin: 0 auto;
    font-size: 1.5em;
    max-width: 400px;
  }

  &__links {
    margin-top: -0.5em;
    a {
      margin: 0 0.5em;
    }
  }
}
</style>
