<template>
  <figure class="card">
    <div class="card__image">
    </div>
    <figcaption class="card__info">
      <div class="card__info__date">
        <span>10.03 - </span>
        <span>28.03</span>
      </div>
      <div class="card__info__text">
        <h4 class="card__info__text__title">Zeig was du drauf hast! Ab auf die Candy-Rollschuhbahn.</h4>
        <p class="card__info__text__time"><img src="../assets/svg/clock.svg" class="card__info__text__time__clock">10.00 – 16.00 Uhr</p>
        <p class="card__info__text__details">Mit tollem Wettbewerb für grosse und kleine Rollschuh-Profis</p> 
      </div>
      <a class="card__info__text__time__download"><img src="../assets/svg/arrow-right.svg" class="card__info__text__time__download__icon"></a>
    </figcaption>
  </figure>
</template>

<script>
export default {
  name: 'Card',
}
</script>

<style scoped>
.card {
  display: flex;
  flex-direction: column;
  position: relative;
  align-content: center;
  background: white;
  box-shadow: 0 2px 60px 0 rgba(0,0,0,0.2);
  max-width: 700px;
  margin: 40px;
}

.card__image {
  background-color: white;
  background-image: url('https://picsum.photos/id/56/1000/1000') ;
  background-size: cover;
  width: 100%;
  min-height: 200px;
  height: 50%;
}

.card__info {
  display: flex;
  flex-direction: column;
  font-family: Gilroy-Bold;
  padding: 40px;
}

.card__info__date {
  position: absolute;
  top: 120px;
  display: flex;
  flex-direction: column;
  background: white;
  border: 2px solid black;
  font-size: 22px;
  line-height: 38px;
  text-align: left;
  height: max-content;
  width: max-content;
  padding: 10px;
}
.card__info__date span {
  white-space: nowrap;
}

.card__info__text {
  text-align: left;
  padding: 10px 0;
}

.card__info__text__time {
  display: flex;
  align-items: center;
  font-size: 16px;
  line-height: 32px;
  letter-spacing: 0.8px;
}

.card__info__text__time__clock {
  height: 25px;
  padding-right: 10px;
}

.card__info__text__details {
  font-family: Gilroy;
  font-size: 18px;
  line-height: 36px;
  letter-spacing: 0.9px;
  display: none;
}

.card__info__text__time__download {
  position: absolute;
  right: 15px;
  bottom: 15px;
  background: transparent;
  border: none;
}

.card__info__text__time__download__icon {
  background: transparent;
  border: 1px solid #642fff;
  border-radius: 50%;
  padding: 10px;
  width: 15px;
  height: 15px;
  transform: rotate(90deg);
  transition: 0.5s;
}

.card__info__text__time__download__icon:hover {
  cursor: pointer;
  background: #fde140;
}

@media (min-width: 768px) {
  .card__image {
    min-height: 350px;
  }

  .card__info {
    flex-direction: row;
  }

  .card__info__date {
    position: relative;
    top: auto;
    border-width: 4px;
  }

  .card__info__text {
    padding: 0 30px;
  }

  .card__info__text__time {
    font-size: 22px;
    letter-spacing: 1.1px;
    line-height: 38px;
  }

  .card__info__text__details {
    display: flex;
  } 

  .card__info__text__time__download__icon {
    padding: 12px;
    width: 20px;
    height: 20px;
  }

}
</style>
