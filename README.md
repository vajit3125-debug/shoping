<!DOCTYPE html>
<html>
<head>
    <title>My Clothing Shop</title>

    <style>
        body {
            font-family: Arial;
            margin: 0;
            background: #f2f2f2;
            text-align: center;
        }

        header {
            background: black;
            color: white;
            padding: 20px;
        }

        .product {
            background: white;
            display: inline-block;
            width: 200px;
            margin: 15px;
            padding: 15px;
            border-radius: 10px;
        }

        .product img {
            width: 100%;
            height: 180px;
            object-fit: cover;
        }

        button {
            background: green;
            color: white;
            border: none;
            padding: 10px;
            cursor: pointer;
        }

        #cart {
            background: white;
            padding: 20px;
            margin: 20px;
        }
    </style>
</head>

<body>

<header>
    <h1>My Clothing Shop</h1>
    <p>Shop Your Favourite Clothes!</p>
</header>

<h2>Our Products</h2>

<div class="product">
    <img src="https://placehold.co/200x180?text=T-Shirt">
    <h3>T-Shirt</h3>
    <p>Price: ₹499</p>
    <button onclick="addToCart('T-Shirt', 499)">
        Add to Cart
    </button>
</div>

<div class="product">
    <img src="https://placehold.co/200x180?text=Shirt">
    <h3>Shirt</h3>
    <p>Price: ₹799</p>
    <button onclick="addToCart('Shirt', 799)">
        Add to Cart
    </button>
</div>

<div class="product">
    <img src="https://placehold.co/200x180?text=Jeans">
    <h3>Jeans</h3>
    <p>Price: ₹999</p>
    <button onclick="addToCart('Jeans', 999)">
        Add to Cart
    </button>
</div>

<div id="cart">
    <h2>My Shopping Cart 🛒</h2>
    <div id="items">No items added</div>
    <h3>Total: ₹<span id="total">0</span></h3>
</div>

<script>
    let total = 0;

    function addToCart(name, price) {
        if (total === 0) {
            document.getElementById("items").innerHTML = "";
        }

        document.getElementById("items").innerHTML +=
            "<p>" + name + " - ₹" + price + "</p>";

        total += price;

        document.getElementById("total").innerText = total;
    }
</script>

</body>
</html>
