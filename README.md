<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>THE FASHION STORE - Trendy & Elegant Fashion</title>
    <style>
        :root {
    --primary-color: #2c3e50;
    --secondary-color: #e74c3c;
    --accent-color: #3498db;
    --text-color: #333;
    --light-gray: #f4f4f4;
    --white: #ffffff;
    --max-width: 1200px;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Arial', sans-serif;
    line-height: 1.6;
    color: var(--text-color);
}

.container {
    max-width: var(--max-width);
    margin: 0 auto;
    padding: 0 2rem;
}

/* Navbar */
#navbar {
    position: fixed;
    top: 0;
    width: 100%;
    background: var(--white);
    padding: 1rem 2rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    z-index: 1000;
}

.nav-brand {
    font-size: 1.5rem;
    font-weight: bold;
    color: var(--primary-color);
}

.nav-items {
    display: flex;
    gap: 2rem;
}

.nav-items a {
    text-decoration: none;
    color: var(--text-color);
    font-weight: 500;
    transition: color 0.3s;
}

.nav-items a:hover,
.nav-items a.active {
    color: var(--accent-color);
}

.nav-actions {
    display: flex;
    align-items: center;
    gap: 1.5rem;
}

.search-bar {
    position: relative;
}

.search-bar input {
    padding: 0.5rem 2rem 0.5rem 1rem;
    border: 1px solid #ddd;
    border-radius: 20px;
    width: 200px;
}

.search-bar i {
    position: absolute;
    right: 0.75rem;
    top: 50%;
    transform: translateY(-50%);
    color: #666;
}

.cart-icon {
    position: relative;
    cursor: pointer;
}

#cart-count {
    position: absolute;
    top: -8px;
    right: -8px;
    background: var(--secondary-color);
    color: var(--white);
    border-radius: 50%;
    padding: 0.2rem 0.5rem;
    font-size: 0.8rem;
}

/* Hero Section */
.hero {
    height: 80vh;
    background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), 
                url('https://images.unsplash.com/photo-1441984904996-e0b6ba687e04');
    background-size: cover;
    background-position: center;
    display: flex;
    align-items: center;
    color: var(--white);
    padding: 0 2rem;
    margin-top: 4rem;
}

.hero-content {
    max-width: var(--max-width);
    margin: 0 auto;
}

.hero h1 {
    font-size: 3.5rem;
    margin-bottom: 1rem;
}

.hero p {
    font-size: 1.2rem;
    margin-bottom: 2rem;
}

.hero-buttons {
    display: flex;
    gap: 1rem;
}

/* Buttons */
.btn {
    display: inline-block;
    padding: 1rem 2rem;
    border-radius: 5px;
    text-decoration: none;
    transition: all 0.3s;
    font-weight: 500;
}

.btn.primary {
    background: var(--accent-color);
    color: var(--white);
}

.btn.primary:hover {
    background: #2980b9;
}

.btn.secondary {
    background: transparent;
    color: var(--white);
    border: 2px solid var(--white);
}

.btn.secondary:hover {
    background: var(--white);
    color: var(--primary-color);
}

/* Features Section */
#features {
    padding: 4rem 0;
    background: var(--light-gray);
}

.feature-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 2rem;
}

.feature-card {
    text-align: center;
    padding: 2rem;
    background: var(--white);
    border-radius: 8px;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
}

.feature-card i {
    font-size: 2rem;
    color: var(--accent-color);
    margin-bottom: 1rem;
}

/* Products Grid */
.products-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
    gap: 2rem;
    margin-top: 2rem;
}

.product-card {
    background: var(--white);
    border-radius: 8px;
    overflow: hidden;
    transition: transform 0.3s;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
}

.product-card:hover {
    transform: translateY(-5px);
}

.product-image {
    width: 100%;
    height: 300px;
    object-fit: cover;
}

.product-info {
    padding: 1.5rem;
}

.product-title {
    font-size: 1.2rem;
    margin-bottom: 0.5rem;
}

.product-price {
    color: var(--accent-color);
    font-weight: bold;
    font-size: 1.1rem;
    margin-bottom: 1rem;
}

/* Categories Section */
.category-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 2rem;
    margin-top: 2rem;
}

.category-card {
    height: 300px;
    position: relative;
    border-radius: 8px;
    overflow: hidden;
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--white);
    text-align: center;
    background-size: cover;
    background-position: center;
}

.category-card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: rgba(0,0,0,0.4);
}

.category-card h3 {
    font-size: 2rem;
    margin-bottom: 1rem;
    position: relative;
    z-index: 1;
}

.category-card .btn {
    position: relative;
    z-index: 1;
}

.women {
    background-image: url('https://images.unsplash.com/photo-1483985988355-763728e1935b');
}

.men {
    background-image: url('https://images.unsplash.com/photo-1490578474895-699cd4e2cf59');
}

.accessories {
    background-image: url('https://images.unsplash.com/photo-1492707892479-7bc8d5a4ee93');
}

/* Newsletter Section */
#newsletter {
    background: var(--primary-color);
    color: var(--white);
    padding: 4rem 0;
}

.newsletter-content {
    text-align: center;
    max-width: 600px;
    margin: 0 auto;
}

.newsletter-form {
    display: flex;
    gap: 1rem;
    margin-top: 2rem;
}

.newsletter-form input {
    flex: 1;
    padding: 1rem;
    border: none;
    border-radius: 5px;
}

/* Footer */
footer {
    background: var(--primary-color);
    color: var(--white);
    padding-top: 4rem;
}

.footer-content {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 2rem;
    padding-bottom: 3rem;
}

.footer-section h3 {
    margin-bottom: 1.5rem;
}

.footer-section ul {
    list-style: none;
}

.footer-section ul li {
    margin-bottom: 0.5rem;
}

.footer-section a {
    color: var(--white);
    text-decoration: none;
    opacity: 0.8;
    transition: opacity 0.3s;
}

.footer-section a:hover {
    opacity: 1;
}

.social-links {
    display: flex;
    gap: 1rem;
    margin-top: 1rem;
}

.social-links a {
    font-size: 1.5rem;
}

.contact-info li {
    display: flex;
    align-items: center;
    gap: 0.5rem;
}

.footer-bottom {
    border-top: 1px solid rgba(255,255,255,0.1);
    padding: 1.5rem 0;
}

.footer-bottom .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.payment-methods {
    display: flex;
    gap: 1rem;
    font-size: 1.5rem;
}

/* Sections */
section {
    padding: 4rem 0;
}

section h2 {
    text-align: center;
    margin-bottom: 2rem;
    font-size: 2rem;
    color: var(--primary-color);
}

/* Responsive Design */
@media (max-width: 768px) {
    .nav-items {
        display: none;
    }
    
    .hero h1 {
        font-size: 2.5rem;
    }
    
    .newsletter-form {
        flex-direction: column;
    }
    
    .footer-bottom .container {
        flex-direction: column;
        gap: 1rem;
        text-align: center;
    }
}

/* Notifications */
.notification {
    position: fixed;
    bottom: 20px;
    right: 20px;
    background: var(--accent-color);
    color: var(--white);
    padding: 1rem 2rem;
    border-radius: 5px;
    box-shadow: 0 2px 5px rgba(0,0,0,0.2);
    z-index: 1000;
}
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
</head>
<body>
    <nav id="navbar">
        <div class="nav-brand">THE FASHION STORE</div>
        <div class="nav-items">
            <a href="#home" class="active">Home</a>
            <a href="#new-arrivals">New Arrivals</a>
            <a href="#categories">Categories</a>
            <a href="#trending">Trending</a>
            <a href="#about">About</a>
        </div>
        <div class="nav-actions">
            <div class="search-bar">
                <input type="text" placeholder="Search products...">
                <i class="fas fa-search"></i>
            </div>
            <div class="cart-icon">
                <i class="fas fa-shopping-cart"></i>
                <span id="cart-count">0</span>
            </div>
        </div>
    </nav>

    <header id="home">
        <div class="hero">
            <div class="hero-content">
                <h1>Summer Collection 2024</h1>
                <p>Discover the latest trends in fashion</p>
                <div class="hero-buttons">
                    <a href="#new-arrivals" class="btn primary">Shop Now</a>
                    <a href="#categories" class="btn secondary">Explore More</a>
                </div>
            </div>
        </div>
    </header>

    <section id="features">
        <div class="container">
            <div class="feature-grid">
                <div class="feature-card">
                    <i class="fas fa-truck"></i>
                    <h3>Free Shipping</h3>
                    <p>On orders over $50</p>
                </div>
                <div class="feature-card">
                    <i class="fas fa-undo"></i>
                    <h3>Easy Returns</h3>
                    <p>30-day return policy</p>
                </div>
                <div class="feature-card">
                    <i class="fas fa-lock"></i>
                    <h3>Secure Payment</h3>
                    <p>100% secure checkout</p>
                </div>
                <div class="feature-card">
                    <i class="fas fa-headset"></i>
                    <h3>24/7 Support</h3>
                    <p>Dedicated support</p>
                </div>
            </div>
        </div>
    </section>

    <section id="new-arrivals">
        <div class="container">
            <h2>New Arrivals</h2>
            <div class="products-grid" id="new-arrivals-container"></div>
        </div>
    </section>

    <section id="categories">
        <div class="container">
            <h2>Shop by Category</h2>
            <div class="category-grid">
                <div class="category-card women">
                    <h3>Women</h3>
                    <a href="#" class="btn">Shop Now</a>
                </div>
                <div class="category-card men">
                    <h3>Men</h3>
                    <a href="#" class="btn">Shop Now</a>
                </div>
                <div class="category-card accessories">
                    <h3>Accessories</h3>
                    <a href="#" class="btn">Shop Now</a>
                </div>
            </div>
        </div>
    </section>

    <section id="trending">
        <div class="container">
            <h2>Trending Now</h2>
            <div class="products-grid" id="trending-container"></div>
        </div>
    </section>

    <section id="newsletter">
        <div class="container">
            <div class="newsletter-content">
                <h2>Subscribe to Our Newsletter</h2>
                <p>Get the latest updates on new products and upcoming sales</p>
                <form id="newsletter-form" class="newsletter-form">
                    <input type="email" placeholder="Your email address" required>
                    <button type="submit" class="btn primary">Subscribe</button>
                </form>
            </div>
        </div>
    </section>

    <footer>
        <div class="footer-content container">
            <div class="footer-section">
                <h3>THE FASHION STORE</h3>
                <p>Your ultimate destination for trendy and elegant fashion.</p>
                <div class="social-links">
                    <a href="#"><i class="fab fa-facebook"></i></a>
                    <a href="#"><i class="fab fa-instagram"></i></a>
                    <a href="#"><i class="fab fa-twitter"></i></a>
                    <a href="#"><i class="fab fa-pinterest"></i></a>
                </div>
            </div>
            <div class="footer-section">
                <h3>Quick Links</h3>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#new-arrivals">New Arrivals</a></li>
                    <li><a href="#categories">Categories</a></li>
                    <li><a href="#trending">Trending</a></li>
                </ul>
            </div>
            <div class="footer-section">
                <h3>Customer Service</h3>
                <ul>
                    <li><a href="#">Contact Us</a></li>
                    <li><a href="#">Shipping Policy</a></li>
                    <li><a href="#">Returns & Exchanges</a></li>
                    <li><a href="#">FAQs</a></li>
                </ul>
            </div>
            <div class="footer-section">
                <h3>Contact Info</h3>
                <ul class="contact-info">
                    <li><i class="fas fa-map-marker-alt"></i> 123 Fashion Street, NY 10001</li>
                    <li><i class="fas fa-phone"></i> +1 234 567 8900</li>
                    <li><i class="fas fa-envelope"></i> info@fashionstore.com</li>
                </ul>
            </div>
        </div>
        <div class="footer-bottom">
            <div class="container">
                <p>&copy; 2024 The Fashion Store. All rights reserved.</p>
                <div class="payment-methods">
                    <i class="fab fa-cc-visa"></i>
                    <i class="fab fa-cc-mastercard"></i>
                    <i class="fab fa-cc-amex"></i>
                    <i class="fab fa-cc-paypal"></i>
                </div>
            </div>
        </div>
    </footer>
<script>
    import { products } from './products.js';
import { addToCart } from './cart.js';
import { showNotification } from './utils.js';

// DOM Elements
const newArrivalsContainer = document.getElementById('new-arrivals-container');
const trendingContainer = document.getElementById('trending-container');
const newsletterForm = document.getElementById('newsletter-form');
const cartIcon = document.querySelector('.cart-icon');
const searchInput = document.querySelector('.search-bar input');

// Load new arrivals (first 4 products)
function loadNewArrivals() {
    if (!newArrivalsContainer) return;
    const newArrivals = products.slice(0, 4);
    renderProducts(newArrivals, newArrivalsContainer);
}

// Load trending products (last 4 products)
function loadTrendingProducts() {
    if (!trendingContainer) return;
    const trending = products.slice(-4);
    renderProducts(trending, trendingContainer);
}

// Render products to container
function renderProducts(products, container) {
    container.innerHTML = products.map(product => `
        <div class="product-card">
            <img src="${product.image}" alt="${product.name}" class="product-image">
            <div class="product-info">
                <h3 class="product-title">${product.name}</h3>
                <p class="product-price">$${product.price}</p>
                <button class="btn primary" onclick="window.handleAddToCart(${product.id})">
                    Add to Cart
                </button>
            </div>
        </div>
    `).join('');
}

// Handle add to cart
window.handleAddToCart = function(productId) {
    const product = products.find(p => p.id === productId);
    if (product) {
        addToCart(product);
        showNotification('Product added to cart!');
    }
}

// Handle cart icon click
cartIcon?.addEventListener('click', () => {
    window.location.href = '/cart.html';
});

// Handle newsletter subscription
newsletterForm?.addEventListener('submit', (e) => {
    e.preventDefault();
    const email = e.target.querySelector('input[type="email"]').value;
    showNotification('Thank you for subscribing!');
    e.target.reset();
});

// Handle search
searchInput?.addEventListener('input', (e) => {
    const searchTerm = e.target.value.toLowerCase();
    const filteredProducts = products.filter(product => 
        product.name.toLowerCase().includes(searchTerm)
    );
    
    if (newArrivalsContainer) {
        renderProducts(filteredProducts.slice(0, 4), newArrivalsContainer);
    }
    if (trendingContainer) {
        renderProducts(filteredProducts.slice(-4), trendingContainer);
    }
});

// Initialize the page
loadNewArrivals();
loadTrendingProducts();

// Smooth scrolling
document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function (e) {
        e.preventDefault();
        const target = document.querySelector(this.getAttribute('href'));
        if (target) {
            target.scrollIntoView({
                behavior: 'smooth'
            });
        }
    });
});
</script>
    
</body>
</html>
