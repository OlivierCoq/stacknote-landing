<template>
  <div>
    <section id="home" class="pt-5" style="opacity: 0; background-image: url('dist/img/hero_bg.jpg');" :style="{'opacity': opacity}">
      <div class="container">
        <div class="row pt-5">
          <div class="col-md-12 col-lg-6">
            <div class="ctr-copy text-start p-3">
              <div class="align-middle me-3">
                <h1 class="fw-bold text-uppercase">Bring your notes to life.</h1>
                <p>The old way of taking computer science notes is dead. <br> Now you can write your notes and run them too.</p>
                <a href="#plans"><button class="btn btn-success">Download now <i class="fa fa-download"></i></button></a>
              </div>
            </div>
          </div>
          <div class="col-md-12 col-lg-6">
            <div class="ctr-mockup pt-5 pb-5">
              <img src="dist/img/screen_shot-1.png" alt="Laptop screenshot">
            </div>
          </div>
        </div>
      </div>
    </section>
    <section id="features" class="mb-5">
      <div class="container">
        <div class="row">
          <div class="col-md-12 col-lg-6 ">
            <img src="dist/img/screen_shot-2.png" class="rounded" alt="Output screenshot">
          </div>
          <div class="col-md-12 col-lg-6 order-xs-first order-sm-first order-md-first order-lg-last">
            <div class="ctr-copy m-5 text-start">
              <h2>Test code in real time.</h2>
              <p>
                Create as many IDEs as you'd like in one note. Run code in the language of your choice.
                Current languages include C, C#, C++, Java, JavaScript, and Python.
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section id="plans" class="pt-5" style="background-image: url('dist/img/plans_bg.jpg');">
      <div class="container">
        <div class="row pt-5">
          <h2>Plans & Pricing</h2>
          <p>Get started with Stack.Notes()</p>
        </div>
        <div class="row pt-5">
          <div class="col-md-12 col-lg-6" v-for="(plan, i) in plans" :key="i">
            <div class="item">
              <div class="card mt-5">
                <div class="card-body p-5">
                  <h3>{{ plan.name }}</h3>
                  <hr>
                  <ul class="list-group text-start mt-5">
                    <li v-for="(feature, i) in plan.features" :key="i" class="list-group-item" :class="feature.premium ? 'active' : ''">
                      <strong> {{ feature.name }} </strong>
                    </li>
                  </ul>
                  <div class="text-center p-5">
                    <button class="btn btn-success">Download <i class="fa fa-download"></i></button>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="container">
        <div id="footer" class="row mt-5">
          <span class="p-2">Product of <strong><a href="https://www.oseeyo.com" target="_blank">Oseeyo</a>.</strong></span>
        </div>
      </div>
    </section>
  </div>
</template>
<script>
  export default {
    name: 'Home',
    components: {},
    data() {
      return {
        opacity: 1,
        plans: [
          {
            name: 'Free',
            features: [
              {
                name:'Unlimited notes',
                premium: false
              },
              {
                name: 'IDE with C, C#, C++, Java, JavaScript, and Python support',
                premium: false
              }
            ],
            download: ''
          },
          {
            name: 'Stack.Notes()++',
            features: [
              {
                name:'Unlimited notes',
                premium: false
              },
              {
                name: 'IDE with C, C#, C++, Java, JavaScript, and Python support',
                premium: false
              },
              {
                name: 'Cloud note access',
                premium: true
              }
            ],
            download: ''
          }
        ]
      }
    },
    created() {},
    methods: {}
  }
</script>
<style lang="scss">
  @import "../sass/main.scss";
</style>
