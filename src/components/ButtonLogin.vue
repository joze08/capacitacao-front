<script>
export default {
  name: "ButtonLogin",
  props: {
    text_content: String,
  },
  methods: {
    log() {
      this.$router.push("/home");
    },
  },
};
</script>

<template>
  <button v-on:click="log()">
    {{ text_content }}
  </button>
</template>

<style scoped>
button {
  background-color: #343842;
  color: #fff;

  font-family: "Roboto", sans-serif;
  font-size: 1.2em;

  width: 15vw;
  padding: 0.8em 0;
  border: none;
  border-radius: 2px;

  box-shadow: 1px 5px 15px rgba(48, 78, 140, 0.5);
}

button:hover {
  cursor: pointer;
}

@media screen and (max-width: 600px) {
  button {
    width: 30vw;
  }
}
</style>
