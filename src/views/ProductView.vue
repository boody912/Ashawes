<template>
    <head>

        <!-- Basic -->
        <meta charset="utf-8" />
        <meta http-equiv="X-UA-Compatible" content="IE=edge" />
        <!-- Mobile Metas -->
        <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no" />
        <!-- Site Metas -->
        <meta name="keywords" content="" />
        <meta name="description" content="" />
        <meta name="author" content="" />
        <link rel="shortcut icon" href="images/favicon.png" type="">


        <!-- bootstrap core css -->
        <link rel="stylesheet" type="text/css" href="../assets/css/bootstrap.css" />

        <link href='https://unpkg.com/boxicons@2.1.4/css/boxicons.min.css' rel='stylesheet'>

        <!--owl slider stylesheet -->
        <link rel="stylesheet" type="text/css"
            href="https://cdnjs.cloudflare.com/ajax/libs/OwlCarousel2/2.3.4/assets/owl.carousel.min.css" />
        <!-- nice select  -->
        <link rel="stylesheet"
            href="https://cdnjs.cloudflare.com/ajax/libs/jquery-nice-select/1.1.0/css/nice-select.min.css"
            integrity="sha512-CruCP+TD3yXzlvvijET8wV5WxxEh5H8P4cmz0RFbKK6FlZ2sYl3AEsKlLPHbniXKSrDdFewhbmBK5skbdsASbQ=="
            crossorigin="anonymous" />
        <!-- font awesome style -->
        <link href="../assets/css/font-awesome.min.css" rel="stylesheet" />

        <!-- Custom styles for this template -->
        <link href="../assets/css/style.css" rel="stylesheet" />
        <!-- responsive style -->
        <link href="../assets/css/responsive.css" rel="stylesheet" />

    </head>

    <body class="sub_page">

        <div class="hero_area">
            <div class="bg-box">
                <img src="../assets/images/nav.jpg" alt="">
            </div>
            <!-- header section strats -->
            <header class="header_section">
                <div class="container">
                    <nav class="navbar navbar-expand-lg custom_nav-container ">

                        <a class="navbar-brand" href="/" target="_blank">
                            <img src="/src/assets/images/fav2.png" alt="Ashawes Logo">
                        </a>


                        <button class="navbar-toggler" v-on:click="toggleNavbar()" type="button" data-toggle="collapse"
                            data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false"
                            aria-label="Toggle navigation">
                            <span class="navbar-toggler-icon"></span>
                        </button>

                        <div class="navbar-collapse" v-if="!isCollapsed" id="navbarSupportedContent">
                            <ul class="navbar-nav  mx-auto ">
                                <i class='bx bx-menu' id="menu-icon"></i>

                                <li class="nav-item ">
                                    <a class="nav-link" href="/">Home </a>
                                </li>
                                <li class="nav-item active">
                                    <a class="nav-link" href="/product">product <span class="sr-only">(current)</span></a>
                                </li>
                                <li class="nav-item">
                                    <a class="nav-link" href="/about">About</a>
                                </li>

                            </ul>
                            <div class="user_option">
                                <!-- <a href="" class="user_link">
                  <i class="fa fa-user" aria-hidden="true"></i>
                </a> -->
                                <a class="cart_link" href="/cart">
                                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24"
                                        strokeWidth={1.5} stroke="currentColor" className="w-6 h-6">
                                        <path strokeLinecap="round" strokeLinejoin="round"
                                            d="M2.25 3h1.386c.51 0 .955.343 1.087.835l.383 1.437M7.5 14.25a3 3 0 00-3 3h15.75m-12.75-3h11.218c1.121-2.3 2.1-4.684 2.924-7.138a60.114 60.114 0 00-16.536-1.84M7.5 14.25L5.106 5.272M6 20.25a.75.75 0 11-1.5 0 .75.75 0 011.5 0zm12.75 0a.75.75 0 11-1.5 0 .75.75 0 011.5 0z" />
                                    </svg>
                                </a>

                            </div>
                        </div>
                    </nav>

                </div>

            </header>
            <!-- end header section -->
        </div>

        <!--  section -->
        <div class="hero_area_video">
            <div class="bg-box_video">
                <!-- <img src="images/hero-bg.jpg" alt=""> -->
                <video src="/src/assets/images/Pyr.mp4" autoplay loop></video>
            </div>
            <section class="food_section layout_padding-bottom">
                <div class="container">
                    <div class="heading_container heading_center">
                        <br><br>
                        <h2 style="color: #e69c00;">
                            Our Product
                        </h2>

                    </div>

                    <ul class="filters_menu">
                        <li class="active" data-filter="*" style="color: white;">All</li>
                        <li data-filter=".tshirts">tshirts</li>
                        <li data-filter=".short">shorts</li>
                    </ul>

                    <div class="filters-content">
                        <div class="row grid">
                            <div class="col-sm-12 offset-md-3 col-lg-6 all tshirts">
                                <div class="box">
                                    <div>
                                        <div class="img-box">
                                            <img src="/src/assets/images/try.jpg" alt="">
                                        </div>
                                        <div class="detail-box">
                                            <h5>tshirt</h5>
                                            <!-- <p>Veniam debitis quaerat officiis quasi cupiditate quo, quisquam velit, magnam
                                                voluptatem repellendus
                                                sed eaque</p> -->
                                            <div class="options">
                                                <!-- <h6>EGP 480</h6> -->
                                                <h6><span class="discounted-price">EGP 500</span> EGP 360 </h6>

                                                <a href="/cart">
                                                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24"
                                                        strokeWidth={1.5} stroke="currentColor" className="w-6 h-6">
                                                        <path strokeLinecap="round" strokeLinejoin="round"
                                                            d="M2.25 3h1.386c.51 0 .955.343 1.087.835l.383 1.437M7.5 14.25a3 3 0 00-3 3h15.75m-12.75-3h11.218c1.121-2.3 2.1-4.684 2.924-7.138a60.114 60.114 0 00-16.536-1.84M7.5 14.25L5.106 5.272M6 20.25a.75.75 0 11-1.5 0 .75.75 0 011.5 0zm12.75 0a.75.75 0 11-1.5 0 .75.75 0 011.5 0z" />
                                                    </svg>
                                                </a>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>

                        </div>
                    </div>


                </div>
            </section>
        </div>
        <!-- end food section -->

        <!-- footer section -->
        <br><br><br><br><br><br><br><br><br>
        <footer class="footer_section">
            <div class="container">
                <div class="row">
                    <div class="col-md-4 footer-col">
                        <!-- <div class="footer_contact">
                            <h4>
                                Contact Us
                            </h4>
                            <div class="contact_link_box">
                    
                                <a href="">
                                    <i class="fa fa-phone" aria-hidden="true"></i>
                                    <span>
                                        Call +01 1234567890
                                    </span>
                                </a>
                                <a href="">
                                    <i class="fa fa-envelope" aria-hidden="true"></i>
                                    <span>
                                        demo@gmail.com
                                    </span>
                                </a>
                            </div>
                        </div> -->
                    </div>
                    <div class="col-md-4 footer-col">
                        <div class="footer_detail">
                            <a href="" class="footer-logo">
                                Ashawes
                            </a>
                            <!--   <p>
                                Necessary, making this the first true generator on the Internet. It uses a dictionary of
                                over 200 Latin
                                words, combined with
                            </p> -->
                            <div class="footer_social">
                                <!-- <a href="">
                                    <i class="fa fa-facebook" aria-hidden="true"></i>
                                </a>
                                <a href="">
                                    <i class="fa fa-twitter" aria-hidden="true"></i>
                                </a>
                                <a href="">
                                    <i class="fa fa-linkedin" aria-hidden="true"></i>
                                </a> -->
                                <a href="https://www.instagram.com/ashaws.eg/">
                                    <i class="fa fa-instagram" aria-hidden="true"></i>
                                </a>

                            </div>
                        </div>
                    </div>
                    <!-- <div class="col-md-4 footer-col">
                        <h4>
                            Opening Hours
                        </h4>
                        <p>
                            Everyday
                        </p>
                        <p>
                            10.00 Am -10.00 Pm
                        </p>
                    </div> -->
                </div>
                <div class="footer-info">
                    <p>
                        &copy; <span id="displayYear"></span> All Rights Reserved 2023
                    </p>
                </div>
            </div>
        </footer>
        <!-- footer section -->



    </body>
</template>

<script>
import { onMounted } from 'vue'

export default {
    data() {
        return {
            isCollapsed: true,
            links: [
                { path: "/", label: "Home" },
                { path: "/menu", label: "Menu" },
                { path: "/about", label: "About" },
                { path: "/book", label: "Book Table" },
            ],
        };
    },
    methods: {
        toggleNavbar() {
            this.isCollapsed = !this.isCollapsed;
        },
    },

    mounted() {
        if (window.innerWidth >= 992) {
            this.isCollapsed = false;
        }
        // Add external scripts to the DOM
        const script1 = document.createElement('script')
        script1.src = '../assets/js/jquery-3.4.1.min'
        script1.src = '../assets/js/jquery-3.4.1.min.js'
        document.body.appendChild(script1)

        const script2 = document.createElement('script')
        script2.src = 'https://cdn.jsdelivr.net/npm/popper.js@1.16.0/dist/umd/popper.min.js'
        script2.integrity = 'sha384-Q6E9RHvbIyZFJoft+2mJbHaEWldlvI9IOYy5n3zV9zzTtmI3UksdQRVvoxMfooAo'
        script2.crossOrigin = 'anonymous'
        document.body.appendChild(script2)

        const script3 = document.createElement('script')
        script3.src = '../assets/js/bootstrap'
        document.body.appendChild(script3)

        const script4 = document.createElement('script')
        script4.src = 'https://cdnjs.cloudflare.com/ajax/libs/OwlCarousel2/2.3.4/owl.carousel.min.js'
        document.body.appendChild(script4)

        const script5 = document.createElement('script')
        script5.src = 'https://unpkg.com/isotope-layout@3.0.4/dist/isotope.pkgd.min.js'
        document.body.appendChild(script5)

        const script6 = document.createElement('script')
        script6.src = 'https://cdnjs.cloudflare.com/ajax/libs/jquery-nice-select/1.1.0/js/jquery.nice-select.min.js'
        document.body.appendChild(script6)

        const script7 = document.createElement('script')
        script7.src = '../assets/js/custom'
        document.body.appendChild(script7)

        const script8 = document.createElement('script')
        script8.src = 'https://maps.googleapis.com/maps/api/js?key=AIzaSyCh39n5U-4IoWpsVGUHWdqB6puEkhRLdmI&callback=myMap'
        document.body.appendChild(script8)

        document.addEventListener("click", (event) => {
            if (this.navOpen && !event.target.closest(".navbar")) {
                this.hideNav();
            }
        });
    },
    setup() {
        // Alternatively, you can import scripts using onMounted
        onMounted(() => {
            import('../assets/js/jquery-3.4.1.min')
            import('https://cdn.jsdelivr.net/npm/popper.js@1.16.0/dist/umd/popper.min.js')
            import('../assets/js/bootstrap')
            import('https://cdnjs.cloudflare.com/ajax/libs/OwlCarousel2/2.3.4/owl.carousel.min.js')
            import('https://unpkg.com/isotope-layout@3.0.4/dist/isotope.pkgd.min.js')
            import('https://cdnjs.cloudflare.com/ajax/libs/jquery-nice-select/1.1.0/js/jquery.nice-select.min.js')
            import('../assets/js/custom')
            import('https://maps.googleapis.com/maps/api/js?key=AIzaSyCh39n5U-4IoWpsVGUHWdqB6puEkhRLdmI&callback=myMap')
        })
    },

}

</script>