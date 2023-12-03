<template>
  <div class="flex flex-col h-screen bg-slate-100">
    <nuxt-page class="flex-1" />
    <navigation />
  </div>
</template>

<style lang="postcss">
button {
  @apply bg-slate-300 text-black px-4 py-2 rounded-md flex gap-2 items-center;
}
button .icon {
  @apply text-2xl;
}
</style>
