<!-- Please remove this file from your project -->
<template>
  <header
    id="masthead"
    class="site-header"
    role="banner"
    style="font-size: 10px"
  >
    <div class="bg-image"></div>
    <div class="nav-placeholder" style="height: 91.1094px"></div>
    <div class="nav-wrap">
      <div class="container">
        <nav
          id="site-navigation"
          class="main-navigation twelve columns"
          role="navigation"
        >
          <a href="/" class="logo sans-serif"
            ><img src="../img/logo.png" style="max-width: 100px" id="logo-ink"
          /></a>
          <h1 class="menu-toggle"><i class="icon-align-justify"></i></h1>
          <div class="screen-reader-text skip-link">
            <a href="#content" title="Skip to content">Skip to content</a>
          </div>
          <div class="menu-menu-1-container">
            <ul id="menu-menu-1" class="menu nav-menu">
              <li
                id="menu-item-23"
                class="menu-item menu-item-type-custom menu-item-object-custom menu-item-home menu-item-23"
              >
                <nuxt-link :to="localePath('/')">{{ $t("home") }}</nuxt-link>
              </li>
              <li
                id="menu-item-26"
                class="menu-item menu-item-type-post_type menu-item-object-page menu-item-26"
              >
                <nuxt-link :to="localePath('/activities')">{{
                  $t("active")
                }}</nuxt-link>
              </li>
              <li
                id="menu-item-27"
                class="menu-item menu-item-type-post_type menu-item-object-page menu-item-27"
              >
                <nuxt-link :to="localePath('/contact')">{{
                  $t("contact")
                }}</nuxt-link>
              </li>
              <li
                id="menu-item-25"
                class="nav-contact menu-item menu-item-type-post_type menu-item-object-page menu-item-25"
              >
                <a
                  href="mailto:
          inkonong@inkoning.hr"
                  >{{ $t("contactus") }}</a
                >
              </li>
              <li
                id="menu-item-23"
                class="menu-item menu-item-type-post_type menu-item-object-page menu-item-23"
              >
                <nuxt-link :to="switchLocalePath('en')">EN</nuxt-link>
              </li>
              <li
                id="menu-item-23"
                class="menu-item menu-item-type-post_type menu-item-object-page menu-item-23"
              >
                <nuxt-link :to="switchLocalePath('hr')">HR</nuxt-link>
              </li>
            </ul>
          </div>
        </nav>
        <!-- #site-navigation -->
      </div>
    </div>

    <div id="mobile-id" class="container wide">
      <div class="row page-title">
        <h1>{{ pageName }}</h1>
      </div>
    </div>
  </header>
</template>

<script>
import Vue from "vue";
import VueI18n from "vue-i18n";

export default {
  name: "Header",
  data() {
    return {
      pageName: "Home",
    };
  },
  watch: {
    $route(to, from) {
      console.log(this.$route.path);
      if (this.$route.path == "/") {
        this.pageName = this.$t("about");
      }
      if (this.$route.path == "/hr") {
        this.pageName = this.$t("about");
      }
      if (this.$route.path.includes("/about-us"))
        this.pageName = this.$t("about");
      if (this.$route.path.includes("/activities"))
        this.pageName = this.$t("activities");
      if (this.$route.path.includes("/contact"))
        this.pageName = this.$t("contact");
    },
  },
  mounted() {
    this.toggle();
    if (this.$route.path == "/") {
      this.pageName = this.$t("about");
    }
    if (this.$route.path == "/hr") {
      this.pageName = this.$t("about");
    }
    if (this.$route.path.includes("/about-us"))
      this.pageName = this.$t("about");
    if (this.$route.path.includes("/activities"))
      this.pageName = this.$t("activities");
    if (this.$route.path.includes("/contact"))
      this.pageName = this.$t("contact");
  },
  methods: {
    toggle() {
      (function () {
        var container, button, menu, bd;

        container = document.getElementById("site-navigation");
        bd = document.getElementsByTagName("body")[0];
        if (!container) return;

        button = container.getElementsByTagName("h1")[0];
        if ("undefined" === typeof button) return;

        menu = container.getElementsByTagName("ul")[0];

        // Hide menu toggle button if menu is empty and return early.
        if ("undefined" === typeof menu) {
          button.style.display = "none";
          return;
        }

        if (-1 === menu.className.indexOf("nav-menu"))
          menu.className += " nav-menu";

        button.onclick = function () {
          if (-1 !== container.className.indexOf("toggled")) {
            container.className = container.className.replace(" toggled", "");
            bd.className = bd.className.replace(" show-mnav", "");
          } else {
            container.className += " toggled";
            bd.className += " show-mnav";
          }
        };
      })();
    },
  },
};
</script>

<style>
@media only screen and (max-width: 720px) {
  #mobile-id {
    width: 100vw !important;
  }

  h1 {
    font-size: 70px !important;
  }

  h3 {
    font-size: 20px;
  }

  .page-title {
    max-width: 100vw !important;
  }

  .panel-content {
    padding: 0 5%;
  }

  .opportunities .image-left {
    width: 100% !important;
  }

  .opportunities .image-left {
    margin-left: 0px !important;
  }

  #logo-ink {
    max-width: 60px !important;
  }
}
</style>
