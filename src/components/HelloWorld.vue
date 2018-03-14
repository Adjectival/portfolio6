<template>
<div class="hello">
  <div>
    <h1 class="embossed">{{ msg }}</h1>
    <h2 class="mb-5">{{ msg2 }}</h2>
    <h2 class="mauvey">Product Portfolio</h2>
    <div class="p-1 m-3">
      <!-- ideally, iterate over a list -->
      <!-- until the Webpack vs img src interpolation is grokked, doing these cards manually ;_; -->
      <ul class="card-deck">
        <!-- proj #1 -->
        <li class="card p-3">
        <a href="https://how-to-crypto.herokuapp.com/">
          <p>
            <h4>How To Crypto</h4>
            <img class="card-image" src="../../static/proj1.png" />
          </p>
          <span class="badge p-1 bg-badge">Bootstrap, Material Design </span>
          <span class="badge p-1 bg-badge">Font Awesome </span>
          <h6 class="mt-2">Lightweight tutorial built at high speed with the handy MDBootstrap micro-framework.</h6>
          <h6>Focus on cross browser and responsive design.</h6>
        </a>
        </li>
        <!-- proj #2 -->
        <li class="card p-3">
        <a href="https://fwt-helper.firebaseapp.com/">
          <p>
            <h4>Fantasy War Tactics Helper</h4>
            <img class="card-image" src="../../static/proj2.png" />
          </p>
          <span class="badge p-1 bg-badge">Angular2</span>
          <span class="badge p-1 bg-badge">pixlr</span>
          <h6 class="mt-2">Helps sort an army of characters into tactical teams.</h6>
          <h6>Dropdowns filter a NoSQL dataset which Angular makes into arrays.</h6>
          <h6>Slicing a flat dataset can work as well as a relational database.</h6>
        </a>
        </li>

        <!-- proj #3 -->
        <li class="card p-3">
        <a href="https://colors-crypto.firebaseapp.com/">
          <p>
            <h4>Colors of Crypto</h4>
            <img class="card-image" src="../../static/proj4.png" />
          </p>
          <span class="badge p-1 bg-badge">React</span>
          <span class="badge p-1 bg-badge">widgets</span>
          <h6 class="mt-2">Dashboard of the top crypto currencies with market values and capitalization.</h6>
          <h6>Live values from script loading a widget. Color branding sometimes based upon existing design.</h6>
        </a>
        </li>
        <!-- proj #4 -->
        <li class="card p-3">
        <a href="https://adjectival.github.io/terra_forma/">
          <p>
            <h4>Terraforma</h4>
            <img class="tf-image" src="../../static/proj5.png" />
          </p>
          <span class="badge p-1 bg-badge">Sketch</span>
          <span class="badge p-1 bg-badge">InVision</span>
          <h6 class="mt-2">Group design case study from code bootcamp.</h6>
          <h6>I created visual assets and written copy for the mockup, as well as initial concept.</h6>
        </a>
        </li>
      </ul>
    </div>
    <!-- crypto zone -->
    <h2 class="raisiny">Crypto~currency</h2>
    <div class="card py-3 m-3">
      <p>Yes, I mine it. Yes, I own it. Yes, I trade it.</p>
      <h5>You can, too!</h5>
      <a href="https://how-to-crypto.herokuapp.com/">
      <button class="btn btn-lg btn-secondary">
        <h4 class="p-1">Click Here to Learn More</h4>
      </button>
      </a>
    </div>
    <h2 class="bg-info">Links to More</h2>
    <!-- social links -->
    <ul class="card-deck offset-3 col-6">
        <!-- resume -->
        <a href="https://docs.google.com/document/d/1DEiZsO13IoLtAhtvzmoPXhWmEltpavy1KebbHRPX3ZE/edit?usp=sharing" target="_blank">
        <li class="card m-3 p-4 social-icon">
          <i class="far fa-file mx-auto pb-2"></i>
          <h6>resume
          </h6>
        </li>
        </a>
        <!-- GH -->
        <a href="https://github.com/Adjectival" target="_blank">
        <li class="card m-3 p-4 social-icon">
          <i class="fab fa-github mx-auto pb-2"></i>
          <h6>code
          </h6>
        </li>
        </a>
        <!-- linkedin -->
        <a href="https://www.linkedin.com/in/alexander-jacks" target="_blank">
        <li class="card m-3 p-4 social-icon">
          <i class="fab fa-linkedin-in mx-auto pb-2"></i>
          <h6>network
          </h6>
        </li>
        </a>
        <!-- insta -->
        <a href="https://www.instagram.com/a.d.jacks/" target="_blank">
        <li class="card m-3 p-4 social-icon">
          <i class="fab fa-instagram mx-auto pb-2"></i>
          <h6>pics
          </h6>
        </li>
        </a>
        <!-- twitter -->
        <a href="https://twitter.com/archdukej" target="_blank">
        <li class="card m-3 p-4 social-icon">
          <i class="fab fa-twitter mx-auto pb-2"></i>
          <h6>views
          </h6>
        </li>
        </a>
        <!-- freedom bomb -->
        <a href="https://www.facebook.com/alexanderd.jacks" target="_blank">
        <li class="card m-3 p-4 social-icon">
          <i class="fab fa-facebook mx-auto pb-2"></i>
          <h6>friends
          </h6>
        </li>
        </a>
    </ul>
    <!-- counter w/ interpolation -->
    <div class="">
      <button class="btn btn-counter my-2" v-on:click="counter++">
        Up counter <i class="fas fa-arrow-up"></i>
      </button>
      <span class="h4">
        Stateless counter at {{counter}} times
      </span>
      <button class="btn btn-counter my-2" v-on:click="counter--">
        Down counter <i class="fas fa-arrow-down"></i>
      </button>
      <p class="">
        How high can it go?
      </p>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      msg: 'Web Design & Cryptocurrency Consultation',
      msg2: 'Alexander Jacks Services',
      // Two-way data binding
      input_val: '',
      // counter w/ interpolation
      counter: 0,
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
    @import "../assets/main.scss";
</style>
