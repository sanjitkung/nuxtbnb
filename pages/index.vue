<template>
  <div>
    <div
      v-for="home in homes"
      :key="home.objectID"
      style="float: left; margin: 10px"
    >
      <nuxt-link :to="`/home/${home.objectID}`">
        <home-card :home="home" />
      </nuxt-link>
    </div>
  </div>
</template>

<script>
import homes from "~/data/homes.json";

export default {
  head() {
    return {
      title: "Homepage",
      meta: [
        {
          name: "description",
          content: "This is homepage!",
          hid: "description",
        },
      ],
    };
  },
  data() {
    return {
      homes: homes.slice(0, 3),
    };
  },
};
</script>
