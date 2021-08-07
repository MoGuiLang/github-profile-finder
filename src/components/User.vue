<template>
  <div class="card">
    <div class="user-info">
      <img :src="data.avatar_url" alt="" />
      <h1>{{ user }}</h1>
    </div>
  </div>
</template>

<script>
export default {
  props: ["user", "data"],
};
</script>

<style scoped>
.card {
  padding: 30px;
  text-align: center;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  margin-top: 50px;
}
a {
  text-decoration: none;
  color: #42b983;
}
img {
  width: 100px;
  border-radius: 50%;
}
ul {
  list-style-type: none;
  margin-left: 50px;
}
</style>
