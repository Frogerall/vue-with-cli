<template>
  <div>
    <header :class="navbarClass">
      <div class="nav-logo">Nav Logo</div>
      <div class="nav-menu">Menu</div>
      <nav>
        <ul>
          <li v-for="(page, index) in pages" :key="index" class="nav-item">

            <a class="nav-link" :class="{ active: activePage == index }"
              :title="'This link goes to this page: ' + page.name" @click.prevent="activePage = index">{{ page.name }}
            </a>

          </li>
          <button @click.prevent="toggleDarkMode = !toggleDarkMode">Theme</button>
        </ul>

      </nav>
    </header>
  </div>
</template>
<script>
export default {
  props: ['pages', 'activePage', 'navLinkClick'],
  data() {
    return {
      toggleDarkMode: false,
    }
  },
  computed: {
    navbarClass() {
      return {
        darkmode: this.toggleDarkMode,
      };
    },
  },
}
</script>

<style lang="">
  
</style>