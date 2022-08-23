<template>
  <main>
    <section v-if="posts" class="w-full max-w-5xl mx-auto">
      <h1 class="title">Announcements</h1>
      <posts post-type="blog" :amount="10" />
    </section>
  </main>
</template>

<script>
export default {
  async asyncData({ $content, error }) {
    let posts
    try {
      posts = await $content('announcement').fetch()
    } catch (e) {
      error({ message: 'Announcement posts not found' })
    }
    return { posts }
  },
}
</script>
