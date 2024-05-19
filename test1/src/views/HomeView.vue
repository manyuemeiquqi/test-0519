<script setup lang="ts">

import ModalContainer, { popup } from '@/components/ModalContainer.vue';
import MoadlItem from '@/components/ModalItem.vue';

const handleAdd =()=>{
  popup(MoadlItem)
}
</script>

<template>
  <main>
    <button @click="handleAdd">添加 modal1</button>

    <ModalContainer/>
  </main>
</template>
