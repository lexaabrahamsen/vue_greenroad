<template>
  <div class="home">
    <div>
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
          <li style="background-image: url(images/header_overlay.jpg);">
            <div class="overlay-gradient"></div>
            <div class="container">
              <div class="col-md-10 col-md-offset-1 text-center js-fullheight slider-text">
                <div class="slider-text-inner">
                  <h2>GreenRoads</h2>
                  <h3>Using Plastic Waste to Pave Roads</h3> 
                  <p><a href="#" class="btn btn-primary btn-lg">Find my recycling center</a></p>
                </div>
              </div>
            </div>
          </li>
<!--           <li style="background-image: url(images/slide_2.jpg);">
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
                  <p><a href="#" class="btn btn-primary btn-lg">Search for my recycling center</a></p>
                </div>
              </div>
            </div>
          </li> -->
          </ul>
        </div>
    </aside>
    <div id="fh5co-services-section">
      <div class="container">
        <div class="row">
          <div class="col-md-6 col-md-offset-3 text-center fh5co-heading animate-box">
            <h2>Paving with Plastic Waste</h2>
            <!-- <p>Paving with Plastic Waste</p> -->
          </div>
        </div>
        <div class="row">
          <div class="col-md-3 animate-box">
            <div class="services">
              <i class="icon-user"></i>
              <div class="desc">
                <h2>3x Longer</h2>
                <p>The expected lifetime of a Green Road is two to three times as long as that of traditional paving.</p>
              </div>
            </div>
          </div>
          <div class="col-md-3 animate-box">
            <div class="services">
              <i class="icon-arrow-right"></i>
              <div class="desc">
                <h2>70% Faster</h2>
                <p>The expected construction time of a new road will be reduced by approximately 70%.</p>
              </div>
            </div>
          </div>
          <div class="col-md-3 animate-box">
            <div class="services">
              <i class="icon-user"></i>
              <div class="desc">
                <h2>4x Lighter</h2>
                <p>A GreenRoads is four times as light as a traditional road structure.</p>
              </div>
            </div>
          </div>
          <div class="col-md-3 animate-box">
            <div class="services">
              <i class="icon-recycle"></i>
              <div class="desc">
                <h2>100% Circular</h2>
                <p>A GreenRoads is 100% curcular and is made from recycled plastic as much as possible.</p>
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
            <p>Enter your city and state</p>
            <p><input type="text" v-model="searchTerm"></p>
            <!-- THIS WILL SHOW THE INDEX OF ALL REC PLACES  -->
<!--             <p>Type your zip code to find your nearest recycling center! {{ places }} </p> -->
          </div>
        </div>
        <div class="row">
          <!-- <div class="col-md-3 animate-box"> -->
          <div class="text-center fh5co-heading animate-box">
          <div v-for="place in filterBy(places, searchTerm, 'address')" class="col-md-6">
            <a href="#" class="item-grid text-center">
              <div class="image" style="background-image: url(images/image_1.jpg)"></div>
              <div class="col-md text-center fh5co-heading animate-box"></div>
              <div class="v-align">
                <div class="v-align-center">
                  <h2 class="title">{{ place.name }}</h2>
                  <p class="address">{{ place.address }}</p>
                  <p class="hours">Hours: {{ place.hours }}</p>
                  <p class="distance">{{ place.distance }} mi</p>
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

<!-- VIEW MORE BUTTON -->
<!--           <div class="col-md-12 text-center animate-box">
            <p><a href="#" class="btn btn-primary with-arrow">View More Projects <i class="icon-arrow-right"></i></a></p>
          </div> -->

        </div>
      </div>
    </div>
<!-- TESTIMONIAL SECTION START -->
<!--     <div id="fh5co-testimony-section">
      <div class="container">
        <div class="row">
          <div class="col-md-6 col-md-offset-3 text-center fh5co-heading animate-box">
            <h2>What People Are Saying About Green Roads</h2>
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
                      <p>"These roads address plastic pollution and help us pave a way toward a cleaner future."</p>
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
                      <p>"Taking action to recycle plastics so they don’t end up polluting the ocean."</p>
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
                      <p>"We are wanting to solve two world problems. On one side we call it the waste plastic epidemic, and on the other side the poor quality of roads that we have to drive on today."</p>
                    </blockquote>
                    <span>Yanna Kuzuki, via <a href="#" class="twitter">Twitter</a></span>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div> -->
<!-- TESTIMONIAL SECTION END -->
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

<!-- THEME PRICING SECTION START   -->
    <div id="fh5co-pricing-section">
      <div class="container">
        <div class="row">
          <div class="col-md-6 col-md-offset-3 text-center fh5co-heading animate-box">
            <h2>Find Out Your Recycling Pickup Schedule</h2>
            <p>Enter your zip code, and we'll let you know which days your recycling pickup are!. </p>
            <p><input type="text" v-model="searchTerm"></p>
          </div>
        </div>
        <div class="row">
          <div class="pricing">
            <div class="col-md-3 animate-box">
              <div class="price-box">
                <h2 class="pricing-plan">Recycling</h2>
                <div class="price"><sup class="currency"></sup>MON<small>Pickup</small></div>
                <p>Collectible items include bottles, bottles, bottles. </p>
                <!-- <a href="#" class="btn btn-select-plan btn-sm">Select Plan</a> -->
              </div>
            </div>

            <div class="col-md-3 animate-box">
              <div class="price-box">
                <h2 class="pricing-plan">Recycling</h2>
                <div class="price"><sup class="currency"></sup>TUE<small>Pickup</small></div>
                <p>Collectible items include bottles, bottles, bottles. </p>
                <!-- <a href="#" class="btn btn-select-plan btn-sm">Select Plan</a> -->
              </div>
            </div>

            <div class="col-md-3 animate-box">
              <div class="price-box">
                <h2 class="pricing-plan">Recycling</h2>
                <div class="price"><sup class="currency"></sup>WED<small>Pickup</small></div>
                <p>Collectible items include bottles, bottles, bottles.</p>
                <!-- <a href="#" class="btn btn-select-plan btn-sm">Select Plan</a> -->
              </div>
            </div>

           <div class="col-md-3 animate-box">
                  <div class="price-box">
                    <h2 class="pricing-plan">Recycling</h2>
                    <div class="price"><sup class="currency"></sup>THU<small>Pickup</small></div>
                    <p>Collectible items include bottles, bottles, bottles.</p>
                    <!-- <a href="#" class="btn btn-select-plan btn-sm">Select Plan</a> -->
                  </div>
                </div>

           <div class="col-md-3 animate-box">
                  <div class="price-box">
                    <h2 class="pricing-plan">Recycling</h2>
                    <div class="price"><sup class="currency"></sup>FRI<small>Pickup</small></div>
                    <p>Collectible items include bottles, bottles, bottles.</p>
                    <!-- <a href="#" class="btn btn-select-plan btn-sm">Select Plan</a> -->
                  </div>
                </div>

           <div class="col-md-3 animate-box">
                  <div class="price-box">
                    <h2 class="pricing-plan">Recycling</h2>
                    <div class="price"><sup class="currency"></sup>SAT<small>Pickup</small></div>
                    <p>Collectible items include bottles, bottles, bottles.</p>
                    <!-- <a href="#" class="btn btn-select-plan btn-sm">Select Plan</a> -->
                  </div>
                </div>

           <div class="col-md-3 animate-box">
                  <div class="price-box">
                    <h2 class="pricing-plan">Recycling</h2>
                    <div class="price"><sup class="currency"></sup>SUN<small>Pickup</small></div>
                    <p>Collectible items include bottles, bottles, bottles.</p>
                    <!-- <a href="#" class="btn btn-select-plan btn-sm">Select Plan</a> -->
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
<!-- THEME PRICING SECTION END   -->
<!-- THEME PRICING SECTION START   -->

<!--     <div id="fh5co-pricing-section">
      <div class="container">
        <div class="row">
          <div class="col-md-6 col-md-offset-3 text-center fh5co-heading animate-box">
          </div>
        </div>
        <div class="row">
          <div class="pricing">
            <div class="col-md-3 animate-box">
              <div class="price-box">
                <h2 class="pricing-plan">Friday</h2>
                <div class="price"><sup class="currency">$</sup>9<small>/month</small></div>
                <p>Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. </p>
               <a href="#" class="btn btn-select-plan btn-sm">Select Plan</a> -->
<!--               </div>
            </div>

            <div class="col-md-3 animate-box">
              <div class="price-box">
                <h2 class="pricing-plan">Saturday</h2>
                <div class="price"><sup class="currency">$</sup>27<small>/month</small></div>
                <p>Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. </p> -->
                <!-- <a href="#" class="btn btn-select-plan btn-sm">Select Plan</a> -->
<!--               </div>
            </div>
          <div class="col-md-3 animate-box">
                  <div class="price-box">
                    <h2 class="pricing-plan">Sunday</h2>
                    <div class="price"><sup class="currency">$</sup>27<small>/month</small></div>
                    <p>Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. </p> -->
                    <!-- <a href="#" class="btn btn-select-plan btn-sm">Select Plan</a> -->
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
<!-- THEME PRICING SECTION END   -->


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


  <!-- </div> -->
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
      searchTerm: "",
      active: true,
      'text-danger': false
    };
  },
  // WORKING LIST OF RECYCLING CENTERS
  created: function() {
    axios.get("/api/places").then(response => {
      console.log(response.data);
      this.places = response.data;
    });
    // NOT WORKING GOOGLE MAPS
    // created: function() {
    //   axios.get("https://maps.googleapis.com/maps/api/place/details/json?placeid=ChIJN1t_tDeuEmsRUsoyG83frY4&fields=name,rating,formatted_phone_number&&key=#{ENV['API_KEY']}").then(response => {
    //     console.log(response.body);
    //     this.places = response.body;
    // });

  },
  methods: {}
};
</script>