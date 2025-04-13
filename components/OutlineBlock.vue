<script setup lang="ts">
interface Props {
  icon: string
}

withDefaults(defineProps<Props>(), {
  icon: ''
})
</script>

<template>
  <div class="flex flex-col items-center p-2 border-2 border-orange-400 border-dashed rounded-lg bg-white/80 transform -rotate-1">
    <div class="rounded-full p-4 bg-yellow-200 mb-2">
      <div class="w-12 h-12 flex items-center justify-center">
        <img :src="icon" class="w-14 h-14" />
      </div>
    </div>
    <span class="text-center text-lg"><slot></slot></span>
  </div>
</template>
