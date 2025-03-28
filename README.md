<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cetenry - Boutique</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: black;
            color: white;
        }
        header {
            background: black;
            color: white;
            padding: 20px;
            font-size: 30px;
            text-transform: uppercase;
            letter-spacing: 2px;
            text-align: center;
        }
        .container {
            max-width: 1200px;
            margin: auto;
            padding: 40px 20px;
        }
        .product {
            background: white;
            color: black;
            padding: 20px;
            margin: 20px;
            border-radius: 10px;
            display: inline-block;
            width: calc(33.333% - 40px);
            text-align: center;
            transition: all 0.3s;
        }
        .product:hover {
            background: #f1f1f1;
        }
        .product img {
            width: 100%;
            max-width: 300px;
            margin-bottom: 15px;
        }
        .product h3 {
            margin: 10px 0;
        }
        .product p {
            font-size: 18px;
        }
        .price {
            font-weight: bold;
            font-size: 24px;
        }
        .btn {
            display: inline-block;
            padding: 10px 20px;
            background: black;
            color: white;
            text-decoration: none;
            margin-top: 15px;
            border-radius: 5px;
        }
        .form-container {
            background: white;
            color: black;
            padding: 20px;
            border-radius: 10px;
            margin-top: 40px;
            width: 100%;
            max-width: 600px;
            margin: auto;
        }
        input, textarea {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ddd;
            border-radius: 5px;
            background: #f9f9f9;
        }
        input[type="submit"] {
            background: black;
            color: white;
            border: none;
            cursor: pointer;
        }
        input[type="submit"]:hover {
            background: #333;
        }
    </style>
</head>
<body>

<header>Cetenry - Marque Indépendante</header>

<div class="container">
    <h2>Nos Produits</h2>

    <!-- Exemple de produit -->
    <div class="product">
        <img src="tshirt.jpg" alt="T-shirt Cetenry">
        <h3>T-shirt Cetenry</h3>
        <p>Un t-shirt élégant, parfait pour tous les jours.</p>
        <p class="price">25€</p>
        <a href="#commande" class="btn">Acheter</a>
    </div>

    <div class="product">
        <img src="hoodie.jpg" alt="Hoodie Cetenry">
        <h3>Hoodie Cetenry</h3>
        <p>Un hoodie doux et confortable.</p>
        <p class="price">50€</p>
        <a href="#commande" class="btn">Acheter</a>
    </div>

</div>

<!-- Formulaire de commande -->
<div id="commande" class="form-container">
    <h3>Informations de Livraison</h3>
    <form action="https://www.paypal.com/cgi-bin/webscr" method="post" target="_blank">
        <label for="nom">Nom :</label>
        <input type="text" id="nom" name="nom" required>
        
        <label for="adresse">Adresse :</label>
        <textarea id="adresse" name="adresse" rows="4" required></textarea>

        <label for="email">Email :</label>
        <input type="email" id="email" name="email" required>

        <label for="produit">Produit sélectionné :</label>
        <input type="text" id="produit" name="produit" value="T-shirt Cetenry" readonly>

        <label for="prix">Prix :</label>
        <input type="text" id="prix" name="prix" value="25" readonly>

        <input type="submit" value="Payer avec PayPal">
    </form>
</div>

</body>
</html>
