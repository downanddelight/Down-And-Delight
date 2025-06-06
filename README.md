<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Dawn & Delight</title>
  <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-yellow-50 font-sans">

  <!-- Header Section with Logo -->
  <section class="text-center p-6">
    <div class="flex flex-col items-center justify-center">
      <img src="images.jpeg" alt="Dawn & Delight Logo" class="w-24 h-24 rounded-full shadow-md mb-2" />
      <h1 class="text-5xl font-bold text-yellow-800">☀️ Dawn & Delight</h1>
      <p class="text-lg text-yellow-600 italic">A joyful start to your day</p>
    </div>
  </section>

  <!-- Product Section -->
  <section class="text-center p-10">
    <img src="delight.jpeg" alt="Premium Breakfast Box" class="mx-auto rounded-lg shadow-md w-60" />
    <p class="mt-4 text-xl text-gray-700 font-semibold">Premium Breakfast Box – Rs. 799</p>
    <button onclick="showLocationForm()" class="mt-6 px-6 py-2 bg-yellow-500 text-white rounded-full hover:bg-yellow-600">
      Order Now
    </button>
  </section>

  <!-- Delivery Location Form (Hidden at first) -->
  <section id="locationForm" class="hidden text-center p-6 bg-white mx-10 rounded-xl shadow-md">
    <h2 class="text-2xl text-yellow-700 mb-4">📍 Where should we deliver your breakfast?</h2>
    <input type="text" id="address" placeholder="Enter your full delivery address" class="w-full px-4 py-2 border rounded mb-4" />
    <button onclick="showPaymentSection()" class="bg-yellow-400 text-white px-4 py-2 rounded hover:bg-yellow-500">Continue to Payment</button>
  </section>

  <!-- Payment Section (Hidden at first) -->
  <section id="paymentSection" class="hidden text-center p-6 bg-white mx-10 mt-4 rounded-xl shadow-md">
    <h2 class="text-2xl text-yellow-700 mb-4">💳 Payment</h2>
    <p class="mb-4">Coming Soon... We accept Khalti, eSewa, and Cash on Delivery</p>
    <button class="bg-green-500 text-white px-4 py-2 rounded hover:bg-green-600">Place Order</button>
  </section>

  <script>
    function showLocationForm() {
      document.getElementById('locationForm').classList.remove('hidden');
    }

    function showPaymentSection() {
      const address = document.getElementById('address').value;
      if (address.trim() === "") {
        alert("Please enter your delivery address.");
        return;
      }
      document.getElementById('paymentSection').classList.remove('hidden');
    }
  </script>
</body>
</html>
