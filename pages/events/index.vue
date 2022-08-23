<template>
  <main>
    <section v-if="posts" class="w-full max-w-5xl mx-auto">
      <nav class="mb-8" aria-label="go back">
        <router-back class="block" />
      </nav>
      <h1 class="title">Events</h1>
      <posts post-type="events" :amount="10" />
    </section>
  </main>
</template>

<script>
export default {
  async asyncData({ $content, error }) {
    let posts
    try {
      posts = await $content('events').fetch()
    } catch (e) {
      error({ message: 'Event posts not found' })
    }
    return { posts }
  },
}
</script>
