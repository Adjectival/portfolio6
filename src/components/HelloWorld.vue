<template>
<div class="hello">
  <div>
    <h1>{{ msg }}</h1>
    <h2 class="mb-5">{{ msg2 }}</h2>
    <h2 class="mauvey">Product Portfolio</h2>
    <div class="p-1 m-3">
      <!-- ideally, iterate over a list -->
      <!-- until the Webpack vs img src interpolation is grokked, doing these cards manually ;_; -->
      <ul class="card-deck">
        <!-- proj #1 -->
        <li class="card p-3">
        <a href="https://fwt-helper.firebaseapp.com/">
          <p>
            <h4>How To Mine Crypto</h4>
            <img class="card-image" src="../../static/proj1.png" />
          </p>
          <span class="card p-1 bg-badge">Bootstrap, Material Design </span>
          <span class="card p-1 bg-badge">Google DataStudio </span>
          <h6>Lightweight tutorial built at high speed with the derring MDBootstrap micro-framework.</h6>
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
          <span class="card p-1 bg-badge">Angular2</span>
          <span class="card p-1 bg-badge">pixlr</span>
          <h6>Helps sort an army of characters into tactical teams.</h6>
          <h6>Dropdowns filter a NoSQL dataset which Angular makes into arrays.</h6>
          <h6>Slicing a flat dataset can work as well as a relational database.</h6>
        </a>
        </li>
        <!-- proj #3 -->
        <li class="card p-3">
        <a href="https://fwt-helper.firebaseapp.com/">
          <p>
            <h4>Font Awesome Cards</h4>
            <img class="card-image" src="../../static/proj3.png" />
          </p>
          <span class="card p-1 bg-badge">VueJS</span>
          <span class="card p-1 bg-badge">Sass</span>
          <h6>Sandbox for exploring CSS effects applied to the ubiquitous Font Awesome library.</h6>
          <h6>Displays usable code for the effects you create.</h6>
        </a>
        </li>
        <!-- proj #4 -->
        <li class="card p-3">
        <a href="https://colors-crypto.firebaseapp.com/">
          <p>
            <h4>Colors of Crypto</h4>
            <img class="card-image" src="../../static/proj4.png" />
          </p>
          <span class="card p-1 bg-badge">React</span>
          <span class="card p-1 bg-badge">widgets</span>
          <h6>Dashboard of the top crypto currencies with market values and capitalization.</h6>
          <h6>Live values from script loading a widget. Color branding sometimes based upon existing design.</h6>
        </a>
        </li>
        <!-- proj #5 -->
        <li class="card p-3">
        <a href="">
          <p>
            <h4>Terraforma</h4>
            <img class="card-image" src="../../static/proj5.png" />
          </p>
          <span class="card p-1 bg-badge">Sketch</span>
          <span class="card p-1 bg-badge">InVision</span>
          <h6>Group project from code bootcamp.</h6>
          <h6>I created visual assets and written copy for the mockup, as well as initial concept.</h6>
        </a>
        </li>
        <!-- proj #6 -->
        <li class="card p-3">
        <a href="https://strangerthings-questionboard.pagefrontapp.com/">
          <p>
            <h4>Answer My Question</h4>
            <img class="card-image" src="../../static/proj6.png" />
          </p>
          <span class="card p-1 bg-badge">EmberJS</span>
          <span class="card p-1 bg-badge">GPC firebase</span>
          <h6>Simple forum built as a learning exercise with EmberJS.</h6>
          <h6>Uses Firebase as cloud data service vs a database server.</h6>
          <h6>Could do with an update to include Season 2!</h6>
        </a>
        </li>
      </ul>
    </div>
    <!-- crypto zone -->
    <h2 class="raisiny">Crypto~currency</h2>
    <div class="card p-1 m-3">
      <p>Yes, I mine it. Yes, I own it. Yes, I trade it.</p>
      <h5>You can, too!</h5>
      <p>Click here to learn more.</p>
    </div>
    <!-- social links -->
    <h2 class="bg-info">Links to More</h2>
    <ul class="">
        <!-- resume -->
        <a href="" target="_blank">
        <li class="card m-3 p-3 social-icon">
          <i class="far fa-file"></i>
          <h6>resume
          </h6>
        </li>
        </a>
        <!-- GH -->
        <a href="https://github.com/Adjectival" target="_blank">
        <li class="card m-3 p-3 social-icon">
          <i class="fab fa-github"></i>
          <h6>sources
          </h6>
        </li>
        </a>
        <!-- linkedin -->
        <a href="https://www.linkedin.com/in/alexander-jacks" target="_blank">
        <li class="card m-3 p-3 social-icon">
          <i class="fab fa-linkedin-in"></i>
          <h6>network
          </h6>
        </li>
        </a>
        <!-- insta -->
        <a href="https://www.instagram.com/a.d.jacks/" target="_blank">
        <li class="card m-3 p-3 social-icon">
          <i class="fab fa-instagram"></i>
          <h6>pics
          </h6>
        </li>
        </a>
    </ul>
    <!-- counter w/ interpolation -->
    <div class="">
      <button class="btn btn-secondary my-2" v-on:click="counter++">
        Up counter <i class="fas fa-arrow-up"></i>
      </button>
      <span class="h4">
        Stateless counter at {{counter}} times
      </span>
      <button class="btn btn-secondary my-2" v-on:click="counter--">
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
<style scoped>
.hello {
  background: linear-gradient(to top, gainsboro, azure);
  padding-top: 4rem;
  height: 100%;
}
h1, h2 {
  font-weight: normal;
}
.mauvey {
  background-color: #ac54a1;
}
.raisiny {
  background-color: #2e120b;
  color: snow;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
.card {
  margin-bottom: 1rem;
  background-color: snow;
}
.card:hover{
  background-color: white;
}
.card-image {
  max-width: 14vw;

}
.bg-badge {
  background-color: #ccc;
}
.social-icon {
  font-size: 3rem;
  border-radius: 1rem;
}

h2 {
  color: #2e120b;
  padding-bottom: 3px;
  padding-top: 3px;
}
a {
  color: #d62291;
  text-decoration: none;
}
a:hover{
  color:navy;
}
a:active{
  color:aqua;
}


</style>
