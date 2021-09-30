<template>
  <div class="hello">
    <p class="title-text">Rax Gallery</p>
    <div class="photos-grid">
      <div
        v-for="item in gallery"
        :key="item.id"
        :class="item.cardClass"
        :style="{ 'background-image': 'url(' + item.img + ')' }"
      >
        <div>
          {{ item.id }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  data() {
    return {
      gallery: [
        {
          id: "1",
          img:
            "https://images.pexels.com/photos/965208/pexels-photo-965208.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500",
          cardClass: "card card-tall card-wide",
        },
        {
          id: "2",
          img:
            "https://images.pexels.com/photos/8188619/pexels-photo-8188619.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500",
          cardClass: "card card-2 card-tall",
        },
        {
          id: "3",
          img:
            "https://images.pexels.com/photos/1320684/pexels-photo-1320684.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500",
          cardClass: "card",
        },
        { id: "4", img: "https://images.pexels.com/photos/5214313/pexels-photo-5214313.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500", cardClass: "card" },
        { id: "5", img: "./img/view.JPG", cardClass: "card" },
        { id: "6", img: "./img/walk.JPG", cardClass: "card" },
        {
          id: "7",
          img:
            "https://images.pexels.com/photos/163185/old-retro-antique-vintage-163185.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500",
          cardClass: "card card-wide",
        },
        {
          id: "8",
          img:
            "https://images.pexels.com/photos/2187662/pexels-photo-2187662.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500",
          cardClass: "card",
        },
        {
          id: "9",
          img:
            "https://images.pexels.com/photos/5745029/pexels-photo-5745029.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260",
          cardClass: "card",
        },
        { id: "10", img: "./img/aDay.jpg", cardClass: "card card-wide" },
        {
          id: "11",
          img: "./img/upView.JPG",
          cardClass: "card",
        },
        {
          id: "12",
          img: "./img/icecream.jpg",
          cardClass: "card card-wide",
        },
        {
          id: "13",
          img: "./img/food.jpg",
          cardClass: "card",
        },
        {
          id: "14",
          img: "./img/light.jpg",
          cardClass: "card",
        },
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.title-text {
  color: white;
  font-weight: bold;
  font-size: 40px;
}
.photos-grid {
  display: grid;
  gap: 1rem;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  grid-row: 240px;
}
.card {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background: #353535;
  font-size: 15rem;
  color: #fff;
  box-shadow: rgba(3, 8, 20, 0.1) 0px 0.15rem 0.5rem,
    rgba(2, 8, 20, 0.1) 0px 0.075rem 0.175rem;
  height: 100%;
  width: 100%;
  border-radius: 4px;
  transition: all 500ms;
  overflow: hidden;

  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  margin: 5px;
}
.card-2{
  color: #868686;
}

.card:hover {
  box-shadow: rgba(2, 8, 20, 0.1) 0px 0.35em 1.175em,
    rgba(2, 8, 20, 0.08) 0px 0.175em 0.5em;
  transform: translateY(-3px) scale(1.1);
}

/* Medium screens */
@media screen and (min-width: 600px) {
  .card-tall {
    grid-row: span 2 / auto;
  }

  .card-wide {
    grid-column: span 2 / auto;
  }
}
</style>
