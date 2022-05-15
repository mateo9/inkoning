<template>
  <div class="panel panel-1 tan contact-container">
    <div class="flex">
      <div class="contact-us-img">
        <img src="../img/contact.jpg" class="contact-us" />
      </div>
      <div
        class="historical-context content-right no-padding flex margin-top margin-left"
      >
        <div class="flex-container">
          <p class="bold">INKONING d.o.o.</p>
          <p>Sv. Mateja 10010 Zagreb</p>
          <p>{{ $t("c1") }}</p>
          <p>{{ $t("mob") }}</p>
          <p>www.inkoning.hr</p>
        </div>
        <div class="flex-container">
          <p>OIB: 16571604360</p>
          <p>IBAN: HR8524020061101001363</p>
          <div class="mail">
            <a
              href="mailto:
          inkonong@inkoning.hr"
              >inkonong@inkoning.hr</a
            >
          </div>
          <div class="mail">
            <a href="mailto: nikola.sulic@inkoning.hr"
              >nikola.sulic@inkoning.hr</a
            >
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style>
.contact-container {
  padding-top: 0 !important;
}
.flex {
  display: flex !important;
}

.no-padding {
  padding-left: 0;
}
.contact-us-img > .contact-us {
  max-width: 20vw;
  height: auto;
}

.flex-container {
  width: 20vw;
}

.margin-top {
  margin-top: 40px;
}

.margin-left {
  margin-left: 10%;
}

.bold {
  font-weight: bold !important;
}

.mail {
  margin-bottom: 10px !important;
}

@media only screen and (max-width: 720px) {
  #mobile-id {
    width: 100vw !important;
  }

  .flex-container {
    width: 30vw;
  }

  .margin-left {
    margin-left: 4%;
    margin-right: 4%;
  }

  .margin-top {
    margin-top: 20px;
  }

  .contact-us-img > .contact-us {
    max-width: 30vw !important;
  }
}
</style>
