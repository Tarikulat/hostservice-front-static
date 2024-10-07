<script setup>
// Import Swiper Vue.js components
import { ref, onMounted } from 'vue'
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/pagination';
import 'swiper/css/navigation';
import { Pagination, Navigation } from 'swiper/modules';
const modules = ref([Pagination, Navigation]);

//slider value changing start.....
const monthly = ref();
const theryMonth = ref();
const halfYear = ref();
const yearly = ref();

const monthlyPrice = () => {
  monthly.value = '4890';
  theryMonth.value = '9890';
  halfYear.value = '14490';
  yearly.value = '25490';
}
const threeMonthPrice = () => {
  monthly.value = '14670';
  theryMonth.value = '29670';
  halfYear.value = '43470';
  yearly.value = '76470';
}
const halfYearPrice = () => {
  monthly.value = '29340';
  theryMonth.value = '59340';
  halfYear.value = '86940';
  yearly.value = '152940';
}
const yearPrice = () => {
  monthly.value = '58680';
  theryMonth.value = '118680';
  halfYear.value = '173880';
  yearly.value = '305880';
}

onMounted(() => {
  monthlyPrice();
})
</script>

<template>
  <section class="hero-equal-height ptb-100 gradient-overly-right:before backvp gradient-overly-right">
    <div class="container">
      <div class="row align-items-center">
        <div class="col-md-7 col-lg-7 media-lan ">
          <div class="hero-content-wrap text-white position-relative">
            <h1 class="text-hup media-lan">BDIX Toofan Server </h1>
            <p class="lead">Build and grow the perfect Website BDIX Toofan server Pro.</p>
            <ul class="list-unstyled tech-feature-list text-white">
              <li class="py-1"><span class="ti-control-forward mr-2"></span>Flexible, Easy to Use Control Panel</li>
              <li class="py-1"><span class="ti-control-forward mr-2"></span><strong>Unmetered</strong> Bandwidth</li>
              <li class="py-1"><span class="ti-control-forward mr-2"></span><strong>Unmetered</strong> Sub Domains, FTP
                Accounts</li>
              <li class="py-1"><span class="ti-control-forward mr-2"></span><strong>99%</strong> Uptime Guarantee</li>
              <li class="py-1"><span class="ti-control-forward mr-2"></span><strong>45-Day</strong> Money-Back Guarantee
              </li>
            </ul>
          </div>
        </div>
        <div class="col-md-5 col-lg-5">

          <div class="hover14 column">
            <div>
              <figure><img src="@/assets/img/rocket_img.png" class="lan img-lan body-landing" /></figure>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- packages starting heading -->
  <section>
    <div class="container">
      <div class="row justify-content-center head">
        <div class="col-md-12 col-lg-7">
          <div class="section-heading  text-center">
            <h3 class="media-la text-brand bt-hj">BDIX Toofan Server Plan </h3>
            <h6 class="h5 med-w">
              6 month purchase <span class="text-rd">5%</span> discount - <span class="text-rd"> hostgift6m
              </span>
            </h6>

            <div>
              <h6 class="h5 med-w ">
                1year purchase <span class="text-rd"> 10% </span> discount -<span class="text-rd"> hostgift1yr</span>
              </h6>
            </div>
          </div>
        </div>

        <div class="col-10 col-sm-8 col-md-7">
          <div class="text-center mb-2 radio-box-wrap billingCycle">
            <div class="single-radio-box" @click="monthlyPrice">
              <input name="billingPlan" id="monthly-plan" value="monthly" class="radio" type="radio" checked>
              <label for="monthly-plan"><span class="custom-check"></span>1 Month</label>
            </div>
            <div class="single-radio-box" @click="threeMonthPrice">
              <input name="billingPlan" id="yearly-plan" value="yearly" class="radio" type="radio">
              <label for="yearly-plan"><span class="custom-check"></span>3 Month</label>
            </div>
            <div class="single-radio-box" @click="halfYearPrice">
              <input name="billingPlan" id="biannual-plan" value="biannual" class="radio" type="radio">
              <label for="biannual-plan"><span class="custom-check"></span>6 Month</label>
            </div>

            <div class="single-radio-box" @click="yearPrice">
              <input name="billingPlan" id="triennial-plan" value="triennial" class="radio" type="radio">
              <label for="triennial-plan"><span class="custom-check"></span>1 Year</label>
            </div>

          </div>
        </div>
      </div>
    </div>
  </section>
  <!-- main packages below -->
  <section>
    <div class="container top-p">

      <swiper :slidesPerView="3" :spaceBetween="50" :loop="true" :pagination="{
        clickable: true,
      }" :breakpoints="{
  '320': {
    slidesPerView: 1,
    spaceBetween: 20,
  },
  '570': {
    slidesPerView: 2,
    spaceBetween: 40,
  },
  '1024': {
    slidesPerView: 3,
    spaceBetween: 50,
  },
}" :navigation="true" :modules="modules" class="mySwiper">

        <swiper-slide>
          <div class="container">
            <div class="row align-items-center justify-content-between">
              <div class="col-lg-12 col-md-12 col-12">
                <div class="card text-center align-items-center single-pricing-pack">
                  <div class="pt-5">
                    <h5 class="mb-0 text-brand">BDIX Toofan server</h5>
                    <p class="mb-0">Rapid Flare </p>
                  </div>
                  <div class="card-header border-0 pricing-header">
                    <div class="price text-center mb-0 ">৳ {{ monthly }}<span>/-BDT Only.</span></div>
                  </div>
                  <div class="card-body">
                    <ul class="list-unstyled mb-4 pricing-feature-list">

                      <li>100 GB NVMe Storage </li>
                      <li>Unlimited Bandwidth </li>
                      <li>4 Core CPU 5.9 GHz Pro </li>
                      <li>8 GB RAM, 4800 MHz </li>
                      <li>400 Mbps I/O </li>
                      <li>500 Entry Processes </li>
                      <li>1000 Number Of Processes </li>
                      <li>Free SSL Certificate </li>
                      <li>LiteSpeed with LSCache </li>
                      <li>Turbo (Up To 20X Faster) </li>
                      <li>Daily Full Backup (Last 7 days) </li>
                      <li>Hourly database backup (Last 24 hours) </li>
                      <li>Free Malware Protection </li>
                      <li>Free Expert Site Migration </li>
                      <li>Latest cPanel </li>
                    </ul>
                    <a href="https://account.hostservice.cloud/index.php?rp=/store/bdix-toofan/rapid-flare"
                      class="btn outline-btn mb-3" target="_blank">Purchase now</a>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </swiper-slide>

        <swiper-slide>
          <div class="container">
            <div class="row align-items-center justify-content-between">
              <div class="col-lg-12 col-md-12 col-12">
                <div class="card text-center align-items-center single-pricing-pack">
                  <div class="pt-5">
                    <h5 class="mb-0 text-brand">BDIX Toofan server</h5>
                    <p class="mb-0"> Speed Xpress </p>
                  </div>
                  <div class="card-header border-0 pricing-header">
                    <div class="price text-center mb-0">৳ {{ theryMonth }}<span>/-BDT Only.</span></div>
                  </div>
                  <div class="card-body">
                    <ul class="list-unstyled mb-4 pricing-feature-list">
                      <li>200 GB NVMe Storage </li>
                      <li>Unlimited Bandwidth </li>
                      <li>8 Core CPU 5.9 GHz Pro </li>
                      <li>16 GB RAM, 4800 MHz </li>
                      <li>800 Mbps I/O </li>
                      <li>1000 Entry Processes </li>
                      <li>2000 Number Of Processes </li>
                      <li>Free SSL Certificate </li>
                      <li>LiteSpeed with LSCache </li>
                      <li>Turbo (Up To 20X Faster) </li>
                      <li>Daily Full Backup (Last 7 days) </li>
                      <li>Hourly database backup (Last 24 hours) </li>
                      <li>Free Malware Protection </li>
                      <li>Free Expert Site Migration </li>
                      <li>Latest cPanel </li>
                    </ul>
                    <a href="https://account.hostservice.cloud/index.php?rp=/store/bdix-toofan/speed-xpress"
                      class="btn outline-btn mb-3" target="_blank">Purchase now</a>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </swiper-slide>

        <swiper-slide>
          <div class="container">
            <div class="row align-items-center justify-content-between">
              <div class="col-lg-12 col-md-12 col-12">
                <div class="card text-center align-items-center single-pricing-pack">
                  <div class="pt-5">
                    <h5 class="mb-0 text-brand">BDIX Toofan server</h5>
                    <p class="mb-0"> Hyper Drive </p>
                  </div>
                  <div class="card-header border-0 pricing-header">
                    <div class="price text-center mb-0">৳ {{ halfYear }}<span>/-BDT Only.</span></div>
                  </div>
                  <div class="card-body">
                    <ul class="list-unstyled mb-4 pricing-feature-list">
                      <li>300 GB NVMe Storage </li>
                      <li>Unlimited Bandwidth </li>
                      <li>16 Core CPU 5.9 GHz Pro </li>
                      <li>32 GB RAM, 4800 MHz </li>
                      <li>1200 Mbps I/O </li>
                      <li>1500 Entry Processes </li>
                      <li>3000 Number Of Processes </li>
                      <li>Free SSL Certificate </li>
                      <li>LiteSpeed with LSCache </li>
                      <li>Turbo (Up To 20X Faster) </li>
                      <li>Daily Full Backup (Last 7 days) </li>
                      <li>Hourly database backup (Last 24 hours) </li>
                      <li>Free Malware Protection </li>
                      <li>Free Expert Site Migration </li>
                      <li>Latest cPanel </li>
                    </ul>
                    <a href="https://account.hostservice.cloud/index.php?rp=/store/bdix-toofan/hyper-drive"
                      class="btn outline-btn mb-3" target="_blank">Purchase now</a>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </swiper-slide>
      </swiper>
    </div>
  </section> <br> <br>
  <br>

  <section class="compare-provider-table ptb-100 gray-light-bg-n">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-md-12 col-lg-7 ">
          <div class="section-heading  text-center mb-5">
            <h3 class="media-la text-brand">BDIX Toofan Server Resource</h3>
            <p class="h5 web-s bt-bl">
              Exclusive BDIX Toofan server resource
            </p>
          </div>
        </div>
        <div class="row table">
          <div class="col-md-12 col-lg-12">
            <div class="table-responsive">
              <table
                class="table w-100 table-res table-hover table-bordered table-striped comparision-table text-center">
                <thead class="comparision-table-head">

                  <tr>
                    <td class="primary-bg" style="width: 25%; text-align: center">
                      <h5 class="text-white">Resource Type</h5>
                    </td>
                    <td style="width: 25%; text-align: center;">
                      <h5>Rapid Flare Standard </h5>
                    </td>
                    <td style="width: 25%; text-align: center;">
                      <h5>Speed Xpress Silver </h5>
                    </td>
                    <td style="width: 25%; text-align: center;">
                      <h5>Hyper Drive Gold </h5>
                    </td>
                    <!-- <td style="width: 20%; text-align: center;">
                      <h5>Rocket Gold </h5>
                    </td> -->
                  </tr>

                </thead>
                <tbody class="comparision-table-body">
                  <tr style="width: 20%; text-align: center">
                    <td class="primary-bg">
                      <h6 class="text-left text-white text-pl">NVMe Storage </h6>
                    </td>
                    <td>
                      <h6>100 GB </h6>
                    </td>
                    <td>
                      <h6>200 GB </h6>
                    </td>
                    <td>
                      <h6>300 GB </h6>
                    </td>
                    <!-- <td>
                      <h6>12 Core CPU 5.7 GHz </h6>
                    </td> -->
                  </tr>
                  <tr style="width: 20%; text-align: center">
                    <td class="primary-bg">
                      <h6 class="text-left text-white text-pl">Bandwidth</h6>
                    </td>
                    <td>
                      <h6>Unlimited </h6>
                    </td>
                    <td>
                      <h6>Unlimited </h6>
                    </td>
                    <td>
                      <h6>Unlimited </h6>
                    </td>
                    <!-- <td>
                      <h6>22 GB, 4800 MHg </h6>
                    </td> -->
                  </tr>

                  <tr style="width: 20%; text-align: center">
                    <td class="primary-bg">
                      <h6 class="text-left text-white text-pl">CPU</h6>
                    </td>
                    <td>
                      <h6>4 Core 5.9 GHz Pro </h6>
                    </td>
                    <td>
                      <h6>8 Core 5.9 GHz Pro </h6>
                    </td>
                    <td>
                      <h6>16 Core 5.9 GHz Pro </h6>
                    </td>
                    <!-- <td>
                      <h6>750 GB </h6>
                    </td> -->
                  </tr>
                  <tr style="width: 20%; text-align: center">
                    <td class="primary-bg">
                      <h6 class="text-left text-white text-pl">RAM & MHz</h6>
                    </td>
                    <td>
                      <h6>8 GB RAM, 4800 MHz</h6>
                    </td>
                    <td>
                      <h6>16 GB RAM, 4800 MHz</h6>
                    </td>
                    <td>
                      <h6>32 GB RAM, 4800 MHz</h6>
                    </td>
                    <!-- <td>
                      <h6>350 MBs</h6>
                    </td> -->
                  </tr>
                  <tr style="width: 20%; text-align: center">
                    <td class="primary-bg">
                      <h6 class="text-left text-white text-pl"> Mbps I/O</h6>
                    </td>
                    <td>
                      <h6>400 Mbps I/O</h6>
                    </td>
                    <td>
                      <h6>800 Mbps I/O</h6>
                    </td>
                    <td>
                      <h6>1200 Mbps I/O </h6>
                    </td>
                    <!-- <td>
                      <h6>Unlimited</h6>
                    </td> -->
                  </tr>
                  <tr style="width: 20%; text-align: center">
                    <td class="primary-bg">
                      <h6 class="text-left text-white text-pl">Processes</h6>
                    </td>
                    <td>
                      <h6>500 Entry Processes </h6>
                    </td>
                    <td>
                      <h6>1000 Entry Processes</h6>
                    </td>
                    <td>
                      <h6>1500 Entry Processes </h6>
                    </td>
                    <!-- <td>
                      <h6>6144</h6>
                    </td> -->
                  </tr>
                  <tr style="width: 20%; text-align: center">
                    <td class="primary-bg">
                      <h6 class="text-left text-white text-pl">Number Of Processes </h6>
                    </td>
                    <td>
                      <h6>1000 </h6>
                    </td>
                    <td>
                      <h6>2000 </h6>
                    </td>
                    <td>
                      <h6>3000 </h6>
                    </td>
                    <!-- <td>
                      <h6>400 </h6>
                    </td> -->
                  </tr>
                  <tr style="width: 20%; text-align: center">
                    <td class="primary-bg">
                      <h6 class="text-left text-white text-pl"> Turbo </h6>
                    </td>
                    <td>
                      <h6>(Up To 20X Faster)</h6>
                    </td>
                    <td>
                      <h6>(Up To 20X Faster)</h6>
                    </td>
                    <td>
                      <h6> (Up To 20X Faster)</h6>
                    </td>
                    <!-- <td>
                      <h6>Unlimited</h6>
                    </td> -->
                  </tr>
                  <tr style="width: 20%; text-align: center">
                    <td class="primary-bg">
                      <h6 class="text-left text-white text-pl">cPanel</h6>
                    </td>
                    <td>
                      <h6>Latest cPanel </h6>
                    </td>
                    <td>
                      <h6>Latest cPanel </h6>
                    </td>
                    <td>
                      <h6>Latest cPanel </h6>
                    </td>
                    <!-- <td class="col-12">
                      <h6>790 </h6>
                    </td> -->
                  </tr>
                </tbody>
              </table>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!--feature section start-->
  <section class="feature-section ptb-100 ">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-md-9 col-lg-8">
          <div class="section-heading text-center mb-5">
            <h3 class="media-la text-brand">Server Platform Features</h3>
            <p class="h5 web-s">Standard Features: Dynamic Open-Source Expansion.</p>
          </div>
        </div>
      </div>
      <div class="row">
        <div class="col-md-6 col-lg-4">
          <div class="feature-feature-list p-4 text-center">
            <span class="ti-harddrives icon-sm d-block color-primary mb-3"></span>
            <h5 class="mb-2">SSD Disk Drives</h5>
            <p>You can never go wrong with our own top-notch dedicated servers loaded</p>
          </div>
        </div>
        <div class="col-md-6 col-lg-4">
          <div class="feature-feature-list p-4 text-center">
            <span class="ti-rss-alt icon-sm d-block color-primary mb-3"></span>
            <h5 class="mb-2">100 Mb/s Network</h5>
            <p>We can guarantee an excellent experience and loading time for your successful</p>
          </div>
        </div>
        <div class="col-md-6 col-lg-4">
          <div class="feature-feature-list p-4 text-center">
            <span class="ti-lock icon-sm d-block color-primary mb-3"></span>
            <h5 class="mb-2">DDoS Protection</h5>
            <p>With full root access you will be able to take full control of your server very easy</p>
          </div>
        </div>
        <div class="col-md-6 col-lg-4">
          <div class="feature-feature-list p-4 text-center">
            <span class="ti-world icon-sm d-block color-primary mb-3"></span>
            <h5 class="mb-2">Dedicated IP</h5>
            <p>One of many premium features is a dedicated IP cheapest BDIX Toofan server plan</p>
          </div>
        </div>
        <div class="col-md-6 col-lg-4">
          <div class="feature-feature-list p-4 text-center">
            <span class="ti-location-pin icon-sm d-block color-primary mb-3"></span>
            <h5 class="mb-2">IPv6 Support</h5>
            <p>Our BDIX Toofan server plan is fully packed with dedicated IPv6 Internet protocol IP</p>
          </div>
        </div>
        <div class="col-md-6 col-lg-4">
          <div class="feature-feature-list p-4 text-center">
            <span class="ti-wallet icon-sm d-block color-primary mb-3"></span>
            <h5 class="mb-2">Money-back Guarantee</h5>
            <p>If you’re not 100% satisfied with Host service, we’ll refund your payment no risk</p>
          </div>
        </div>
      </div>
    </div>
  </section>
  <!--feature section end-->

  <!--call to action new section start-->
  <section class="call-to-action backvps ptb-100 gradient-overlay">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-md-9 col-lg-8">
          <div class="cta-new-wrap text-white text-center">
            <h3 class="text-white bm-d">30-day Money-back Guarantee</h3>
            <p class="lead">Globally parallel task granular alignments through excellent intellectual capital.
              Globally deploy vertical leadership.</p>
            <div class="action-btns mt-4">
              <a href="#" class="btn solid-white-btn animated-btn mr-lg-3">Get
                Started Now</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
  <!--call to action new section end-->
  <!--testimonial and review section start-->
  <section class="client-review-section ptb-100 gray-light-bg">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-md-9 col-lg-8">
          <div class="section-heading text-center mb-5">
            <h3 class="media-la text-brand">Our Customers Say About Us?</h3>
            <p class="h5 web-s bt-bl">Revitalizing E-Markets: Tested & Researched Approach.</p>
          </div>
        </div>
      </div>
      <div class="row">
        <div class="col-md-6 mr-con col-lg-4">
          <div class="single-testimonial white-bg shadow-sm rounded p-5">
            <ul class="list-inline ratting-list mb-2">
              <li class="list-inline-item"><span class="fas fa-star"></span></li>
              <li class="list-inline-item"><span class="fas fa-star"></span></li>
              <li class="list-inline-item"><span class="fas fa-star"></span></li>
              <li class="list-inline-item"><span class="fas fa-star"></span></li>
              <li class="list-inline-item"><span class="fas fa-star"></span></li>
            </ul>
            <div class="ratting-content">
              <h5>Exceptional BDIX Toofan server!</h5>
              <p>I've been using their BDIX Toofan server for my e-commerce website, and the performance has been
                outstanding.
                The dedicated resources ensure consistent speed and reliability, even during peak traffic periods. </p>
            </div>
            <div class="ratting-author mt-3">
              <h6>Alex Khamer</h6>
              <small class="text-right">6 days ago</small>
            </div>
          </div>
        </div>
        <div class="col-md-6 mr-con col-lg-4">
          <div class="single-testimonial white-bg shadow-sm rounded p-5">
            <ul class="list-inline ratting-list mb-2">
              <li class="list-inline-item"><span class="fas fa-star"></span></li>
              <li class="list-inline-item"><span class="fas fa-star"></span></li>
              <li class="list-inline-item"><span class="fas fa-star"></span></li>
              <li class="list-inline-item"><span class="fas fa-star"></span></li>
              <li class="list-inline-item"><span class="fas fa-star"></span></li>
            </ul>
            <div class="ratting-content">
              <h5>BDIX Toofan server Provider!</h5>
              <p>I switched to this BDIX Toofan server provider after experiencing frequent downtime with my previous
                host. Since
                making the switch,
                I've been impressed by the stability and performance of their servers.</p>
            </div>
            <div class="ratting-author mt-3">
              <h6>Ryan H.</h6>
              <small class="text-right">3 days ago</small>
            </div>
          </div>
        </div>
        <div class="col-md-6 mr-con col-lg-4">
          <div class="single-testimonial white-bg shadow-sm rounded p-5">
            <ul class="list-inline ratting-list mb-2">
              <li class="list-inline-item"><span class="fas fa-star"></span></li>
              <li class="list-inline-item"><span class="fas fa-star"></span></li>
              <li class="list-inline-item"><span class="fas fa-star"></span></li>
              <li class="list-inline-item"><span class="fas fa-star"></span></li>
              <li class="list-inline-item"><span class="fas fa-star"></span></li>
            </ul>
            <div class="ratting-content">
              <h5>Impressive Performance Server!</h5>
              <p>As a developer, I require a reliable BDIX Toofan solution for my projects, and this server service
                delivers
                exactly that.
                The BDIX Toofan performance is impressive, The support team is responsive.</p>
            </div>
            <div class="ratting-author mt-3">
              <h6>Jolio Darix</h6>
              <small class="text-right">8 days ago</small>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
  <!--testimonial and review section end-->
  <!-- faq -->
  <section>
    <div class="container">
      <div id="faq" class="ptb-100">
        <div class="container">
          <div class="row">
            <div class="col-md-9 col-lg-8">
              <div class="section-heading mb-5">
                <h3 class="media-la text-brand">Frequently Asked Queries</h3>
                <p class="h5 web-s">Server Made Simple: Ask Us Anything ! <a href="contact" class="page-scroll"> Contact
                    us</a></p>
              </div>
            </div>
          </div>
          <div class="row">
            <div class="col-md-12 col-lg-12">
              <div id="accordion-one" class="accordion accordion-faq">
                <div class="card mb-0">
                  <a class="card-header collapsed" data-toggle="collapse" href="#collapseOne">
                    <h6 class="mb-0 d-inline-block">What is BDIX Toofan Server?
                    </h6>
                  </a>
                  <div id="collapseOne" class="collapse" data-parent="#accordion-one">
                    <div class="card-body">
                      <p> BDIX Toofan server is a high-performance solution designed to deliver exceptional speed,
                        security,
                        and scalability for websites and applications.
                      </p>
                    </div>
                  </div>
                </div>
                <div class="card mb-0">
                  <a class="card-header collapsed" data-toggle="collapse" href="#collapseTwo">
                    <h6 class="mb-0 d-inline-block">What makes BDIX Toofan server stand out from other options?</h6>
                  </a>
                  <div id="collapseTwo" class="collapse" data-parent="#accordion-one">
                    <div class="card-body">
                      <p>BDIX Toofan server utilizes advanced optimization techniques and server configurations to
                        ensure
                        blazing-fast performance and seamless scalability for online projects of all sizes.
                      </p>
                    </div>
                  </div>
                </div>
                <div class="card mb-0">
                  <a class="card-header collapsed" data-toggle="collapse" href="#collapseThree">
                    <h6 class="mb-0 d-inline-block">Which types of websites or applications are best suited for BDIX
                      Toofan server?
                    </h6>
                  </a>
                  <div id="collapseThree" class="collapse" data-parent="#accordion-one">
                    <div class="card-body">
                      <p>BDIX Toofan server is ideal for websites and applications that require high-speed performance,
                        such as e-commerce platforms, content-heavy websites, and media streaming services.
                      </p>
                    </div>
                  </div>
                </div>
                <div class="card mb-0">
                  <a class="card-header collapsed" data-toggle="collapse" href="#collapseFour">
                    <h6 class="mb-0 d-inline-block">Does BDIX Toofan server offer security features to protect my
                      website
                      or application?
                    </h6>
                  </a>
                  <div id="collapseFour" class="collapse" data-parent="#accordion-one">
                    <div class="card-body">
                      <p>Yes, BDIX Toofan server includes robust security measures such as DDoS protection, firewalls,
                        malware scanning, and SSL encryption to safeguard your online assets from threats.
                      </p>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style>
.slider-demo-block {
  display: flex;
  align-items: center;
}

.slider-demo-block .el-slider {
  margin-top: 0;
  margin-left: 12px;
}

.backvp {
  background-image: url("@/assets/img/baner2.webp");
}

.backvps {
  background-image: url("@/assets/img/z2.png");
}


#app {
  height: 100%;
}

html,
body {
  position: relative;
  height: 60%;
}

body {
  background: #eee;
  font-family: Helvetica Neue, Helvetica, Arial, sans-serif;
  font-size: 14px;
  color: #000;
  margin: 0;
  padding: 0;
}

.swiper {
  width: 100%;
  height: 60%;
  padding-top: 0px;
}

.swiper-slide {
  text-align: center;
  font-size: 18px;
  background: #fff;

  /* Center slide text vertically */
  display: flex;
  justify-content: center;
  align-items: center;
}

.swiper-slide img {
  display: block;
  width: 600%;
  height: 60%;
  object-fit: cover;
}</style>