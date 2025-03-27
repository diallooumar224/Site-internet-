# LANFAALA GROUPE 
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TechShop - Votre boutique en ligne</title>
    <link rel="stylesheet" href="css/style.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>
    <header>
        <div class="top-bar">
            <div class="container">
                <div class="currency-selector">
                    <select id="currency">
                        <option value="EUR">€ EUR</option>
                        <option value="USD">$ USD</option>
                        <option value="GBP">£ GBP</option>
                    </select>
                </div>
                <div class="auth-links">
                    <a href="login.html" id="login-link"><i class="fas fa-user"></i> Connexion</a>
                    <a href="register.html" id="register-link"><i class="fas fa-user-plus"></i> Inscription</a>
                </div>
            </div>
        </div>
        <nav class="main-nav">
            <div class="container">
                <div class="logo">
                    <a href="index.html">TechShop</a>
                </div>
                <div class="search-bar">
                    <input type="text" placeholder="Rechercher des produits...">
                    <button><i class="fas fa-search"></i></button>
                </div>
                <div class="nav-links">
                    <a href="index.html">Accueil</a>
                    <a href="products.html">Boutique</a>
                    <a href="about.html">À propos</a>
                    <a href="contact.html">Contact</a>
                </div>
                <div class="cart-icon">
                    <a href="cart.html"><i class="fas fa-shopping-cart"></i> <span id="cart-count">0</span></a>
                </div>
            </div>
        </nav>
    </header>

    <main>
        <section class="hero">
            <div class="hero-content">
                <h1>Découvrez nos nouveautés</h1>
                <p>Jusqu'à 30% de réduction sur les derniers produits</p>
                <a href="products.html" class="btn">Voir la collection</a>
            </div>
        </section>

        <section class="featured-products">
            <div class="container">
                <h2>Produits populaires</h2>
                <div class="products-grid" id="featured-products">
                    <!-- Produits chargés via JavaScript -->
                </div>
            </div>
        </section>

        <section class="categories">
            <div class="container">
                <h2>Catégories</h2>
                <div class="categories-grid">
                    <div class="category-card">
                        <img src="images/category-electronics.jpg" alt="Électronique">
                        <h3>Électronique</h3>
                    </div>
                    <div class="category-card">
                        <img src="images/category-fashion.jpg" alt="Mode">
                        <h3>Mode</h3>
                    </div>
                    <div class="category-card">
                        <img src="images/category-home.jpg" alt="Maison">
                        <h3>Maison</h3>
                    </div>
                    <div class="category-card">
                        <img src="images/category-sports.jpg" alt="Sports">
                        <h3>Sports</h3>
                    </div>
                </div>
            </div>
        </section>

        <section class="newsletter">
            <div class="container">
                <h2>Abonnez-vous à notre newsletter</h2>
                <p>Recevez des offres exclusives et des mises à jour sur nos nouveaux produits</p>
                <form id="newsletter-form">
                    <input type="email" placeholder="Votre adresse email" required>
                    <button type="submit" class="btn">S'abonner</button>
                </form>
            </div>
        </section>
    </main>

    <footer>
        <div class="container">
            <div class="footer-section">
                <h3>Aide & Contact</h3>
                <ul>
                    <li><a href="contact.html">Contactez-nous</a></li>
                    <li><a href="faq.html">FAQ</a></li>
                    <li><a href="shipping.html">Livraison</a></li>
                    <li><a href="returns.html">Retours</a></li>
                </ul>
            </div>
            <div class="footer-section">
                <h3>À propos</h3>
                <ul>
                    <li><a href="about.html">Notre histoire</a></li>
                    <li><a href="careers.html">Carrières</a></li>
                    <li><a href="blog.html">Blog</a></li>
                </ul>
            </div>
            <div class="footer-section">
                <h3>Paiements sécurisés</h3>
                <div class="payment-methods">
                    <i class="fab fa-cc-visa"></i>
                    <i class="fab fa-cc-mastercard"></i>
                    <i class="fab fa-cc-paypal"></i>
                    <i class="fab fa-cc-apple-pay"></i>
                </div>
            </div>
            <div class="footer-section">
                <h3>Suivez-nous</h3>
                <div class="social-links">
                    <a href="#"><i class="fab fa-facebook"></i></a>
                    <a href="#"><i class="fab fa-twitter"></i></a>
                    <a href="#"><i class="fab fa-instagram"></i></a>
                    <a href="#"><i class="fab fa-pinterest"></i></a>
                </div>
            </div>
        </div>
        <div class="copyright">
            <p>&copy; 2023 TechShop. Tous droits réservés.</p>
        </div>
    </footer>

    <script src="js/main.js"></script>
    <script src="js/products.js"></script>
    <script src="js/cart.js"></script>
</body>
</html>

/* Reset et base */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

body {
    line-height: 1.6;
    color: #333;
    background-color: #f9f9f9;
}

.container {
    width: 90%;
    max-width: 1200px;
    margin: 0 auto;
}

.btn {
    display: inline-block;
    padding: 10px 20px;
    background-color: #4CAF50;
    color: white;
    text-decoration: none;
    border-radius: 4px;
    transition: background-color 0.3s;
}

.btn:hover {
    background-color: #45a049;
}

/* Header */
.top-bar {
    background-color: #333;
    color: white;
    padding: 8px 0;
    font-size: 0.9rem;
}

.top-bar .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.auth-links a {
    color: white;
    text-decoration: none;
    margin-left: 15px;
}

.auth-links a:hover {
    text-decoration: underline;
}

.main-nav {
    background-color: white;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    padding: 15px 0;
}

.main-nav .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.logo a {
    font-size: 1.8rem;
    font-weight: bold;
    color: #4CAF50;
    text-decoration: none;
}

.search-bar {
    display: flex;
    flex-grow: 0.5;
    margin: 0 20px;
}

.search-bar input {
    width: 100%;
    padding: 8px 15px;
    border: 1px solid #ddd;
    border-radius: 4px 0 0 4px;
}

.search-bar button {
    padding: 8px 15px;
    background-color: #4CAF50;
    color: white;
    border: none;
    border-radius: 0 4px 4px 0;
    cursor: pointer;
}

.nav-links a {
    color: #333;
    text-decoration: none;
    margin: 0 10px;
    font-weight: 500;
}

.nav-links a:hover {
    color: #4CAF50;
}

.cart-icon a {
    color: #333;
    text-decoration: none;
    font-weight: 500;
}

.cart-icon a:hover {
    color: #4CAF50;
}

/* Hero section */
.hero {
    background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('../images/hero-bg.jpg');
    background-size: cover;
    background-position: center;
    color: white;
    text-align: center;
    padding: 100px 20px;
}

.hero-content h1 {
    font-size: 2.5rem;
    margin-bottom: 20px;
}

.hero-content p {
    font-size: 1.2rem;
    margin-bottom: 30px;
}

/* Produits */
.featured-products {
    padding: 60px 0;
}

.products-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
    gap: 30px;
    margin-top: 30px;
}

.product-card {
    background: white;
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    transition: transform 0.3s, box-shadow 0.3s;
}

.product-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 5px 15px rgba(0,0,0,0.1);
}

.product-image {
    height: 200px;
    overflow: hidden;
}

.product-image img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: transform 0.3s;
}

.product-card:hover .product-image img {
    transform: scale(1.05);
}

.product-info {
    padding: 15px;
}

.product-info h3 {
    margin-bottom: 10px;
    font-size: 1.1rem;
}

.product-price {
    font-weight: bold;
    color: #4CAF50;
    margin-bottom: 15px;
}

.product-rating {
    color: #FFD700;
    margin-bottom: 15px;
}

.add-to-cart {
    width: 100%;
    padding: 8px 0;
    background-color: #4CAF50;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    transition: background-color 0.3s;
}

.add-to-cart:hover {
    background-color: #45a049;
}

/* Catégories */
.categories {
    padding: 60px 0;
    background-color: #f1f1f1;
}

.categories-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    gap: 20px;
    margin-top: 30px;
}

.category-card {
    background: white;
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    text-align: center;
    transition: transform 0.3s;
}

.category-card:hover {
    transform: translateY(-5px);
}

.category-card img {
    width: 100%;
    height: 120px;
    object-fit: cover;
}

.category-card h3 {
    padding: 15px;
    font-size: 1.1rem;
}

/* Newsletter */
.newsletter {
    padding: 60px 0;
    text-align: center;
    background-color: #4CAF50;
    color: white;
}

.newsletter h2 {
    margin-bottom: 15px;
}

.newsletter p {
    margin-bottom: 30px;
    font-size: 1.1rem;
}

.newsletter form {
    display: flex;
    max-width: 500px;
    margin: 0 auto;
}

.newsletter input {
    flex-grow: 1;
    padding: 10px 15px;
    border: none;
    border-radius: 4px 0 0 4px;
}

.newsletter button {
    padding: 10px 20px;
    background-color: #333;
    color: white;
    border: none;
    border-radius: 0 4px 4px 0;
    cursor: pointer;
}

.newsletter button:hover {
    background-color: #222;
}

/* Footer */
footer {
    background-color: #333;
    color: white;
    padding: 60px 0 0;
}

.footer-section {
    margin-bottom: 30px;
}

.footer-section h3 {
    margin-bottom: 20px;
    font-size: 1.2rem;
}

.footer-section ul {
    list-style: none;
}

.footer-section ul li {
    margin-bottom: 10px;
}

.footer-section ul li a {
    color: #ddd;
    text-decoration: none;
}

.footer-section ul li a:hover {
    color: white;
    text-decoration: underline;
}

.payment-methods, .social-links {
    display: flex;
    gap: 15px;
    font-size: 1.5rem;
}

.social-links a {
    color: #ddd;
}

.social-links a:hover {
    color: white;
}

.copyright {
    text-align: center;
    padding: 20px 0;
    border-top: 1px solid #444;
    margin-top: 30px;
    font-size: 0.9rem;
    color: #aaa;
}

/* Responsive */
@media (max-width: 768px) {
    .main-nav .container {
        flex-direction: column;
    }

    .search-bar {
        width: 100%;
        margin: 15px 0;
    }

    .nav-links {
        margin-top: 15px;
    }

    .products-grid, .categories-grid {
        grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    }

    .footer .container {
        grid-template-columns: 1fr;
    }
}
// Données des produits (en réalité, cela viendrait d'une API)
const products = [
    {
        id: 1,
        name: "Smartphone Premium",
        price: 799.99,
        image: "images/product1.jpg",
        category: "Électronique",
        rating: 4.5,
        description: "Un smartphone haut de gamme avec écran AMOLED et triple caméra."
    },
    {
        id: 2,
        name: "Casque Bluetooth",
        price: 149.99,
        image: "images/product2.jpg",
        category: "Électronique",
        rating: 4.2,
        description: "Casque sans fil avec réduction de bruit active."
    },
    {
        id: 3,
        name: "Montre Connectée",
        price: 199.99,
        image: "images/product3.jpg",
        category: "Électronique",
        rating: 4.7,
        description: "Suivi d'activité, notifications et autonomie de 7 jours."
    },
    {
        id: 4,
        name: "Sac à Dos Urbain",
        price: 59.99,
        image: "images/product4.jpg",
        category: "Mode",
        rating: 4.3,
        description: "Sac résistant à l'eau avec compartiment pour ordinateur portable."
    },
    {
        id: 5,
        name: "Enceinte Portable",
        price: 89.99,
        image: "images/product5.jpg",
        category: "Électronique",
        rating: 4.1,
        description: "Son stéréo puissant et résistance à l'eau."
    },
    {
        id: 6,
        name: "T-shirt Premium",
        price: 29.99,
        image: "images/product6.jpg",
        category: "Mode",
        rating: 4.0,
        description: "100% coton biologique, design minimaliste."
    }
];

// Afficher les produits sur la page d'accueil
function displayFeaturedProducts() {
    const featuredContainer = document.getElementById('featured-products');
    
    // Sélectionner 4 produits au hasard (ou les 4 premiers)
    const featuredProducts = products.slice(0, 4);
    
    featuredProducts.forEach(product => {
        const productElement = document.createElement('div');
        productElement.className = 'product-card';
        productElement.innerHTML = `
            <div class="product-image">
                <img src="${product.image}" alt="${product.name}">
            </div>
            <div class="product-info">
                <h3>${product.name}</h3>
                <div class="product-price">$${product.price.toFixed(2)}</div>
                <div class="product-rating">
                    ${generateStarRating(product.rating)}
                </div>
                <button class="add-to-cart" data-id="${product.id}">Ajouter au panier</button>
            </div>
        `;
        
        featuredContainer.appendChild(productElement);
    });
    
    // Ajouter les écouteurs d'événements pour les boutons "Ajouter au panier"
    document.querySelectorAll('.add-to-cart').forEach(button => {
        button.addEventListener('click', addToCart);
    });
}

// Générer le HTML pour les étoiles de notation
function generateStarRating(rating) {
    const fullStars = Math.floor(rating);
    const hasHalfStar = rating % 1 >= 0.5;
    let stars = '';
    
    for (let i = 1; i <= 5; i++) {
        if (i <= fullStars) {
            stars += '<i class="fas fa-star"></i>';
        } else if (i === fullStars + 1 && hasHalfStar) {
            stars += '<i class="fas fa-star-half-alt"></i>';
        } else {
            stars += '<i class="far fa-star"></i>';
        }
    }
    
    return stars;
}

// Charger les produits quand la page est prête
document.addEventListener('DOMContentLoaded', function() {
    displayFeaturedProducts();
});
// Gestion du panier
let cart = JSON.parse(localStorage.getItem('cart')) || [];

// Ajouter un produit au panier
function addToCart(event) {
    const productId = parseInt(event.target.getAttribute('data-id'));
    const product = products.find(p => p.id === productId);
    
    if (!product) return;
    
    // Vérifier si le produit est déjà dans le panier
    const existingItem = cart.find(item => item.id === productId);
    
    if (existingItem) {
        existingItem.quantity += 1;
    } else {
        cart.push({
            id: product.id,
            name: product.name,
            price: product.price,
            image: product.image,
            quantity: 1
        });
    }
    
    // Mettre à jour le localStorage
    localStorage.setItem('cart', JSON.stringify(cart));
    
    // Mettre à jour le compteur du panier
    updateCartCount();
    
    // Afficher une notification
    showNotification(`${product.name} a été ajouté au panier`);
}

// Mettre à jour le compteur du panier
function updateCartCount() {
    const count = cart.reduce((total, item) => total + item.quantity, 0);
    document.getElementById('cart-count').textContent = count;
}

// Afficher une notification
function showNotification(message) {
    const notification = document.createElement('div');
    notification.className = 'notification';
    notification.textContent = message;
    
    document.body.appendChild(notification);
    
    setTimeout(() => {
        notification.classList.add('show');
    }, 10);
    
    setTimeout(() => {
        notification.classList.remove('show');
        setTimeout(() => {
            document.body.removeChild(notification);
        }, 300);
    }, 3000);
}

// Initialiser le compteur du panier au chargement
document.addEventListener('DOMContentLoaded', function() {
    updateCartCount();
});
const express = require('express');
const bodyParser = require('body-parser');
const path = require('path');
const app = express();

// Middleware
app.use(bodyParser.json());
app.use(bodyParser.urlencoded({ extended: true }));
app.use(express.static(path.join(__dirname, 'public')));

// Simuler une base de données
let users = [
    { id: 1, email: 'user@example.com', password: 'password123' }
];

let orders = [];

// Routes API
app.get('/api/products', (req, res) => {
    // En réalité, cela viendrait d'une base de données
    const products = [
        // Même liste de produits que dans products.js
    ];
    res.json(products);
});

app.post('/api/login', (req, res) => {
    const { email, password } = req.body;
    const user = users.find(u => u.email === email && u.password === password);
    
    if (user) {
        res.json({ success: true, message: 'Connexion réussie' });
    } else {
        res.status(401).json({ success: false, message: 'Email ou mot de passe incorrect' });
    }
});

app.post('/api/register', (req, res) => {
    const { email, password } = req.body;
    
    if (users.some(u => u.email === email)) {
        return res.status(400).json({ success: false, message: 'Email déjà utilisé' });
    }
    
    const newUser = {
        id: users.length + 1,
        email,
        password
    };
    
    users.push(newUser);
    res.json({ success: true, message: 'Inscription réussie' });
});

app.post('/api/checkout', (req, res) => {
    const { cart, userInfo, paymentInfo } = req.body;
    
    // Enregistrer la commande
    const newOrder = {
        id: orders.length + 1,
        date: new Date(),
        items: cart,
        userInfo,
        paymentInfo,
        status: 'processing'
    };
    
    orders.push(newOrder);
    
    // En réalité, on traiterait le paiement ici
    
    res.json({ 
        success: true, 
        orderId: newOrder.id,
        message: 'Commande passée avec succès' 
    });
});

// Servir les pages HTML
app.get('*', (req, res) => {
    res.sendFile(path.join(__dirname, 'public', 'index.html'));
});

// Démarrer le serveur
const PORT = process.env.PORT || 3000;
app.listen(PORT, () => {
    console.log(`Serveur démarré sur le port ${PORT}`);
});
// Dans products.js
function setupSearch() {
    const searchInput = document.querySelector('.search-bar input');
    
    searchInput.addEventListener('input', debounce(function() {
        const searchTerm = this.value.toLowerCase();
        const filteredProducts = products.filter(product => 
            product.name.toLowerCase().includes(searchTerm) || 
            product.description.toLowerCase().includes(searchTerm)
        );
        
        displayProducts(filteredProducts);
    }, 300));
}

function debounce(func, wait) {
    let timeout;
    return function() {
        const context = this, args = arguments;
        clearTimeout(timeout);
        timeout = setTimeout(() => func.apply(context, args), wait);
    };
}
