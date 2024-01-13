<template>
  <main class="container">
    <section class="menu-section">
      <h2>Menu</h2>
      <div class="menu-items">
        <div v-for="(item, index) in items" :key="index">
          <div class="item-card">
            <p class="item-name">{{ item.name }}</p>
            <p class="item-price">{{ item.price }}</p>
            <p class="item-description">{{ item.description }}</p>
            <button @click="addToCart(item)">Add to Cart</button>
          </div>
        </div>
      </div>
    </section>

    <section class="specials-section">
      <h2>Specials</h2>
      <div class="specials-items">
        <div v-for="(special, index) in specials" :key="index">
          <div class="special-card">
            <p class="special-name">{{ special.name }}</p>
            <p class="special-price">{{ special.price }}</p>
            <p class="special-description">{{ special.description }}</p>
            <button @click="addToCart(special)">Add to Cart</button>
          </div>
        </div>
      </div>
    </section>

    <!-- Cart Sidebar -->
    <aside class="cart-sidebar">
      <h2>Cart</h2>
      <div class="cart-items">
        <div v-for="(cartItem, index) in cart" :key="index">
          <p>{{ cartItem.name }} - ${{ cartItem.price }}</p>
        </div>
      </div>

      <div class="checkout-section">
        <p class="total">Total: ${{ calculateTotal() }}</p>
        <button @click="checkout">Checkout</button>
      </div>
    </aside>
  </main>
</template>

<script setup>
import { ref, onMounted } from 'vue';

const items = ref([]);
const specials = ref([]);
const cart = ref([]);

const getAllItems = async () => {
  try {
    const response = await fetch('menu.json');
    items.value = await response.json();
  } catch (error) {
    console.error('Error fetching items:', error);
  }
};

const getAllSpecials = async () => {
  try {
    const response = await fetch('specials.json');
    specials.value = await response.json();
  } catch (error) {
    console.error('Error fetching specials:', error);
  }
};

const addToCart = (item) => {
  const parsedPrice = parseFloat(item.price);
  if (!isNaN(parsedPrice)) {
    cart.value.push({ ...item, price: parsedPrice });
  } else {
    console.error(`Invalid price for item: ${item.name}`);
  }
};

const calculateTotal = () => {
  return cart.value.reduce((total, item) => total + parseFloat(item.price), 0).toFixed(2);
};

const checkout = async () => {
  try {
    const response = await confirmCheckout();
    if (response.success) {
      alert(`Checkout successful! Total amount: $${calculateTotal()}`);
      cart.value = [];
    } else {
      alert(`Checkout failed. Please try again.`);
    }
  } catch (error) {
    console.error('Error during checkout:', error);
    alert(`An error occurred during checkout. Please try again.`);
  }
};

const confirmCheckout = () => {
  return new Promise((resolve) => {
    setTimeout(() => {
      resolve({ success: true });
      // Simulated error response
      // resolve({ success: false, error: 'Payment processing failed.' });
    }, 1000);
  });
};

onMounted(() => {
  getAllItems();
  getAllSpecials();
});
</script>

<style scoped>
.container {
  display: flex;
  justify-content: space-between;
  padding: 20px;
}

.menu-section,
.specials-section {
  flex: 1;
  margin-right: 20px;
}

.menu-items,
.specials-items {
  display: flex;
  flex-wrap: wrap;
}

.item-card,
.special-card {
  margin: 10px;
  padding: 15px;
  border: 1px solid #ddd;
  border-radius: 8px;
  text-align: center;
}

.item-name,
.special-name {
  font-size: 1.2rem;
  font-weight: bold;
}

.item-price,
.special-price {
  color: var(--red);
  font-size: 1.1rem;
}

.item-description,
.special-description {
  margin-top: 0.5rem;
  font-size: 1rem;
}

button {
  margin-top: 1rem;
  background-color: var(--red);
  color: white;
  padding: 0.5rem 1rem;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

.cart-sidebar {
  width: 300px;
  padding: 20px;
  background-color: #f8f8f8;
  border: 1px solid #ddd;
  border-radius: 8px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.cart-sidebar h2 {
  color: var(--red);
  font-size: 1.5rem;
  margin-bottom: 10px;
}

.cart-items {
  display: flex;
  flex-direction: column;
}

.cart-items div {
  margin: 10px 0;
}

.total {
  margin-top: 1rem;
  font-weight: 600;
}
</style>
