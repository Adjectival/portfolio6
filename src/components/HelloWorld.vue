<template>
<div class="hello">
  <div>
    <h1>{{ msg }}</h1>
    <h2 class="mb-5">{{ msg2 }}</h2>
    <h2 class="mauvey">Product Portfolio</h2>
    <div class="p-1 m-3">
      <!-- iterate over a list -->
      <ul class="card-deck">
        <li v-for="product in products" v-bind:key="product"
        class="card p-3">
        <a :href="product.p_url">
          <h4>{{ product.p_title }}</h4>
          <img :src="product.p_image" />
          <span class="badge">{{ product.p_tech }}</span>
          <span class="badge">{{ product.p_tool }}</span>
          <h6>{{ product.p_desc }}</h6>
        </a>
        </li>
      </ul>
    </div>
    <!-- crypto zone -->
    <h2 class="raisiny">Crypto ~ currency</h2>
    <div class="card p-1 m-3">
      <p>Yes, I mine it. Yes, I own it. Yes, I trade it.</p>
      <p>Yes, you can, too.</p>
    </div>

    <!-- social links -->
    <h2 class="bg-info">Links to More</h2>
    <ul class="">
      <li class="card p-1 m-3"><i class="fas fa-book"></i>
        <a
          href=""
          target="_blank"
        >
        </a>
      </li>
      <li class="card p-1 m-3"><i class="fas fa-heart"></i>
        <a
          href=""
          target="_blank"
        >
        </a>
      </li>
      <li class="card p-1 m-3"><i class="fab fa-github"></i>
        <a
          href=""
          target="_blank"
        >
        </a>
      </li>
      <li class="card p-1 m-3"><i class="fab fa-twitter"></i>
        <a
          href=""
          target="_blank"
        >
        </a>
      </li>
    </ul>
    <!-- counter w/ interpolation -->
    <div class="">
      <button class="btn btn-secondary my-2" v-on:click="counter++">
        Up counter <i class="fas fa-arrow-up"></i>
      </button>
      <span class="h4">
        Counter at {{counter}} times
      </span>
      <button class="btn btn-secondary my-2" v-on:click="counter--">
        Down counter <i class="fas fa-arrow-down"></i>
      </button>
      <p class="">
        How many high can it go?
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
      // iterate over a list
      products: [
        { p_title: 'Fantasy War Tactics Helper',
          p_image: '../assets/p_image_coc.png',
          p_url: 'https://fwt-helper.firebaseapp.com/',
          p_tech: 'Angular2',
          p_tool: 'pixlr',
          p_desc: 'Helps sort the large army of characters in the game Fantasy War Tactics-R by Nexon. Dropdown menus filter a NoSQL dataset that Angular transforms into object arrays. Slicing a flat dataset can work as well as a relational database.',
        },
        { p_title: 'Font Awesome Cards',
          p_image: '../assets/p_image_coc.png',
          p_url: 'https://fwt-helper.firebaseapp.com/',
          p_tech: 'VueJS',
          p_tool: 'Sass',
          p_desc: 'Sanbox for exploring CSS effects in the ubiquitous Font Awesome library. Exports usable code for the effects you create.',
        },
        { p_title: 'Colors of Crypto',
          p_image: '../assets/p_imagecoc.png',
          p_url: 'https://colors-crypto.firebaseapp.com/',
          p_tech: 'React',
          p_tool: 'widgets',
          p_desc: 'Dashboard of the top crypto currencies and their market values and capitalization. Descriptive icons from Font Awesome. Live values from script loading a widget. Color branding sometimes based upon existing design.',
        },
        { p_title: 'MDB dashboard w google infographic',
          p_image: '../assets/p_imagecoc.png',
          p_url: 'https://fwt-helper.firebaseapp.com/',
          p_tech: 'Bootstrap, Material Design',
          p_tool: 'Google DataStudio',
          p_desc: 'Lightweight dashboard prototype built at high speed with the derring MDBootstrap micro-framework.',
        },
        { p_title: 'Terraforma',
          p_image: '../assets/p_imagecoc.png',
          p_url: 'https://fwt-helper.firebaseapp.com/',
          p_tech: 'Sketch',
          p_tool: 'InVision',
          p_desc: 'Group project from code bootcamp. I created visual assets and written copy for the portfolio mockup, as well as initial concept.',
        },
        { p_title: 'Answer My Question',
          p_image: '../assets/p_imagecoc.png',
          p_url: 'https://strangerthings-questionboard.pagefrontapp.com/',
          p_tech: 'EmberJS',
          p_tool: 'GPC firebase',
          p_desc: 'Went overboard on the styling because I love this show and Ember is fun. Uses Firebase as cloud data service vs a database server. Could do with an update to include Season 2!',
        },
      ],
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
}
h2 {
  color: #2e120b;
  padding-bottom: 3px;
  padding-top: 3px;
}
a {
  color: #d62291;
}


</style>
