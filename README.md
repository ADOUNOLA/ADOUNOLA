- 👋<!DOCTYPE html><html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ADOUNOLA Store</title>
  <style>
    /* Styles identiques au code précédent */
    /* ... (inchangé pour la lisibilité ici) ... */
    #cart button {
      margin-top: 1rem;
      width: 100%;
    }
  </style>
</head>
<body>
  <!-- Code HTML identique -->  <div id="cart">
    <h3>Votre panier</h3>
    <ul id="cartItems"></ul>
    <p><strong>Total : </strong><span id="cartTotal">0</span>€</p>
    <button onclick="toggleCart()">Fermer</button>
    <button onclick="checkout()">Payer maintenant</button>
  </div>  <footer>
    <p>&copy; 2025 ADOUNOLA Store. Tous droits réservés.</p>
  </footer>  <script>
    let cart = [];

    function addToCart(product, price) {
      cart.push({ product, price });
      updateCartDisplay();
      alert(product + ' a été ajouté au panier.');
    }

    function updateCartDisplay() {
      const cartItems = document.getElementById("cartItems");
      const cartTotal = document.getElementById("cartTotal");
      const cartCount = document.getElementById("cartCount");

      cartItems.innerHTML = "";
      let total = 0;
      cart.forEach(item => {
        const li = document.createElement("li");
        li.textContent = `${item.product} - ${item.price}€`;
        cartItems.appendChild(li);
        total += item.price;
      });

      cartTotal.textContent = total.toFixed(2);
      cartCount.textContent = cart.length;
    }

    function toggleCart() {
      const cartBox = document.getElementById("cart");
      cartBox.style.display = cartBox.style.display === "block" ? "none" : "block";
    }

    function checkout() {
      if (cart.length === 0) {
        alert("Votre panier est vide.");
        return;
      }
      const total = cart.reduce((sum, item) => sum + item.price, 0);
      alert(`Montant total à payer : ${total.toFixed(2)}€\n(Nous intégrerons bientôt un vrai système de paiement)`);
    }
  </script></body>
</html> Hi, I’m @ADOUNOLA
 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
ADOUNOLA/ADOUNOLA is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
