<template>
  <a-table>
    <a-space size="large">
    <a-switch :beforeChange="handleChangeIntercept"/>
    <a-switch type="round" :beforeChange="handleChangeIntercept2"/>
    <a-switch type="line" :beforeChange="handleChangeIntercept3"/>
  </a-space>
  </a-table>
  
</template>

<script setup>
import { Message } from '@arco-design/web-vue';

async function handleChangeIntercept (newValue)  {
  await new Promise((resolve) => setTimeout(resolve, 500))
  console.log('ddd',newValue)
  return true

  
    }

    const handleChangeIntercept2 = async (newValue) => {
      await new Promise((resolve) => setTimeout(resolve, 500))
      if (!newValue) {
        Message.error("OH, You can't change")
        return false
      }
      return true
    }
</script>
