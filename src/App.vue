<template>
  <section id="app">
    <h1 class="title">Kinderevents</h1>
    <h1 class="title--mobile">Events</h1>
    <Card/>
    <button class="btn--primary">Evenkalender anzeigen</button>
  </section>
</template>
<script>
import Card from './components/Card.vue'

export default {
  name: 'App',
  components: {
    Card
  }
}
</script>

<style>
@font-face {
  font-family: "Gilroy";
  src: url("assets/fonts/Gilroy-Regular/font.woff") format("woff");
}

@font-face {
  font-family: "Gilroy-Bold";
  src: url("assets/fonts/Gilroy-Bold/font.woff") format("woff");
}

@font-face {
  font-family: "Gilroy-LightItalic";
  src: url("assets/fonts/Gilroy-LightItalic/font.woff") format("woff");
}

html {
  width: 100%; 
  background: #FDE140;
  background-image: linear-gradient(220.76deg, #FDE140, #F9C01E);
  background-repeat: no-repeat;
  background-size: cover;
}

body {
  height: 100%;
  font-family: Gilroy, sans-serif;
  font-size: 22px;
  text-align: center;
}

#app {
  display: flex;
  flex-direction: column;
  align-items: center;
}

h1 {
  font-family: Gilroy-Bold;
  font-size: 50px;
  line-height: 70px;
  letter-spacing: 1px;
  color: #642fff;
}

h4 {
  font-family: Gilroy-Bold;
  font-size: 28px;
  line-height: 46px;
  letter-spacing: 0.93px;
  margin: 0;
}

.title {
  display: none;
}

.title--mobile {
  display: flex;
}

.btn--primary {
  background: transparent;
  border: 1px solid #642fff;
  border-radius: 30px;
  font-family: Gilroy-Bold;
  font-size: 18px;
  line-height: 36px;
  letter-spacing: 0.9px;
  padding: 10px 25px;
  color: #642fff;
  margin: 20px;
  align-self: center;
  transition: 0.5s;
  white-space: nowrap;
}

.btn--primary:hover {
  background: #642fff;
  border: 1px solid #642fff;
  color: #fde140;
  cursor: pointer;
}

@media (min-width: 768px) {
  .title {
    display: flex;
  }

  .title--mobile {
    display: none;
  }

  .btn--primary {
    font-family: Gilroy-Bold;
    font-size: 22px;
    line-height: 40px;
    letter-spacing: 1.1px;
  }

}
</style>
