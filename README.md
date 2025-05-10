# Store
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TechStore</title>
    <link rel="stylesheet" href="styles.css">
</head>
<style>
    /* Reset and base styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
    line-height: 1.6;
    color: #333;
    background-color: #f5f5f5;
}

.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 50px;
}

/* Header styles */
header {
    background-color: white;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    top: 0;
    z-index: 1;
}

nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem;
    max-width: 1200px;
    margin: 0 auto;
}

.logo {
    font-size: 1.5rem;
    font-weight: bold;
    color: #333;
}

.search-bar {
    flex: 1;
    max-width: 500px;
    margin: 0 2rem;
    display: flex;
}

.search-bar input {
    width: 100%;
    padding: 0.5rem 1rem;
    border: 1px solid #ddd;
    border-radius: 4px 0 0 4px;
    outline: none;
}

.search-btn {
    padding: 0.5rem 1rem;
    background-color: #2563eb;
    color: white;
    border: none;
    border-radius: 0 4px 4px 0;
    cursor: pointer;
}

.nav-buttons a {
    margin-left: 1.5rem;
    text-decoration: none;
    color: #333;
}

/* Categories section */
.categories {
    padding: 2rem 0;
}

.categories .container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 1.5rem;
}

.category-card {
    background: white;
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    transition: transform 0.2s;
}

.category-card:hover {
    transform: translateY(-4px);
}

.category-card img {
    width: 100%;
    height: 200px;
    object-fit: cover;
}

.category-card h3 {
    padding: 1rem;
    text-align: center;
}

/* Hero section */
.hero {
    background: linear-gradient(to right, #2563eb, #1d4ed8);
    color: white;
    padding: 4rem 0;
    margin-bottom: 4rem;
}

.hero .container {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 2rem;
    align-items: center;
}

.hero-content h1 {
    font-size: 3rem;
    margin-bottom: 1rem;
}

.hero-content p {
    font-size: 1.25rem;
    margin-bottom: 2rem;
}

.cta-button {
    display: inline-block;
    padding: 1rem 2rem;
    background-color: white;
    color: #2563eb;
    text-decoration: none;
    border-radius: 9999px;
    font-weight: 600;
    transition: background-color 0.2s;
}

.cta-button:hover {
    background-color: #f8f9fa;
}

.hero-image img {
    width: 100%;
    border-radius: 8px;
    box-shadow: 0 4px 6px rgba(0,0,0,0.1);
}

/* Products section */
.products {
    padding: 4rem 0;
}

.products h2 {
    font-size: 2rem;
    margin-bottom: 2rem;
    text-align: center;
}

.product-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 2rem;
}

.product-card {
    background: white;
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    transition: box-shadow 0.2s;
}

.product-card:hover {
    box-shadow: 0 4px 8px rgba(0,0,0,0.2);
}

.product-card img {
    width: 100%;
    height: 250px;
    object-fit: cover;
}

.product-info {
    padding: 1.5rem;
}

.category {
    color: #2563eb;
    font-size: 0.875rem;
    font-weight: 500;
}

.product-info h3 {
    margin: 0.5rem 0;
    font-size: 1.25rem;
}

.product-info p {
    color: #666;
    margin-bottom: 1rem;
}

.product-footer {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.price {
    font-size: 1.5rem;
    font-weight: bold;
}

.add-to-cart {
    padding: 0.5rem 1rem;
    background-color: #2563eb;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    transition: background-color 0.2s;
}

.add-to-cart:hover {
    background-color: #1d4ed8;
}

/* Footer styles */
footer {
    background-color: #1f2937;
    color: white;
    padding: 4rem 0 2rem;
}

.footer-content {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 2rem;
    margin-bottom: 2rem;
}

.footer-section h3 {
    margin-bottom: 1rem;
    font-size: 1.25rem;
}

.footer-section ul {
    list-style: none;
}

.footer-section ul li {
    margin-bottom: 0.5rem;
}

.footer-section a {
    color: #9ca3af;
    text-decoration: none;
    transition: color 0.2s;
}

.footer-section a:hover {
    color: white;
}

.newsletter {
    display: flex;
    margin-top: 1rem;
}

.newsletter input {
    flex: 1;
    padding: 0.5rem;
    border: none;
    border-radius: 4px 0 0 4px;
    background-color: #374151;
    color: white;
}

.newsletter button {
    padding: 0.5rem 1rem;
    background-color: #2563eb;
    color: white;
    border: none;
    border-radius: 0 4px 4px 0;
    cursor: pointer;
}

.footer-bottom {
    text-align: center;
    padding-top: 2rem;
    border-top: 1px solid #374151;
    color: #9ca3af;
}

/* Responsive design */
@media (max-width: 932px) {
    .hero .container {
        grid-template-columns: 1fr;
        text-align: center;
    }

    .search-bar {
        display: none;
    }

    .nav-buttons {
        display: none;
    }

    .hero-content {
        order: 2;
    }

    .hero-image {
        order: 1;
        margin-bottom: 2rem;
    }

    .footer-content {
        grid-template-columns: 1fr;
        text-align: center;
    }

    .newsletter {
        justify-content: center;
    }
}
@media (max-width: 768px) {
    .hero .container {
        grid-template-columns: 1fr;
        text-align: center;
    }

    .search-bar {
        display: none;
    }

    .nav-buttons {
        display: none;
    }

    .hero-content {
        order: 2;
    }

    .hero-image {
        order: 1;
        margin-bottom: 2rem;
    }

    .footer-content {
        grid-template-columns: 1fr;
        text-align: center;
    }

    .newsletter {
        justify-content: center;
    }
}
</style>
<body>
    <!-- Header -->
    <header>
        <nav>
            <div class="logo"Emmystore Tech>
                <img src="" alt="">
            </div>
            <div class="search-bar">
                <input type="text" placeholder="Search products...">
                <button class="search-btn">Search</button>
            </div>
            <div class="nav-buttons">
                <a href="#" class="wishlist">Wishlist</a>
                <a href="#" class="cart">Cart (3)</a>
            </div>
        </nav>
    </header>

    <!-- Categories -->
    <section class="categories">
        <div class="container">
            <div class="category-card">
                <img src="https://images.unsplash.com/photo-1517336714731-489689fd1ca8?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1026&q=80" alt="Laptops">
                <h3>Laptops</h3>
            </div>
            <div class="category-card">
                <img src="https://images.unsplash.com/photo-1592750475338-74b7b21085ab?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=987&q=80" alt="Smartphones">
                <h3>Smartphones</h3>
            </div>
            <div class="category-card">
                <img src="https://images.unsplash.com/photo-1618366712010-f4ae9c647dcb?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=987&q=80" alt="Audio">
                <h3>Audio</h3>
            </div>
            <div class="category-card">
                <img src="https://images.unsplash.com/photo-1434493789847-2f02dc6ca35d?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2071&q=80" alt="Wearables">
                <h3>Wearables</h3>
            </div>
        </div>
    </section>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <div class="hero-content">
                <h1>New MacBook Pro</h1>
                <p>Supercharged by Apple M2 Pro and M2 Max</p>
                <a href="#" class="cta-button">Shop Now</a>
            </div>
            <div class="hero-image">
                <img src="https://images.unsplash.com/photo-1517336714731-489689fd1ca8?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1026&q=80" alt="MacBook Pro">
            </div>
        </div>
    </section>

    <!-- Products Grid -->
    <section class="products">
        <div class="container">
            <h2>Featured Products</h2>
            <div class="product-grid">
                <div class="product-card">
                    <img src="https://images.unsplash.com/photo-1517336714731-489689fd1ca8?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1026&q=80" alt="MacBook Pro">
                    <div class="product-info">
                        <span class="category">Laptops</span>
                        <h3>MacBook Pro 16"</h3>
                        <p>Apple M2 Pro chip, 32GB RAM, 1TB SSD</p>
                        <div class="product-footer">
                            <span class="price">$2,499</span>
                            <button class="add-to-cart">Add to Cart</button>
                        </div>
                    </div>
                </div>
                <div class="product-card">
                    <img src="https://images.unsplash.com/photo-1592750475338-74b7b21085ab?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=987&q=80" alt="iPhone 15 Pro">
                    <div class="product-info">
                        <span class="category">Smartphones</span>
                        <h3>iPhone 15 Pro</h3>
                        <p>A17 Pro chip, 256GB, Titanium</p>
                        <div class="product-footer">
                            <span class="price">$999</span>
                            <button class="add-to-cart">Add to Cart</button>
                        </div>
                    </div>
                </div>
                <div class="product-card">
                    <img src="https://images.unsplash.com/photo-1618366712010-f4ae9c647dcb?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=987&q=80" alt="Sony WH-1000XM5">
                    <div class="product-info">
                        <span class="category">Audio</span>
                        <h3>Sony WH-1000XM5</h3>
                        <p>Wireless Noise Cancelling Headphones</p>
                        <div class="product-footer">
                            <span class="price">$399</span>
                            <button class="add-to-cart">Add to Cart</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>About TechStore</h3>
                    <p>Your one-stop destination for premium tech products and accessories.</p>
                </div>
                <div class="footer-section">
                    <h3>Quick Links</h3>
                    <ul>
                        <li><a href="#">Shop</a></li>
                        <li><a href="#">About</a></li>
                        <li><a href="#">Contact</a></li>
                        <li><a href="#">Support</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h3>Customer Service</h3>
                    <ul>
                        <li><a href="#">Shipping Policy</a></li>
                        <li><a href="#">Returns & Exchanges</a></li>
                        <li><a href="#">FAQs</a></li>
                        <li><a href="#">Track Order</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h3>Newsletter</h3>
                    <p>Subscribe to get special offers and updates.</p>
                    <div class="newsletter">
                        <input type="email" placeholder="Enter your email">
                        <button>Subscribe</button>
                    </div>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2024 TechStore. All rights reserved.</p>
            </div>
        </div>
    </footer>
</body>
</html>
