<template>
  <div class="opportunities">
    <div id="mobile-id" class="container wide lighttan">
      <div
        class="investors image-left columns five"
        style="background-image: url ('../img/ttt.jpg')"
      ></div>
      <div class="nine columns panel-content">
        <h3 class="sans-serif">{{ $t("am1") }}</h3>
        <p class="custom-margin">{{ $t("am2") }}</p>
        <ul class="ul-two">
          <li>{{ $t("am3") }}</li>
          <li>{{ $t("am4") }}</li>
          <li>{{ $t("am5") }}</li>
          <li>{{ $t("am6") }}</li>
        </ul>
        <p class="custom-margin">
          {{ $t("am7") }}
        </p>
      </div>
    </div>
    <div id="mobile-id" class="container wide tan">
      <div
        class="startups image-left columns five"
        style="background-image: ('../img/ui.jpg')"
      ></div>
      <div class="nine columns panel-content">
        <h3 class="sans-serif">{{ $t("am8") }}</h3>
        <p>
          {{ $t("am9") }}
        </p>
        <br />
        <h3 class="sans-serif">{{ $t("am10") }}</h3>
        <br />
        <h3 class="sans-serif">{{ $t("am11") }}</h3>
      </div>
    </div>
    <div id="mobile-id" class="container wide lighttan">
      <div
        class="thirdparties image-left columns five"
        style="background-image: ('../img/ttt.jpg')"
      ></div>
      <div class="nine columns panel-content">
        <h3 class="sans-serif">{{ $t("am12") }}</h3>
        <br />
        <h3 class="sans-serif">{{ $t("am13") }}</h3>
        <ul class="ul-two">
          <li>{{ $t("am15") }}</li>
          <li>{{ $t("am16") }}</li>
          <li>{{ $t("am17") }}</li>
          <li>{{ $t("am18") }}</li>
          <li>{{ $t("am19") }}</li>
          <li>{{ $t("am20") }}</li>
        </ul>
      </div>
    </div>
    <div id="mobile-id" class="container wide lighttan">
      <div
        class="celik image-left columns five"
        style="background-image: ('../img/ttt.jpg')"
      ></div>
      <div class="nine columns panel-content">
        <h3 class="sans-serif">{{ $t("am21") }}</h3>
        <ul class="ul-one">
          <li>{{ $t("am22") }}</li>
          <li>{{ $t("am23") }}</li>
        </ul>
        <br />
        <h3 class="sans-serif">{{ $t("am24") }}</h3>
      </div>
    </div>
  </div>
</template>

<style>
@media only screen and (max-width: 720px) {
  #mobile-id {
    width: 100vw !important;
  }
}
</style>
