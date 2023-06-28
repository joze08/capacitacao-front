<template>
  <div class="home">
    <NavbarComponent />
    <main id="mainContent">
      <h1 id="title">Nós somos a CompJr</h1>
      <p id="text">
        Texto informativo nessa parte Lorem ipsum dolor, sit amet consectetur
        adipisicing elit. Reprehenderit sunt modi voluptates, explicabo non
        alias, ab praesentium iure deserunt ut accusamus tenetur esse quo libero
        delectus expedita distinctio molestiae possimus!
      </p>
    </main>
    <CarouselComponent />
  </div>
</template>

<script>
import NavbarComponent from "@/components/NavbarComponent.vue";
import CarouselComponent from "@/components/CarrosselComponent.vue";

export default {
  name: "HomeView",
  components: {
    NavbarComponent,
    CarouselComponent,
  },
};
</script>

<style scoped>
main#mainContent {
  margin: 0;
  padding: 5vh 6vw 0;

  width: auto;
  height: 100vh;

  background-color: #2c497f;
  color: #fff;
}

h1#title {
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
</style>
