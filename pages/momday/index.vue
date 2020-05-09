<template>
  <div class="base">
    <div class="text">
      <div class="my-title">
        Happy Mother's Day!
      </div>
      <div class="message">
        Enjoy the tulips in Washington Park, Albany, NY
      </div>
      <a class="more" href="https://anlach.github.io/momday2020/">
        All photos
      </a>
    </div>
    <div class="photos">
      <div class="A im"></div>
      <div class="B im"></div>
      <div class="C im"></div>
      <div class="D im"></div>
      <div class="E im"></div>
      <div class="F im"></div>
      <div class="G im"></div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.text {
  width: 100vw;
  position: fixed;
  text-align: center;
  margin: auto;
  z-index: 1;
  font-family: 'Raleway', sans-serif;
  font-size: 32px;
  text-shadow: 2px 2px 10px black;
}
.my-title {
  font-family: 'Calligraffitti', cursive;
  font-size: 100px;
}

.im {
  background-size: cover;
  border-radius: 15px;
}
.photos {
  height: 420vh;
  width: 100vw;
  display: grid;
  grid-template-areas:
    'B B B A'
    'B B B F'
    'D D D F'
    'D D D F'
    'E E G G'
    'C C C C';
  background-color: rgb(2, 51, 2);
  grid-gap: 10px;
}
.A {
  grid-area: A;
  background-image: url('https://anlach.github.io/momday2020/img/IMG_20200507_145223388_HDR.jpg');
}

.B {
  grid-area: B;
  background-image: url('https://anlach.github.io/momday2020/img/IMG_20200507_145021368.jpg');
}

.C {
  grid-area: C;
  background-position-y: center;
  /* background-image: url('https://anlach.github.io/momday2020/img/IMG_20200507_145526106.jpg'); */
  background-image: url('https://anlach.github.io/momday2020/img/IMG_20200507_144929896_HDR.jpg');
}
.D {
  grid-area: D;
  background-position: center;
  background-image: url('https://anlach.github.io/momday2020/img/IMG_20200507_145057363_HDR.jpg');
}
.E {
  grid-area: E;
  background-position-y: 60%;
  background-image: url('https://anlach.github.io/momday2020/img/IMG_20200507_150146591_HDR.jpg');
}
.F {
  grid-area: F;
  background-position-x: 50%;
  background-image: url('https://anlach.github.io/momday2020/img/IMG_20200507_150313137_HDR.jpg');
}
.G {
  grid-area: G;
  background-image: url('https://anlach.github.io/momday2020/img/IMG_20200507_145128469_HDR.jpg');
}
</style>
