# benstrendthrift<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Benstrend Thrift</title>

  <!-- Google Tag Manager -->
  <script async src="https://www.googletagmanager.com/gtm.js?id=GTM-XXXXXXX"></script>
  <!-- End Google Tag Manager -->

  <link rel="stylesheet" href="styles.css" />
  <style>
    body { font-family: Arial, sans-serif; background: #f5f5f5; margin: 0; padding: 0; text-align: center; }
    header { background: #333; color: #fff; padding: 20px 0; font-size: 28px; font-weight: bold; }
    .container { padding: 20px; }
    .product-grid { display: flex; flex-wrap: wrap; justify-content: center; gap: 20px; margin-top: 30px; }
    .product { background: #fff; padding: 15px; border-radius: 10px; width: 250px; box-shadow: 0 0 10px rgba(0,0,0,0.1); }
    .product img { width: 100%; border-radius: 5px; }
    .product h3 { margin: 10px 0; font-size: 20px; }
    .quantity { margin: 10px 0; }
    .contact { margin-top: 40px; padding: 20px; background: #fff; display: inline-block; box-shadow: 0 0 10px rgba(0,0,0,0.1); border-radius: 10px; }
    footer { margin-top: 40px; font-size: 14px; color: #888; }
  </style>
</head>
<body>
  <!-- Google Tag Manager (noscript) -->
  <noscript><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-XXXXXXX"
  height="0" width="0" style="display:none;visibility:hidden"></iframe></noscript>
  <!-- End Google Tag Manager (noscript) -->

  <header>Benstrend Thrift</header>
  <div class="container">
    <h2>Shop Our Trending Products</h2>
    <div class="product-grid">
      <div class="product">
        <img src="images/denim.jpg" alt="Denim Shirt">
        <h3>Denim Shirt</h3>
        <div class="quantity">
          Quantity: <input type="number" min="1" value="1">
        </div>
      </div>
      <div class="product">
        <img src="images/nakedwolfe.jpg" alt="Naked Wolfe">
        <h3>Naked Wolfe</h3>
        <div class="quantity">
          Quantity: <input type="number" min="1" value="1">
        </div>
      </div>
      <div class="product">
        <img src="images/nike.jpg" alt="Nike">
        <h3>Nike</h3>
        <div class="quantity">
          Quantity: <input type="number" min="1" value="1">
        </div>
      </div>
      <div class="product">
        <img src="images/adidas.jpg" alt="Adidas">
        <h3>Adidas</h3>
        <div class="quantity">
          Quantity: <input type="number" min="1" value="1">
        </div>
      </div>
      <div class="product">
        <img src="images/jordan.jpg" alt="Jordan">
        <h3>Jordan</h3>
        <div class="quantity">
          Quantity: <input type="number" min="1" value="1">
        </div>
      </div>
    </div>

    <div class="contact">
      <h2>Contact Info</h2>
      <p>Phone: 0792218893</p>
      <p>Till Number: 55555000</p>
      <p id="ip-address">Server IP Address: Loading...</p>
      <p id="location">Location: Loading...</p>
    </div>
  </div>

  <footer>
    &copy; 2025 Benstrend Thrift. All rights reserved.
  </footer>

  <script>
    fetch('https://api.ipify.org?format=json')
      .then(res => res.json())
      .then(data => {
        document.getElementById('ip-address').textContent = 'Server IP Address: ' + data.ip;
      });

    fetch('https://ipapi.co/json/')
      .then(res => res.json())
      .then(data => {
        document.getElementById('location').textContent = 'Location: ' + data.city + ', ' + data.country_name;
      });
  </script>
</body>
</html>

