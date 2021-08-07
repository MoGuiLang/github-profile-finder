<template>
  <div class="search">
    <input
      type="text"
      v-model="search"
      placeholder="Search..."
      @keydown.enter="sendEmit"
    />
    <button @click="sendEmit">Search</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      search: "",
    };
  },
  methods: {
    sendEmit() {
      this.$emit("search-profile", this.search);
      this.search = "";
    },
  },
};
</script>

<style scoped>
.search {
  width: 500px;
  margin: 0 auto;
  /* background-color: #ccc; */
}
input {
  padding: 5px 10px;
  width: 50%;
  outline: none;
  border: none;
  border-bottom: 2px solid #ccc;
  margin-right: 30px;
  transition: all 0.2s ease-in-out;
}
input:focus {
  border-bottom-color: #42b983;
}
button {
  border: none;
  background-color: #42b983;
  border-radius: 5px;
  color: white;
  cursor: pointer;
  font-size: 16px;
  padding: 10px 15px;
  transition: all 0.2s ease-in-out;
}
button:hover {
  transform: scale(1.1);
}
</style>
