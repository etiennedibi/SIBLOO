
<template>
  <v-row justify="center" align="center">
    <v-dialog
      v-model="dialog"
      persistent
      max-width="900"
    >
      <v-card>
        <v-card-title class="text-h5">
          Bloo-Drive
        </v-card-title>
        <v-card-text  style="height: 450px;">
          <iframe src="https://gitlab.com/" width="100%" height="100%" style="border:none;"></iframe>
          </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn
            color="green darken-1"
            text
            @click="dialog = false"
          >
            Quit
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>

    <v-col cols="12" class="welcomme">
      <video id="background-video" autoplay loop muted>
        <source src="../static/background.mp4" type="video/mp4">
      </video>
      <div class="cover">
          <img src="../static/Blooraid_Consortium_Logo1.png" alt="" srcset="">
         <p>BLOORAID.c</p>
         <p>INFORMATION SYSTEME - LINK PAGE</p> 
      </div>
    </v-col>
    <v-col cols="12" sm="4" md="4" class="box box1">
      <a href="https://web.telegram.org/z/" class="cta" target="blink">
        <span>Chat</span>
        <svg width="13px" height="10px" viewBox="0 0 13 10">
          <path d="M1,5 L11,5"></path>
          <polyline points="8 1 12 5 8 9"></polyline>
        </svg>
      </a>
    </v-col>
    <v-col cols="12" sm="4" md="4" class="box box2">
    <a  href="https://github.com/login" class="cta" target="blink" > 
        <span>Drive</span>
        <svg width="13px" height="10px" viewBox="0 0 13 10">
          <path d="M1,5 L11,5"></path>
          <polyline points="8 1 12 5 8 9"></polyline>
        </svg>
      </a>
    </v-col>
    <v-col cols="12" sm="4" md="4" class="box box3">
    <a href="https://meet.google.com/" class="cta" target="blink">
        <span>Meet</span>
        <svg width="13px" height="10px" viewBox="0 0 13 10">
          <path d="M1,5 L11,5"></path>
          <polyline points="8 1 12 5 8 9"></polyline>
        </svg>
      </a>
    </v-col>
  </v-row>
</template>




<script>
export default {
  name: 'IndexPage',


  data () {
      return {
        dialog: false,
        dialog2: false,
      }
    },
}
</script>





<style scoped>
*{
  margin: 0;
  padding: 0;
}
.welcomme{
  height: 60vh;
}
#background-video {
  width: 100%;
  height: 60vh;
  object-fit: cover;
  /* position: fixed;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  z-index: -1; */
}
.cover{
  /* height: 60vh; */
  height: 61vh;
  width: 100%;
  background: #0B1A20B6;
  position:absolute;
  top: 0;
  left: 0;
  text-align:center;
  color: #fff;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content:center;
  font-family: Avenir, sans-serif;
  /* z-index: -1; */
}
.cover > img{
  height: 100px;
  width:100px
}
.cover p:nth-child(2){
  font-size: 50px;
  margin-bottom: -10px;
}




.box{
  height: 40vh;
  display: flex;
  justify-content: center;
  align-items: center
}
.box1{
  background-image: linear-gradient(to top, #071319, #0b1a20, #0b2127, #0b292c, #0d3031);
}
.box2{
   background-image: linear-gradient(to top, #071319, #03191b, #0a1e17, #19200f, #2a210c);
}
.box3{
    background-image: linear-gradient(to top, #071319, #0b1a20, #0b2127, #0b292c, #0d3031);
}






a {
  font-family: Avenir, sans-serif;
  text-decoration: none;
  color: white !important;
}

.cta {
  cursor: pointer;
  font-family: Avenir, sans-serif;
  text-decoration: none;
  color: white !important;
  position: relative;
  margin: auto;
  padding: 19px 22px;
  transition: all 0.2s ease;
}
.cta:before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  display: block;
  border-radius: 28px;
  background: rgba(255, 172, 157, 0.5);
  width: 56px;
  height: 56px;
  transition: all 0.3s ease;
}
.cta span {
  position: relative;
  font-size: 16px;
  line-height: 18px;
  font-weight: 900;
  letter-spacing: 0.25em;
  text-transform: uppercase;
  vertical-align: middle;
}
.cta svg {
  position: relative;
  top: 0;
  margin-left: 10px;
  fill: none;
  stroke-linecap: round;
  stroke-linejoin: round;
  stroke: #111;
  stroke-width: 2;
  transform: translateX(-5px);
  transition: all 0.3s ease;
}
.cta:hover:before {
  width: 100%;
  background: #ffab9d;
}
.cta:hover svg {
  transform: translateX(0);
}
.cta:active {
  transform: scale(0.96);
}
</style>