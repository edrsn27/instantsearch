<template>
  <div class="container">
    <div>
      <h1 class="title">
        Algolia Vue Instant Search
      </h1>
      <p class="subtitle">
        Let's make search and filter thru thousands of query extremely fast
      </p>

      <nuxt-link to="/products">see example</nuxt-link>
      <p>Styled using <a href="https://getbootstrap.com/">Bootstrap</a></p>
      <p>Seach Engine using <a href=" https://www.algolia.com/">Algoia</a></p>

      <p>by <a href="https://github.com/edrsn27">@edrsn27</a></p>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
