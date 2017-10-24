<template>
  <!-- 3)display items component -->
  <div>
    <Items>
    </Items>
  </div>
</template>
<script>
  import Items from "~/components/Items.vue"
  //1)index page loads Items component
  export default {
    components: {
      Items
    },
//2)load items into the store by dispatching LOAD_ITEMS action, with payload of topstories.json
    async fetch({ store }){
      await store.dispatch("LOAD_ITEMS", "askstories.json")
    }
  }
</script>
