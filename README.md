<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hospital</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-rbsA2VBKQhggwzxH7pPCaAqO46MgnOM80zW1RWuH61DGLwZJEdK2Kadq2F9CUG65" crossorigin="anonymous">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-kenU1KFdBIe4zVF0s0G1M5b4hcpxyD9F7jL+jjXkk+Q2h455rYXK/7HAuoJl+0I4" crossorigin="anonymous"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins&display=swap" rel="stylesheet">
    <script src="https://kit.fontawesome.com/c5637dc904.js" crossorigin="anonymous"></script>
    <style>
        .navbar
        {
            padding: 25px;
            margin: 25px;
            color:black;
            background-color: rgb(240, 255, 247);
        }
        #navbar,head{
            position:sticky;
            top: 0;
            left: 0;
            z-index: 100;
            box-shadow: 5px 5px 20px black rgba(0,0,0,.5);
        }
        li{
            display: inline;
        }
        a{
            color: rgb(110, 101, 101);
            font: 1em sans-serif;
            font-size: 20px;
            padding:30px;
            margin:30px;
            text-align: center;
            text-decoration: none;
            justify-content: center;

        }
        a:hover{
            color:rgb(219, 48, 105);
        }
        .iconnavbar{
            padding: 15px;
            margin: 0px;
            font-size: 0px;
            border-radius:0px solid;
        }
        .iconnavbar a{
            padding:0px;
            font-size: 25px;
            color:white
        }
        .iconnavbar a:hover{
            color: #29f700;
        }
        .service-item {
        height: 320px;
        padding: 30px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        text-align: center;
        background: #ffffff;
        box-shadow: 10 0 45px rgba(243, 237, 237, 0.08);
        transition: .5s;
        }

        .service-item:hover {
            background: var(--primary);
        }

        .service-item .service-icon {
            margin: 0 auto 30px auto;
            width: 65px;
            height: 65px;
            transition: .5s;
        }

        .service-item i,
        .service-item h5,
        .service-item p {
            transition: .5s;
        }

        .service-item:hover i,
        .service-item:hover h5,
        .service-item:hover p {
            color: #ffffff !important;
        }
        #box:hover{
            background-color: orange;
        }
        .section-title {
            position: relative;
            display: inline-block;
        }
        .section-title::before {
            position: absolute;
            content: "";
            width: 45px;
            height: 2px;
            top: 50%;
            left: -55px;
            margin-top: -1px;
            background: var(--primary);
        }
        .section-title::after {
            position: absolute;
            content: "";
            width: 45px;
            height: 2px;
            top: 50%;
            right: -55px;
            margin-top: -1px;
            background: var(--primary);
        }

        .section-title.text-start::before,
        .section-title.text-end::after {
            display: none;
        }

        .bgimg-1, .bgimg-2, .bgimg-3, .bgimg-4 {
            position: relative;
            opacity: 0.65;
            background-attachment: fixed;
            background-position: center;
            background-repeat: no-repeat;
            background-size: cover;

        }

        .bgimg-1 {
            background-image: url("hov1.jpg");
            min-height: 500px;
        }

        .bgimg-2 {
            background-image: url("hov4.jpg");
            min-height: 500px;
        }

        .bgimg-3 {
            background-image: url("hov5.png");
            min-height: 500px;
        }

        .bgimg-4 {
            background-image: url("hov6.png");
            min-height: 500px;
        }

        .caption {
            position: absolute;
            left: 0;
            top: 45%;
            width: 100%;
            text-align: center;
            color: #000;
        }

        .caption span.border {
            background-color: #111;
            color: #fff;
            padding: 18px;
            font-size: 25px;
            letter-spacing: 10px;
        }
        @media only screen and (max-device-width: 1024px) {
            .bgimg-1, .bgimg-2, .bgimg-3, .bgimg-4 {
                background-attachment: scroll;
            }
        }
        .flip-card {
            background-color: transparent;
            width: 300px;
            height: 400px;
            border: 1px solid #f1f1f1;
            perspective: 1000px; 
        }
        .flip-card-inner {
            position: relative;
            width: 100%;
            height: 100%;
            text-align: center;
            transition: transform 0.8s;
            transform-style: preserve-3d;
        }
        .flip-card:hover .flip-card-inner {
            transform: rotateY(180deg);
        }
        .flip-card-front, .flip-card-back {
            position: absolute;
            width: 100%;
            height: 100%;
            -webkit-backface-visibility: hidden; 
            backface-visibility: hidden;
        }
        .flip-card-front {
            background-color: #bbb;
            color: black;
        }
        .flip-card-back {
            background-color:#FFC4C4;
            color: black;
            transform: rotateY(180deg);
            font-family: sans-serif;
            letter-spacing: 3px;
        }
        .flip-card-back h1{
            color:#D61355;
            font-size: 30px;
            font-weight: 59px;
        }
        .iconr{
            background-color: black;
            font-size:50px;
            font-weight:70px;
            color: white;
            margin-top: 8px;
        }
        .iconr1{
            background-color: black;
            font-size:50px;
            font-weight:70px;
            color: white;
        }
        .servicesText.card {
            height: 480px;
            cursor: pointer;
        }
        .servicesIcon {
            font-size: 36px;
            text-align: center;
            width: 100%;
        }
        .card-title {
            text-align: center;
        }
        .card:hover .servicesIcon {
            color: #9ae950;
        }
        .card-title:hover{
            color:  #9ae950;
        }
        .servicesText:hover {
            border: 1px solid #9ae950;
        }
        .card{
            height: 700px;
        }
        .btn.btn-social {
            margin-right: 5px;
            width: 35px;
            height: 35px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--light);
            border: 1px solid #FFFFFF;
            border-radius: 35px;
            transition: .3s;
            text-decoration: none;
        }
        .btn.btn-social:hover {
            color: var(--primary);
        }
        .btn.btn-link {
            display: block;
            margin-bottom: 5px;
            padding: 0;
            text-align: left;
            color: #FFFFFF;
            font-size: 15px;
            font-weight: normal;
            text-transform: capitalize;
            transition: .3s;
            text-decoration: none;
        }
        .btn.btn-link::before {
            position: relative;
            content: "\f105";
            font-family: "Font Awesome 5 Free";
            font-weight: 900;
            margin-right: 10px;
        }
        .btn.btn-link:hover {
            letter-spacing: 1px;
            box-shadow: none;
        }
    </style>
</head>
<body>
    <div class="container-fluid " id="home">
        <div class="row">
            <div class="iconnavbar col-4 p-3 text-white bg-dark " >
                <a href="#"><i class="fa-brands fa-square-facebook"></i></a>
                <a href="#"><i class="fa-brands fa-instagram"> </i></a>
                <a href="#"><i class="fa-brands fa-twitter"></i></a>
                <a href="#"><i class="fa-brands fa-whatsapp"></i></a>
            </div>
            <div class=" col-4 p-4 text-white bg-dark">
                <p>Call Now : 0413-2200017 -18 / 4210018 / 080565 55330</p>
            </div>
            <div class="iconnavbar col-4 pe-5 text-end bg-dark">
                <a href="#"><i class="fas fa-ambulance fa-2x"></i> 24/7 </a>
            </div>
        </div>
    </div>
    <nav class=" navbar-expand-sm container-fluid bg-light" id="head">
        <div class="container-fluid row" style=" text-align: center;">
            <img src="orthos.jpg" alt="logo" style="width: 150px; margin-left: 115px; margin-top: 12px; margin-bottom: 12px;" class="rounded-pill ">
            <h1 class="col p-6" style=" margin-top: 45px; text-align: left;">THE POSH-PONDY ORTHO SPECIALITY HOSPITAL</h1>
        </div>
    </nav>
    <div id="navbar" class="container-fluid navbar-expand-sm mb-2 row p-2 mx-0 align-middle" style="text-align: center; background-color: rgb(230, 228, 228)" >
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <ul>
            <li class="nav-item"><a href="#home" class="col p-2">HOME</a></li>
            <li class="nav-item"><a href="#service" class="col p-2">SERVICES</a></li>
            <li class="nav-item"><a href="#About" class="col p-2">ABOUT</a></li>
            <li class="nav-item"><a href="#dept" class="col p-2">DEPARTMENT</a></li>
            <li class="nav-item"><a href="#htips" class="col p-2">HEALTH TIPS</a></li>
            <li class="nav-item"><a href="#test" class="col p-2">TESTIMONIALS</a></li>
            <li class="nav-item"><a href="#footer" class="col p-2">CONTACT</a></li>
        </ul> 
    </div>

    <div id="demo" class="carousel slide" data-bs-ride="carousel">
        <!-- Indicators/dots -->
        <div class="carousel-indicators">
          <button type="button" data-bs-target="#demo" data-bs-slide-to="0" class="active"></button>
          <button type="button" data-bs-target="#demo" data-bs-slide-to="1"></button>
          <button type="button" data-bs-target="#demo" data-bs-slide-to="2"></button>
        </div>
        
        <!-- The slideshow/carousel -->
        <div class="carousel-inner">
          <div class="carousel-item active">
            <img src="sl2.png" class="d-block" style="width:100%">
          </div>
          <div class="carousel-item">
            <img src="sl1.png" class="d-block" style="width:100%">
          </div>
          <div class="carousel-item">
            <img src="sl3.jpg" class="d-block" style="width:100%">
          </div>
        </div>
        
        <!-- Left and right controls/icons -->
        <button class="carousel-control-prev" type="button" data-bs-target="#demo" data-bs-slide="prev">
          <span class="carousel-control-prev-icon"></span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#demo" data-bs-slide="next">
          <span class="carousel-control-next-icon"></span>
        </button>
        
      <div style="background-color: black;" class="mt-3"></div>
    </div>


    <div class="bgimg-1" id="service">
        <div class="caption">
            <span class="border" style="background-color:transparent; font-size:45px; font-weight: bold; color: black;">SERVICES</span>
        </div>
    </div>
      
      
    <div class="container-xxl py-5"  style="background-color: rgb(94, 86, 86); color: aliceblue;">
        <div class="container" id="service">
            <div class="row g-4">
                <div class="col-lg-4 col-md-6 ">
                    <a class="service-item rounded"  id="box" href="#">
                        <div class="service-icon bg-transparent border rounded p-1">
                            <div class="w-100 h-100 border rounded d-flex align-items-center justify-content-center">
                                <i class="fa fa-hospital-alt fa-2x" style="color: #ec09a4;"></i>
                            </div>
                        </div>
                        <h5 style="color: blue;">DEPARTMENTS</h5>
                        <p class="text-body mb-0">The Posh Hospital is a multispeciality hospital that has 14 departments that are fully-functional, ably-staffed and well-equipped.</p>
                    </a>
                </div>
                <div class="col-lg-4 col-md-6 ">
                    <a class="service-item rounded"  id="box" href="#">
                        <div class="service-icon bg-transparent border rounded p-1">
                            <div class="w-100 h-100 border rounded d-flex align-items-center justify-content-center">
                                <i class="fa fa-heartbeat fa-2x" style="color: #ec09a4;"></i>
                            </div>
                        </div>
                        <h5 class="mb-3" style="color: blue;">HEALTH TIPS</h5>
                        <p class="text-body mb-0">Making suitable lifestyle choices may also help men and women prevent some health problems.</p>
                    </a>
                </div>
                <div class="col-lg-4 col-md-6">
                    <a class="service-item rounded"  id="box" href="#">
                        <div class="service-icon bg-transparent border rounded p-1">
                            <div class="w-100 h-100 border rounded d-flex align-items-center justify-content-center">
                                <i class="fa fa-stethoscope fa-2x" style="color: #ec09a4;"></i>
                            </div>
                        </div>
                        <h5 class="mb-3" style="color: blue;">FIND A DOCTOR</h5>
                        <p class="text-body mb-0">Well trained and experienced senior physicians work as a single team in tackling severe cases and critically ill patients.</p>
                    </a>
                </div>
                <div class="col-lg-4 col-md-6 ">
                    <a class="service-item rounded"  id="box" href="#">
                        <div class="service-icon bg-transparent border rounded p-1">
                            <div class="w-100 h-100 border rounded d-flex align-items-center justify-content-center">
                                <i class="fa fa-user-md fa-2x" style="color: #ec09a4;"></i>
                            </div>
                        </div>
                        <h5 class="mb-3" style="color: blue;">TESTIMONIALS</h5>
                        <p class="text-body mb-0">We love that our patients feel inspired to write about the care they received here at new medical centre.</p>
                    </a>
                </div>
                <div class="col-lg-4 col-md-6 ">
                    <a class="service-item rounded"  id="box" href="#">
                        <div class="service-icon bg-transparent border rounded p-1">
                            <div class="w-100 h-100 border rounded d-flex align-items-center justify-content-center">
                                <i class="fa fa-heart-o fa-2x" style="color: #ec09a4;"></i>
                            </div>
                        </div>
                        <h5 class="mb-3" style="color: blue;">HAPPY CLIENTS</h5>
                        <p class="text-body mb-0">Our success is measured by results, the most important being how our clients feel about their experience with us.</p>
                    </a>
                </div>
                <div class="col-lg-4 col-md-6 ">
                    <a class="service-item rounded"  id="box" href="#">
                        <div class="service-icon bg-transparent border rounded p-1">
                            <div class="w-100 h-100 border rounded d-flex align-items-center justify-content-center">
                                <i class="fa fa-wheelchair fa-2x" style="color: #ec09a4;"></i>
                            </div>
                        </div>
                        <h5 class="mb-3" style="color: blue;">FACILITIES</h5>
                        <p class="text-body mb-0">Sometimes, the best thing we can do for our patients is to tell them what the best behavior is and then negotiate something they can live with.</p>
                    </a>
                </div>
            </div>
        </div>
    </div>
      
      <div class="bgimg-2" id="About">
        <div class="caption">
        <span class="border" style="background-color:transparent; font-size:45px; font-weight: bold; color: black;">ABOUT US</span>
        </div>
      </div>
      
      <section style="background-color: black;">
        <div class="container-fluid">
            <div class="row">
                <div class="col-lg-6 col-md-6 col-12 p-lg-25 p-md-4 p-2 my-5 img-container drop-shadow" >
                    <img src="md.png" class="img-thumbnail mx-auto d-block " alt="Cinque Terre" width="350px" height="350px">
                </div>
                <div class="col-lg-6 col-md-6 col-12 p-lg-25 p-md-4 p-2 my-5 " style=" color: #ffffff;">
                    <P style="font-size: large;">“Welcome to THE POSH . We operate at PONDICHERRY as a private surgical hospital, and our focus is on delivering quality care and value for money. We play a key role in improving the health of PONDICHERRY , by providing access to quality elective surgical services round the year.​​</p>
                    <p style="font-size: large;">​The POSH represents about the private ORTHO surgery market in the town and, across a wide range of medical specialties.. Although we operate independently, with a separate Board of Directors, we make up part of businesses that include Health Insurance, Primary Care. The Posh reaches all the people in and around the territory, making it one of the most well known and trusted healthcare hospitals.</P>
                    <p style="font-size: large;">​Its range of health care and services, combined with a not-for-profit focus and significant size and experience, gives The Posh an important role in the Pondicherry health sector. Since we were established in 2005 as Pondy Ortho Clinic . We have grown in both size and scope of services offered as The POSH in 2017 . We’re passionate about achieving our vision.</p>
                    </div>
            </div>
        </div>
    </section>
      
      <div class="bgimg-3" id="dept">
        <div class="caption">
        <span class="border" style="background-color:transparent; font-size:45px; font-weight: bold; color: black;">DEPARTMENT</span>
        </div>
      </div>
      <div style="background-color: black;" class="mt-3"></div>
      <div id="demo" class="carousel slide" data-bs-ride="carousel">
        <!-- Indicators/dots -->
        <div class="carousel-indicators">
          <button type="button" data-bs-target="#demo" data-bs-slide-to="0" class="active"></button>
          <button type="button" data-bs-target="#demo" data-bs-slide-to="1"></button>
          <button type="button" data-bs-target="#demo" data-bs-slide-to="2"></button>
        </div>
        
        <!-- The slideshow/carousel -->
        <div class="carousel-inner">
          <div class="carousel-item active">
            <img src="dep1.png" class="d-block" style="width:100%">
          </div>
          <div class="carousel-item">
            <img src="dep2.png" class="d-block" style="width:100%">
          </div>
        
        <!-- Left and right controls/icons -->
        <button class="carousel-control-prev" type="button" data-bs-target="#demo" data-bs-slide="prev">
          <span class="carousel-control-prev-icon"></span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#demo" data-bs-slide="next">
          <span class="carousel-control-next-icon"></span>
        </button>
    </div>

    <section id="Portfolio" class="p-5" style="background-color: black;">
        <div class="container">
            <div class="row">
                <div class="col-lg-4 mt-4">
                    <div class="card servicesText">
                        <div class="card-body" style="background-color: black; color: white;">
                            <i class="servicesIcon fas fa-user-md fa-2x"></i>
                            <h4 class="card-title mt-3">WELL TRAINED STAFFS ENGAGING IN PERSONALISED CARE!</h4>
                            <p class="card-text mt-3">One of the biggest advantages of OUR POSH is the holistic treatment we can offer you. We have a family of well trained experienced staffs who gives you constant care and we are conducting them regular seminars and symposiums regarding recent medical updates.We will give you consistent care from diagnosis through to recovery and after-care. We concentrate more on the patients rather than the diseases which helps in achieving remendous health care to the patients.</p>
                        </div>
                    </div>  
                </div>
                <div class="col-lg-4 mt-4">
                    <div class="card servicesText">
                        <div class="card-body" style="background-color: black; color: white;">
                            <i class='servicesIcon fas fa-clinic-medical fa-2x'></i>
                            <h4 class="card-title mt-3">BEST HYGIENIC HOSPITAL IN PUDUCHERRY!</h4>
                            <p class="card-text mt-3">OUR POSH was awarded first rank in the level of sanitation and cleanliness services and awarded SWACHH BHARAT MISSION SWACHH RANKING CERTIFICATE by government of puducherry in the year 2019. We also have zero infection rate in operation theatres for the past 5 years and we try to achieve it in the future.                            </p>
                        </div>
                    </div>  
                </div>

                <div class="col-lg-4 mt-4">
                    <div class="card servicesText">
                        <div class="card-body" style="background-color: black; color: white;">
                            <i class="servicesIcon fas fa-diagnoses fa-2x"></i>
                            <h4 class="card-title mt-3">SURGERY WITHIN 24 HOURS OF ADMISSION!</h4>
                            <p class="card-text mt-3">One of our biggest flex we tend to operate the patient within 24 hours of admission which is considered as a GOLDEN PERIOD in our field. We have a set of operating teams consisting surgeons of various departments(refer our doctors to know more) who works round the clock to make it possible.</p>
                        </div>
                    </div>  
                </div>
            </div>
        </div>
    </section>


      
      <div class="bgimg-4" id="htips">
        <div class="caption">
        <span class="border" style="background-color:transparent; font-size:45px; font-weight: bold; color: black;">HEALTH TIPS</span>
        </div>
      </div>
    
    <section class=" row" id="RRR" style="background-color: black;">
    <div class="flip-card  col-4 my-5" style="margin-left: 17%;">
      <div class="flip-card-inner">
        <div class="flip-card-front">
            <h1>Consume less salt and sugar </h1>
            <p>Filipinos consume twice the recommended amount of sodium, putting them at risk of high blood pressure, which in turn increases the risk of heart disease and stroke. Most people get their sodium through salt.</p>
            <div class="iconr">
                <i class="fa fa-heartbeat fa-2x"></i>
            </div>
        </div>
        <div class="flip-card-back ">
            <h1>Eat a healthy diet</h1>
            <p>Eat a combination of different foods, including fruit, vegetables, nuts and whole grains. Adults should eat at least five portions of fruit and vegetables per day.Eating fresh fruit and vegetables as snacks;</p>
            <div class="iconr1">
             <i class="fa fa-heart-o fa-2x"></i>
            </div>
        </div>
      </div>
    </div>
    
    
    <div class="flip-card  col-4 my-5">
      <div class="flip-card-inner">
        <div class="flip-card-front">
            <h1>Avoid harmful use of alcohol </h1>
            <p>Consuming alcohol can lead to health problems such as mental and behavioural disorders, liver cirrhosis, cancers and heart diseases, as well as injuries resulting from violence and road clashes and collisions.</p>
            <div class="iconr">
                <i class="fa fa-heartbeat fa-2x"></i>
            </div>
        </div>
        <div class="flip-card-back">
          <h1>Don’t smoke</h1>
          <p>Tobacco kills not only the direct smokers but even non-smokers through second-hand exposure.  Currently, there are around 15.9 million Filipino adults who smoke tobacco but 7 in 10 smokers are interested or plan to quit. </p>
          <div class="iconr1">
          <i class="fa fa-heart-o fa-2x"></i>
          </div>
        </div>
      </div>
    </div>
    
    <div class="flip-card col-4 my-5">
      <div class="flip-card-inner">
        <div class="flip-card-front">
            <h1>Clean your hands properly</h1>
            <p>Clean hands can prevent the spread of infectious illnesses. You should handwash using soap and water when your hands are visibly soiled or handrub using an alcohol-based product.</p>
            <div class="iconr">
                <i class="fa fa-heartbeat fa-2x"></i>
            </div>
        </div>
        <div class="flip-card-back">
            <h1> Be active</h1>
            <p>This includes exercise and activities undertaken while working, playing, travelling, and engaging in recreational pursuits. You need depends on your age group  should do moderate-intensity throughout the week.</p>
             <div class="iconr1">
            <i class="fa fa-heart-o fa-2x"></i>
           </div>
        </div>
      </div>
    </div>
    </section>
    <div id="demo" class="carousel slide" data-bs-ride="carousel">
        <!-- Indicators/dots -->
        <div class="carousel-indicators">
          <button type="button" data-bs-target="#demo" data-bs-slide-to="0" class="active"></button>
          <button type="button" data-bs-target="#demo" data-bs-slide-to="1"></button>
          <button type="button" data-bs-target="#demo" data-bs-slide-to="2"></button>
        </div>
        
        <!-- The slideshow/carousel -->
        <div class="carousel-inner" id="test">
            <div class="carousel-item active">
              <img src="tst1.png" class="d-block" style="width:100%">
            </div>
            <div class="carousel-item">
              <img src="tst2.png" class="d-block" style="width:100%">
            </div>
            <div class="carousel-item">
              <img src="tst3.png" class="d-block" style="width:100%">
            </div>
          </div>
        <!-- Left and right controls/icons -->
        <button class="carousel-control-prev" type="button" data-bs-target="#demo" data-bs-slide="prev">
          <span class="carousel-control-prev-icon"></span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#demo" data-bs-slide="next">
          <span class="carousel-control-next-icon"></span>
        </button>
    </div>

    <section id="footer">
        <div class="container-fluid bg-dark text-light footer ">
            <div class="container pb-5">
                <div class="row g-5">
                    <div class="col-md-6 ">
                            <a href="#"><h1 class="text-white text-uppercase mb-3">THE POSH HOSPITAL</h1></a>
                            <p class="text-white mb-0">
                                “Welcome to THE POSH .
                                We operate at PONDICHERRY as a
                                private surgical hospital, and
                                our focus is on delivering quality
                                care and value for money.
                                We play a key role in improving
                                the health of PONDICHERRY...
                                
							</p>
                    </div>
                    <div class="col-md-6 ">
                        <h6 class="section-title text-start text-primary text-uppercase mb-4 p-3">Contact</h6>
                        <p class="mb-2"><i class="fa fa-map-marker-alt me-3"></i>

                            CONTACT US
                            R.S. NO.30/11,AMBAI NGAR MAIN ROAD,
                            SARATHAMBAL NAGAR, NEAR PATRICK SCHOOL,
                            PUDUCHERRY - 605 009</p>
                        <p class="mb-2"><i class="fa fa-phone-alt me-3"></i>80565 55330</p>
                        <p class="mb-2"><i class="fa fa-envelope me-3"></i>theposhhospital@gmail.com</p>
                        <div class="d-flex pt-2">
                            <a class="btn btn-outline-light btn-social" href=""><i class="fab fa-twitter"></i></a>
                            <a class="btn btn-outline-light btn-social" href=""><i class="fab fa-facebook-f"></i></a>
                            <a class="btn btn-outline-light btn-social" href=""><i class="fab fa-youtube"></i></a>
                            <a class="btn btn-outline-light btn-social" href=""><i class="fab fa-linkedin-in"></i></a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</body>
</html>
