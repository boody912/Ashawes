<template>
    <head>


    </head>

    <body class="sub_page">

        <div class="hero_area">
            <div class="bg-box">
                <!-- <img src="images/hero-bg.jpg" alt=""> -->
                <img src="/src/assets/images/nav.jpg" alt="">
            </div>
            <!-- header section strats -->
            <header class="header_section">
                <div class="container">
                    <nav class="navbar navbar-expand-lg custom_nav-container ">

                        <a class="navbar-brand" href="/" target="_self" rel="noopener noreferrer">
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
                                <li class="nav-item">
                                    <a class="nav-link" href="/product">product</a>
                                </li>
                                <li class="nav-item ">
                                    <a class="nav-link" href="/about">About </a>
                                </li>

                            </ul>
                            <div class="user_option active">
                                <a class="cart_link" href="#">
                                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24"
                                        strokeWidth="1.5" stroke="currentColor" class="w-6 h-6">
                                        <path strokeLinecap="round" strokeLinejoin="round"
                                            d="M2.25 3h1.386c.51 0 .955.343 1.087.835l.383 1.437M7.5 14.25a3 3 0 00-3 3h15.75m-12.75-3h11.218c1.121-2.3 2.1-4.684 2.924-7.138a60.114 60.114 0 00-16.536-1.84M7.5 14.25L5.106 5.272M6 20.25a.75.75 0 11-1.5 0 .75.75 0 011.5 0zm12.75 0a.75.75 0 11-1.5 0 .75.75 0 011.5 0z" />
                                    </svg>
                                    <span class="sr-only">(current)</span>
                                </a>
                            </div>
                        </div>
                    </nav>

                </div>

            </header>
            <!-- end header section -->
        </div>

        <!-- cart section -->
        <section class="about_section layout_padding">
            <div class="container  ">
                <!-- <div class="cart">
                    <h3>Shopping Cart</h3>
                    <br>

                    <div v-for="(item, index) in cartItems" :key="index" class="cart-item">
                        <img src="/src/assets/images/try.jpg" class="product-image">
                        <div class="product-details">
                            <h3>{{ item.name }}</h3>
                            <br>
                            <p>Price:={{ item.price }} EGP</p>
                            <br>
                            <div class="quantity-input">
                                <label for="quantity">Quantity:</label>
                                <input style="color: black;" type="number" v-model="item.quantity" min="1" max="10">
                            </div>
                            <br>
                            <div class="size-input">
                                <label for="size">Size:</label>
                                <select style="color: black;" v-model="item.size">
                                    <option value="XS">XS</option>
                                    <option value="S">S</option>
                                    <option value="M">M</option>
                                    <option value="L">L</option>
                                </select>
                            </div>
                        </div>
                    </div>

                     <div class="subtotal">
                        <p>Subtotal: {{ calculateSubtotal }} EGP</p>
                    </div>
                    <br>
                    <div class="subtotal">
                        <p>Shipping: 50 EGP</p>
                    </div>
                    <br>
                    <div class="subtotal">
                        <p>Total: {{ calculatetotal }} EGP</p>
                    </div>

                     <div class="checkout-button">
                        <button @click="proceedToCheckout">Proceed to Checkout</button>
                    </div>
                </div> -->


                <div class="row">
                    <div class="col-75">
                        <div class="container">
                            <form action="https://usebasin.com/f/41aee71d13e2" method="POST">

                                <div class="row">
                                    <div class="col-75">
                                        <h3>Billing Address</h3>
                                        <br>
                                        <label for="fname"><i class="fa fa-user"></i> Full Name</label>
                                        <input type="text" id="fname" name="firstname" placeholder="John M. Doe" required>

                                        <label for="email"><i class="fa fa-envelope"></i> Email</label>
                                        <input type="text" id="email" name="email" placeholder="john@example.com" required>

                                        <label for="number"><i class="fa fa-phone"></i> Phone</label>
                                        <input type="text" id="phone" name="phone" placeholder="0123456789" required>

                                        <label for="adr"><i class="fa fa-address-card-o"></i> Address</label>
                                        <input type="text" id="adr" name="address" placeholder="542 W. 15th Street"
                                            required>

                                        <label for="city"><i class="fa fa-institution"></i> City</label>
                                        <input type="text" id="city" name="city" placeholder="Cairo" required>
                                    </div>

                                    <div class="col-25">
                                        <h3>Product Details</h3>
                                        <div v-for="(item, index) in cartItems" :key="index" class="cart-item">
                                            <!-- <img src="/src/assets/images/try.jpg" class="product-image"> -->
                                            <div class="slider">
                                                <div class="slider-container">
                                                    <img src="/src/assets/images/image1.jpeg" alt="Image 1">
                                                    <img src="/src/assets/images/image2.jpeg" alt="Image 2">
                                                    <img src="/src/assets/images/image3.jpeg" alt="Image 3">
                                                    <img src="/src/assets/images/image4.jpeg" alt="Image 4">
                                                    <img src="/src/assets/images/image5.jpeg" alt="Image 5">
                                                    <img src="/src/assets/images/image6.jpeg" alt="Image 6">
                                                    <img src="/src/assets/images/image7.jpeg" alt="Image 7">
                                                    <img src="/src/assets/images/image8.jpeg" alt="Image 8">
                                                    <img src="/src/assets/images/image9.jpeg" alt="Image 9">
                                                    <img src="/src/assets/images/image10.jpeg" alt="Image 10">
                                                    <img src="/src/assets/images/image11.jpeg" alt="Image 11">
                                                    <img src="/src/assets/images/image13.jpeg" alt="Image 12">
                                                    <!-- Add more images here -->
                                                </div>
                                                <button id="prevButton">Previous</button>
                                                &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                                                &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                                                &nbsp;&nbsp;&nbsp;&nbsp;
                                                <button id="nextButton">Next</button>
                                            </div>
                                            <br>
                                            <div class="product-details">
                                                <h3>{{ item.name }}</h3>
                                                <br>
                                                <p>
                                                <h6>Price: <span class="discounted-price">EGP 500</span> EGP 360 </h6>
                                                </p>
                                                <br>
                                                <div class="quantity-input">
                                                    <label for="quantity">Quantity:</label>
                                                    <input style="color: black;" type="number" id="quantity" name="quantity"
                                                        v-model="item.quantity" min="1" max="10" required>
                                                </div>
                                                <br>
                                                <div class="size-input">
                                                    <label for="size">Size:</label>
                                                    <select style="color: black;" id="size" name="size" v-model="item.size"
                                                        required>
                                                        <option value="XS">XS</option>
                                                        <option value="S">S</option>
                                                        <option value="M">M</option>
                                                        <option value="L">L</option>
                                                    </select>
                                                </div>
                                            </div>
                                        </div>
                                    </div>

                                </div>

                                <div class="container">
                                    <h4>Cart
                                        <span class="price" style="color:black">
                                            <i class="fa fa-shopping-cart"></i>
                                            <b>1</b>
                                        </span>
                                    </h4>
                                    <p><a href="#">T-shirt: &nbsp; </a> <span class="price">{{ calculateSubtotal }}
                                            EGP</span></p>

                                    <hr>

                                    <p><a href="#">Shipping: &nbsp; </a> <span class="price">50 EGP</span></p>
                                    <hr>

                                    <p>Total: &nbsp; <span class="price" style="color:black"><b>{{ calculatetotal }}
                                                EGP</b></span></p>
                                </div>

                                <input type="submit" value="Submit" class="btnn">
                            </form>

                        </div>
                    </div>

                    <!-- <div class="col-25">
                        <div class="container">
                            <h4>Cart
                                <span class="price" style="color:black">
                                    <i class="fa fa-shopping-cart"></i>
                                    <b>1</b>
                                </span>
                            </h4>
                            <p><a href="#">Subtotal: &nbsp; </a> <span class="price">{{ calculateSubtotal }} EGP</span></p>
                            <hr>
                            <p><a href="#">Shipping: &nbsp; </a> <span class="price">50 EGP</span></p>
                            <hr>

                            <p>Total: &nbsp; <span class="price" style="color:black"><b>{{ calculatetotal }} EGP</b></span>
                            </p>
                        </div>
                    </div> -->
                </div>


            </div>
        </section>
        <!-- cart end -->

        <!-- end cart section -->

        <!-- footer section -->
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
            cartItems: [
                {
                    name: 'Ashawes tshirt',
                    price: 360,
                    image: '/src/assets/images/pic.png',
                    quantity: 1,
                    size: 'XS'
                },
            ]
        };
    },
    computed: {
        calculateSubtotal() {
            return this.cartItems.reduce((total, item) => {
                return total + item.price * item.quantity;
            }, 0);
        },
        calculatetotal() {
            return this.cartItems.reduce((total, item) => {
                return total + item.price * item.quantity;
            }, 0) + 50;
        },
        /* initializeSlider() {
            // Get the slider container
            var sliderContainer = document.querySelector('.slider-container');

            // Set the initial position
            var position = 0;

            // Calculate the slide width based on the number of visible slides
            var slideWidth = sliderContainer.offsetWidth / 3; // Adjust the number according to the desired number of visible slides

            // Variables for tracking swipe gestures
            var touchStartX = 0;
            var touchEndX = 0;

            // Function to handle the slide movement
            function slide(direction) {
                // Calculate the new position based on the slide width and direction
                position += direction * slideWidth;

                // Apply the transform style to move the slider
                sliderContainer.style.transform = 'translateX(' + position + 'px)';
            }

            // Event listeners for previous and next buttons
            document.getElementById('prevButton').addEventListener('click', function () {
                slide(1); // Slide to the right
            });

            document.getElementById('nextButton').addEventListener('click', function () {
                slide(-1); // Slide to the left
            });

            // Touch event listeners for swipe
            sliderContainer.addEventListener('touchstart', function (event) {
                touchStartX = event.touches[0].clientX;
            });

            sliderContainer.addEventListener('touchmove', function (event) {
                touchEndX = event.touches[0].clientX;
            });

            sliderContainer.addEventListener('touchend', function () {
                var swipeThreshold = slideWidth / 3; // Adjust the threshold as needed

                if (touchStartX - touchEndX > swipeThreshold) {
                    slide(-1); // Slide to the left
                } else if (touchEndX - touchStartX > swipeThreshold) {
                    slide(1); // Slide to the right
                }
            });
        } */

    },
    methods: {
        toggleNavbar() {
            this.isCollapsed = !this.isCollapsed;
        },
        proceedToCheckout() {
            // Logic for proceeding to checkout
            console.log('Proceeding to checkout');
            window.location.href = '/check';
        },
        initializeSlider() {
            // Get the slider container
            var sliderContainer = document.querySelector('.slider-container');

            // Set the initial position
            var position = 0;

            // Calculate the slide width based on the number of visible slides
            var slideWidth = sliderContainer.offsetWidth / 3; // Adjust the number according to the desired number of visible slides

            // Variables for tracking swipe gestures
            var touchStartX = 0;
            var touchEndX = 0;

            // Function to handle the slide movement
            function slide(direction) {
                // Calculate the new position based on the slide width and direction
                position += direction * slideWidth;

                // Apply the transform style to move the slider
                sliderContainer.style.transform = 'translateX(' + position + 'px)';
            }

            // Event listeners for previous and next buttons
            document.getElementById('prevButton').addEventListener('click', function () {
                slide(1); // Slide to the right
            });

            document.getElementById('nextButton').addEventListener('click', function () {
                slide(-1); // Slide to the left
            });

            // Touch event listeners for swipe
            sliderContainer.addEventListener('touchstart', function (event) {
                touchStartX = event.touches[0].clientX;
            });

            sliderContainer.addEventListener('touchmove', function (event) {
                touchEndX = event.touches[0].clientX;
            });

            sliderContainer.addEventListener('touchend', function () {
                var swipeThreshold = slideWidth / 3; // Adjust the threshold as needed

                if (touchStartX - touchEndX > swipeThreshold) {
                    slide(-1); // Slide to the left
                } else if (touchEndX - touchStartX > swipeThreshold) {
                    slide(1); // Slide to the right
                }
            });
        }



    },

    mounted() {
        this.initializeSlider();
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

<style>
.row {
    display: -ms-flexbox;
    /* IE10 */
    display: flex;
    -ms-flex-wrap: wrap;
    /* IE10 */
    flex-wrap: wrap;
    margin: 0 -16px;
}

.col-25 {
    -ms-flex: 25%;
    /* IE10 */
    flex: 25%;
}

.col-50 {
    -ms-flex: 50%;
    /* IE10 */
    flex: 50%;
}

.col-75 {
    -ms-flex: 75%;
    /* IE10 */
    flex: 75%;
}

.col-25,
.col-50,
.col-75 {
    padding: 0 16px;
}



input[type=text] {
    width: 100%;
    color: black;
    margin-bottom: 20px;
    padding: 12px;
    border: 1px solid #ccc;
    border-radius: 3px;
}

label {
    margin-bottom: 10px;
    display: block;
}

.icon-container {
    margin-bottom: 20px;
    padding: 7px 0;
    font-size: 24px;
}

.btnn {
    background-color: #04AA6D;
    color: white;
    padding: 12px;
    margin: 10px 0;
    border: none;
    width: 100%;
    border-radius: 3px;
    cursor: pointer;
    font-size: 17px;
}

.btnn:hover {
    background-color: #45a049;
}

span.price {
    float: right;
    color: grey;
}

/* Responsive layout - when the screen is less than 800px wide, make the two columns stack on top of each other instead of next to each other (and change the direction - make the "cart" column go on top) */
@media (max-width: 800px) {
    .row {
        flex-direction: column-reverse;
    }

    .col-25 {
        margin-bottom: 20px;
    }
}

.slider {
    width: 100%;
    overflow: hidden;
}

.slider-container {
    display: flex;
    transition: transform 0.3s ease-in-out;
}

.slider-container img {
    width: 100%;
    height: auto;
}
</style>
  
  
  
  
  