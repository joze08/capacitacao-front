<template>
  <b-navbar toggleable="md" sticky="true" id="navBody">
    <b-navbar-brand href="#" v-show="seeElements">
      <img src="../assets/Logo.png" id="logo" />
    </b-navbar-brand>

    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

    <div class="right">
      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav class="ml-auto">
          <b-nav-item
            ><router-link to="/about" id="navLink"
              >Quem somos?</router-link
            ></b-nav-item
          >
          <b-nav-item
            ><router-link to="/about" id="navLink"
              >Projetos</router-link
            ></b-nav-item
          >
          <b-nav-item
            ><router-link to="/about" id="navLink"
              >Contatos</router-link
            ></b-nav-item
          >
        </b-navbar-nav>
      </b-collapse>

      <div class="input" v-show="seeElements">
        <button id="search">
          <img src="../assets/lupa.png" id="input-lupa" />
        </button>
        <input type="text" placeholder="Pesquisar..." />
      </div>
    </div>
  </b-navbar>
</template>

<script>
export default {
  name: "NavbarComponent",
  data() {
    return {
      seeElements: true,
    };
  },
  mounted() {
    this.checkWindowSize();
    window.addEventListener("resize", this.checkWindowSize);
  },
  methods: {
    checkWindowSize() {
      if (window.innerWidth <= 768) {
        this.seeElements = false;
      } else {
        this.seeElements = true;
      }
    },
    showElements() {
      if (window.innerWidth <= 768) {
        this.seeElements = true;
      }
    },
    hideElements() {
      if (window.innerWidth <= 768) {
        this.seeElements = false;
      }
    },
  },
};
</script>

<style scoped>
#navBody {
  margin: 0;
  padding: 0.5% 5% 0.5%;

  display: flex;
  justify-content: space-between;
  align-items: center;
  font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
  background-color: #2c497f;

  border-bottom: 1px solid rgb(64, 87, 170);
  box-shadow: 0 4px 8px 0 rgba(32, 32, 32, 0.085);
}

@media screen and (max-width: 768px) {
  #div.right {
    padding: 5%;
  }
}

img#logo {
  height: 45px;
  width: 45px;
  margin: 0.2em;
}

div.right {
  width: 80%;
  display: flex;
  justify-content: flex-end;
  align-items: center;
}

#navLink {
  text-decoration: none;
  font-size: 1.05em;
  color: #fff;
}

#navLink:hover {
  text-decoration: underline;
}

div.input {
  margin: 0 0 0 5%;
  padding: 0.2%;
  border: 1px solid;
  border-radius: 4px;

  display: flex;
  align-items: center;
}

button#search {
  border: none;
  border-radius: 4px;

  padding: 0.25em 0.5em;
  background-color: transparent;

  display: flex;
  align-items: center;
}

img#input-lupa {
  height: 1em;
  width: 1em;
}

button#search:hover {
  cursor: pointer;
}

input {
  margin-left: 5px;
  box-sizing: border-box;
  border: none;
  background-color: transparent;

  color: #fff;
  font-weight: 100;
}

input::placeholder {
  color: #fff;
  font-weight: 100;
}

input:focus {
  outline: none;
}

input:focus::placeholder {
  color: transparent;
}
</style>
