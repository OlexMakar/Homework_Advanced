<template>
  <div class="container">
    <div>
      <div class="tag"></div>
      <div class="title">
        {{ title }}
      </div>
      <div class="img-container">
        <img
          v-for="(user, ind) in users"
          :key="ind"
          :src="user.photo"
          :alt="user.name"
          :title="user.name"
          class="user-photo"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TaskCard",
  props: {
    category: {
      type: Number,
      default: 0,
    },
    title: {
      type: String,
      default: "nulltitle",
    },
    users: {
      type: Array,
      default: () => [],
    },
  },
};
</script>

<style lang="css" scoped>
.container {
  border-radius: 8px;
  border: 2px white;
  width: 300px;
  padding: 10px;
  background-color: lightcyan;
  margin-bottom: 10px;
  margin-top: 10px;
}
.tag {
  border-radius: 5px;
  width: 60px;
  height: 10px;
  background-color: violet;
}
.user-photo {
  border-radius: 50%;
  height: 40px;
  background-color: lightsalmon;
  margin-inline: 5px;
  margin-top: 5px;
}
.img-container {
  text-align: right;
}
.title {
  font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
}
</style>