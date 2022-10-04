<template>
  <div>
    <Header />
    <h1>single user with ID {{ $route.params.id }}</h1>
  </div>
</template>

<script>
import Header from "../../../components/Header.vue";
export default {
  validate(data) {
    return /^\d+$/.test(data.params.id);
  },
  layout: "users",
  components: { Header },
};
</script>
