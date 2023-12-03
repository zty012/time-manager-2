<template>
  <div class="flex flex-col">
    <section class="flex justify-between">
      <button>
        <icon name="fluent:arrow-left-32-regular" />
      </button>
      <button>
        <icon name="fluent:edit-32-regular" />
        <span>管理分类</span>
      </button>
      <button>
        <icon name="fluent:add-32-regular" />
        <span>添加时段</span>
      </button>
      <button>
        <icon name="fluent:arrow-right-32-regular" />
      </button>
    </section>
    <section class="flex-1 flex">
      <div class="flex-1 bg-slate-800"></div>
      <div class="flex-1 border-gray-400 bg-slate-800 text-white" v-for="n in 7"></div>
    </section>
    <section class="flex-1 flex" v-for="n in 24">
      <div class="flex-1 bg-slate-800"></div>
      <div class="flex-1 text-white" v-for="n in 7"></div>
    </section>
  </div>
</template>
