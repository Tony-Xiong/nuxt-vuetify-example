<template>
    <h2>index Page</h2>
  <div>
    <button @click="enableCustomLayout">Update layout</button>
  </div>
</template>

<script setup>
function enableCustomLayout () {
    let route = useRoute()
    if (route.meta.layout == "default") {
        setPageLayout(false)
    } else {
        setPageLayout("default")
    }
    
}
definePageMeta({
  layout: "default",
});
</script>