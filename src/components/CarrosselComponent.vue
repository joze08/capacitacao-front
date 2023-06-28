<template>
  <div id="carouselBody">
    <b-carousel
      id="carousel"
      v-model="slide"
      :interval="intervalValue"
      no-hover-pause
      controls
      indicators
      img-width="1024"
      img-height="480"
      background="#ababab"
      style="text-shadow: 1px 1px 2px #333"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
      <div @click="pause()">
        <b-carousel-slide
          caption="HomeOffice"
          text="Lorem ipsum dolor, sit amet consectetur adipisicing
        elit. Reprehenderit sunt modi voluptates, explicabo non alias, ab
        praesentium iure deserunt ut accusamus tenetur esse quo libero delectus
        expedita distinctio molestiae possimus!"
          img-src="../assets/foto1.jpg"
        ></b-carousel-slide>
      </div>

      <div @click="pause()">
        <b-carousel-slide
          caption="Goals setting"
          text="Lorem ipsum dolor, sit amet consectetur adipisicing
        elit. Reprehenderit sunt modi voluptates, explicabo non alias, ab
        praesentium iure deserunt ut accusamus tenetur esse quo libero delectus
        expedita distinctio molestiae possimus!"
          img-src="../assets/foto2.jpg"
        ></b-carousel-slide>
      </div>

      <div @click="pause()">
        <b-carousel-slide
          caption="Healphy workspace..."
          text="Lorem ipsum dolor, sit amet consectetur adipisicing
        elit. Reprehenderit sunt modi voluptates, explicabo non alias, ab
        praesentium iure deserunt ut accusamus tenetur esse quo libero delectus
        expedita distinctio molestiae possimus!"
          img-src="../assets/foto3.jpg"
        ></b-carousel-slide>
      </div>

      <div @click="pause()">
        <b-carousel-slide
          caption="Good comunication..."
          text="Lorem ipsum dolor, sit amet consectetur adipisicing
        elit. Reprehenderit sunt modi voluptates, explicabo non alias, ab
        praesentium iure deserunt ut accusamus tenetur esse quo libero delectus
        expedita distinctio molestiae possimus!"
          img-src="../assets/foto4.jpg"
        ></b-carousel-slide>
      </div>
    </b-carousel>
  </div>
</template>

<script>
export default {
  name: "CarouselComponent",
  data() {
    return {
      sliding: null,
      slideClicked: false,
      intervalValue: 4000,
    };
  },

  methods: {
    onSlideStart() {
      this.sliding = true;
    },
    onSlideEnd() {
      this.sliding = false;
    },
    pause() {
      if (this.slideClicked) {
        this.slideClicked = false;
        this.intervalValue = 4000;
      } else {
        this.slideClicked = true;
        this.intervalValue = 0;
      }
    },
  },
};
</script>

<style scoped>
div#carouselBody {
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
