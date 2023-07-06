<template>
  <div class="text-center mb-16" width="100%">
    <v-pagination v-model="page" :length="6"></v-pagination>
  </div>
</template>
<script>
export default {
  data() {
    return {
      page: 1,
    };
  },
};
</script>

<!-- <style>
width: ;
</style> -->
