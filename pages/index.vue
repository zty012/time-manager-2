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
      <div class="flex flex-col">
        <div class="flex-1 bg-slate-800 px-2" ref="corner"></div>
        <div class="flex-1 bg-slate-800 text-sm text-slate-100 flex justify-center items-center" v-for="n in 24">
          {{ n }}
        </div>
      </div>
      <div class="flex-1 flex flex-col">
        <div class="flex">
          <div
            class="flex-1 bg-slate-800 text-sm text-slate-100 flex justify-center items-center"
            :style="{ height: lineHeight + 'px' }"
            v-for="n in 7"
          >
            <span>{{ " 一二三四五六日".at(n) }}</span>
            <sup>{{ dayjs().format("M-D") }}</sup>
          </div>
        </div>
        <canvas class="flex-1" ref="canvas"></canvas>
      </div>
    </section>
  </div>
</template>

<script lang="ts" setup>
import dayjs from "dayjs";

const corner = ref<HTMLDivElement | null>(null);
const canvas = ref<HTMLCanvasElement | null>(null);
const lineHeight = ref(0);

onMounted(() => {
  lineHeight.value = corner.value?.getBoundingClientRect().height ?? 0;
  const canvasRect = canvas.value?.getBoundingClientRect()!;
  canvas.value!.width = canvasRect.width ?? 0 * devicePixelRatio;
  canvas.value!.height = canvasRect.height ?? 0 * devicePixelRatio;
  const ctx = canvas.value?.getContext("2d")!;
  ctx.fillText("Hello canvas", 0, 0);
});
</script>
