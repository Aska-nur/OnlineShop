<script setup>
const navItems = [
  { path: '/', name: 'Landing' },
  { path: '/product', name: 'Product' },
  { path: '/about', name: 'About' },
  { path: '/contact', name: 'Contact' },
]
</script>

<template>
  <nav class="navbar">
    <div class="brand">SMK Yadika Soreang - Onlineshop</div>

    <div class="nav-links">
      <RouterLink
        v-for="item in navItems"
        :key="item.path"
        :to="item.path"
        class="nav-link"
      >
        {{ item.name }}
      </RouterLink>
    </div>
  </nav>
</template>

<style scoped>
.navbar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 1rem;
  background: linear-gradient(135deg, #ffffff, #edf5ff);
  padding: 1rem 2rem;
  border-bottom: 1px solid #dfeaf9;
  box-shadow: 0 6px 20px rgba(15, 23, 42, 0.08);
}

.brand {
  margin: 0;
  font-size: 1.2rem;
  font-weight: 700;
  color: #224c8d;
}

.nav-links {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  flex-wrap: wrap;
}

.nav-link {
  text-decoration: none;
  color: #374151;
  font-weight: 600;
  padding: 0.65rem 1rem;
  border-radius: 0.75rem;
  transition: all 0.2s ease;
}

.nav-link:hover {
  background: #eff6ff;
  color: #1d4ed8;
}

.nav-link.router-link-active,
.nav-link.router-link-exact-active {
  background: linear-gradient(135deg, #2563eb, #3b82f6);
  color: #ffffff;
  box-shadow: 0 8px 16px rgba(37, 99, 235, 0.2);
}

@media (max-width: 640px) {
  .navbar {
    flex-direction: column;
    align-items: flex-start;
    padding: 1rem;
  }

  .nav-links {
    width: 100%;
  }

  .nav-link {
    flex: 1 1 auto;
    text-align: center;
  }
}
</style>