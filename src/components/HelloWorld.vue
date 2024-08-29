<template>
  <div id="horizontal" class="scrollContainer">
    <div class="loading-page content-section section">
      <div class="text-center align-items-center user-info">
        <div class="image">
          <img class="img-user" src="../assets/user.png" />
        </div>
        <h5 class="text-white font-weight-normal small-text">I'm</h5>
        <h1 class="user-name text-uppercase text-primary mb-2">NGAN NGUYEN</h1>
        <code>UI/UX Design - Frontend Developer</code>
      </div>
      <div class="scroll">
        <div class="m-scroll hozRight1">
          <span><large>GRAPHIC</large> DESIGN</span>
          <span><large>VUE</large> FRAMEWORK</span>
          <span><large>HTML</large> FRONTEND</span>
          <span><large>GRAPHIC</large> DESIGN</span>
          <span><large>GRAPHIC</large> DESIGN</span>
          <span><large>CSS</large> STYLE</span>
          <span><large>GRAPHIC</large> DESIGN</span>
        </div>
        <div class="m-scroll hozRight">
          <span><large>GRAPHIC</large> DESIGN</span>
          <span><large>VUE</large> FRAMEWORK</span>
          <span><large>HTML</large> FRONTEND</span>
          <span><large>GRAPHIC</large> DESIGN</span>
          <span><large>GRAPHIC</large> DESIGN</span>
          <span><large>CSS</large> STYLE</span>
          <span><large>GRAPHIC</large> DESIGN</span>
        </div>
        <div class="m-scroll hozLeft">
          <span>
            <b class="fill">UI / UX</b>
            <small>DESIGN</small>
          </span>
          <span>
            <b class="fill txt-pink">UI/UX</b>
            <small>DESIGN</small>
          </span>
          <span>
            <b class="fill">UI/UX</b>
            <small>DESIGN</small>
          </span>
          <span>
            <b class="fill txt-pink">UI/UX</b>
            <small>DESIGN</small>
          </span>
          <span>
            <b class="fill">UI/UX</b>
            <small>DESIGN</small>
          </span>
        </div>
      </div>
    </div>
    <section id="section01" class="content-section section blue">
      <div class="container">
        <div class></div>
        <div class="section-des col-3">
          <h3>I'm</h3>
          <h2>Ngannguyen</h2>
          <h4>And here these I'm able to use</h4>
        </div>
        <div class="container section-content col-9">
          <div class="row">
            <div class="col-4 box box01">
              <h3 class="bl">Figma</h3>
              <img src="../assets/section03/figma.svg" />
            </div>
            <div class="col-4 box box02">
              <h3 class="white">Adobe</h3>
              <img src="../assets/section03/adobe.svg" />
            </div>
            <div class="col-4 box box03">
              <h3 class="bl">Vuejs</h3>
              <img src="../assets/section03/vuejs.svg" />
            </div>
          </div>
          <div class="row">
            <div class="col-4 box box03">
              <h3 class="bl">Figma</h3>
              <img src="../assets/section03/figma.svg" />
            </div>
            <div class="col-4 box box02">
              <h3 class="white">Adobe</h3>
              <img src="../assets/section03/adobe.svg" />
            </div>
            <div class="col-4 box box01">
              <h3 class="bl">Vuejs</h3>
              <img src="../assets/section03/vuejs.svg" />
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="section03" class="content-section section"></section>
    <section id="" class="content-section section">
      <div class="">
        <h1>content 2</h1>
      </div>
    </section>
    <section id="" class="content-section section">
      <div class="">
        <h1>content 3</h1>
      </div>
    </section>
    <section id="" class="content-section section">
      <div class="">
        <h1>content 4</h1>
      </div>
    </section>
  </div>
</template>
<script>
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
export default {
  mounted() {
     gsap.registerPlugin(ScrollTrigger);

    const sections = gsap.utils.toArray("#horizontal .content-section");

    gsap.to(sections, {
      xPercent: -100 * (sections.length - 1),
      //   ease: "none",
      scrollTrigger: {
        trigger: "#horizontal",
        pin: true,
        scrub: 1,
        snap: 1 / (sections - 1),
        // base vertical scrolling on how wide the container is so it feels more natural.
        end: "+=3500",
        // end: () => "+=" + (sections.offsetWidth - innerWidth),
        //end: () => horizontalScrollContainer.scrollWidth

      },
    });
   
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Oswald", sans-serif;
  scrollbar-width: none;
}
body {
  margin: 0;
  padding: 0;
  overscroll-behavior: none;
  height: 100vh;
}

* ::-webkit-scrollbar,
::-webkit-scrollbar {
  width: 0;
  display: none;
}

.img-user {
  width: 200px;
  box-sizing: border-box;
  padding: 8px;
  border-radius: 100%;
  background: linear-gradient(45deg, #8356ec 0%, #f48ace 100%);
  transition: transform 0.6s cubic-bezier(0.76, 0, 0.24, 1),
    box-shadow 0.8s cubic-bezier(0.76, 0, 0.24, 1);
}

#horizontal {
  display: flex;
  overflow: hidden;
  width: 100%;
}
#horizontal .content-section {
  height: 100vh;
  width: 100vw;
  display: grid;
  flex-shrink: 0;
  place-items: center;
  //  margin-left: -0%;
}
#horizontal .content-section:nth-child(1) {
  /* background: #e3fc6c; */
}
#horizontal .content-section:nth-child(2) {
  // background: #fff;
}
#horizontal .content-section:nth-child(3) {
  // background: #8356ec;
}
#horizontal .content-section:nth-child(4) {
  background: #fff;
}
#horizontal .content-section:nth-child(5) {
  background: #313;
}
.loading-page {
  position: relative;
  width: 100%;
  height: 100%;
  overflow: hidden;
  background: #724acf;
  background: rgb(244, 138, 184);
  background: linear-gradient(243deg, rgba(244, 138, 184, 1) 0%, #724acf 52%);
}

.hozRight span {
  font-size: 7rem;
  opacity: 0.2;
}
.hozRight {
  animation: hozRight-scroll 50s infinite linear;
  color: #fff;
  top: 40%;
  position: absolute;
  display: flex;
}
.hozRight1 {
  animation: hozRight-scroll 40s infinite linear;
  color: #fff;
  top: 4%;
  position: absolute;
  opacity: 0.2;
  display: flex;
}
.hozLeft {
  animation: hozLeft-scroll 50s infinite linear;
  -webkit-text-stroke: 2px;
  -webkit-text-stroke-color: #e3fc6c;
  color: transparent;
  top: 65%;
  position: absolute;
  opacity: 0.5;
  display: flex;
}
.ico-arrow {
  width: 40px;
  position: absolute;
  right: 3%;
  top: 0;
}
.user-info {
  position: absolute;
  top: 15%;
  left: 0;
  right: 0;
  z-index: 9;
  max-width: 0 auto;
  text-align: center;
}
.small-text {
  text-align: center;
  color: #fff;
  font-family: monospace;
  font-size: 20px;
  margin-bottom: -30px;
}
code {
  color: #fff;
  /* margin-bottom: -10px !important; */
  font-size: 20px;
  font-family: monospace;
}
span {
  display: inline-block;
  margin-right: 100px;
  padding: 0;
  font-size: 10rem;
}
large {
  font-size: 140%;
  font-weight: bold;
  opacity: 0.3 !important;
}
.user-name {
  text-align: center;
}
.txt-pink {
  color: #fd7fd1;
}
.fill {
  color: #e3fc6c;
}

@keyframes hozRight-scroll {
  from {
    transform: translateX(0%);
  }
  to {
    transform: translateX(-50%);
  }
}
@keyframes hozLeft-scroll {
  from {
    transform: translateX(-50%);
  }
  to {
    transform: translateX(0%);
  }
}

.text-primary {
  color: #ffffff !important;
  font-size: 100px;
  font-family: "Oswald", sans-serif;

  text-align: center;
  margin: 0 auto;
  font-weight: 400;
}
.text-uppercase {
  text-transform: uppercase !important;
}
.loading-page {
  background: url("/src/assets/ggg.jpg") 100% 100% no-repeat;
  background-size: cover;
}
/* ///////////////////section01////////////////// */

h1 {
  color: #333;
  font-family: tahoma;
  font-size: 3rem;
  font-weight: 100;
  line-height: 1.5;
  text-transform: uppercase;
  white-space: nowrap;
  overflow: hidden;
  position: relative;
  width: 550px;
}
h1 span {
  font-size: 40px;
  margin-left: 40px;
}

.message {
  background-color: yellow;
  color: #333;
  display: block;
  font-weight: 900;
  overflow: hidden;
  position: absolute;
  padding-left: 0.5rem;
  top: 0.2rem;
  left: 270px;
  animation: openclose 5s ease-in-out infinite;
}

.word1,
.word2,
.word3 {
  font-family: tahoma;
}

@keyframes openclose {
  0% {
    top: 0.2rem;
    width: 0;
  }
  5% {
    width: 0;
  }
  15% {
    width: 230px;
  }
  30% {
    top: 0.2rem;
    width: 230px;
  }
  33% {
    top: 0.2rem;
    width: 0;
  }
  35% {
    top: 0.2rem;
    width: 0;
  }
  38% {
    top: -4.5rem;
  }
  48% {
    top: -4.5rem;
    width: 190px;
  }
  62% {
    top: -4.5rem;
    width: 190px;
  }
  66% {
    top: -4.5rem;
    width: 0;
    text-indent: 0;
  }
  71% {
    top: -9rem;
    width: 0;
    text-indent: 5px;
  }
  86% {
    top: -9rem;
    width: 285px;
  }
  95% {
    top: -9rem;
    width: 285px;
  }
  98% {
    top: -9rem;
    width: 0;
    text-indent: 5px;
  }
  100% {
    top: 0;
    width: 0;
    text-indent: 0;
  }
}

/* ////////////////////////////////////////////// */
#section03 {
  ///////////////////////////icon///////////////////
}
#section01 {
  background: #edf2fa;
  h2 {
    font-size: 80px;
    margin-bottom: 30px;
  }
  h3 {
    font-weight: 300;
    font-size: 40px;
  }
  .white {
    color: #fff;
  }
  .box {
    margin: 10px;
    width: 300px;
    height: 300px;
    padding: 50px;
    border-radius: 20px;
    text-align: center;
    margin-top: 30px;
    img {
      width: 60%;
    }
  }
  .box01 {
    color: #111111;
    background-color: #a178df;
  }
  .box02 {
    background-image: linear-gradient(
        0deg,
        rgb(42 41 51 / 57%),
        rgba(42, 41, 51, 0.8)
      ),
      url(/src/assets/section03/02.jpg);
    background-position: 100% 100%;
    background-size: cover;
  }
  .box03 {
    color: #111111;
    background-color: #f7e045;
  }
  .box04 {
    background-image: linear-gradient(
        0deg,
        rgba(42, 41, 51, 0.8),
        rgba(42, 41, 51, 0.8)
      ),
      url("../assets/section03/04.jpg");
    background-position: 100% 100%;
    background-size: cover;
  }
}
</style>
