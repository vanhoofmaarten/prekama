<template>
  <div class="container flex flex-col gap-9 py-9">
    <header class="flex items-center justify-between">
      <h1 class="text-4xl font-extrabold tracking-tighter">{{ title }}</h1>
      <slot name="actions" />
    </header>
    <div class="bg-white rounded-lg shadow-xl" :class="{ 'p-6 md:p-12': spacing }">
      <slot />
    </div>
  </div>
</template>

<script setup lang="ts">
interface Props {
  title: string;
  spacing?: boolean;
}
withDefaults(defineProps<Props>(), { spacing: true });
</script>
