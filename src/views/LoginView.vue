<script>
import ButtonLogin from "../components/ButtonLogin.vue";

export default {
  name: "LoginView",
  components: {
    ButtonLogin,
  },
};
</script>

<template>
  <div class="Login-Body">
    <div class="left">
      <h1 id="left-title">Projeto trainee</h1>

      <p id="text">
        Caso seja sua primeira vez aqui,
        <router-link to="/register" id="sign-in">clique aqui</router-link> para
        realizar seu cadastro!
      </p>
    </div>

    <div class="right">
      <b-form>
        <h1 id="form-title">Iniciar Sessão</h1>

        <div class="input">
          <img src="../assets/email.png" class="icon" />
          <input
            type="email"
            placeholder="Email"
            class="input-field"
            required
          />
        </div>

        <div class="input" style="margin-bottom: 10vh">
          <img src="../assets/cadeado.png" class="icon" />
          <input
            type="password"
            placeholder="Senha"
            class="input-field"
            required
          />
        </div>

        <ButtonLogin text_content="Entrar" />

        <router-link to="/about" id="forgot-password">
          Esqueceu sua senha?
        </router-link>
      </b-form>
    </div>
  </div>
</template>

<style scoped>
div.Login-Body {
  display: flex;

  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

div.left {
  width: 62vw;
  height: 100vh;

  padding: 5vh 6vw 0;
  background-color: #2c497f;
}

h1#left-title {
  font-family: "Montserrat", sans-serif;
  font-weight: 700;
  font-size: 2.5em;

  margin: 12vh 0 13vh 0;
  justify-content: start;
  color: #fff;
}

p#text {
  font-family: "Montserrat", sans-serif;
  font-weight: 400;
  width: 50%;
  color: #fff;
}

#sign-in {
  text-decoration: none;
  color: #808a9f;
  font-weight: bold;
}

#sign-in:hover {
  cursor: pointer;
  color: #96c2e1;
}

/* ===== FORMULÁRIO ===== */

div.right {
  display: flex;
  align-items: center;
  justify-content: flex-start;
  flex-direction: column;

  width: 38vw;
  margin: 15vh 0 0 0;
}

form {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  border-radius: 10px;
}

h1#form-title {
  font-family: "Montserrat", sans-serif;
  font-weight: 400;

  margin: 0 0 12vh 0;
  color: #5c80bc;
}

div.input {
  display: flex;
  align-items: center;

  border-radius: 4px;
  padding: 1em 0.7em 1em;
  margin: 0 0 2.5vh 0;
  width: 20vw;

  position: relative;

  background-color: #e4e4e4;
}

img.icon {
  height: 1em;
  width: 1em;
  margin: 0 5px;
}

input.input-field {
  background-color: #e4e4e4;
  font-size: 16px;
  margin: 0 0 0 0.3em;

  width: 100%;

  outline: none;
  border: none;
}

#forgot-password {
  font-family: "Roboto", sans-serif;
  font-size: 14px;
  text-decoration: none;
  color: #1b2d50;

  margin: 3vh 0 0 0;
}

#forgot-password:hover {
  cursor: pointer;
}

@media screen and (max-width: 992px) {
  div.left {
    width: 50vw;
  }
  div.right {
    width: 50vw;
  }
}

@media screen and (max-width: 600px) {
  div.Login-Body {
    display: flex;
    flex-direction: column;
  }
  div.left {
    display: flex;
    flex-direction: column;
    width: 100vw;
    align-items: center;
    height: 75vh;
    padding: 0;
  }
  div.right {
    width: 100%;
  }
  div.input {
    width: 100%;
  }
  #forgot-password {
    margin: 3vh 0 10vh 0;
  }
}
</style>
