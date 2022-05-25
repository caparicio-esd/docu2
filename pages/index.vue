<template>
  <main>
    <nuxt-content :document="page" />
  </main>
</template>

<script>
export default {
  async asyncData ({ $content }) {
    const page = await $content('home').fetch()
    return {
      page
    }
  }
}
</script>