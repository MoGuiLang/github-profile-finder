<template>
  <div class="saved-profile">
    <h1>Search a GitHub Profile for details</h1>
    <Search @search-profile="searchProfile" />
    <UserDetail :user="user" :data="data" :repo="repo" />
  </div>
</template>

<script>
import Search from "../components/Search.vue";
import UserDetail from "../components/UserDetail.vue";
export default {
  components: {
    Search,
    UserDetail,
  },
  data() {
    return {
      user: "",
      data: {},
      repo: [],
    };
  },
  methods: {
    async searchProfile(user) {
      const getProfile = await fetch(`https://api.github.com/users/${user}`);
      const getProfileJson = await getProfile.json();
      const getRepositories = await fetch(getProfileJson.repos_url);
      const getRepoJson = await getRepositories.json();

      if (getProfileJson) {
        this.user = getProfileJson.login;
        this.repo = getRepoJson;
        this.data = getProfileJson;
        // console.log(this.user);
        // console.log(this.repo);
        // console.log(this.data);
      }
    },
  },
};
</script>

<style></style>
