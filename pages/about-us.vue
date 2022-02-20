<template>
  <div class="panel panel-1 tan margin-top-au">
    <div class="container">
      <div class="historical-context content-right">
        <p class="mobile-p">
          {{ $t("au1") }}
        </p>
        <p class="mobile-p">
          {{ $t("au2") }}
        </p>

        <p class="mobile-p">
          {{ $t("au3") }}
        </p>
        <p class="mobile-p">
          {{ $t("au4") }}
        </p>
      </div>
    </div>
  </div>
</template>

<style>
@media only screen and (max-width: 720px) {
  .margin-top-au {
    margin-top: 40px;
  }

  .mobile-p {
    font-size: 16px;
  }
}
</style>
