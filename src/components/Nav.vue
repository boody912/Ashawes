<template>
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
      <div class="container">
        <router-link class="navbar-brand" to="/">
          Ashawes
        </router-link>
        <button class="navbar-toggler" type="button" @click="toggleNavbar">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" :class="{ show: !isCollapsed }">
          <ul class="navbar-nav ml-auto">
            <li class="nav-item" v-for="link in links" :key="link.path">
              <router-link class="nav-link" :to="link.path" @click="toggleNavbar">
                {{ link.label }}
              </router-link>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </template>
  

<!-- jQery -->
<script>
import { onMounted } from 'vue'

export default {
    data() {
    return {
      isCollapsed: true,
      links: [
        { path: "/", label: "Home" },
        { path: "/menu", label: "Menu" },
        { path: "/about", label: "About" },
        { path: "/book", label: "Book Table" },
      ],
    };
  },
  methods: {
    toggleNavbar() {
      this.isCollapsed = !this.isCollapsed;
    },
  },
    
}
</script>


