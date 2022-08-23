<template>
  <main>
    <section class="flex flex-col items-center self-center justify-center flex-1">
      <h1 class="text-center title">Euskadi Gaels</h1>
      <h2 class="text-center subtitle">Bilbao's Gaelic Football Club</h2>
    </section>

    <section class="p-8 mt-8 bg-green-600">
      <h2 class="text-center text-white">Who are the Euskadi Gaels?</h2>
      <p class="max-w-5xl mx-auto text-white">
        Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem
        aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo.
      </p>
      <p class="max-w-5xl mx-auto text-white">
        Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni dolores
        eos qui ratione voluptatem sequi nesciunt. Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet,
        consectetur, adipisci velit, sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam aliquam
        quaerat voluptatem.
      </p>
      <p class="max-w-5xl mx-auto text-white">
        Ut enim ad minima veniam, quis nostrum exercitationem ullam corporis suscipit laboriosam, nisi ut aliquid ex ea
        commodi consequatur? Quis autem vel eum iure reprehenderit qui in ea voluptate velit esse quam nihil molestiae
        consequatur, vel illum qui dolorem eum fugiat quo voluptas nulla pariatur?
      </p>
    </section>

    <section class="mt-8">
      <h3 class="max-w-5xl mx-auto text-primary-600 dark:text-primary-400">
        <nuxt-link to="/announcements">Latest Announcements</nuxt-link>
      </h3>
      <posts post-type="announcements" :amount="3" />
    </section>

    <section class="mt-8">
      <h3 class="max-w-5xl mx-auto text-primary-600 dark:text-primary-400">
        <nuxt-link to="/events">Events</nuxt-link>
      </h3>
      <posts post-type="announcements" :amount="3" />
    </section>
  </main>
</template>
