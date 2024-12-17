<!DOCTYPE html>
<html lang="nl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PartsWorld.nl - Auto Onderdelen Webshop</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <h1><a href="/">PartsWorld.nl</a></h1>
            <nav>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#producten">Producten</a></li>
                    <li><a href="#winkelwagen">Winkelwagen (0)</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Image -->
    <section id="home" class="hero">
        <div class="container">
            <h2>Welkom bij PartsWorld.nl</h2>
            <p>De beste auto onderdelen, altijd snel geleverd.</p>
        </div>
    </section>

    <!-- Producten -->
    <section id="producten" class="container">
        <h2>Onze Populaire Producten</h2>
        <div class="product-container">
            <!-- Product 1 -->
            <div class="product">
                <img src="https://via.placeholder.com/250" alt="Product 1">
                <h3>Auto Onderdeel 1</h3>
                <p>Prijs: €50,00</p>
                <!-- Shopify Buy Button -->
                <div id="product-component-1"></div>
                <script type="text/javascript">
                    !function() {
                        var script = document.createElement('script');
                        script.src = 'https://sdks.shopifycdn.com/buy-button/latest/buy-button.min.js';
                        script.async = true;
                        script.onload = function() {
                            ShopifyBuy.UI.onReady(b16adffb30cbacaef263b6c1570fc922).then(function(ui) {
                                ui.createComponent('product', {
                                    id: 'PRODUCT_ID',  // Product ID uit je Shopify winkel
                                    node: document.getElementById('product-component-1'),
                                    options: {
                                        product: {
                                            layout: "horizontal",
                                            buttonDestination: "checkout",
                                            variantId: "variant-id",
                                            contents: {
                                                img: true,
                                                title: true,
                                                price: true,
                                                button: true
                                            }
                                        }
                                    }
                                });
                            });
                        };
                        document.head.appendChild(script);
                    }();
                </script>
            </div>

            <!-- Product 2 -->
            <div class="product">
                <img src="https://via.placeholder.com/250" alt="Product 2">
                <h3>Auto Onderdeel 2</h3>
                <p>Prijs: €75,00</p>
                <!-- Shopify Buy Button -->
                <div id="product-component-2"></div>
                <script type="text/javascript">
                    !function() {
                        var script = document.createElement('script');
                        script.src = 'https://sdks.shopifycdn.com/buy-button/latest/buy-button.min.js';
                        script.async = true;
                        script.onload = function() {
                            ShopifyBuy.UI.onReady(SHOPIFY_API_KEY).then(function(ui) {
                                ui.createComponent('product', {
                                    id: 'PRODUCT_ID',  // Product ID uit je Shopify winkel
                                    node: document.getElementById('product-component-2'),
                                    options: {
                                        product: {
                                            layout: "horizontal",
                                            buttonDestination: "checkout",
                                            variantId: "variant-id",
                                            contents: {
                                                img: true,
                                                title: true,
                                                price: true,
                                                button: true
                                            }
                                        }
                                    }
                                });
                            });
                        };
                        document.head.appendChild(script);
                    }();
                </script>
            </div>
        </div>
    </section>

    <!-- Winkelwagen -->
    <section id="winkelwagen" class="container">
        <h2>Jouw Winkelwagen</h2>
        <div id="cart-items">Geen producten in winkelwagen.</div>
        <button id="checkout-btn">Afrekenen</button>
    </section>

    <!-- Contact -->
    <section id="contact" class="container">
        <h2>Neem Contact Op</h2>
        <form>
            <input type="text" placeholder="Naam" required>
            <input type="email" placeholder="E-mail" required>
            <textarea placeholder="Bericht" required></textarea>
            <button type="submit">Verstuur</button>
        </form>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <p>&copy; 2024 PartsWorld.nl | Alle rechten voorbehouden</p>
        </div>
    </footer>

    <!-- Scripts -->
    <script src="script.js"></script>
</body>
</html>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Roboto', sans-serif;
    background-color: #f4f4f4;
}

.container {
    width: 80%;
    margin: 0 auto;
}

header {
    background-color: #1f3a63;
    color: white;
    padding: 20px 0;
    text-align: center;
}

header h1 a {
    text-decoration: none;
    color: white;
    font-size: 2.5em;
}

nav ul {
    list-style-type: none;
    padding: 0;
    margin-top: 20px;
}

nav ul li {
    display: inline;
    margin: 0 20px;
}

nav ul li a {
    color: white;
    text-decoration: none;
    font-weight: bold;
}

nav ul li a:hover {
    text-decoration: underline;
}

.hero {
    background-color: #34495e;
    color: white;
    padding: 60px 0;
    text-align: center;
}

h2 {
    font-size: 2.5em;
    margin-bottom: 20px;
}

.product-container {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
}

.product {
    background-color: white;
    padding: 20px;
    margin: 15px;
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    width: 30%;
    text-align: center;
}

.product img {
    width: 100%;
    height: auto;
    border-radius: 5px;
}

.product h3 {
    font-size: 1.2em;
    margin-top: 15px;
}

.product p {
    color: #333;
}

form input, form textarea {
    margin: 10px 0;
    padding: 12px;
    border-radius: 5px;
    border: 1px solid #ccc;
}

form button {
    background-color: #1f3a63;
    color: white;
    padding: 12px 20px;
    border: none;
    cursor: pointer;
    border-radius: 5px;
}

form button:hover {
    background-color: #34495e;
}

footer {
    background-color: #1f3a63;
    color: white;
    padding: 20px;
    text-align: center;
}


let cart = [];

function addToCart(productName, price) {
    cart.push({ productName, price });
    updateCart();
}

function updateCart() {
    const cartItemsDiv = document.getElementById('cart-items');
    if (cart.length === 0) {
        cartItemsDiv.innerHTML = 'Geen producten in winkelwagen.';
    } else {
        cartItemsDiv.innerHTML = '';
        cart.forEach((item, index) => {
            const itemDiv = document.createElement('div');
            itemDiv.innerHTML = `${item.productName} - €${item.price}`;
            cartItemsDiv.appendChild(itemDiv);
        });
    }
}

document.getElementById('checkout-btn').addEventListener('click', () => {
    alert('Afrekenen - Hier kan je je betaalpagina integr

