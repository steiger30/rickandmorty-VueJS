<script >
import { RouterView } from 'vue-router';
import vContainer from "@/components/container.vue"
export default {
  components: {
    vContainer
  }
}
</script>

<template>
  <div id="app">
    <a>asdf</a>

    <vContainer>

      <RouterView />
    </vContainer>
  </div>
</template>

<style lang="scss"></style>
