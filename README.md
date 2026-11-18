# online-food-ordering-system-
The Online Food Ordering System is a web-based application that allows customers to browse food items, view prices, add items to their cart, and place orders online. It provides user management, food management, order tracking, and payment facilities, making food ordering simple, fast, and convenient.
he Online Food Ordering System is a web-based application designed to make food ordering easier, faster, and more convenient for customers. This system allows users to browse restaurants, explore different food items, view prices, and place orders online without visiting the restaurant physically.

The main objective of this project is to provide a user-friendly platform that connects customers and restaurants through an online system. Users can register and log in to their accounts, view available food categories, search for their favourite dishes, add items to the shopping cart, and place orders according to their preferences. The system also provides details such as food descriptions, prices, quantities, and order summaries.

The application consists of different modules, including User Management, Restaurant Management, Food Management, Cart Management, Order Management, Payment Management, and Admin Management. The administrator has the authority to manage users, restaurants, food items, prices, and customer orders. Customers can track their order status and view their previous orders.

The system helps restaurants manage incoming orders efficiently, reduce manual work, and improve customer service. It also saves customers time and provides the convenience of ordering food from anywhere using a computer or smartphone.

This project can be developed using technologies such as HTML, CSS, JavaScript, PHP, Python, Java, and MySQL for database management. The choice of technologies depends on the project requirements and development approach.

In conclusion, the Online Food Ordering System is a useful application that simplifies the food ordering process by providing a digital platform for customers and restaurants. It improves efficiency, reduces paperwork, saves time, and offers a convenient way to order food online. This project demonstrates how technology can be used to improve traditional food ordering services.

<!DOCTYPE html>
<html>
<head>
    <title>Online Food Ordering System</title>
    <style>
        body {
            font-family: Arial;
            background: #f5f5f5;
            text-align: center;
        }
        h1 {
            background: orange;
            color: white;
            padding: 20px;
        }
        .food {
            display: inline-block;
            background: white;
            padding: 20px;
            margin: 15px;
            width: 200px;
            border-radius: 10px;
        }
        button {
            background: orange;
            color: white;
            border: none;
            padding: 10px;
            cursor: pointer;
        }
    </style>
</head>
<body>

<h1>Online Food Ordering System</h1>

<h2>Our Food Menu</h2>

<div class="food">
    <h3>Pizza</h3>
    <p>Price: ₹150</p>
    <button onclick="addToCart('Pizza',150)">Add to Cart</button>
</div>

<div class="food">
    <h3>Burger</h3>
    <p>Price: ₹100</p>
    <button onclick="addToCart('Burger',100)">Add to Cart</button>
</div>

<div class="food">
    <h3>Dosa</h3>
    <p>Price: ₹60</p>
    <button onclick="addToCart('Dosa',60)">Add to Cart</button>
</div>

<h2>Shopping Cart</h2>

<ul id="cart"></ul>

<h3>Total: ₹<span id="total">0</span></h3>

<button onclick="placeOrder()">Place Order</button>

<script>
let total = 0;

function addToCart(name, price) {
    let item = document.createElement("li");
    item.innerHTML = name + " - ₹" + price;
    document.getElementById("cart").appendChild(item);

    total += price;
    document.getElementById("total").innerText = total;
}

function placeOrder() {
    if (total === 0) {
        alert("Please add food items first!");
    } else {
        alert("Your order has been placed successfully!");
        document.getElementById("cart").innerHTML = "";
        total = 0;
        document.getElementById("total").innerText = total;
    }
}
</script>

</body>
</html>
