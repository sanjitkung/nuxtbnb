<template>
  <div style="text-align: center">
    <h1>Error!</h1>
    {{ error.message }} {{ error.statusCode }}
  </div>
</template>

<script>
export default {
  props: {
    error: Object,
    required: true,
  },
  head() {
    return {
      title: "Something went wrong!",
    };
  },
};
</script>
