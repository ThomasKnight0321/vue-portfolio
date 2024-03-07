<template>
  <v-app id="home">
    <NavBar />
    <v-container fluid>
      <div class="head">
        <v-row>
          <v-col cols="5">
            <div style="position:relative" class="mt-16">
              <h1 class="text-grey">Hello,</h1>
              <h1 class="text-white">I'M Thomas Yang</h1>
              <span class="text-grey">Frontend Engineer & AutoTesting Engineer</span><br />
              <v-btn dark class="text-yellow mt-8" variant="outlined">Contact me</v-btn>
            </div>
          </v-col>
          <v-col cols="2">
            <div style="position: absolute; z-index: 9999; bottom: 0; margin-left:auto;
            margin-right: auto; left: 0; right: 0; text-align: center;">
              <v-icon>fas fa-angle-double-down</v-icon>  
            </div>
          </v-col>
          <v-col cols="5">
            <div style="position: absolute; z-index: 9999;" class="mt-16"></div>
            <v-img src="1.JPG" style="z-index: 9999;" contain max-height="200"></v-img>
          </v-col>
        </v-row>
      </div>
      <v-col cols="12" class="mt-16" id="about">
        <div>
          <v-row>
            <v-col col="12" sm="6">
              <div class="egg">
                <v-img src="me.png" max-height="300"></v-img>
              </div>
            </v-col>
            <v-col cols="12" sm="6">
              <h5 class="mt-16">About me</h5>
              <div style="width: 120px">
                <v-slider v-model="slider2" color="yellow"></v-slider>
              </div>
              <h4 class="mt-4">I Am a Creative Web Design</h4>
              <h4>And Developer</h4>
              <p class="text-grey">Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                Aspernatur, ullam perspiciatis fugiat temporibus laboriosam
                accusamus tempora repellendus sequi sed cum dolorum vero est.
                Placeat dicta architecto reiciendis est veniam. Unde.</p>
              <br />
              <p class="text-grey">Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                Aspernatur, ullam perspiciatis fugiat temporibus laboriosam
                accusamus tempora repellendus sequi sed cum dolorum vero est.
                Placeat dicta architecto reiciendis est veniam. Unde.</p>
              <v-btn dark color="yellow" class="mt-4">Download Resume</v-btn>
            </v-col>
          </v-row>
        </div>
      </v-col>  
      <div class="text-center mt-4">
        <h2>What we Do</h2>
        <div style="width: 120px; margin: 0 auto">
          <v-slider v-model="slider2" color="yellow"></v-slider>
        </div>
      </div>
      <v-col cols="12" class="padd" id="portfolio">
        <div class="first" id="project">
          <v-row>
            <v-col cols="12">
              <div class="child">
                <v-btn icon="fas fa-laptop" color="#FBDF7E" class="text-white"></v-btn>
                <h3 class="ml-3 mt-3">App Design</h3>
                <p class="text-grey">
                  Lorem ipsum dolor sit, amet <br /> consectetur adipisicing 
                  <br /> elit Aspernatur
                </p>
              </div>
              <div class="child">
                <v-btn icon="fas fa-mobile-alt" color="#FBDF7E" class="text-white"></v-btn>
                <h3 class="ml-3 mt-3">App Design</h3>
                <p class="text-grey">
                  Lorem ipsum dolor sit, amet <br /> consectetur adipisicing 
                  <br /> elit Aspernatur
                </p>
              </div>
              <div class="child">
                <v-btn icon="fas fa-camera" color="#FBDF7E" class="text-white"></v-btn>
                <h3 class="ml-3 mt-3">App Design</h3>
                <p class="text-grey">
                  Lorem ipsum dolor sit, amet <br /> consectetur adipisicing 
                  <br /> elit Aspernatur
                </p>
              </div>
            </v-col>
          </v-row>
          <v-divider></v-divider>
        </div>
      </v-col>
      <v-col cols="12" sm="12" id="services">
        <div class="d-flex justify-center mb-6">
          <v-btn color="#FBDF7E" class="mr-2">All</v-btn>
          <v-btn class="mr-2" variant="tonal">Web Design</v-btn>
          <v-btn class="mr-2" variant="tonal">Frontend Design</v-btn>
          <v-btn class="mr-2" variant="tonal">Backend Design</v-btn>
          <v-btn class="mr-2" variant="tonal">Environment</v-btn>
        </div>
      </v-col>
      <v-col col="12" class="imgHover">
        <v-row class="fill-height" align="center" justify="center">
          <template v-for="(item, i) in items" :key="i">
            <v-col cols="12" md="4">
              <v-hover v-slot="{isHovering, props}">
                <v-card :elevation="isHovering ? 12 : 2" :class="{'on-hover' : isHovering}" v-bind="props">
                  <v-img :src="item.JPG" height="225px" cover></v-img>
                </v-card>
              </v-hover>
            </v-col>
          </template>
        </v-row>
      </v-col>
      <v-col cols="12" sm="12">
        <div class="d-flex justify-center mb-6">
          <v-btn color="#FBDF7E" class="mt-4">Load More</v-btn>
        </div>
      </v-col>
      <v-col cols="12" id="page">
        <div class="pre">
          <v-row>
            <v-col cols="12" sm="4">
              <v-card class="mw-auto" max-width="344" height="">
                <v-img src="1.JPG" height="200px" cover></v-img>
                <v-card-title>We provide you the best</v-card-title>
                <v-card-subtitle>By AAE IdeaPro | 06 Sep 2024</v-card-subtitle>
                <v-card-text>
                  Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                Aspernatur, ullam perspiciatis fugiat 
                </v-card-text>
              </v-card>
            </v-col>
            <v-col cols="12" sm="4">
              <v-card class="mw-auto" max-width="344" height="">
                <v-img src="2.JPG" height="200px" cover></v-img>
                <v-card-title>We provide you the best</v-card-title>
                <v-card-subtitle>By AAE IdeaPro | 06 Sep 2024</v-card-subtitle>
                <v-card-text>
                  Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                Aspernatur, ullam perspiciatis fugiat 
                </v-card-text>
              </v-card>
            </v-col>
            <v-col cols="12" sm="4">
              <v-card class="mw-auto" max-width="344" height="">
                <v-img src="3.JPG" height="200px" cover></v-img>
                <v-card-title>We provide you the best</v-card-title>
                <v-card-subtitle>By AAE IdeaPro | 06 Sep 2024</v-card-subtitle>
                <v-card-text>
                  Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                Aspernatur, ullam perspiciatis fugiat 
                </v-card-text>
              </v-card>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <v-col cols="12" id="biog">
        <div class="hire">
          <v-row>
            <v-col cols="12" sm="8">
              <h1 class="mt-9">Hire me for your awesome porjects</h1>
              <p class="text-grey">Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                Aspernatur, ullam perspiciatis fugiat </p>
            </v-col>
            <v-col cols="12" sm="4">
              <v-btn color="#FBDF7E" class="mt-15">Hire me</v-btn>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <v-col cols="12" sm="12" class="px-16" id="contact">
        <v-row>
          <v-col cols="12" sm="4">
            <div class="child">
              <h1>Contact info.</h1>
              <v-btn icon="fas fa-map-marker-alt" class="mt-10" variant="outlined"></v-btn><br />
              <span class="text-caption">Your Street SYO, Your Area Dream</span><br />
              <v-btn icon="fas fa-phone-alt" class="mt-10" variant="outlined"></v-btn><br />
              <span class="text-caption">00235 - 6547</span><br />
              <span class="text-caption">00235 - 6547</span><br />
              <v-btn icon="fas fa-envelope" class="mt-10" variant="outlined"></v-btn><br />
              <span class="text-caption">asdasd@gmail.com</span><br />
              <span class="text-caption">asdasd@gmail.com</span><br />
            </div>
          </v-col>
          <v-col cols="12" sm="8">
            <h1 class="mt-8">Send your message</h1>
            <v-divider></v-divider>
            <span class="text-caption">Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                Aspernatur, ullam perspiciatis fugiat </span>
            <v-row class="mt-10">
              <v-col cols="12" sm="6">
                <v-text-field label="Name" persistent-hint variant="outlined"></v-text-field>
              </v-col>
              <v-col cols="12" sm="6">
                <v-text-field label="Phone No" persistent-hint variant="outlined"></v-text-field>
              </v-col>
            </v-row>
            <v-textarea label="Message" persistent-hint variant="outlined"></v-textarea>
            <v-btn color="#FBDF7E" class="mt-2">Submit Now</v-btn>
          </v-col>
        </v-row>
      </v-col>
    </v-container>
    <FooterView />
  </v-app>
</template>

<script>
import { defineComponent } from 'vue';

// Components
import NavBar from '@/components/NavBar.vue';
import FooterView from '@/components/FooterView.vue';

export default defineComponent({
  name: 'HomeView',
  setup() {
    return {
      slider2: 50,
      items: [
        { img: "3.JPG "},
        { img: "4.JPG "},
        { img: "5.JPG "},
        { img: "6.JPG "},
      ]
    }
  },
  components: {
    NavBar,
    FooterView
  },
});
</script>
<style scoped>
  .v-container {
    padding: 16px 0;
  }

  .head {
    position: relative;
    text-align: center;
    padding: 12px;
    margin-bottom: 6px;
    height: 400px;
    width: 100%;
    color: white;
  }

  .head:before {
    content: " ";
    position: absolute;
    top: 0;
    left: 0;
    height: 100%;
    width: 50%;
    background: black;
    transform: skew(0deg, 6deg);
  }

  .head:after {
    content: " ";
    position: absolute;
    top: 0;
    right: 0;
    height: 100%;
    width: 50%;
    background: black;
    transform: skew(0deg, -6deg);
  }

  .egg {
    display: block;
    margin-left: 100px;
    margin-top: 50px;
    width: 356px;
    height: 300px;
    background-color: #FBDF7E;
    border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
  }

  .first {
    width: 100%;
    height: 280px;
    text-align: center;
    padding: 2rem 2rem;
  }

  .child {
    display: inline-block;
    padding: 2rem 1rem;
    vertical-align: middle;
    text-align: center;
    margin-right: 8px;
  }

  .imgHover {
    padding: 0 200px;
  }

  .pre {
    width: 100%;
    height: 380px;
    text-align: center;
    padding: 0 200px;
    background-color: #f5f5f5;
  }

  .hire {
    width: 100%;
    height: 200px;
    padding: 0 200px;
    background-color: #e9e9e9;
    margin-top: -24px;
  }
</style>
