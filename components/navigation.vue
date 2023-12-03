<template>
  <nav class="h-16 bg-slate-300 flex m-2 rounded-lg overflow-hidden">
    <nuxt-link class="flex-1 h-full flex justify-center items-center flex-col" to="/">
      <icon class="text-3xl" name="fluent:clock-32-regular" />
      <span class="text-sm">时间</span>
    </nuxt-link>
    <nuxt-link class="flex-1 h-full flex justify-center items-center flex-col" to="/repeats">
      <icon class="text-3xl" name="fluent:calendar-ltr-32-regular" />
      <span class="text-sm">周常</span>
    </nuxt-link>
    <nuxt-link class="flex-1 h-full flex justify-center items-center flex-col" to="/counters">
      <icon class="text-3xl" name="fluent:calendar-arrow-counterclockwise-32-regular" />
      <span class="text-sm">倒数</span>
    </nuxt-link>
    <nuxt-link class="flex-1 h-full flex justify-center items-center flex-col" to="/notes">
      <icon class="text-3xl" name="fluent:notepad-32-regular" />
      <span class="text-sm">总结</span>
    </nuxt-link>
    <nuxt-link class="flex-1 h-full flex justify-center items-center flex-col" to="/ideas">
      <icon class="text-3xl" name="fluent:lightbulb-filament-32-regular" />
      <span class="text-sm">灵感</span>
    </nuxt-link>
    <nuxt-link class="flex-1 h-full flex justify-center items-center flex-col" to="/settings">
      <icon class="text-3xl" name="fluent:settings-32-regular" />
      <span class="text-sm">设置</span>
    </nuxt-link>
  </nav>
</template>

<style lang="postcss" scoped>
a[class*="active"] {
  @apply bg-slate-400;
}
</style>
