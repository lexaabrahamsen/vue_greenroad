<template>
  <div class="home">
    <header id="fh5co-header" role="banner">
      <div class="container">
      </div>
    </header>
    
    <div class="container">
      
    </div>
<!-- FEATURES START -->
    <aside id="fh5co-hero" class="js-fullheight">
      <div class="flexslider js-fullheight">
        <ul class="slides">
          <li style="background-image: url(images/slide_1.jpg);">
            <div class="overlay-gradient"></div>
            <div class="container">
              <div class="col-md-10 col-md-offset-1 text-center js-fullheight slider-text">
                <div class="slider-text-inner">
                  <h2>Green Roads</h2>
                  <h3>Getting rid of our plastic waste, one road at a time.</h3> 
                  <p><a href="#" class="btn btn-primary btn-lg">Get started</a></p>
                </div>
              </div>
            </div>
          </li>
          <li style="background-image: url(images/slide_2.jpg);">
            <div class="container">
              <div class="col-md-10 col-md-offset-1 text-center js-fullheight slider-text">
                <div class="slider-text-inner">
                  <h2>Take Your Business To The Next Level</h2>
                  <p><a href="#" class="btn btn-primary btn-lg">Get started</a></p>
                </div>
              </div>
            </div>
          </li>
          <li style="background-image: url(images/slide_3.jpg);">
            <div class="container">
              <div class="col-md-10 col-md-offset-1 text-center js-fullheight slider-text">
                <div class="slider-text-inner">
                  <h2>We Think Different That Others Can't</h2>
                  <p><a href="#" class="btn btn-primary btn-lg">Get started</a></p>
                </div>
              </div>
            </div>
          </li>
          </ul>
        </div>
    </aside>
    <div id="fh5co-services-section">
      <div class="container">
        <div class="row">
          <div class="col-md-6 col-md-offset-3 text-center fh5co-heading animate-box">
            <h2>Green Roads Are</h2>
            <p>The Green Road is a completely circular product that is based on recycled plastics. It has a significantly smaller carbon footprint than traditional road structures thanks to the longer lifespan and the reduction of transport movements involved in its construction.</p>
          </div>
        </div>
        <div class="row">
          <div class="col-md-3 animate-box">
            <div class="services">
              <i class="icon-recycle"></i>
              <div class="desc">
                <h3>3x Longer</h3>
                <p>The expected lifetime of a Green Road is two to three times as long as that of traditional paving.</p>
              </div>
            </div>
          </div>
          <div class="col-md-3 animate-box">
            <div class="services">
              <i class="icon-recycle"></i>
              <div class="desc">
                <h3>70% Faster</h3>
                <p>The expected construction time of a new road will be reduced by approximately 70%.</p>
              </div>
            </div>
          </div>
          <div class="col-md-3 animate-box">
            <div class="services">
              <i class="icon-recycle"></i>
              <div class="desc">
                <h3>4x Lighter</h3>
                <p>A Green Road is four times as light as a traditional road structure.</p>
              </div>
            </div>
          </div>
          <div class="col-md-3 animate-box">
            <div class="services">
              <i class="icon-recycle"></i>
              <div class="desc">
                <h3>100% Circular</h3>
                <p>A Green Road is 100% curcular and is made from recycled plastic as much as possible.</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div id="fh5co-work-section" class="fh5co-light-grey-section">
      <div class="container">
        <div class="row">
          <div class="col-md-6 col-md-offset-3 text-center fh5co-heading animate-box">
            <h2>Find Your Nearest Recycling Center</h2>
            <p><input type="text" v-model="searchTerm"></p>
            <!-- THIS WILL SHOW THE INDEX OF ALL REC PLACES  -->
            <p>Type your zip code to find your nearest recycling center! {{ places }} </p>
            <div v-for="place in filterBy(places, searchTerm, 'address')">
            <br>
            <h2>{{ place.name }}</h2>
            <p>{{ place.address }}</p>
            <p>{{ place.hours }}</p>
            <p>{{ place.distance }} mi</p>
            </div> -->
          </div>
        </div>
        <div class="row">
          <div class="col-md-4 animate-box">
            <a href="#" class="item-grid text-center">
              <div class="image" style="background-image: url(images/image_1.jpg)"></div>
              <div class="v-align">
                <div class="v-align-middle">
                  <h3 class="title">Geographical App</h3>
                  <h5 class="category">Web Application</h5>
                </div>
              </div>
            </a>
          </div>
          <!-- <div class="col-md-4 animate-box">
            <a href="#" class="item-grid text-center">
              <div class="image" style="background-image: url(images/image_2.jpg)"></div>
              <div class="v-align">
                <div class="v-align-middle">
                  <h3 class="title">Geographical App</h3>
                  <h5 class="category">User Interface</h5>
                </div>
              </div>
            </a>
          </div>
          <div class="col-md-4 animate-box">
            <a href="#" class="item-grid text-center">
              <div class="image" style="background-image: url(images/image_3.jpg)"></div>
              <div class="v-align">
                <div class="v-align-middle">
                  <h3 class="title">Geographical App</h3>
                  <h5 class="category">Branded</h5>
                </div>
              </div>
            </a>
          </div>
          <div class="col-md-4 animate-box">
            <a href="#" class="item-grid text-center">
              <div class="image" style="background-image: url(images/image_4.jpg)"></div>
              <div class="v-align">
                <div class="v-align-middle">
                  <h3 class="title">Geographical App</h3>
                  <h5 class="category">Web</h5>
                </div>
              </div>
            </a>
          </div>
          <div class="col-md-4 animate-box">
            <a href="#" class="item-grid text-center">
              <div class="image" style="background-image: url(images/image_5.jpg)"></div>
              <div class="v-align">
                <div class="v-align-middle">
                  <h3 class="title">Geographical App</h3>
                  <h5 class="category">Illustration</h5>
                </div>
              </div>
            </a>
          </div>
          <div class="col-md-4 animate-box">
            <a href="#" class="item-grid text-center">
              <div class="image" style="background-image: url(images/image_6.jpg)"></div>
              <div class="v-align">
                <div class="v-align-middle">
                  <h3 class="title">Geographical App</h3>
                  <h5 class="category">Web Application</h5>
                </div>
              </div>
            </a>
          </div> -->
          <div class="col-md-12 text-center animate-box">
            <p><a href="#" class="btn btn-primary with-arrow">View More Projects <i class="icon-arrow-right"></i></a></p>
          </div>
        </div>
      </div>
    </div>
    <div id="fh5co-testimony-section">
      <div class="container">
        <div class="row">
          <div class="col-md-6 col-md-offset-3 text-center fh5co-heading animate-box">
            <h2>What People Are Saying</h2>
            <p>Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. </p>
          </div>
        </div>
        <div class="row">
          <div class="col-md-12 col-offset-0 to-animate">
            <div class="wrap-testimony animate-box">
              <div class="owl-carousel-fullwidth">
                <div class="item">
                  <div class="testimony-slide active text-center">
                    <figure>
                      <img src="images/person1.jpg" alt="user">
                    </figure>
                    <blockquote>
                      <p>"Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. Separated they live in Bookmarksgrove right at the coast of the Semantics, a large language ocean."</p>
                    </blockquote>
                    <span>Athan Smith, via <a href="#" class="twitter">Twitter</a></span>
                  </div>
                </div>
                <div class="item">
                  <div class="testimony-slide active text-center">
                    <figure>
                      <img src="images/person2.jpg" alt="user">
                    </figure>
                    <blockquote>
                      <p>"Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. Separated they live in Bookmarksgrove right at the coast of the Semantics, a large language ocean."</p>
                    </blockquote>
                    <span>Nathalie Kosley, via <a href="#" class="twitter">Twitter</a></span>
                  </div>
                </div>
                <div class="item">
                  <div class="testimony-slide active text-center">
                    <figure>
                      <img src="images/person3.jpg" alt="user">
                    </figure>
                    <blockquote>
                      <p>"Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. Separated they live in Bookmarksgrove right at the coast of the Semantics, a large language ocean."</p>
                    </blockquote>
                    <span>Yanna Kuzuki, via <a href="#" class="twitter">Twitter</a></span>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

<!-- THEME BLOG CARDS START   -->
    <!-- <div id="fh5co-blog-section" class="fh5co-light-grey-section">
      <div class="container">
        <div class="row">
          <div class="col-md-6 col-md-offset-3 text-center fh5co-heading animate-box">
            <h2>Recent from Blog</h2>
            <p>Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. </p>
          </div>
        </div>
        <div class="row">
          <div class="col-md-6 col-sm-6 animate-box">
            <a href="#" class="item-grid">
              <div class="image" style="background-image: url(images/image_1.jpg)"></div>
              <div class="v-align">
                <div class="v-align-middle">
                  <h3 class="title">We Create Mobile App</h3>
                  <h5 class="date"><span>June 23, 2016</span> | <span>4 Comments</span></h5>
                  <p>Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. Separated they live in Bookmarksgrove.</p>
                </div>
              </div>
            </a>
          </div>
          <div class="col-md-6 col-sm-6 animate-box">
            <a href="#" class="item-grid">
              <div class="image" style="background-image: url(images/image_2.jpg)"></div>
              <div class="v-align">
                <div class="v-align-middle">
                  <h3 class="title">Geographical App</h3>
                  <h5 class="date"><span>June 22, 2016</span> | <span>10 Comments</span></h5>
                  <p>Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. Separated they live in Bookmarksgrove.</p>
                </div>
              </div>
            </a>
          </div>
          <div class="col-md-12 text-center animate-box">
            <p><a href="#" class="btn btn-primary with-arrow">View More Post <i class="icon-arrow-right"></i></a></p>
          </div>
        </div>
      </div>
    </div> -->
<!-- THEME BLOG CARDS END    -->

    <div id="fh5co-pricing-section">
      <div class="container">
        <div class="row">
          <div class="col-md-6 col-md-offset-3 text-center fh5co-heading animate-box">
            <h2>Pricing</h2>
            <p>Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. </p>
          </div>
        </div>
        <div class="row">
          <div class="pricing">
            <div class="col-md-3 animate-box">
              <div class="price-box">
                <h2 class="pricing-plan">Starter</h2>
                <div class="price"><sup class="currency">$</sup>9<small>/month</small></div>
                <p>Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. </p>
                <a href="#" class="btn btn-select-plan btn-sm">Select Plan</a>
              </div>
            </div>

            <div class="col-md-3 animate-box">
              <div class="price-box">
                <h2 class="pricing-plan">Basic</h2>
                <div class="price"><sup class="currency">$</sup>27<small>/month</small></div>
                <p>Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. </p>
                <a href="#" class="btn btn-select-plan btn-sm">Select Plan</a>
              </div>
            </div>

            <div class="col-md-3 animate-box">
              <div class="price-box popular">
                <h2 class="pricing-plan pricing-plan-offer">Pro <span>Best Offer</span></h2>
                <div class="price"><sup class="currency">$</sup>74<small>/month</small></div>
                <p>Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. </p>
                <a href="#" class="btn btn-select-plan btn-sm">Select Plan</a>
              </div>
            </div>

            <div class="col-md-3 animate-box">
              <div class="price-box">
                <h2 class="pricing-plan">Unlimited</h2>
                <div class="price"><sup class="currency">$</sup>140<small>/month</small></div>
                <p>Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. </p>
                <a href="#" class="btn btn-select-plan btn-sm">Select Plan</a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

<!-- START SECTION - WE TRY TO UPDATE THE SITE EVERYDAY -->
<!--     <div class="fh5co-cta" style="background-image: url(images/slide_2.jpg);">
      <div class="overlay"></div>
      <div class="container">
        <div class="col-md-12 text-center animate-box">
          <h3>We Try To Update The Site Everyday</h3>
          <p><a href="#" class="btn btn-primary btn-outline with-arrow">Get started now! <i class="icon-arrow-right"></i></a></p>
        </div>
      </div>
    </div>
  </div> -->
<!-- END SECTION - WE TRY TO UPDATE THE SITE EVERYDAY -->

<!-- START OF ORIGINAL CODE -->
<!--     <h1>{{ message }}</h1>
    <h2>Getting rid of our plastic waste, one road at a time.</h2>
    <br>
    <p>Search for your closest Recycling Center</hp>
    <p><input type="text" v-model="searchTerm"></p> -->
    <!-- THIS WILL SHOW THE INDEX OF ALL REC PLACES  -->
<!--     <p>Find your closest recycling center! {{ places }}</p> 
    <div v-for="place in filterBy(places, searchTerm, 'address')">
    <br>
    <h2>{{ place.name }}</h2>
    <p>{{ place.address }}</p>
    <p>{{ place.hours }}</p>
    <p>{{ place.distance }} mi</p>
    </div> -->
<!-- END OF ORIGINAL CODE -->
  </div>
</template>


<style>
</style>


<script>
import axios from "axios";
import Vue2Filters from "vue2-filters";

export default {
  mixins: [Vue2Filters.mixin],
  data: function() {
    return {
      message: "Green Roads",
      places: [],
      searchTerm: ""
    };
  },
  created: function() {
    axios.get("/api/places").then(response => {
      console.log(response.data);
      this.places = response.data;
    });
  },
  methods: {}
};
</script>