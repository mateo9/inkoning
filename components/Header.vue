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
                <a href="http://chattanoogarenaissancefund.com/">Home</a>
              </li>
              <li
                id="menu-item-24"
                class="menu-item menu-item-type-post_type menu-item-object-page menu-item-24"
              >
                <a href="https://chattanoogarenaissancefund.com/about-us/"
                  >About Us</a
                >
              </li>
              <li
                id="menu-item-26"
                class="menu-item menu-item-type-post_type menu-item-object-page menu-item-26"
              >
                <a href="https://chattanoogarenaissancefund.com/investments/"
                  >Investments</a
                >
              </li>
              <li
                id="menu-item-27"
                class="menu-item menu-item-type-post_type menu-item-object-page menu-item-27"
              >
                <a href="https://chattanoogarenaissancefund.com/opportunities/"
                  >Opportunities</a
                >
              </li>
              <li
                id="menu-item-233"
                class="menu-item menu-item-type-post_type menu-item-object-page menu-item-233"
              >
                <a href="https://chattanoogarenaissancefund.com/blog/">News</a>
              </li>
              <li
                id="menu-item-25"
                class="nav-contact menu-item menu-item-type-post_type menu-item-object-page menu-item-25"
              >
                <a href="https://chattanoogarenaissancefund.com/contact-us/"
                  >Contact Us</a
                >
              </li>
            </ul>
          </div>
        </nav>
        <!-- #site-navigation -->
      </div>
    </div>

    <div class="container wide">
      <div class="row page-title">
        <h1>{{ pageName }}</h1>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      pageName: "Home",
    };
  },
  mounted() {
    if (this.$route.path == "/about-us") {
      this.pageName = "About Us";
    }
  },
};
</script>
