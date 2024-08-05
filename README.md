<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Spar$hade - Abbigliamento di Marca</title>
    <link href="https://fonts.googleapis.com/css2?family=Aurora+Pro&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f0f0f0;
        }
        header {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 1em;
        }
        header h1 {
            font-family: 'Aurora Pro', sans-serif;
            font-size: 2.5em;
        }
        nav {
            background-color: #444;
            padding: 0.5em;
        }
        nav ul {
            list-style-type: none;
            padding: 0;
        }
        nav ul li {
            display: inline;
            margin-right: 1em;
        }
        nav ul li a {
            color: white;
            text-decoration: none;
        }
        main {
            padding: 2em;
            max-width: 800px;
            margin: 0 auto;
        }
        .product {
            background-color: white;
            border: 1px solid #ddd;
            padding: 1em;
            margin-bottom: 1em;
        }
        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 1em;
            position: fixed;
            bottom: 0;
            width: 100%;
        }
    </style>
</head>
<body>
    <header>
        <h1>Spar$hade</h1>
    </header>
    <nav>
        <ul>
            <li><a href="#prodotti">Prodotti</a></li>
            <li><a href="#chi-siamo">Chi Siamo</a></li>
            <li><a href="#contatti">Contatti</a></li>
        </ul>
    </nav>
    <main>
        <section id="prodotti">
            <h2>I Nostri Prodotti</h2>
            <div id="product-list"></div>
            
            <div class="product">
                <h3>Wisionary Close Hoodie</h3>
                <img src="percorso_dell_immagine/wisionary_close_hoodie.jpg" alt="Wisionary Close Hoodie" style="max-width: 100%; height: auto;">
                <p>Una comoda felpa con cappuccio nera con il logo Spar$hade.</p>
                <p>Prezzo: €59.99</p>
              function displayProducts() {
    const productList = document.getElementById('product-list');
    products.forEach(product => {
        const productDiv = document.createElement('div');
        productDiv.className = 'product';
        productDiv.innerHTML = `
            <h3>${product.name}</h3>
            ${product.image ? `<img src="${product.image}" alt="${product.name}" style="max-width: 100%; height: auto;">` : ''}
            <p>Prezzo: €${product.price}</p>
            <button onclick="addToCart('${product.name}')">Aggiungi al Carrello</button>
        `;
        productList.appendChild(productDiv);
    });
}
                <button onclick="addToCart('Wisionary Close Hoodie')">Aggiungi al Carrello</button>
            </div>
        </section>
    </main>
    <footer>
        <p>&copy; 2024 Spar$hade. Tutti i diritti riservati.</p>
    </footer>

    <script>
        const products = [
            { name: "T-Shirt Classica", price: 29.99 },
            { name: "Jeans Slim Fit", price: 59.99 },
            { name: "Felpa con Cappuccio", price: 49.99 },
            { name: "Wisionary Close Hoodie", price: 59.99, image: "percorso_dell_immagine/wisionary_close_hoodie.jpg" }
        ];

        function displayProducts() {
            const productList = document.getElementById('product-list');
            products.forEach(product => {
                const productDiv = document.createElement('div');
                productDiv.className = 'product';
                productDiv.innerHTML = `
                    <h3>${product.name}</h3>
                    ${product.image ? `<img src="${product.image}" alt="${product.name}" style="max-width: 100%; height: auto;">` : ''}
                    <p>Prezzo: €${product.price}</p>
                    <button onclick="addToCart('${product.name}')">Aggiungi al Carrello</button>
                `;
                productList.appendChild(productDiv);
            });
        }

        function addToCart(productName) {
            alert(`Prodotto aggiunto al carrello: ${productName}`);
        }

        window.onload = displayProducts;
    </script>
</body>
</html>
