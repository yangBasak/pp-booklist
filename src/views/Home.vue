<template>
  <div class="home">
    <ListPage />
  </div>
</template>

<script>
// @ is an alias to /src
import ListPage from "@/components/ListPage.vue";

export default {
  name: "Home",
  components: {
    ListPage,
  },
};
</script>
