<template>
  <div class="user-detail">
    <div class="user-info">
      <img :src="data.avatar_url" alt="" />
      <h1>
        <a :href="data.html_url" target="_blank">{{ user }}</a>
      </h1>
      <h3>Name: {{ data.name }}</h3>
      <h3>Bio: {{ data.bio }}</h3>
      <h3>
        Blog: <a :href="data.blog" target="_blank">{{ data.blog }}</a>
      </h3>
      <h3>Company: {{ data.company }}</h3>
      <h3>Followers: {{ data.followers }}</h3>
      <h3>Following: {{ data.following }}</h3>
      <h3>Location: {{ data.location }}</h3>
      <h3>Public Repos: {{ data.public_repos }}</h3>
    </div>
  </div>
</template>

<script>
export default {
  props: ["user", "data", "repo"],
};
</script>

<style>
.user-info {
  margin-top: 50px;
}
img {
  width: 100px;
  border-radius: 50%;
}
a {
  text-decoration: none;
  color: #42b983;
}
</style>
