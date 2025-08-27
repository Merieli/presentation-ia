<script setup lang="ts">
import { ref } from 'vue';

interface Item {
    label?: string,
    text: string
}

interface ListProps {
    items: Item[] 
}

defineProps<ListProps>();

const listStyle = ref({
  'padding-left': '50px',
  'list-style-type': 'disc'
});

const itemStyle = ref({});
</script>

<template>
  <ul :style="listStyle">
    <li v-for="(item, index) in items" :key="index" :style="itemStyle">
      <strong v-if="item.label">{{ item.label }}: </strong>{{ item.text }}
    </li>
  </ul>
</template>
