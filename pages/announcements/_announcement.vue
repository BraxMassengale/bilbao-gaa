<template>
  <main>
    <section v-if="post">
      <nav class="mb-8" aria-label="go back">
        <router-back class="block" />
      </nav>

      <article>
        <h5
          v-if="post.createdAt"
          class="inline-block px-2 py-1 my-2 text-sm font-medium text-white whitespace-no-wrap rounded-sm bg-gray"
        >
          {{ formatDate(post.createdAt) }}
        </h5>
        <h1 class="">{{ post.title }}</h1>
        <p class="mt-1 mb-4 text-primary-600 dark:text-primary-400">{{ post.description }}</p>
        <nuxt-content :document="post" />
      </article>
    </section>
  </main>
</template>

<script>
export default {
  async asyncData({ $content, params, error }) {
    let post
    try {
      post = await $content('announcement', params.announcement).fetch()
    } catch (e) {
      error({ message: 'Announcement post not found' })
    }
    return { post }
  },
  methods: {
    formatDate(dateString) {
      const date = new Date(dateString)
      return date.toLocaleDateString(process.env.lang) || ''
    },
  },
}
</script>
