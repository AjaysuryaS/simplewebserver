# EX01 Developing a Simple Webserver
## Date:24.03.2024

## AIM:
To develop a simple webserver to serve html pages.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Serving the HTML pages.

### Step 5:
Testing the webserver.

## PROGRAM:
from http.server import BaseHTTPRequestHandler, HTTPServer

<!doctype html>
<html lang="en">
  
<head>
   <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
    <meta name="description" content="Ajay - Creative Personal CV/Resume HTML Template">
    <meta name="author" content="Ajay">

    <title>Ajay - Creative Personal CV/Resume HTML Template</title>

    <!-- CSS -->
    <link rel="stylesheet" href="css/style.css">

    <!-- Favicon -->
    <link rel="icon" type="image/jpg" href="my.jpg">
  </head>
  <body class="fixed-footer">

    <!-- Loader -->
   <div class="loader">
    <div class="spinner"><div class="double-bounce1"></div><div class="double-bounce2"></div></div>
   </div>

    <!-- Click capture -->
    <div class="click-capture d-lg-none"></div>

    <!-- Navbar -->  
    <nav id="scrollspy" class="navbar navbar-desctop">
        
      <div class="d-flex align-items-center position-relative w-100">

        <!-- Brand-->
        <a class="navbar-brand" href="#">Ajay</a>

        <div class="container">
          <ul class="navbar-nav navbar-nav-desctop  d-none d-lg-block">
            <li><a class="nav-link" href="#home">Home</a></li>
            <li><a class="nav-link" href="#about">About</a></li>
            <li><a class="nav-link" href="#specialization">Specialization</a></li>
            <li><a class="nav-link" href="#works">Projects</a></li>
            <li><a class="nav-link" href="#experience">Experience</a></li>
            <li><a class="nav-link" href="#contact">Contact</a></li>
          </ul>

          <!-- Social -->
          <ul class="social-icons d-none d-lg-block">
            <li><a href="#"><ion-icon name="logo-facebook"></ion-icon></a></li>
            <li><a href="#"><ion-icon name="logo-twitter"></ion-icon></a></li>
            <li><a href="#"><ion-icon name="logo-linkedin"></ion-icon></a></li>
          </ul>
        </div>
          
        <!-- Toggler -->
        <button class="toggler d-block d-lg-none">
          <span class="toggler-icon"></span>
          <span class="toggler-icon"></span>
          <span class="toggler-icon"></span>
        </button>
      </div>
    </nav>

    <!-- Navbar Mobile -->  
    <nav class="navbar navbar-mobile d-lg-none">
      <ion-icon class="close" name="close-outline"></ion-icon>

      <!-- Language -->
      <ul class="language">
         <li class="active"><a href="#">Eng</a></li>
         <li><a href="#">Fra</a></li>
         <li><a href="#">Ger</a></li>
      </ul>

      <ul class="navbar-nav navbar-nav-mobile">
        <li><a class="nav-link" href="#home">Home</a></li>
        <li><a class="nav-link" href="#about">About</a></li>
        <li><a class="nav-link" href="#specialization">Specialization</a></li>
        <li><a class="nav-link" href="#works">Projects</a></li>
        <li><a class="nav-link" href="#experience">Experience</a></li>
        <li><a class="nav-link" href="#contact">Contact</a></li>
      </ul>
     <div class="navbar-mobile-footer">
      <p>© 2020 Ajay. All Rights Reserved.</p>
     </div>
    </nav>

    <div class="wrapper">

 <!-- Masthead -->
<main id="home" class="masthead jarallax" style="background-image: url('img/bg/IMG_3050.JPG');" role="main">
  <!-- Lines -->
  <div class="lines">
    <div class="container">
      <div class="row">
        <div class="col-md-6 col-lg-4"></div>
        <div class="col-md-6 hidden-sm col-lg-4"></div>
        <div class="col-md-6 col-lg-4 hidden-md"></div>
      </div>
    </div>
  </div>

  <!-- Opener -->
  <div class="opener blur-scroll">
    <div class="container">
      <div class="row mx-0">
        <div class="col-md-4 px-0">
          <p class="text-dark">Saveetha Student</p>
          <h1 class="my-0"><span class="text-primary">Hello,</span> i’m Ajay Surya.</h1>
        </div>
      </div>
    </div>
  </div>
</main>

      <!-- Content -->
      <div class="content">

        <!-- Lines -->
        <div class="lines">
          <div class="container">
            <div class="row">
              <div class="col-md-6 col-lg-4"></div>
              <div class="col-md-6 hidden-sm col-lg-4"></div>
              <div class="col-md-6 col-lg-4 hidden-md"></div>
            </div>
          </div>
        </div>

        <!-- About -->
        <section id="about" class="section pb-0">
          <section class="container">
            <div class="row mx-0 align-items-center">
              <div class="col-md-6 col-lg-4 px-0 offset-lg-4">
                <h2 class="mt-0 wide-lg mb-5 mb-md-0" data-aos="fade-up">My <span class="text-primary">mission</span>  is develope the best websites<br> <span class="text-primary">around</span></h2>
              </div>
              <div class="col-md-6 col-lg-4 px-0" data-aos="blur">
                <img alt="" class="w-100" src="img/370x434-1.jpg">
              </div>
            </div>
            <div class="row mx-0">
              <div class="col-lg-4 px-0 mt-5 mt-md-0 mb-5 mb-lg-0">
                <ul class="my-0">
                  <li data-aos="fade-up">
                    <a href="#" class="text-body">
                      <span class="media">
                        <span class="pr-4">01.</span>
                        <span class="media-body">Logo Design</span>
                      </span>
                    </a>
                  </li>
                  <li data-aos="fade-up" data-aos-delay="100">
                    <a href="#" class="text-body">
                      <span class="media">
                        <span class="pr-4">02.</span>
                        <span class="media-body">Business Card Design</span>
                      </span>
                    </a>
                  </li>
                  <li data-aos="fade-up" data-aos-delay="200">
                    <a href="#" class="text-body">
                      <span class="media">
                        <span class="pr-4">03.</span>
                        <span class="media-body">Stationery Design</span>
                      </span>
                    </a>
                  </li>
                  <li data-aos="fade-up" data-aos-delay="300">
                    <a href="#" class="text-body">
                      <span class="media">
                        <span class="pr-4">04.</span>
                        <span class="media-body">Letterhead Design</span>
                      </span>
                    </a>
                  </li>
                  <li data-aos="fade-up" data-aos-delay="400">
                    <a href="#" class="text-body">
                      <span class="media">
                        <span class="pr-4">05.</span>
                        <span class="media-body">Brouchers</span>
                      </span>
                    </a>
                  </li>
                </ul>
              </div>
            </div>
          </section>
        </section>
        
        <!-- Specialization -->
        <section id="specialization" class="section py-0">
          <div class="container">
            <div class="row mx-0 align-items-center">
              <div class="col-md-6 order-md-2 order-lg-1 col-lg-4 px-0">
                <h2 class="my-0 wide-lg float-md-right float-lg-none offset-lg-5 mb-5 mb-md-0" data-aos="fade-right">I <span class="text-primary">use</span> the latest technology</h2>
              </div>
              <div class="col-md-6 order-md-1 order-lg-2 col-lg-4 px-0"  data-aos="blur">
                <img alt="" class="w-100" src="img/370x434-2.jpg">
              </div>
              <div class="col-md-6 offset-md-6 offset-lg-0 order-md-3 order-lg-3 col-lg-4 mt-5 pl-0 pl-md-30 mt-md-0" data-aos="fade-up">
                <p class="mb-0 pl-md-30px">We have experience in implementing projects for many large domestic and foreign corporations, enterprises in many elds such as nance, banking, F&B, education, communication.</p>
              </div>
            </div>
            <section class="section-sm pb-0">
              <div class="row mx-0">
                <div class="col-md-12 col-lg-4 px-0 pr-lg-30px mb-5 mb-lg-0">
                  <div class="d-flex justify-content-between">
                    <h6 class="mt-0 d-flex">Web Design</h6>
                    <h6 class="mt-0 d-flex">80%</h6>
                  </div>
                  <div class="progress">
                    <div class="progress-bar" role="progressbar" style="width: 80%" aria-valuenow="80" aria-valuemin="0" aria-valuemax="80">
                      <div class="progress-bar-line" data-aos="width"></div>
                    </div>
                  </div>
                </div>
                <div class="col-md-12 col-lg-4 px-0 pr-lg-30px mb-5 mb-lg-0">
                  <div class="d-flex justify-content-between">
                    <h6 class="mt-0 d-flex">Figma</h6>
                    <h6 class="mt-0 d-flex">70%</h6>
                  </div>
                  <div class="progress">
                    <div class="progress-bar" role="progressbar" style="width: 70%" aria-valuenow="70" aria-valuemin="0" aria-valuemax="70">
                      <div class="progress-bar-line" data-aos-delay="200" data-aos="width"></div>
                    </div>
                  </div>
                </div>
                <div class="col-md-12 col-lg-4 pl-0 pr-lg-30px">
                  <div class="d-flex justify-content-between">
                    <h6 class="mt-0 d-flex">WordPress</h6>
                    <h6 class="mt-0 d-flex">90%</h6>
                  </div>
                  <div class="progress">
                    <div class="progress-bar" role="progressbar" style="width: 90%" aria-valuenow="90" aria-valuemin="0" aria-valuemax="90">
                      <div class="progress-bar-line" data-aos-delay="400" data-aos="width" ></div>
                    </div>
                  </div>
                </div>
              </div>
            </section>
          </div>
        </section>
        
        <!-- Latest Works -->
        <section id="works" class="section pb-0">
          <div class="container">
            <h2 class="my-0" data-aos="fade-right">Latest works</h2>
          </div>
          <section class="section-sm section-right pb-0" data-aos="blur">
            <div class="works-carousel owl-carousel">
              <div>
                <a href="#">
                <figure class="hover">
                  <img alt="" class="img-responsive" src="img/portfolio/740x540-1.jpg">
                    <figcaption>
                       <mark class="h3 my-0 text-white">Creative Man</mark><br>
                       <mark class="mt-2 category">Photography</mark>
                    </figcaption>
                  </figure>
                </a>
              </div>
              <div>
                <a href="#">
                <figure class="hover">
                  <img alt="" class="img-responsive" src="img/portfolio/740x540-2.jpg">
                    <figcaption>
                       <mark class="h3 my-0 text-white">Quanima</mark><br>
                       <mark class="mt-2 category">Product Design</mark>
                    </figcaption>
                  </figure>
                </a>
              </div>
              <div>
                <a href="#">
                <figure class="hover">
                  <img alt="" class="img-responsive" src="img/portfolio/740x540-3.jpg">
                    <figcaption>
                       <mark class="h3 my-0 text-white">Atm Pizza</mark><br>
                       <mark class="mt-2 category">Branding</mark>
                    </figcaption>
                  </figure>
                </a>
              </div>
              <div>
                <a href="#">
                <figure class="hover">
                  <img alt="" class="img-responsive" src="img/portfolio/740x540-4.jpg">
                    <figcaption>
                       <mark class="h3 my-0 text-white">Lick</mark><br>
                       <mark class="mt-2 category">Product Design</mark>
                    </figcaption>
                  </figure>
                </a>
              </div>
            </div>
          </section>
        </section>
        
        <!-- Experience -->
        <section id="experience" class="section pb-0" data-aos="fade-up">
          <div class="container">
            <div class="row mx-0">
              <div class="col-lg-4 offset-lg-4 px-0">
                <h2 class="my-0">Experience</h2>
              </div>
            </div>
          </div>
          <section class="section-sm pb-0">
            <div class="container">
              <div class="experience-carousel owl-carousel">
                <div>
                  <div class="row mx-0" data-aos="fade-in">
                    <div class="col-lg-4 px-0 text-dark text-right text-lg-left mb-2 mb-lg-0">
                      2019-2020
                    </div>
                    <div class="col-lg-4 pl-0 mb-4 mb-lg-0">
                      <div class="media align-items-center">
                        <img alt=""  class="mr-4" src="img/behance.png">
                        <div class="media-body">
                          <h5 class="my-0">UI/UX Designer,<br> <span class="text-body font-weight-normal">Behance.</span></h5>
                        </div>
                      </div>
                    </div>
                    <div class="col-lg-4 px-0">
                      <p class="mb-0">We have experience in implementing projects for many large domestic and foreign corporations, enterprises in many elds such as nance, banking, F&B, education, communication.</p>
                    </div>
                  </div>
                  <div class="section-sm" data-aos="fade-in">
                    <div class="position-relative section-sm bg-gray">

                      <!-- Lines -->
                      <div class="lines">
                        <div class="container px-0">
                          <div class="row">
                            <div class="col-md-6 col-lg-4"></div>
                            <div class="col-md-6 hidden-sm col-lg-4"></div>
                            <div class="col-md-6 col-lg-4 hidden-md"></div>
                          </div>
                        </div>
                      </div>
                      <section class="row mx-0">
                        <div class="col-lg-4 order-2 pl-0 mb-4 mb-lg-0">
                          <div class="media align-items-center">
                            <img alt=""  class="mr-4" src="img/cssdesignawards.png">
                            <div class="media-body">
                              <h5 class="my-0">Product Designer,<br> <span class="text-body font-weight-normal">Cssdesignawards</span></h5>
                            </div>
                          </div>
                        </div>
                        <div class="col-lg-4 order-3 pl-0">
                          <p class="mb-0">We have experience in implementing projects for many large domestic and foreign corporations, enterprises in many elds such as nance, banking, F&B, education, communication.</p>
                        </div>
                        <div class="col-lg-4 order-1 order-lg-3 text-dark text-right mb-2 mb-lg-0 px-0">
                          2018-2019
                        </div>
                      </section>
                    </div>
                  </div>
                  <div class="row mx-0" data-aos="fade-in">
                    <div class="col-lg-4 pl-0 text-dark  text-right text-lg-left mb-2 mb-lg-0">
                      2019-2020
                    </div>
                    <div class="col-lg-4 pl-0 mb-4 mb-lg-0">
                      <div class="media align-items-center">
                        <img alt=""  class="mr-4" src="img/envato.png">
                        <div class="media-body">
                          <h5 class="my-0">Frontend Developer,<br> <span class="text-body font-weight-normal">Envato.</span></h5>
                        </div>
                      </div>
                    </div>
                    <div class="col-lg-4 px-0">
                      <p class="mb-0">We have experience in implementing projects for many large domestic and foreign corporations, enterprises in many elds such as nance, banking, F&B, education, communication.</p>
                    </div>
                  </div>
                </div>
                <div>
                  <div class="row mx-0" data-aos="fade-in">
                    <div class="col-lg-4 px-0 text-dark text-right text-lg-left mb-2 mb-lg-0">
                      2019-2020
                    </div>
                    <div class="col-lg-4 pl-0 mb-4 mb-lg-0">
                      <div class="media align-items-center">
                        <img alt=""  class="mr-4" src="img/behance.png">
                        <div class="media-body">
                          <h5 class="my-0">UI/UX Designer,<br> <span class="text-body font-weight-normal">Behance.</span></h5>
                        </div>
                      </div>
                    </div>
                    <div class="col-lg-4 px-0">
                      <p class="mb-0">We have experience in implementing projects for many large domestic and foreign corporations, enterprises in many elds such as nance, banking, F&B, education, communication.</p>
                    </div>
                  </div>
                  <div class="section-sm" data-aos="fade-in">
                    <div class="position-relative section-sm bg-gray">

                     <!-- Lines -->
                      <div class="lines">
                        <div class="container px-0">
                          <div class="row">
                            <div class="col-md-6 col-lg-4"></div>
                            <div class="col-md-6 hidden-sm col-lg-4"></div>
                            <div class="col-md-6 col-lg-4 hidden-md"></div>
                          </div>
                        </div>
                      </div>
                      <section class="row mx-0">
                        <div class="col-lg-4 order-2 pl-0 mb-4 mb-lg-0">
                          <div class="media align-items-center">
                            <img alt=""  class="mr-4" src="img/cssdesignawards.png">
                            <div class="media-body">
                              <h5 class="my-0">Product Designer,<br> <span class="text-body font-weight-normal">Cssdesignawards</span></h5>
                            </div>
                          </div>
                        </div>
                        <div class="col-lg-4 order-3 pl-0">
                          <p class="mb-0">We have experience in implementing projects for many large domestic and foreign corporations, enterprises in many elds such as nance, banking, F&B, education, communication.</p>
                        </div>
                        <div class="col-lg-4 order-1 order-lg-3 text-dark text-right mb-2 mb-lg-0 px-0">
                          2018-2019
                        </div>
                      </section>
                    </div>
                  </div>
                  <div class="row mx-0" data-aos="fade-in">
                    <div class="col-lg-4 pl-0 text-dark  text-right text-lg-left mb-2 mb-lg-0">
                      2019-2020
                    </div>
                    <div class="col-lg-4 pl-0 mb-4 mb-lg-0">
                      <div class="media align-items-center">
                        <img alt=""  class="mr-4" src="img/envato.png">
                        <div class="media-body">
                          <h5 class="my-0">Frontend Developer,<br> <span class="text-body font-weight-normal">Envato.</span></h5>
                        </div>
                      </div>
                    </div>
                    <div class="col-lg-4 px-0">
                      <p class="mb-0">We have experience in implementing projects for many large domestic and foreign corporations, enterprises in many elds such as nance, banking, F&B, education, communication.</p>
                    </div>
                  </div>
                </div>
                <div>
                  <div class="row mx-0" data-aos="fade-in">
                    <div class="col-lg-4 px-0 text-dark text-right text-lg-left mb-2 mb-lg-0">
                      2019-2020
                    </div>
                    <div class="col-lg-4 pl-0 mb-4 mb-lg-0">
                      <div class="media align-items-center">
                        <img alt=""  class="mr-4" src="img/behance.png">
                        <div class="media-body">
                          <h5 class="my-0">UI/UX Designer,<br> <span class="text-body font-weight-normal">Behance.</span></h5>
                        </div>
                      </div>
                    </div>
                    <div class="col-lg-4 px-0">
                      <p class="mb-0">We have experience in implementing projects for many large domestic and foreign corporations, enterprises in many elds such as nance, banking, F&B, education, communication.</p>
                    </div>
                  </div>
                  <div class="section-sm" data-aos="fade-in">
                    <div class="position-relative section-sm bg-gray">

                      <!-- Lines -->
                      <div class="lines">
                        <div class="container px-0">
                          <div class="row">
                            <div class="col-md-6 col-lg-4"></div>
                            <div class="col-md-6 hidden-sm col-lg-4"></div>
                            <div class="col-md-6 col-lg-4 hidden-md"></div>
                          </div>
                        </div>
                      </div>
                      <section class="row mx-0">
                        <div class="col-lg-4 order-2 pl-0 mb-4 mb-lg-0">
                          <div class="media align-items-center">
                            <img alt=""  class="mr-4" src="img/cssdesignawards.png">
                            <div class="media-body">
                              <h5 class="my-0">Product Designer,<br> <span class="text-body font-weight-normal">Cssdesignawards</span></h5>
                            </div>
                          </div>
                        </div>
                        <div class="col-lg-4 order-3 pl-0">
                          <p class="mb-0">We have experience in implementing projects for many large domestic and foreign corporations, enterprises in many elds such as nance, banking, F&B, education, communication.</p>
                        </div>
                        <div class="col-lg-4 order-1 order-lg-3 text-dark text-right mb-2 mb-lg-0 px-0">
                          2018-2019
                        </div>
                      </section>
                    </div>
                  </div>
                  <div class="row mx-0" data-aos="fade-in">
                    <div class="col-lg-4 pl-0 text-dark  text-right text-lg-left mb-2 mb-lg-0">
                      2019-2020
                    </div>
                    <div class="col-lg-4 pl-0 mb-4 mb-lg-0">
                      <div class="media align-items-center">
                        <img alt=""  class="mr-4" src="img/envato.png">
                        <div class="media-body">
                          <h5 class="my-0">Frontend Developer,<br> <span class="text-body font-weight-normal">Envato.</span></h5>
                        </div>
                      </div>
                    </div>
                    <div class="col-lg-4 px-0">
                      <p class="mb-0">We have experience in implementing projects for many large domestic and foreign corporations, enterprises in many elds such as nance, banking, F&B, education, communication.</p>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </section>
        </section>
        
        <!-- Testimonials -->
        <section id="testimonials" class="section pb-0">
          <div class="container">
            <div class="row align-items-center mx-0">
              <div class="col-md-6 col-lg-4 col-xl-3 z-index-2 px-0 mb-5 mb-md-0">
                <div class="px-0 offset-lg-5 offset-xl-0">
                  <h2 class="testimonials-title my-0 wide-lg" data-aos="fade-right">Testimonials <span class="text-primary">from<br> my best</span>  Clients</h2>
                </div>
              </div>
              <div class="col-md-6 col-lg-8 col-xl-9 px-0">
                <div class="testimonials-carousel owl-carousel">
                  <div>
                    <div class="row align-items-center mx-0">
                      <div class="col-lg-6 col-xl-auto px-0 mr-xl-4" data-aos="blur">
                        <img alt="" class="w-100" src="img/testimonials/370x434-1.jpg">
                      </div>
                      <div class="col-lg-6 col-xl-5 offset-xl-1 px-0 pl-lg-30px pl-xl-0 mt-5 mt-lg-0">
                        <div class="quote mb-5"><img alt="" src="img/quote.png"></div>
                        <p class="mb-0">"I will give you a complete account of the system, and expound the actual teachings of the great explorer of the truth, the master-builder of human happiness."</p>
                        <h5 class="mt-4 mb-0">Hayley<br> <span class="text-body font-weight-normal">Apple inc.</span></h5>
                      </div>
                    </div>
                  </div>
                  <div>
                    <div class="row align-items-center mx-0">
                      <div class="col-lg-6 col-xl-auto px-0 mr-xl-4" data-aos="blur">
                        <img alt="" class="w-100" src="img/testimonials/370x434-2.jpg">
                      </div>
                      <div class="col-lg-6 col-xl-5 offset-xl-1 px-0 pl-lg-30px pl-xl-0 mt-5 mt-lg-0">
                        <div class="quote mb-5"><img alt="" src="img/quote.png"></div>
                        <p class="mb-0">"I will give you a complete account of the system, and expound the actual teachings of the great explorer of the truth, the master-builder of human happiness."</p>
                        <h5 class="mt-4 mb-0">Richard<br> <span class="text-body font-weight-normal">Envato</span></h5>
                      </div>
                    </div>
                  </div>
                  <div>
                    <div class="row align-items-center mx-0">
                      <div class="col-lg-6 col-xl-auto px-0 mr-xl-4" data-aos="blur">
                        <img alt="" class="w-100" src="img/testimonials/370x434-3.jpg">
                      </div>
                      <div class="col-lg-6 col-xl-5 offset-xl-1 px-0 pl-lg-30px pl-xl-0 mt-5 mt-lg-0">
                        <div class="quote mb-5"><img alt="" src="img/quote.png"></div>
                        <p class="mb-0">"I will give you a complete account of the system, and expound the actual teachings of the great explorer of the truth, the master-builder of human happiness."</p>
                        <h5 class="mt-4 mb-0">Amanda<br> <span class="text-body font-weight-normal">Google inc.</span></h5>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </section>
          
         <!-- Partners -->
        <section id="partners" class="section pb-0">
          <div class="container">
            <div class="row align-items-center text-center justify-content-between">
              <div class="col-sm-auto my-4 my-lg-0" data-aos="fade-up">
                <img alt="" src="img/partners/1.png">
              </div>
              <div class="col-sm-auto my-4 my-lg-0" data-aos="fade-up"  data-aos-delay="100">
                <img alt="" src="img/partners/2.png">
              </div>
              <div class="col-sm-auto my-4 my-lg-0" data-aos="fade-up"  data-aos-delay="200">
                <img alt="" src="img/partners/3.png">
              </div>
              <div class="col-sm-auto my-4 my-lg-0" data-aos="fade-up"  data-aos-delay="300">
                <img alt="" src="img/partners/4.png">
              </div>
            </div>
          </div>
        </section>
        
        <!-- News -->
        <section id="news" class="section pb-0">
          <div class="container">
            <div class="row mx-0">
              <div class="col-lg-4 px-0" data-aos="fade-right">
                <h2 class="my-0">Journal</h2>
              </div>
            </div>
            <section class="section-sm pb-0">
              <div class="row mx-0 align-items-center" data-aos="fade-up">
                <div class="col-md-6 col-lg-4 px-0" data-aos="blur">
                  <a href="#"><figure class="hover"><img alt="" class="w-100" src="img/news/370x434-1.jpg"></figure></a>
                </div>
                <div class="col-md-6 col-lg-4 mt-5 mt-md-0 px-sm-0 pl-md-30px pr-lg-30px">
                  <h4 class="my-0 mb-2"><a href="#">Top 20 Illustrations Winners: Academy</a></h4>
                  <p><a href="#" class="text-dark font-weight-bold">Illustration</a> / June 06, 2020</p>
                </div>
                <div class="col-md-6 col-lg-4 px-0 mt-4 mt-lg-0">
                  <p class="mb-0">We have experience in implementing projects for many large domestic and foreign corporations, enterprises in many elds such as nance, banking, F&B, education, communication... <a href="#">read more</a></p>
                </div>
              </div>
              <div class="row mx-0 align-items-center mt-5 mt-lg-0" data-aos="fade-up">
                <div class="col-md-6 col-lg-4 mt-5 mt-md-0 order-2 order-md-1 pl-0 pr-md-30px">
                  <h4 class="my-0 mb-2"><a href="#">Mapp MTL</a></h4>
                  <p><a href="#" class="text-dark font-weight-bold">Branding</a> / June 06, 2020</p>
                </div>
                <div class="col-md-6 offset-md-6 offset-lg-0 col-lg-4 order-3 order-lg-2  pl-0 pr-md-30px">
                  <div class="mt-4 mt-lg-0">
                    <p class="mb-0">There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injected humour... <a href="#">read more</a></p>
                  </div>
                </div>
                <div class="hover col-md-6 col-lg-4 order-1 order-md-2 order-lg-3  px-0" data-aos="blur">
                  <a href="#"><figure class="hover"><img alt="" class="w-100" src="img/news/370x434-2.jpg"></figure></a>
                </div>
              </div>
            </section>
          </div>
        </section>
        
        <!-- Contact -->
        <section  id="contact" class="section">
          <div class="container">
            <div class="row mx-0">
              <div class="col-lg-4 px-0">
                <div data-aos="fade-up">
                  <h2 class="my-0">Contact</h2>
                  <p class="mt-5 mb-0">You'll called for yielding male, so lights Stars abundantly, is their.</p>
                </div>
                <div data-aos="fade-up">
                  <section class="section-sm pb-0">
                    <h3 class="my-0">2nd street, Vellore</h3>
                  </section>
                </div>
                <div data-aos="fade-up">
                  <h3 class="mt-5 mb-0">9566344895</h3>
                  <p class="mt-5 mb-0">suriyasajai16@gmail.com</p>
                </div>
              </div>
              <div class="col-lg-6 offset-lg-2 mt-5 mt-lg-0 px-0">
                <h3 class="my-0" data-aos="fade-up">Let's grab a coffee and jump on conversation <span class="text-primary">chat with me.</span></h3>
                <section class="section-sm pb-0" data-aos="fade-up">
                  <form class="js-ajax-form">
                    <div class="form-group">
                      <input type="text" name="name" class="form-control" placeholder="Name">
                    </div>
                    <div class="form-group">
                      <input type="email" name="email"  class="form-control" required="" placeholder="Email *">
                    </div>
                    <div class="form-group">
                      <textarea rows="3" name="message"  class="form-control" placeholder="Message"></textarea>
                    </div>
                    <div class="message" id="success-message">Your message is successfully sent...</div>
                    <div class="message" id="error-message">Sorry something went wrong</div>
                    <div class="form-group mb-0">
                     <button type="submit" class="btn">Contact me</button>
                   </div>
                  </form>
                </section>
              </div>
            </div>
          </div>
        </section>
      </div>
    </div>

    <!-- Footer-->
    <footer class="section bg-gray">
      <div class="container">

        <!-- Lines -->
        <div class="lines">
          <div class="container">
            <div class="row">
              <div class="col-md-6 col-lg-4"></div>
              <div class="col-md-6 hidden-sm col-lg-4"></div>
              <div class="col-md-6 col-lg-4 hidden-md"></div>
            </div>
          </div>
        </div>

        <div class="row mx-0">
          <div class="col-md-6 col-lg-4  pl-0 pr-md-30px">
            <a class="brand" href="#">Ajay</a>
            <p class="size-sm">Personal</p>
            <p class="mt-4">
              <strong class="text-uppercase text-dark">Address:</strong><br>
              Vellore 2nd street 
            </p>
            <p class="mt-4">
              <strong class="text-uppercase text-dark">Email:</strong><br>
              suriyasajai16@gmail.com
            </p>
          </div>
          <div class="col-md-6 col-lg-4  order-md-3  order-lg-2 pl-0 pr-md-30px mt-5 mt-md-0">
            <strong class="text-uppercase text-dark">Menu:</strong><br>
            <ul class="navbar-nav mt-4 menu">
              <li><a class="nav-link" href="#home">Home</a></li>
              <li><a class="nav-link" href="#about">About</a></li>
              <li><a class="nav-link" href="#specialization">Specialization</a></li>
              <li><a class="nav-link" href="#works">Projects</a></li>
              <li><a class="nav-link" href="#experience">Experience</a></li>
              <li><a class="nav-link" href="#contact">Contact</a></li>
            </ul>
          </div>
          <div class="col-md-6 col-lg-4 order-md-2  order-lg-3  mt-5 mt-lg-0 px-0">
        <section class="section-sm pb-0">
          <div class="row mx-0">
            <div class="col-md-6 col-lg-4 pl-0 pr-md-30px">
              <p class="mb-0">© Ajay. 2024<br> All Rights Resevered</p>
            </div>
            <div class="col-md-6 col-lg-4 pl-0 pr-md-30px mt-5 mt-md-0">
                <!-- Social -->
                <ul class="social-icons d-none d-sm-block">
                  <li><a href="#"><ion-icon name="logo-facebook"></ion-icon></a></li>
                  <li><a href="#"><ion-icon name="logo-twitter"></ion-icon></a></li>
                  <li><a href="#"><ion-icon name="logo-linkedin"></ion-icon></a></li>
                </ul>
            </div>
            <div class="col-md-6 col-lg-4 pl-0 mt-5 mt-lg-0">  
              <!-- Language -->
              <ul class="language">
                 <li class="active"><a href="#">Eng</a></li>
                 <li><a href="#">Fra</a></li>
                 <li><a href="#">Ger</a></li>
              </ul>
            </div>
          </div>
        </section>
      </div>
    </footer>

    <!-- Optional JavaScript -->
    <script src="js/jquery-1.12.4.min.js"></script>
    <script src="js/popper.min.js" ></script>
    <script src="js/bootstrap.min.js"></script>
    <script src="js/jarallax.min.js"></script>
    <script src="js/jquery.validate.min.js"></script>
    <script src="../../../unpkg.com/ionicons%405.1.2/dist/ionicons.js"></script>
    <script src="js/jquery.ajaxchimp.min.js"></script>
    <script src="js/aos.js"></script>
    <script src="js/owl.carousel.min.js"></script>
    <script src="js/interface.js"></script>
  </body>

<!-- Mirrored from paul-themes.com/html/simone/home-personal.html?storefront=envato-elements by HTTrack Website Copier/3.x [XR&CO'2014], Sun, 24 Mar 2024 11:39:22 GMT -->
</html>

class SimpleHTTPRequestHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request recieved")
        self.send_response(200)
        self.send_header('Content-type', 'text/html')
        self.end_headers()
        self.wfile.write(b"Hello, world!")

def run(server_class=HTTPServer, handler_class=SimpleHTTPRequestHandler, port=8000):
    server_address = ('', 80000)
    httpd = server_class(server_address, handler_class)
    print(f"Server running on port...")
    httpd.serve_forever()


## OUTPUT:
![image](https://github.com/AjaysuryaS/simplewebserver/assets/114158396/00ac2283-6cec-414f-a0e2-b1dc733ed452)
![image](https://github.com/AjaysuryaS/simplewebserver/assets/114158396/45cec423-9378-481f-9ee1-7c123ac7dd15)
![image](https://github.com/AjaysuryaS/simplewebserver/assets/114158396/28abc04a-62fd-4516-a7dd-fe0dc31f854f)



## RESULT:
The program for implementing simple webserver is executed successfully.
