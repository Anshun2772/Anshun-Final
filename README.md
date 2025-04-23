<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Ashirwad Super Market</title>
  <style>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #fdf6e3;
      color: #333;
    }
    header {
      background-color: #f4d03f;
      color: #000;
      padding: 20px 0;
      text-align: center;
      box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    }
    nav a {
      margin: 0 15px;
      color: #000;
      text-decoration: none;
      font-weight: bold;
    }
    section {
      padding: 40px 20px;
      max-width: 1000px;
      margin: auto;
    }
    .hero {
      text-align: center;
      padding: 60px 20px;
      background: linear-gradient(to right, #fff8dc, #fff3b0);
      border-radius: 12px;
      box-shadow: 0 6px 12px rgba(0,0,0,0.1);
    }
    .hero h1 {
      font-size: 2.8em;
      margin-bottom: 10px;
    }
    .products, .contact, .order-form {
      background-color: #ffffff;
      margin: 20px 0;
      padding: 30px;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.05);
    }
    .product-list {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
    }
    .product-item {
      background-color: #fdf1c8;
      padding: 15px;
      border-radius: 10px;
      box-shadow: 0 2px 6px rgba(0,0,0,0.05);
      transition: transform 0.2s;
    }
    .product-item:hover {
      transform: scale(1.03);
    }
    form {
      display: flex;
      flex-direction: column;
    }
    input, textarea, select {
      padding: 10px;
      margin: 10px 0;
      border: 1px solid #ccc;
      border-radius: 6px;
    }
    button {
      background-color: #f4d03f;
      border: none;
      padding: 12px;
      border-radius: 6px;
      font-weight: bold;
      cursor: pointer;
    }
    button:hover {
      background-color: #e2bd2a;
    }
    footer {
      text-align: center;
      padding: 20px;
      background-color: #f4d03f;
      color: #000;
      position: relative;
    }
    #backToTopBtn {
      display: none;
      position: fixed;
      bottom: 30px;
      right: 30px;
      z-index: 100;
      background-color: #f4d03f;
      color: #000;
      padding: 12px 16px;
      border: none;
      border-radius: 8px;
      font-size: 16px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <header>
    <h1>Ashirwad Super Market</h1>
    <nav>
      <a href="#products">Products</a>
      <a href="#order">Order</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <section class="hero">
    <h1>Welcome to Ashirwad Super Market</h1>
    <p>Your neighborhood’s go-to place for everyday essentials.</p>
  </section>

  <section id="products" class="products">
    <h2>Our Product Categories</h2>
    <div class="product-list">
      <div class="product-item">
        <h3>Fruits & Vegetables</h3>
        <p>Fresh produce sourced daily from local farmers.</p>
      </div>
      <div class="product-item">
        <h3>Dairy & Bakery</h3>
        <p>Fresh milk, paneer, bread, and snacks made with care.</p>
      </div>
      <div class="product-item">
        <h3>Snacks & Beverages</h3>
        <p>Your favorite chips, biscuits, and drinks in one place.</p>
      </div>
    </div>
  </section>

  <section id="order" class="order-form">
    <h2>Place Your Order</h2>
    <form onsubmit="submitOrder(event)">
      <input type="text" placeholder="Your Name" required />
      <input type="text" placeholder="Product Needed" required />
      <textarea placeholder="Address" required></textarea>
      <button type="submit">Submit Order</button>
    </form>
  </section>

  <section id="contact" class="contact">
    <h2>Supplier Inquiry</h2>
    <form onsubmit="submitContact(event)">
      <input type="text" placeholder="Company Name" required />
      <input type="text" placeholder="Contact Number" required />
      <textarea placeholder="Message" required></textarea>
      <button type="submit">Send Inquiry</button>
    </form>
  </section>

  <footer>
    <p>&copy; <span id="year"></span> Ashirwad Super Market</p>
  </footer>

  <button onclick="topFunction()" id="backToTopBtn" title="Go to top">Top</button>

  <script>
    function submitOrder(e) {
      e.preventDefault();
      alert('Order submitted! Thank you.');
    }

    function submitContact(e) {
      e.preventDefault();
      alert('Inquiry sent! We will contact you soon.');
    }

    const topButton = document.getElementById('backToTopBtn');

    window.onscroll = function() {
      topButton.style.display = (document.body.scrollTop > 200 || document.documentElement.scrollTop > 200) ? 'block' : 'none';
    };

    function topFunction() {
      document.body.scrollTop = 0;
      document.documentElement.scrollTop = 0;
    }

    document.getElementById("year").innerText = new Date().getFullYear();
  </script>
</body>
</html>
