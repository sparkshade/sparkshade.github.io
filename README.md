<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Spar$hade - Abbigliamento di Marca</title>
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
        </section>
    </main>
    <footer>
        <p>&copy; 2024 Spar$hade. Tutti i diritti riservati.</p>
    </footer>

    <script>
        // Simulazione di un database di prodotti
        const products = [
            { name: "T-Shirt Classica", price: 29.99 },
            { name: "Jeans Slim Fit", price: 59.99 },
            { name: "Felpa con Cappuccio", price: 49.99 }
        ];

        // Funzione per visualizzare i prodotti
        function displayProducts() {
            const productList = document.getElementById('product-list');
            products.forEach(product => {
                const productDiv = document.createElement('div');
                productDiv.className = 'product';
                productDiv.innerHTML = `
                    <h3>${product.name}</h3>
                    <p>Prezzo: €${product.price}</p>
                    <button onclick="addToCart('${product.name}')">Aggiungi al Carrello</button>
                `;
                productList.appendChild(productDiv);
            });
        }

        // Funzione per aggiungere al carrello (da implementare)
        function addToCart(productName) {
            alert(`Prodotto aggiunto al carrello: ${productName}`);
            // Qui potresti implementare la logica del carrello
        }

        // Carica i prodotti quando la pagina è pronta
        window.onload = displayProducts;
    </script>
</body>
</html>
