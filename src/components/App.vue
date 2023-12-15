<template>
  <navbar :pages="pages" :active-page="activePage" :nav-link-click="(index) => activePage = index"></navbar>
  <page-viewer :page="pages[activePage]"></page-viewer>
</template>

<script>
import Navbar from './Navbar.vue';
import PageViewer from './PageViewer.vue'


export default {
  components: {
    Navbar,
    PageViewer
  },

  data() {
    return {
      activePage: 0,
      pages: [
        { name: "Home", url: "index.html", content: "Hello guys this is Home" },
        { name: "Menu", url: "menu.html", content: "Hello guys this is Menu" },
        {
          name: "Projects", url: "project.html", content: "Hello guys this is Projects",
        },
      ],
    };
  },

};
</script>
