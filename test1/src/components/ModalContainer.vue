<template>
  <div :key="item.id" v-for="item in componentList">
    <component :is="item.component" />
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue'
const componentList = ref<any[]>([])
const ModalContainer = defineComponent({
  setup() {
    return {
      componentList
    }
  }
})
let i = 0
export const popup = (comp: any) => {
  componentList.value?.push({
    component: comp,
    id: i++
  })
}
export default ModalContainer
</script>

<style lang="scss" scoped></style>
