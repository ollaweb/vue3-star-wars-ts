<template>
  <h1>Home page</h1>
</template>

<script lang="ts">
import { defineComponent, onMounted } from 'vue'
import DataService from '@/services/DataServise'
import ResponseData from '@/types/ResponseData'

export default defineComponent({
  setup() {
    onMounted(() => {
      getPeople()
    })

    const getPeople = () => {
      DataService.getAll()
        .then((res: ResponseData) => console.log(res.data))
        .catch((e: Error) => console.log(e))
    }
  }
})
</script>
