<template>
  <div>
    <Header />
    <Nuxt />
  </div>
</template>

<style>
@font-face {
  font-family: "FontAwesome";
  font-style: normal;
  font-weight: normal;
  src: url("../fonts/AvenirNext.otf") format("otf");
}

.clip-group,
.options-icon,
a {
  cursor: pointer;
}

.loading,
.shortcut {
  font-variant: small-caps;
}

body,
html {
  margin: 0;
  padding: 0;
  height: 100%;
  font-size: 16px;
}

.copycat-container {
  position: relative;
  min-height: 100%;
}

.footer,
.trans-overlay {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
}

.copycat-contents {
  padding-bottom: 22px;
}

.nav-header {
  clear: both;
  padding: 10px 0;
}

.archive-count,
.clip-count {
  padding-left: 4px;
}

.nav-header h4 {
  display: inline;
}

.nav-header .options {
  float: right;
  color: #000;
  text-decoration: none;
}

.footer {
  background: #ff8a00;
  height: 22px;
  color: #fff;
  text-align: center;
  font-size: 10px;
  padding-top: 3px;
}

.clip-count,
.clip-date,
.clip-show,
.options-note {
  font-size: x-small;
}

.clip-image {
  max-width: 438px;
}

.clip-group-expander {
  float: right;
  cursor: pointer;
}

.clip-group {
  display: block;
  margin: 10px 0;
  -webkit-user-select: none;
  user-select: none;
}

.clip-title {
  word-wrap: break-word;
}

.clip-count {
  color: gray;
}

.options-icon {
  float: right;
  top: -24px;
}

.options-note {
  font-style: italic;
  margin-left: 15px;
}

.table.shortcuts-table {
  margin-bottom: 0;
}

.archive-buttons {
  margin: 10px 0;
}

.trans-overlay {
  height: 40px;
  background: linear-gradient(rgba(255, 255, 255, 0), rgba(255, 255, 255, 1));
}

.clip-text-container {
  position: relative;
}

.selection-text {
  display: block;
  font-size: 12px;
  max-height: 100px;
  line-height: normal;
  overflow: hidden;
}

.selection-text-expanded {
  max-height: none;
}

.selection-text-control {
  width: 100%;
  display: block;
  text-align: center;
}

.copycat-logo {
  vertical-align: top;
}

.btn-copy {
  color: #fff;
  background-color: #ff8a00;
  border-color: #eea236;
}

.tutorial-page {
  text-align: center;
  padding: 0 1em;
}

.tutorial-page h4 {
  margin: 2em 0;
}

.tutorial-page p {
  margin-bottom: 3em;
}

.clip-search {
  margin: 20px 0;
}

.no-search-results {
  top: 300px;
  position: absolute;
  right: 200px;
  font-size: x-large;
  color: grey;
}

.fake-button {
  border: 1px solid #ccc;
  border-radius: 3px;
  cursor: auto;
  padding: 3px 5px;
  font-size: 12px;
  line-height: 1.5;
  color: #333;
  background-color: #fff;
}

.highlightedText {
  color: #ff8a00;
  font-weight: 700;
}

.dot-loading {
  display: inline-block;
}

.dot {
  background-color: #ccc;
  float: left;
  height: 4px;
  margin-left: 3px;
  width: 4px;
  opacity: 0.3;
  border-radius: 4px;
  -webkit-animation-name: bounce_dot;
  animation-name: bounce_dot;
  -webkit-animation-duration: 1.5s;
  animation-duration: 1.5s;
  -webkit-animation-iteration-count: infinite;
  animation-iteration-count: infinite;
  -webkit-animation-direction: linear;
  animation-direction: linear;
}

.dot_1 {
  -webkit-animation-delay: 0.3s;
  animation-delay: 0.3s;
}

.dot_2 {
  -webkit-animation-delay: 0.7s;
  animation-delay: 0.7s;
}

.dot_3 {
  -webkit-animation-delay: 0.9s;
  animation-delay: 0.9s;
}

@-webkit-keyframes bounce_dot {
  0%,
  100% {
    opacity: 0.3;
  }

  50% {
    opacity: 1;
    background-color: #111;
  }
}

@keyframes bounce_dot {
  0%,
  100% {
    opacity: 0.3;
  }

  50% {
    opacity: 1;
    background-color: #111;
  }
}

.loading {
  padding-top: 10px;
}

input[type="search"]::-webkit-search-cancel-button {
  -webkit-appearance: searchfield-cancel-button;
}

/*!
 * Bootstrap v3.3.5 (http://getbootstrap.com)
 * Copyright 2011-2015 Twitter, Inc.
 * Licensed under MIT (https://github.com/twbs/bootstrap/blob/master/LICENSE)
 */
/*! normalize.css v3.0.3 | MIT License | github.com/necolas/normalize.css */
.label,
sub,
sup {
  vertical-align: baseline;
}

.btn,
.btn-group,
.btn-group-vertical,
.caret,
.checkbox-inline,
.radio-inline,
img {
  vertical-align: middle;
}

hr,
img {
  border: 0;
}

body,
figure {
  margin: 0;
}

.navbar-fixed-bottom .navbar-collapse,
.navbar-fixed-top .navbar-collapse,
.pre-scrollable {
  max-height: 340px;
}

.btn-group > .btn-group,
.btn-toolbar .btn,
.btn-toolbar .btn-group,
.btn-toolbar .input-group,
.col-xs-1,
.col-xs-10,
.col-xs-11,
.col-xs-12,
.col-xs-2,
.col-xs-3,
.col-xs-4,
.col-xs-5,
.col-xs-6,
.col-xs-7,
.col-xs-8,
.col-xs-9,
.dropdown-menu {
  float: left;
}

html {
  font-family: sans-serif;
  -webkit-text-size-adjust: 100%;
  -ms-text-size-adjust: 100%;
  font-size: 10px;
  -webkit-tap-highlight-color: transparent;
}

article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
main,
menu,
nav,
section,
summary {
  display: block;
}

audio,
canvas,
progress,
video {
  display: inline-block;
  vertical-align: baseline;
}

audio:not([controls]) {
  display: none;
  height: 0;
}

[hidden],
template {
  display: none;
}

a {
  background-color: transparent;
}

a:active,
a:hover {
  outline: 0;
}

b,
optgroup,
strong {
  font-weight: 700;
}

dfn {
  font-style: italic;
}

h1 {
  margin: 0.67em 0;
}

mark {
  color: #000;
  background: #ff0;
}

sub,
sup {
  position: relative;
  font-size: 75%;
  line-height: 0;
}

sup {
  top: -0.5em;
}

sub {
  bottom: -0.25em;
}

svg:not(:root) {
  overflow: hidden;
}

hr {
  height: 0;
  -webkit-box-sizing: content-box;
  -moz-box-sizing: content-box;
  box-sizing: content-box;
}

*,
:after,
:before,
input[type="checkbox"],
input[type="radio"] {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
}

pre,
textarea {
  overflow: auto;
}

code,
kbd,
pre,
samp {
  font-size: 1em;
}

button,
input,
optgroup,
select,
textarea {
  margin: 0;
  font: inherit;
  color: inherit;
}

.glyphicon,
address {
  font-style: normal;
}

button {
  overflow: visible;
}

button,
select {
  text-transform: none;
}

button,
html input[type="button"],
input[type="reset"],
input[type="submit"] {
  -webkit-appearance: button;
  cursor: pointer;
}

button[disabled],
html input[disabled] {
  cursor: default;
}

button::-moz-focus-inner,
input::-moz-focus-inner {
  padding: 0;
  border: 0;
}

input[type="checkbox"],
input[type="radio"] {
  box-sizing: border-box;
  padding: 0;
}

input[type="number"]::-webkit-inner-spin-button,
input[type="number"]::-webkit-outer-spin-button {
  height: auto;
}

input[type="search"]::-webkit-search-cancel-button,
input[type="search"]::-webkit-search-decoration {
  -webkit-appearance: none;
}

table {
  border-spacing: 0;
  border-collapse: collapse;
}

td,
th {
  padding: 0;
}

/*! Source: https://github.com/h5bp/html5-boilerplate/blob/master/src/css/main.css */
@media print {
  blockquote,
  img,
  pre,
  tr {
    page-break-inside: avoid;
  }

  *,
  :after,
  :before {
    color: #000 !important;
    text-shadow: none !important;
    background: 0 0 !important;
    -webkit-box-shadow: none !important;
    box-shadow: none !important;
  }

  a,
  a:visited {
    text-decoration: underline;
  }

  a[href]:after {
    content: " (" attr(href) ")";
  }

  abbr[title]:after {
    content: " (" attr(title) ")";
  }

  a[href^="javascript:"]:after,
  a[href^="#"]:after {
    content: "";
  }

  blockquote,
  pre {
    border: 1px solid #999;
  }

  thead {
    display: table-header-group;
  }

  img {
    max-width: 100% !important;
  }

  h2,
  h3,
  p {
    orphans: 3;
    widows: 3;
  }

  h2,
  h3 {
    page-break-after: avoid;
  }

  .navbar {
    display: none;
  }

  .btn > .caret,
  .dropup > .btn > .caret {
    border-top-color: #000 !important;
  }

  .label {
    border: 1px solid #000;
  }

  .table {
    border-collapse: collapse !important;
  }

  .table td,
  .table th {
    background-color: #fff !important;
  }

  .table-bordered td,
  .table-bordered th {
    border: 1px solid #ddd !important;
  }
}

.dropdown-menu,
.modal-content {
  -webkit-background-clip: padding-box;
}

.btn,
.btn-danger.active,
.btn-danger:active,
.btn-default.active,
.btn-default:active,
.btn-info.active,
.btn-info:active,
.btn-primary.active,
.btn-primary:active,
.btn-warning.active,
.btn-warning:active,
.btn.active,
.btn:active,
.dropdown-menu > .disabled > a:focus,
.dropdown-menu > .disabled > a:hover,
.form-control,
.navbar-toggle,
.open > .dropdown-toggle.btn-danger,
.open > .dropdown-toggle.btn-default,
.open > .dropdown-toggle.btn-info,
.open > .dropdown-toggle.btn-primary,
.open > .dropdown-toggle.btn-warning {
  background-image: none;
}

.img-thumbnail,
body {
  background-color: #fff;
}

.glyphicon {
  position: relative;
  top: 1px;
  display: inline-block;
  font-weight: 400;
  line-height: 1;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.glyphicon-asterisk:before {
  content: "\2a";
}

.glyphicon-plus:before {
  content: "\2b";
}

.glyphicon-eur:before,
.glyphicon-euro:before {
  content: "\20ac";
}

.glyphicon-minus:before {
  content: "\2212";
}

.glyphicon-cloud:before {
  content: "\2601";
}

.glyphicon-envelope:before {
  content: "\2709";
}

.glyphicon-pencil:before {
  content: "\270f";
}

.glyphicon-glass:before {
  content: "\e001";
}

.glyphicon-music:before {
  content: "\e002";
}

.glyphicon-search:before {
  content: "\e003";
}

.glyphicon-heart:before {
  content: "\e005";
}

.glyphicon-star:before {
  content: "\e006";
}

.glyphicon-star-empty:before {
  content: "\e007";
}

.glyphicon-user:before {
  content: "\e008";
}

.glyphicon-film:before {
  content: "\e009";
}

.glyphicon-th-large:before {
  content: "\e010";
}

.glyphicon-th:before {
  content: "\e011";
}

.glyphicon-th-list:before {
  content: "\e012";
}

.glyphicon-ok:before {
  content: "\e013";
}

.glyphicon-remove:before {
  content: "\e014";
}

.glyphicon-zoom-in:before {
  content: "\e015";
}

.glyphicon-zoom-out:before {
  content: "\e016";
}

.glyphicon-off:before {
  content: "\e017";
}

.glyphicon-signal:before {
  content: "\e018";
}

.glyphicon-cog:before {
  content: "\e019";
}

.glyphicon-trash:before {
  content: "\e020";
}

.glyphicon-home:before {
  content: "\e021";
}

.glyphicon-file:before {
  content: "\e022";
}

.glyphicon-time:before {
  content: "\e023";
}

.glyphicon-road:before {
  content: "\e024";
}

.glyphicon-download-alt:before {
  content: "\e025";
}

.glyphicon-download:before {
  content: "\e026";
}

.glyphicon-upload:before {
  content: "\e027";
}

.glyphicon-inbox:before {
  content: "\e028";
}

.glyphicon-play-circle:before {
  content: "\e029";
}

.glyphicon-repeat:before {
  content: "\e030";
}

.glyphicon-refresh:before {
  content: "\e031";
}

.glyphicon-list-alt:before {
  content: "\e032";
}

.glyphicon-lock:before {
  content: "\e033";
}

.glyphicon-flag:before {
  content: "\e034";
}

.glyphicon-headphones:before {
  content: "\e035";
}

.glyphicon-volume-off:before {
  content: "\e036";
}

.glyphicon-volume-down:before {
  content: "\e037";
}

.glyphicon-volume-up:before {
  content: "\e038";
}

.glyphicon-qrcode:before {
  content: "\e039";
}

.glyphicon-barcode:before {
  content: "\e040";
}

.glyphicon-tag:before {
  content: "\e041";
}

.glyphicon-tags:before {
  content: "\e042";
}

.glyphicon-book:before {
  content: "\e043";
}

.glyphicon-bookmark:before {
  content: "\e044";
}

.glyphicon-print:before {
  content: "\e045";
}

.glyphicon-camera:before {
  content: "\e046";
}

.glyphicon-font:before {
  content: "\e047";
}

.glyphicon-bold:before {
  content: "\e048";
}

.glyphicon-italic:before {
  content: "\e049";
}

.glyphicon-text-height:before {
  content: "\e050";
}

.glyphicon-text-width:before {
  content: "\e051";
}

.glyphicon-align-left:before {
  content: "\e052";
}

.glyphicon-align-center:before {
  content: "\e053";
}

.glyphicon-align-right:before {
  content: "\e054";
}

.glyphicon-align-justify:before {
  content: "\e055";
}

.glyphicon-list:before {
  content: "\e056";
}

.glyphicon-indent-left:before {
  content: "\e057";
}

.glyphicon-indent-right:before {
  content: "\e058";
}

.glyphicon-facetime-video:before {
  content: "\e059";
}

.glyphicon-picture:before {
  content: "\e060";
}

.glyphicon-map-marker:before {
  content: "\e062";
}

.glyphicon-adjust:before {
  content: "\e063";
}

.glyphicon-tint:before {
  content: "\e064";
}

.glyphicon-edit:before {
  content: "\e065";
}

.glyphicon-share:before {
  content: "\e066";
}

.glyphicon-check:before {
  content: "\e067";
}

.glyphicon-move:before {
  content: "\e068";
}

.glyphicon-step-backward:before {
  content: "\e069";
}

.glyphicon-fast-backward:before {
  content: "\e070";
}

.glyphicon-backward:before {
  content: "\e071";
}

.glyphicon-play:before {
  content: "\e072";
}

.glyphicon-pause:before {
  content: "\e073";
}

.glyphicon-stop:before {
  content: "\e074";
}

.glyphicon-forward:before {
  content: "\e075";
}

.glyphicon-fast-forward:before {
  content: "\e076";
}

.glyphicon-step-forward:before {
  content: "\e077";
}

.glyphicon-eject:before {
  content: "\e078";
}

.glyphicon-chevron-left:before {
  content: "\e079";
}

.glyphicon-chevron-right:before {
  content: "\e080";
}

.glyphicon-plus-sign:before {
  content: "\e081";
}

.glyphicon-minus-sign:before {
  content: "\e082";
}

.glyphicon-remove-sign:before {
  content: "\e083";
}

.glyphicon-ok-sign:before {
  content: "\e084";
}

.glyphicon-question-sign:before {
  content: "\e085";
}

.glyphicon-info-sign:before {
  content: "\e086";
}

.glyphicon-screenshot:before {
  content: "\e087";
}

.glyphicon-remove-circle:before {
  content: "\e088";
}

.glyphicon-ok-circle:before {
  content: "\e089";
}

.glyphicon-ban-circle:before {
  content: "\e090";
}

.glyphicon-arrow-left:before {
  content: "\e091";
}

.glyphicon-arrow-right:before {
  content: "\e092";
}

.glyphicon-arrow-up:before {
  content: "\e093";
}

.glyphicon-arrow-down:before {
  content: "\e094";
}

.glyphicon-share-alt:before {
  content: "\e095";
}

.glyphicon-resize-full:before {
  content: "\e096";
}

.glyphicon-resize-small:before {
  content: "\e097";
}

.glyphicon-exclamation-sign:before {
  content: "\e101";
}

.glyphicon-gift:before {
  content: "\e102";
}

.glyphicon-leaf:before {
  content: "\e103";
}

.glyphicon-fire:before {
  content: "\e104";
}

.glyphicon-eye-open:before {
  content: "\e105";
}

.glyphicon-eye-close:before {
  content: "\e106";
}

.glyphicon-warning-sign:before {
  content: "\e107";
}

.glyphicon-plane:before {
  content: "\e108";
}

.glyphicon-calendar:before {
  content: "\e109";
}

.glyphicon-random:before {
  content: "\e110";
}

.glyphicon-comment:before {
  content: "\e111";
}

.glyphicon-magnet:before {
  content: "\e112";
}

.glyphicon-chevron-up:before {
  content: "\e113";
}

.glyphicon-chevron-down:before {
  content: "\e114";
}

.glyphicon-retweet:before {
  content: "\e115";
}

.glyphicon-shopping-cart:before {
  content: "\e116";
}

.glyphicon-folder-close:before {
  content: "\e117";
}

.glyphicon-folder-open:before {
  content: "\e118";
}

.glyphicon-resize-vertical:before {
  content: "\e119";
}

.glyphicon-resize-horizontal:before {
  content: "\e120";
}

.glyphicon-hdd:before {
  content: "\e121";
}

.glyphicon-bullhorn:before {
  content: "\e122";
}

.glyphicon-bell:before {
  content: "\e123";
}

.glyphicon-certificate:before {
  content: "\e124";
}

.glyphicon-thumbs-up:before {
  content: "\e125";
}

.glyphicon-thumbs-down:before {
  content: "\e126";
}

.glyphicon-hand-right:before {
  content: "\e127";
}

.glyphicon-hand-left:before {
  content: "\e128";
}

.glyphicon-hand-up:before {
  content: "\e129";
}

.glyphicon-hand-down:before {
  content: "\e130";
}

.glyphicon-circle-arrow-right:before {
  content: "\e131";
}

.glyphicon-circle-arrow-left:before {
  content: "\e132";
}

.glyphicon-circle-arrow-up:before {
  content: "\e133";
}

.glyphicon-circle-arrow-down:before {
  content: "\e134";
}

.glyphicon-globe:before {
  content: "\e135";
}

.glyphicon-wrench:before {
  content: "\e136";
}

.glyphicon-tasks:before {
  content: "\e137";
}

.glyphicon-filter:before {
  content: "\e138";
}

.glyphicon-briefcase:before {
  content: "\e139";
}

.glyphicon-fullscreen:before {
  content: "\e140";
}

.glyphicon-dashboard:before {
  content: "\e141";
}

.glyphicon-paperclip:before {
  content: "\e142";
}

.glyphicon-heart-empty:before {
  content: "\e143";
}

.glyphicon-link:before {
  content: "\e144";
}

.glyphicon-phone:before {
  content: "\e145";
}

.glyphicon-pushpin:before {
  content: "\e146";
}

.glyphicon-usd:before {
  content: "\e148";
}

.glyphicon-gbp:before {
  content: "\e149";
}

.glyphicon-sort:before {
  content: "\e150";
}

.glyphicon-sort-by-alphabet:before {
  content: "\e151";
}

.glyphicon-sort-by-alphabet-alt:before {
  content: "\e152";
}

.glyphicon-sort-by-order:before {
  content: "\e153";
}

.glyphicon-sort-by-order-alt:before {
  content: "\e154";
}

.glyphicon-sort-by-attributes:before {
  content: "\e155";
}

.glyphicon-sort-by-attributes-alt:before {
  content: "\e156";
}

.glyphicon-unchecked:before {
  content: "\e157";
}

.glyphicon-expand:before {
  content: "\e158";
}

.glyphicon-collapse-down:before {
  content: "\e159";
}

.glyphicon-collapse-up:before {
  content: "\e160";
}

.glyphicon-log-in:before {
  content: "\e161";
}

.glyphicon-flash:before {
  content: "\e162";
}

.glyphicon-log-out:before {
  content: "\e163";
}

.glyphicon-new-window:before {
  content: "\e164";
}

.glyphicon-record:before {
  content: "\e165";
}

.glyphicon-save:before {
  content: "\e166";
}

.glyphicon-open:before {
  content: "\e167";
}

.glyphicon-saved:before {
  content: "\e168";
}

.glyphicon-import:before {
  content: "\e169";
}

.glyphicon-export:before {
  content: "\e170";
}

.glyphicon-send:before {
  content: "\e171";
}

.glyphicon-floppy-disk:before {
  content: "\e172";
}

.glyphicon-floppy-saved:before {
  content: "\e173";
}

.glyphicon-floppy-remove:before {
  content: "\e174";
}

.glyphicon-floppy-save:before {
  content: "\e175";
}

.glyphicon-floppy-open:before {
  content: "\e176";
}

.glyphicon-credit-card:before {
  content: "\e177";
}

.glyphicon-transfer:before {
  content: "\e178";
}

.glyphicon-cutlery:before {
  content: "\e179";
}

.glyphicon-header:before {
  content: "\e180";
}

.glyphicon-compressed:before {
  content: "\e181";
}

.glyphicon-earphone:before {
  content: "\e182";
}

.glyphicon-phone-alt:before {
  content: "\e183";
}

.glyphicon-tower:before {
  content: "\e184";
}

.glyphicon-stats:before {
  content: "\e185";
}

.glyphicon-sd-video:before {
  content: "\e186";
}

.glyphicon-hd-video:before {
  content: "\e187";
}

.glyphicon-subtitles:before {
  content: "\e188";
}

.glyphicon-sound-stereo:before {
  content: "\e189";
}

.glyphicon-sound-dolby:before {
  content: "\e190";
}

.glyphicon-sound-5-1:before {
  content: "\e191";
}

.glyphicon-sound-6-1:before {
  content: "\e192";
}

.glyphicon-sound-7-1:before {
  content: "\e193";
}

.glyphicon-copyright-mark:before {
  content: "\e194";
}

.glyphicon-registration-mark:before {
  content: "\e195";
}

.glyphicon-cloud-download:before {
  content: "\e197";
}

.glyphicon-cloud-upload:before {
  content: "\e198";
}

.glyphicon-tree-conifer:before {
  content: "\e199";
}

.glyphicon-tree-deciduous:before {
  content: "\e200";
}

.glyphicon-cd:before {
  content: "\e201";
}

.glyphicon-save-file:before {
  content: "\e202";
}

.glyphicon-open-file:before {
  content: "\e203";
}

.glyphicon-level-up:before {
  content: "\e204";
}

.glyphicon-copy:before {
  content: "\e205";
}

.glyphicon-paste:before {
  content: "\e206";
}

.glyphicon-alert:before {
  content: "\e209";
}

.glyphicon-equalizer:before {
  content: "\e210";
}

.glyphicon-king:before {
  content: "\e211";
}

.glyphicon-queen:before {
  content: "\e212";
}

.glyphicon-pawn:before {
  content: "\e213";
}

.glyphicon-bishop:before {
  content: "\e214";
}

.glyphicon-knight:before {
  content: "\e215";
}

.glyphicon-baby-formula:before {
  content: "\e216";
}

.glyphicon-tent:before {
  content: "\26fa";
}

.glyphicon-blackboard:before {
  content: "\e218";
}

.glyphicon-bed:before {
  content: "\e219";
}

.glyphicon-apple:before {
  content: "\f8ff";
}

.glyphicon-erase:before {
  content: "\e221";
}

.glyphicon-hourglass:before {
  content: "\231b";
}

.glyphicon-lamp:before {
  content: "\e223";
}

.glyphicon-duplicate:before {
  content: "\e224";
}

.glyphicon-piggy-bank:before {
  content: "\e225";
}

.glyphicon-scissors:before {
  content: "\e226";
}

.glyphicon-bitcoin:before,
.glyphicon-btc:before,
.glyphicon-xbt:before {
  content: "\e227";
}

.glyphicon-jpy:before,
.glyphicon-yen:before {
  content: "\00a5";
}

.glyphicon-rub:before,
.glyphicon-ruble:before {
  content: "\20bd";
}

.glyphicon-scale:before {
  content: "\e230";
}

.glyphicon-ice-lolly:before {
  content: "\e231";
}

.glyphicon-ice-lolly-tasted:before {
  content: "\e232";
}

.glyphicon-education:before {
  content: "\e233";
}

.glyphicon-option-horizontal:before {
  content: "\e234";
}

.glyphicon-option-vertical:before {
  content: "\e235";
}

.glyphicon-menu-hamburger:before {
  content: "\e236";
}

.glyphicon-modal-window:before {
  content: "\e237";
}

.glyphicon-oil:before {
  content: "\e238";
}

.glyphicon-grain:before {
  content: "\e239";
}

.glyphicon-sunglasses:before {
  content: "\e240";
}

.glyphicon-text-size:before {
  content: "\e241";
}

.glyphicon-text-color:before {
  content: "\e242";
}

.glyphicon-text-background:before {
  content: "\e243";
}

.glyphicon-object-align-top:before {
  content: "\e244";
}

.glyphicon-object-align-bottom:before {
  content: "\e245";
}

.glyphicon-object-align-horizontal:before {
  content: "\e246";
}

.glyphicon-object-align-left:before {
  content: "\e247";
}

.glyphicon-object-align-vertical:before {
  content: "\e248";
}

.glyphicon-object-align-right:before {
  content: "\e249";
}

.glyphicon-triangle-right:before {
  content: "\e250";
}

.glyphicon-triangle-left:before {
  content: "\e251";
}

.glyphicon-triangle-bottom:before {
  content: "\e252";
}

.glyphicon-triangle-top:before {
  content: "\e253";
}

.glyphicon-console:before {
  content: "\e254";
}

.glyphicon-superscript:before {
  content: "\e255";
}

.glyphicon-subscript:before {
  content: "\e256";
}

.glyphicon-menu-left:before {
  content: "\e257";
}

.glyphicon-menu-right:before {
  content: "\e258";
}

.glyphicon-menu-down:before {
  content: "\e259";
}

.glyphicon-menu-up:before {
  content: "\e260";
}

*,
:after,
:before {
  box-sizing: border-box;
}

body {
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 14px;
  line-height: 1.42857143;
  color: #333;
}

button,
input,
select,
textarea {
  font-family: inherit;
  font-size: inherit;
  line-height: inherit;
}

a {
  color: #337ab7;
  text-decoration: none;
}

a:focus,
a:hover {
  color: #23527c;
  text-decoration: underline;
}

a:focus {
  outline: dotted thin;
  outline: -webkit-focus-ring-color auto 5px;
  outline-offset: -2px;
}

.carousel-inner > .item > a > img,
.carousel-inner > .item > img,
.img-responsive,
.thumbnail a > img,
.thumbnail > img {
  display: block;
  max-width: 100%;
  height: auto;
}

.img-rounded {
  border-radius: 6px;
}

.img-thumbnail {
  display: inline-block;
  max-width: 100%;
  height: auto;
  padding: 4px;
  line-height: 1.42857143;
  border: 1px solid #ddd;
  border-radius: 4px;
  -webkit-transition: all 0.2s ease-in-out;
  -o-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
}

.img-circle {
  border-radius: 50%;
}

hr {
  margin-top: 20px;
  margin-bottom: 20px;
  border-top: 1px solid #eee;
}

.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}

.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}

[role="button"] {
  cursor: pointer;
}

.h1,
.h2,
.h3,
.h4,
.h5,
.h6,
h1,
h2,
h3,
h4,
h5,
h6 {
  font-family: inherit;
  font-weight: 500;
  line-height: 1.1;
  color: inherit;
}

.h1 .small,
.h1 small,
.h2 .small,
.h2 small,
.h3 .small,
.h3 small,
.h4 .small,
.h4 small,
.h5 .small,
.h5 small,
.h6 .small,
.h6 small,
h1 .small,
h1 small,
h2 .small,
h2 small,
h3 .small,
h3 small,
h4 .small,
h4 small,
h5 .small,
h5 small,
h6 .small,
h6 small {
  font-weight: 400;
  line-height: 1;
  color: #777;
}

.h1,
.h2,
.h3,
h1,
h2,
h3 {
  margin-top: 20px;
  margin-bottom: 10px;
}

.h1 .small,
.h1 small,
.h2 .small,
.h2 small,
.h3 .small,
.h3 small,
h1 .small,
h1 small,
h2 .small,
h2 small,
h3 .small,
h3 small {
  font-size: 65%;
}

.h4,
.h5,
.h6,
h4,
h5,
h6 {
  margin-top: 10px;
  margin-bottom: 10px;
}

.h4 .small,
.h4 small,
.h5 .small,
.h5 small,
.h6 .small,
.h6 small,
h4 .small,
h4 small,
h5 .small,
h5 small,
h6 .small,
h6 small {
  font-size: 75%;
}

.h1,
h1 {
  font-size: 36px;
}

.h2,
h2 {
  font-size: 30px;
}

.h3,
h3 {
  font-size: 24px;
}

.h4,
h4 {
  font-size: 18px;
}

.h5,
h5 {
  font-size: 14px;
}

.h6,
h6 {
  font-size: 12px;
}

p {
  margin: 0 0 10px;
}

.lead {
  margin-bottom: 20px;
  font-size: 16px;
  font-weight: 300;
  line-height: 1.4;
}

dt,
kbd kbd,
label {
  font-weight: 700;
}

address,
blockquote .small,
blockquote footer,
blockquote small,
dd,
dt,
pre {
  line-height: 1.42857143;
}

@media (min-width: 768px) {
  .lead {
    font-size: 21px;
  }
}

.small,
small {
  font-size: 85%;
}

.mark,
mark {
  padding: 0.2em;
  background-color: #fcf8e3;
}

.list-inline,
.list-unstyled {
  padding-left: 0;
  list-style: none;
}

.text-left {
  text-align: left;
}

.text-right {
  text-align: right;
}

.text-center {
  text-align: center;
}

.text-justify {
  text-align: justify;
}

.text-nowrap {
  white-space: nowrap;
}

.text-lowercase {
  text-transform: lowercase;
}

.text-uppercase {
  text-transform: uppercase;
}

.text-capitalize {
  text-transform: capitalize;
}

.text-muted {
  color: #777;
}

.text-primary {
  color: #337ab7;
}

a.text-primary:focus,
a.text-primary:hover {
  color: #286090;
}

.text-success {
  color: #3c763d;
}

a.text-success:focus,
a.text-success:hover {
  color: #2b542c;
}

.text-info {
  color: #31708f;
}

a.text-info:focus,
a.text-info:hover {
  color: #245269;
}

.text-warning {
  color: #8a6d3b;
}

a.text-warning:focus,
a.text-warning:hover {
  color: #66512c;
}

.text-danger {
  color: #a94442;
}

a.text-danger:focus,
a.text-danger:hover {
  color: #843534;
}

.bg-primary {
  color: #fff;
  background-color: #337ab7;
}

a.bg-primary:focus,
a.bg-primary:hover {
  background-color: #286090;
}

.bg-success {
  background-color: #dff0d8;
}

a.bg-success:focus,
a.bg-success:hover {
  background-color: #c1e2b3;
}

.bg-info {
  background-color: #d9edf7;
}

a.bg-info:focus,
a.bg-info:hover {
  background-color: #afd9ee;
}

.bg-warning {
  background-color: #fcf8e3;
}

a.bg-warning:focus,
a.bg-warning:hover {
  background-color: #f7ecb5;
}

.bg-danger {
  background-color: #f2dede;
}

a.bg-danger:focus,
a.bg-danger:hover {
  background-color: #e4b9b9;
}

pre code,
table {
  background-color: transparent;
}

.page-header {
  padding-bottom: 9px;
  margin: 40px 0 20px;
  border-bottom: 1px solid #eee;
}

dl,
ol,
ul {
  margin-top: 0;
}

blockquote ol:last-child,
blockquote p:last-child,
blockquote ul:last-child,
ol ol,
ol ul,
ul ol,
ul ul {
  margin-bottom: 0;
}

address,
dl {
  margin-bottom: 20px;
}

ol,
ul {
  margin-bottom: 10px;
}

.list-inline {
  margin-left: -5px;
}

.list-inline > li {
  display: inline-block;
  padding-right: 5px;
  padding-left: 5px;
}

dd {
  margin-left: 0;
}

@media (min-width: 768px) {
  .dl-horizontal dt {
    float: left;
    width: 160px;
    overflow: hidden;
    clear: left;
    text-align: right;
    text-overflow: ellipsis;
    white-space: nowrap;
  }

  .dl-horizontal dd {
    margin-left: 180px;
  }

  .container {
    width: 750px;
  }
}

abbr[data-original-title],
abbr[title] {
  cursor: help;
  border-bottom: 1px dotted #777;
}

.initialism {
  font-size: 90%;
  text-transform: uppercase;
}

blockquote {
  padding: 10px 20px;
  margin: 0 0 20px;
  font-size: 17.5px;
  border-left: 5px solid #eee;
}

blockquote .small,
blockquote footer,
blockquote small {
  display: block;
  font-size: 80%;
  color: #777;
}

legend,
pre {
  display: block;
  color: #333;
}

blockquote .small:before,
blockquote footer:before,
blockquote small:before {
  content: "\2014 \00A0";
}

.blockquote-reverse,
blockquote.pull-right {
  padding-right: 15px;
  padding-left: 0;
  text-align: right;
  border-right: 5px solid #eee;
  border-left: 0;
}

code,
kbd {
  padding: 2px 4px;
  font-size: 90%;
}

caption,
th {
  text-align: left;
}

.blockquote-reverse .small:before,
.blockquote-reverse footer:before,
.blockquote-reverse small:before,
blockquote.pull-right .small:before,
blockquote.pull-right footer:before,
blockquote.pull-right small:before {
  content: "";
}

.blockquote-reverse .small:after,
.blockquote-reverse footer:after,
.blockquote-reverse small:after,
blockquote.pull-right .small:after,
blockquote.pull-right footer:after,
blockquote.pull-right small:after {
  content: "\00A0 \2014";
}

code {
  color: #c7254e;
  background-color: #f9f2f4;
  border-radius: 4px;
}

kbd {
  color: #fff;
  background-color: #333;
  border-radius: 3px;
  -webkit-box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.25);
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.25);
}

kbd kbd {
  padding: 0;
  font-size: 100%;
  -webkit-box-shadow: none;
  box-shadow: none;
}

pre {
  padding: 9.5px;
  margin: 0 0 10px;
  font-size: 13px;
  word-break: break-all;
  word-wrap: break-word;
  background-color: #f5f5f5;
  border: 1px solid #ccc;
  border-radius: 4px;
}

.container,
.container-fluid {
  margin-right: auto;
  margin-left: auto;
}

pre code {
  padding: 0;
  font-size: inherit;
  color: inherit;
  white-space: pre-wrap;
  border-radius: 0;
}

.container,
.container-fluid {
  padding-right: 15px;
  padding-left: 15px;
}

.pre-scrollable {
  overflow-y: scroll;
}

@media (min-width: 992px) {
  .container {
    width: 970px;
  }
}

@media (min-width: 1200px) {
  .container {
    width: 1170px;
  }
}

.row {
  margin-right: -15px;
  margin-left: -15px;
}

.col-lg-1,
.col-lg-10,
.col-lg-11,
.col-lg-12,
.col-lg-2,
.col-lg-3,
.col-lg-4,
.col-lg-5,
.col-lg-6,
.col-lg-7,
.col-lg-8,
.col-lg-9,
.col-md-1,
.col-md-10,
.col-md-11,
.col-md-12,
.col-md-2,
.col-md-3,
.col-md-4,
.col-md-5,
.col-md-6,
.col-md-7,
.col-md-8,
.col-md-9,
.col-sm-1,
.col-sm-10,
.col-sm-11,
.col-sm-12,
.col-sm-2,
.col-sm-3,
.col-sm-4,
.col-sm-5,
.col-sm-6,
.col-sm-7,
.col-sm-8,
.col-sm-9,
.col-xs-1,
.col-xs-10,
.col-xs-11,
.col-xs-12,
.col-xs-2,
.col-xs-3,
.col-xs-4,
.col-xs-5,
.col-xs-6,
.col-xs-7,
.col-xs-8,
.col-xs-9 {
  position: relative;
  min-height: 1px;
  padding-right: 15px;
  padding-left: 15px;
}

.col-xs-12 {
  width: 100%;
}

.col-xs-11 {
  width: 91.66666667%;
}

.col-xs-10 {
  width: 83.33333333%;
}

.col-xs-9 {
  width: 75%;
}

.col-xs-8 {
  width: 66.66666667%;
}

.col-xs-7 {
  width: 58.33333333%;
}

.col-xs-6 {
  width: 50%;
}

.col-xs-5 {
  width: 41.66666667%;
}

.col-xs-4 {
  width: 33.33333333%;
}

.col-xs-3 {
  width: 25%;
}

.col-xs-2 {
  width: 16.66666667%;
}

.col-xs-1 {
  width: 8.33333333%;
}

.col-xs-pull-12 {
  right: 100%;
}

.col-xs-pull-11 {
  right: 91.66666667%;
}

.col-xs-pull-10 {
  right: 83.33333333%;
}

.col-xs-pull-9 {
  right: 75%;
}

.col-xs-pull-8 {
  right: 66.66666667%;
}

.col-xs-pull-7 {
  right: 58.33333333%;
}

.col-xs-pull-6 {
  right: 50%;
}

.col-xs-pull-5 {
  right: 41.66666667%;
}

.col-xs-pull-4 {
  right: 33.33333333%;
}

.col-xs-pull-3 {
  right: 25%;
}

.col-xs-pull-2 {
  right: 16.66666667%;
}

.col-xs-pull-1 {
  right: 8.33333333%;
}

.col-xs-pull-0 {
  right: auto;
}

.col-xs-push-12 {
  left: 100%;
}

.col-xs-push-11 {
  left: 91.66666667%;
}

.col-xs-push-10 {
  left: 83.33333333%;
}

.col-xs-push-9 {
  left: 75%;
}

.col-xs-push-8 {
  left: 66.66666667%;
}

.col-xs-push-7 {
  left: 58.33333333%;
}

.col-xs-push-6 {
  left: 50%;
}

.col-xs-push-5 {
  left: 41.66666667%;
}

.col-xs-push-4 {
  left: 33.33333333%;
}

.col-xs-push-3 {
  left: 25%;
}

.col-xs-push-2 {
  left: 16.66666667%;
}

.col-xs-push-1 {
  left: 8.33333333%;
}

.col-xs-push-0 {
  left: auto;
}

.col-xs-offset-12 {
  margin-left: 100%;
}

.col-xs-offset-11 {
  margin-left: 91.66666667%;
}

.col-xs-offset-10 {
  margin-left: 83.33333333%;
}

.col-xs-offset-9 {
  margin-left: 75%;
}

.col-xs-offset-8 {
  margin-left: 66.66666667%;
}

.col-xs-offset-7 {
  margin-left: 58.33333333%;
}

.col-xs-offset-6 {
  margin-left: 50%;
}

.col-xs-offset-5 {
  margin-left: 41.66666667%;
}

.col-xs-offset-4 {
  margin-left: 33.33333333%;
}

.col-xs-offset-3 {
  margin-left: 25%;
}

.col-xs-offset-2 {
  margin-left: 16.66666667%;
}

.col-xs-offset-1 {
  margin-left: 8.33333333%;
}

.col-xs-offset-0 {
  margin-left: 0;
}

@media (min-width: 768px) {
  .col-sm-1,
  .col-sm-10,
  .col-sm-11,
  .col-sm-12,
  .col-sm-2,
  .col-sm-3,
  .col-sm-4,
  .col-sm-5,
  .col-sm-6,
  .col-sm-7,
  .col-sm-8,
  .col-sm-9 {
    float: left;
  }

  .col-sm-12 {
    width: 100%;
  }

  .col-sm-11 {
    width: 91.66666667%;
  }

  .col-sm-10 {
    width: 83.33333333%;
  }

  .col-sm-9 {
    width: 75%;
  }

  .col-sm-8 {
    width: 66.66666667%;
  }

  .col-sm-7 {
    width: 58.33333333%;
  }

  .col-sm-6 {
    width: 50%;
  }

  .col-sm-5 {
    width: 41.66666667%;
  }

  .col-sm-4 {
    width: 33.33333333%;
  }

  .col-sm-3 {
    width: 25%;
  }

  .col-sm-2 {
    width: 16.66666667%;
  }

  .col-sm-1 {
    width: 8.33333333%;
  }

  .col-sm-pull-12 {
    right: 100%;
  }

  .col-sm-pull-11 {
    right: 91.66666667%;
  }

  .col-sm-pull-10 {
    right: 83.33333333%;
  }

  .col-sm-pull-9 {
    right: 75%;
  }

  .col-sm-pull-8 {
    right: 66.66666667%;
  }

  .col-sm-pull-7 {
    right: 58.33333333%;
  }

  .col-sm-pull-6 {
    right: 50%;
  }

  .col-sm-pull-5 {
    right: 41.66666667%;
  }

  .col-sm-pull-4 {
    right: 33.33333333%;
  }

  .col-sm-pull-3 {
    right: 25%;
  }

  .col-sm-pull-2 {
    right: 16.66666667%;
  }

  .col-sm-pull-1 {
    right: 8.33333333%;
  }

  .col-sm-pull-0 {
    right: auto;
  }

  .col-sm-push-12 {
    left: 100%;
  }

  .col-sm-push-11 {
    left: 91.66666667%;
  }

  .col-sm-push-10 {
    left: 83.33333333%;
  }

  .col-sm-push-9 {
    left: 75%;
  }

  .col-sm-push-8 {
    left: 66.66666667%;
  }

  .col-sm-push-7 {
    left: 58.33333333%;
  }

  .col-sm-push-6 {
    left: 50%;
  }

  .col-sm-push-5 {
    left: 41.66666667%;
  }

  .col-sm-push-4 {
    left: 33.33333333%;
  }

  .col-sm-push-3 {
    left: 25%;
  }

  .col-sm-push-2 {
    left: 16.66666667%;
  }

  .col-sm-push-1 {
    left: 8.33333333%;
  }

  .col-sm-push-0 {
    left: auto;
  }

  .col-sm-offset-12 {
    margin-left: 100%;
  }

  .col-sm-offset-11 {
    margin-left: 91.66666667%;
  }

  .col-sm-offset-10 {
    margin-left: 83.33333333%;
  }

  .col-sm-offset-9 {
    margin-left: 75%;
  }

  .col-sm-offset-8 {
    margin-left: 66.66666667%;
  }

  .col-sm-offset-7 {
    margin-left: 58.33333333%;
  }

  .col-sm-offset-6 {
    margin-left: 50%;
  }

  .col-sm-offset-5 {
    margin-left: 41.66666667%;
  }

  .col-sm-offset-4 {
    margin-left: 33.33333333%;
  }

  .col-sm-offset-3 {
    margin-left: 25%;
  }

  .col-sm-offset-2 {
    margin-left: 16.66666667%;
  }

  .col-sm-offset-1 {
    margin-left: 8.33333333%;
  }

  .col-sm-offset-0 {
    margin-left: 0;
  }
}

@media (min-width: 992px) {
  .col-md-1,
  .col-md-10,
  .col-md-11,
  .col-md-12,
  .col-md-2,
  .col-md-3,
  .col-md-4,
  .col-md-5,
  .col-md-6,
  .col-md-7,
  .col-md-8,
  .col-md-9 {
    float: left;
  }

  .col-md-12 {
    width: 100%;
  }

  .col-md-11 {
    width: 91.66666667%;
  }

  .col-md-10 {
    width: 83.33333333%;
  }

  .col-md-9 {
    width: 75%;
  }

  .col-md-8 {
    width: 66.66666667%;
  }

  .col-md-7 {
    width: 58.33333333%;
  }

  .col-md-6 {
    width: 50%;
  }

  .col-md-5 {
    width: 41.66666667%;
  }

  .col-md-4 {
    width: 33.33333333%;
  }

  .col-md-3 {
    width: 25%;
  }

  .col-md-2 {
    width: 16.66666667%;
  }

  .col-md-1 {
    width: 8.33333333%;
  }

  .col-md-pull-12 {
    right: 100%;
  }

  .col-md-pull-11 {
    right: 91.66666667%;
  }

  .col-md-pull-10 {
    right: 83.33333333%;
  }

  .col-md-pull-9 {
    right: 75%;
  }

  .col-md-pull-8 {
    right: 66.66666667%;
  }

  .col-md-pull-7 {
    right: 58.33333333%;
  }

  .col-md-pull-6 {
    right: 50%;
  }

  .col-md-pull-5 {
    right: 41.66666667%;
  }

  .col-md-pull-4 {
    right: 33.33333333%;
  }

  .col-md-pull-3 {
    right: 25%;
  }

  .col-md-pull-2 {
    right: 16.66666667%;
  }

  .col-md-pull-1 {
    right: 8.33333333%;
  }

  .col-md-pull-0 {
    right: auto;
  }

  .col-md-push-12 {
    left: 100%;
  }

  .col-md-push-11 {
    left: 91.66666667%;
  }

  .col-md-push-10 {
    left: 83.33333333%;
  }

  .col-md-push-9 {
    left: 75%;
  }

  .col-md-push-8 {
    left: 66.66666667%;
  }

  .col-md-push-7 {
    left: 58.33333333%;
  }

  .col-md-push-6 {
    left: 50%;
  }

  .col-md-push-5 {
    left: 41.66666667%;
  }

  .col-md-push-4 {
    left: 33.33333333%;
  }

  .col-md-push-3 {
    left: 25%;
  }

  .col-md-push-2 {
    left: 16.66666667%;
  }

  .col-md-push-1 {
    left: 8.33333333%;
  }

  .col-md-push-0 {
    left: auto;
  }

  .col-md-offset-12 {
    margin-left: 100%;
  }

  .col-md-offset-11 {
    margin-left: 91.66666667%;
  }

  .col-md-offset-10 {
    margin-left: 83.33333333%;
  }

  .col-md-offset-9 {
    margin-left: 75%;
  }

  .col-md-offset-8 {
    margin-left: 66.66666667%;
  }

  .col-md-offset-7 {
    margin-left: 58.33333333%;
  }

  .col-md-offset-6 {
    margin-left: 50%;
  }

  .col-md-offset-5 {
    margin-left: 41.66666667%;
  }

  .col-md-offset-4 {
    margin-left: 33.33333333%;
  }

  .col-md-offset-3 {
    margin-left: 25%;
  }

  .col-md-offset-2 {
    margin-left: 16.66666667%;
  }

  .col-md-offset-1 {
    margin-left: 8.33333333%;
  }

  .col-md-offset-0 {
    margin-left: 0;
  }
}

@media (min-width: 1200px) {
  .col-lg-1,
  .col-lg-10,
  .col-lg-11,
  .col-lg-12,
  .col-lg-2,
  .col-lg-3,
  .col-lg-4,
  .col-lg-5,
  .col-lg-6,
  .col-lg-7,
  .col-lg-8,
  .col-lg-9 {
    float: left;
  }

  .col-lg-12 {
    width: 100%;
  }

  .col-lg-11 {
    width: 91.66666667%;
  }

  .col-lg-10 {
    width: 83.33333333%;
  }

  .col-lg-9 {
    width: 75%;
  }

  .col-lg-8 {
    width: 66.66666667%;
  }

  .col-lg-7 {
    width: 58.33333333%;
  }

  .col-lg-6 {
    width: 50%;
  }

  .col-lg-5 {
    width: 41.66666667%;
  }

  .col-lg-4 {
    width: 33.33333333%;
  }

  .col-lg-3 {
    width: 25%;
  }

  .col-lg-2 {
    width: 16.66666667%;
  }

  .col-lg-1 {
    width: 8.33333333%;
  }

  .col-lg-pull-12 {
    right: 100%;
  }

  .col-lg-pull-11 {
    right: 91.66666667%;
  }

  .col-lg-pull-10 {
    right: 83.33333333%;
  }

  .col-lg-pull-9 {
    right: 75%;
  }

  .col-lg-pull-8 {
    right: 66.66666667%;
  }

  .col-lg-pull-7 {
    right: 58.33333333%;
  }

  .col-lg-pull-6 {
    right: 50%;
  }

  .col-lg-pull-5 {
    right: 41.66666667%;
  }

  .col-lg-pull-4 {
    right: 33.33333333%;
  }

  .col-lg-pull-3 {
    right: 25%;
  }

  .col-lg-pull-2 {
    right: 16.66666667%;
  }

  .col-lg-pull-1 {
    right: 8.33333333%;
  }

  .col-lg-pull-0 {
    right: auto;
  }

  .col-lg-push-12 {
    left: 100%;
  }

  .col-lg-push-11 {
    left: 91.66666667%;
  }

  .col-lg-push-10 {
    left: 83.33333333%;
  }

  .col-lg-push-9 {
    left: 75%;
  }

  .col-lg-push-8 {
    left: 66.66666667%;
  }

  .col-lg-push-7 {
    left: 58.33333333%;
  }

  .col-lg-push-6 {
    left: 50%;
  }

  .col-lg-push-5 {
    left: 41.66666667%;
  }

  .col-lg-push-4 {
    left: 33.33333333%;
  }

  .col-lg-push-3 {
    left: 25%;
  }

  .col-lg-push-2 {
    left: 16.66666667%;
  }

  .col-lg-push-1 {
    left: 8.33333333%;
  }

  .col-lg-push-0 {
    left: auto;
  }

  .col-lg-offset-12 {
    margin-left: 100%;
  }

  .col-lg-offset-11 {
    margin-left: 91.66666667%;
  }

  .col-lg-offset-10 {
    margin-left: 83.33333333%;
  }

  .col-lg-offset-9 {
    margin-left: 75%;
  }

  .col-lg-offset-8 {
    margin-left: 66.66666667%;
  }

  .col-lg-offset-7 {
    margin-left: 58.33333333%;
  }

  .col-lg-offset-6 {
    margin-left: 50%;
  }

  .col-lg-offset-5 {
    margin-left: 41.66666667%;
  }

  .col-lg-offset-4 {
    margin-left: 33.33333333%;
  }

  .col-lg-offset-3 {
    margin-left: 25%;
  }

  .col-lg-offset-2 {
    margin-left: 16.66666667%;
  }

  .col-lg-offset-1 {
    margin-left: 8.33333333%;
  }

  .col-lg-offset-0 {
    margin-left: 0;
  }
}

caption {
  padding-top: 8px;
  padding-bottom: 8px;
  color: #777;
}

.table {
  width: 100%;
  max-width: 100%;
  margin-bottom: 20px;
}

.table > tbody > tr > td,
.table > tbody > tr > th,
.table > tfoot > tr > td,
.table > tfoot > tr > th,
.table > thead > tr > td,
.table > thead > tr > th {
  padding: 8px;
  line-height: 1.42857143;
  vertical-align: top;
  border-top: 1px solid #ddd;
}

.table > thead > tr > th {
  vertical-align: bottom;
  border-bottom: 2px solid #ddd;
}

.table > caption + thead > tr:first-child > td,
.table > caption + thead > tr:first-child > th,
.table > colgroup + thead > tr:first-child > td,
.table > colgroup + thead > tr:first-child > th,
.table > thead:first-child > tr:first-child > td,
.table > thead:first-child > tr:first-child > th {
  border-top: 0;
}

.table > tbody + tbody {
  border-top: 2px solid #ddd;
}

.table .table {
  background-color: #fff;
}

.table-condensed > tbody > tr > td,
.table-condensed > tbody > tr > th,
.table-condensed > tfoot > tr > td,
.table-condensed > tfoot > tr > th,
.table-condensed > thead > tr > td,
.table-condensed > thead > tr > th {
  padding: 5px;
}

.table-bordered,
.table-bordered > tbody > tr > td,
.table-bordered > tbody > tr > th,
.table-bordered > tfoot > tr > td,
.table-bordered > tfoot > tr > th,
.table-bordered > thead > tr > td,
.table-bordered > thead > tr > th {
  border: 1px solid #ddd;
}

.table-bordered > thead > tr > td,
.table-bordered > thead > tr > th {
  border-bottom-width: 2px;
}

.table-striped > tbody > tr:nth-of-type(odd) {
  background-color: #f9f9f9;
}

.table-hover > tbody > tr:hover,
.table > tbody > tr.active > td,
.table > tbody > tr.active > th,
.table > tbody > tr > td.active,
.table > tbody > tr > th.active,
.table > tfoot > tr.active > td,
.table > tfoot > tr.active > th,
.table > tfoot > tr > td.active,
.table > tfoot > tr > th.active,
.table > thead > tr.active > td,
.table > thead > tr.active > th,
.table > thead > tr > td.active,
.table > thead > tr > th.active {
  background-color: #f5f5f5;
}

table col[class*="col-"] {
  position: static;
  display: table-column;
  float: none;
}

table td[class*="col-"],
table th[class*="col-"] {
  position: static;
  display: table-cell;
  float: none;
}

.table-hover > tbody > tr.active:hover > td,
.table-hover > tbody > tr.active:hover > th,
.table-hover > tbody > tr:hover > .active,
.table-hover > tbody > tr > td.active:hover,
.table-hover > tbody > tr > th.active:hover {
  background-color: #e8e8e8;
}

.table > tbody > tr.success > td,
.table > tbody > tr.success > th,
.table > tbody > tr > td.success,
.table > tbody > tr > th.success,
.table > tfoot > tr.success > td,
.table > tfoot > tr.success > th,
.table > tfoot > tr > td.success,
.table > tfoot > tr > th.success,
.table > thead > tr.success > td,
.table > thead > tr.success > th,
.table > thead > tr > td.success,
.table > thead > tr > th.success {
  background-color: #dff0d8;
}

.table-hover > tbody > tr.success:hover > td,
.table-hover > tbody > tr.success:hover > th,
.table-hover > tbody > tr:hover > .success,
.table-hover > tbody > tr > td.success:hover,
.table-hover > tbody > tr > th.success:hover {
  background-color: #d0e9c6;
}

.table > tbody > tr.info > td,
.table > tbody > tr.info > th,
.table > tbody > tr > td.info,
.table > tbody > tr > th.info,
.table > tfoot > tr.info > td,
.table > tfoot > tr.info > th,
.table > tfoot > tr > td.info,
.table > tfoot > tr > th.info,
.table > thead > tr.info > td,
.table > thead > tr.info > th,
.table > thead > tr > td.info,
.table > thead > tr > th.info {
  background-color: #d9edf7;
}

.table-hover > tbody > tr.info:hover > td,
.table-hover > tbody > tr.info:hover > th,
.table-hover > tbody > tr:hover > .info,
.table-hover > tbody > tr > td.info:hover,
.table-hover > tbody > tr > th.info:hover {
  background-color: #c4e3f3;
}

.table > tbody > tr.warning > td,
.table > tbody > tr.warning > th,
.table > tbody > tr > td.warning,
.table > tbody > tr > th.warning,
.table > tfoot > tr.warning > td,
.table > tfoot > tr.warning > th,
.table > tfoot > tr > td.warning,
.table > tfoot > tr > th.warning,
.table > thead > tr.warning > td,
.table > thead > tr.warning > th,
.table > thead > tr > td.warning,
.table > thead > tr > th.warning {
  background-color: #fcf8e3;
}

.table-hover > tbody > tr.warning:hover > td,
.table-hover > tbody > tr.warning:hover > th,
.table-hover > tbody > tr:hover > .warning,
.table-hover > tbody > tr > td.warning:hover,
.table-hover > tbody > tr > th.warning:hover {
  background-color: #faf2cc;
}

.table > tbody > tr.danger > td,
.table > tbody > tr.danger > th,
.table > tbody > tr > td.danger,
.table > tbody > tr > th.danger,
.table > tfoot > tr.danger > td,
.table > tfoot > tr.danger > th,
.table > tfoot > tr > td.danger,
.table > tfoot > tr > th.danger,
.table > thead > tr.danger > td,
.table > thead > tr.danger > th,
.table > thead > tr > td.danger,
.table > thead > tr > th.danger {
  background-color: #f2dede;
}

.table-hover > tbody > tr.danger:hover > td,
.table-hover > tbody > tr.danger:hover > th,
.table-hover > tbody > tr:hover > .danger,
.table-hover > tbody > tr > td.danger:hover,
.table-hover > tbody > tr > th.danger:hover {
  background-color: #ebcccc;
}

.table-responsive {
  min-height: 0.01%;
  overflow-x: auto;
}

@media screen and (max-width: 767px) {
  .table-responsive {
    width: 100%;
    margin-bottom: 15px;
    overflow-y: hidden;
    -ms-overflow-style: -ms-autohiding-scrollbar;
    border: 1px solid #ddd;
  }

  .table-responsive > .table {
    margin-bottom: 0;
  }

  .table-responsive > .table > tbody > tr > td,
  .table-responsive > .table > tbody > tr > th,
  .table-responsive > .table > tfoot > tr > td,
  .table-responsive > .table > tfoot > tr > th,
  .table-responsive > .table > thead > tr > td,
  .table-responsive > .table > thead > tr > th {
    white-space: nowrap;
  }

  .table-responsive > .table-bordered {
    border: 0;
  }

  .table-responsive > .table-bordered > tbody > tr > td:first-child,
  .table-responsive > .table-bordered > tbody > tr > th:first-child,
  .table-responsive > .table-bordered > tfoot > tr > td:first-child,
  .table-responsive > .table-bordered > tfoot > tr > th:first-child,
  .table-responsive > .table-bordered > thead > tr > td:first-child,
  .table-responsive > .table-bordered > thead > tr > th:first-child {
    border-left: 0;
  }

  .table-responsive > .table-bordered > tbody > tr > td:last-child,
  .table-responsive > .table-bordered > tbody > tr > th:last-child,
  .table-responsive > .table-bordered > tfoot > tr > td:last-child,
  .table-responsive > .table-bordered > tfoot > tr > th:last-child,
  .table-responsive > .table-bordered > thead > tr > td:last-child,
  .table-responsive > .table-bordered > thead > tr > th:last-child {
    border-right: 0;
  }

  .table-responsive > .table-bordered > tbody > tr:last-child > td,
  .table-responsive > .table-bordered > tbody > tr:last-child > th,
  .table-responsive > .table-bordered > tfoot > tr:last-child > td,
  .table-responsive > .table-bordered > tfoot > tr:last-child > th {
    border-bottom: 0;
  }
}

fieldset,
legend {
  padding: 0;
  border: 0;
}

fieldset {
  min-width: 0;
  margin: 0;
}

legend {
  width: 100%;
  margin-bottom: 20px;
  font-size: 21px;
  line-height: inherit;
  border-bottom: 1px solid #e5e5e5;
}

label {
  display: inline-block;
  max-width: 100%;
  margin-bottom: 5px;
}

input[type="search"] {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
  -webkit-appearance: none;
}

input[type="checkbox"],
input[type="radio"] {
  margin: 4px 0 0;
  margin-top: 1px\9;
  line-height: normal;
}

.form-control,
output {
  font-size: 14px;
  line-height: 1.42857143;
  color: #555;
  display: block;
}

input[type="file"] {
  display: block;
}

input[type="range"] {
  display: block;
  width: 100%;
}

select[multiple],
select[size] {
  height: auto;
}

input[type="checkbox"]:focus,
input[type="file"]:focus,
input[type="radio"]:focus {
  outline: dotted thin;
  outline: -webkit-focus-ring-color auto 5px;
  outline-offset: -2px;
}

output {
  padding-top: 7px;
}

.form-control {
  width: 100%;
  height: 34px;
  padding: 6px 12px;
  background-color: #fff;
  border: 1px solid #ccc;
  border-radius: 4px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out 0.15s,
    -webkit-box-shadow ease-in-out 0.15s;
  -o-transition: border-color ease-in-out 0.15s, box-shadow ease-in-out 0.15s;
  transition: border-color ease-in-out 0.15s, box-shadow ease-in-out 0.15s;
}

.form-control:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075),
    0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075),
    0 0 8px rgba(102, 175, 233, 0.6);
}

.form-control::-moz-placeholder {
  color: #999;
  opacity: 1;
}

.form-control:-ms-input-placeholder {
  color: #999;
}

.form-control::-webkit-input-placeholder {
  color: #999;
}

.has-success .checkbox,
.has-success .checkbox-inline,
.has-success .control-label,
.has-success .form-control-feedback,
.has-success .help-block,
.has-success .radio,
.has-success .radio-inline,
.has-success.checkbox label,
.has-success.checkbox-inline label,
.has-success.radio label,
.has-success.radio-inline label {
  color: #3c763d;
}

.form-control[disabled],
.form-control[readonly],
fieldset[disabled] .form-control {
  background-color: #eee;
  opacity: 1;
}

.form-control[disabled],
fieldset[disabled] .form-control {
  cursor: not-allowed;
}

textarea.form-control {
  height: auto;
}

@media screen and (-webkit-min-device-pixel-ratio: 0) {
  input[type="date"].form-control,
  input[type="datetime-local"].form-control,
  input[type="month"].form-control,
  input[type="time"].form-control {
    line-height: 34px;
  }

  .input-group-sm input[type="date"],
  .input-group-sm input[type="datetime-local"],
  .input-group-sm input[type="month"],
  .input-group-sm input[type="time"],
  input[type="date"].input-sm,
  input[type="datetime-local"].input-sm,
  input[type="month"].input-sm,
  input[type="time"].input-sm {
    line-height: 30px;
  }

  .input-group-lg input[type="date"],
  .input-group-lg input[type="datetime-local"],
  .input-group-lg input[type="month"],
  .input-group-lg input[type="time"],
  input[type="date"].input-lg,
  input[type="datetime-local"].input-lg,
  input[type="month"].input-lg,
  input[type="time"].input-lg {
    line-height: 46px;
  }
}

.form-group {
  margin-bottom: 15px;
}

.checkbox,
.radio {
  position: relative;
  display: block;
  margin-top: 10px;
  margin-bottom: 10px;
}

.checkbox label,
.radio label {
  min-height: 20px;
  padding-left: 20px;
  margin-bottom: 0;
  font-weight: 400;
  cursor: pointer;
}

.checkbox input[type="checkbox"],
.checkbox-inline input[type="checkbox"],
.radio input[type="radio"],
.radio-inline input[type="radio"] {
  position: absolute;
  margin-top: 4px\9;
  margin-left: -20px;
}

.checkbox + .checkbox,
.radio + .radio {
  margin-top: -5px;
}

.checkbox-inline,
.radio-inline {
  position: relative;
  display: inline-block;
  padding-left: 20px;
  margin-bottom: 0;
  font-weight: 400;
  cursor: pointer;
}

.checkbox-inline + .checkbox-inline,
.radio-inline + .radio-inline {
  margin-top: 0;
  margin-left: 10px;
}

.checkbox-inline.disabled,
.checkbox.disabled label,
.radio-inline.disabled,
.radio.disabled label,
fieldset[disabled] .checkbox label,
fieldset[disabled] .checkbox-inline,
fieldset[disabled] .radio label,
fieldset[disabled] .radio-inline,
fieldset[disabled] input[type="checkbox"],
fieldset[disabled] input[type="radio"],
input[type="checkbox"].disabled,
input[type="checkbox"][disabled],
input[type="radio"].disabled,
input[type="radio"][disabled] {
  cursor: not-allowed;
}

.form-control-static {
  min-height: 34px;
  padding-top: 7px;
  padding-bottom: 7px;
  margin-bottom: 0;
}

.form-control-static.input-lg,
.form-control-static.input-sm {
  padding-right: 0;
  padding-left: 0;
}

.form-group-sm .form-control,
.input-sm {
  padding: 5px 10px;
  border-radius: 3px;
  font-size: 12px;
}

.input-sm {
  height: 30px;
  line-height: 1.5;
}

select.input-sm {
  height: 30px;
  line-height: 30px;
}

select[multiple].input-sm,
textarea.input-sm {
  height: auto;
}

.form-group-sm .form-control {
  height: 30px;
  line-height: 1.5;
}

.form-group-lg .form-control,
.input-lg {
  border-radius: 6px;
  padding: 10px 16px;
  font-size: 18px;
}

.form-group-sm select.form-control {
  height: 30px;
  line-height: 30px;
}

.form-group-sm select[multiple].form-control,
.form-group-sm textarea.form-control {
  height: auto;
}

.form-group-sm .form-control-static {
  height: 30px;
  min-height: 32px;
  padding: 6px 10px;
  font-size: 12px;
  line-height: 1.5;
}

.input-lg {
  height: 46px;
  line-height: 1.3333333;
}

select.input-lg {
  height: 46px;
  line-height: 46px;
}

select[multiple].input-lg,
textarea.input-lg {
  height: auto;
}

.form-group-lg .form-control {
  height: 46px;
  line-height: 1.3333333;
}

.form-group-lg select.form-control {
  height: 46px;
  line-height: 46px;
}

.form-group-lg select[multiple].form-control,
.form-group-lg textarea.form-control {
  height: auto;
}

.form-group-lg .form-control-static {
  height: 46px;
  min-height: 38px;
  padding: 11px 16px;
  font-size: 18px;
  line-height: 1.3333333;
}

.has-feedback {
  position: relative;
}

.has-feedback .form-control {
  padding-right: 42.5px;
}

.form-control-feedback {
  position: absolute;
  top: 0;
  right: 0;
  z-index: 2;
  display: block;
  width: 34px;
  height: 34px;
  line-height: 34px;
  text-align: center;
  pointer-events: none;
}

.collapsing,
.dropdown,
.dropup {
  position: relative;
}

.form-group-lg .form-control + .form-control-feedback,
.input-group-lg + .form-control-feedback,
.input-lg + .form-control-feedback {
  width: 46px;
  height: 46px;
  line-height: 46px;
}

.form-group-sm .form-control + .form-control-feedback,
.input-group-sm + .form-control-feedback,
.input-sm + .form-control-feedback {
  width: 30px;
  height: 30px;
  line-height: 30px;
}

.has-success .form-control {
  border-color: #3c763d;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}

.has-success .form-control:focus {
  border-color: #2b542c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
}

.has-success .input-group-addon {
  color: #3c763d;
  background-color: #dff0d8;
  border-color: #3c763d;
}

.has-warning .checkbox,
.has-warning .checkbox-inline,
.has-warning .control-label,
.has-warning .form-control-feedback,
.has-warning .help-block,
.has-warning .radio,
.has-warning .radio-inline,
.has-warning.checkbox label,
.has-warning.checkbox-inline label,
.has-warning.radio label,
.has-warning.radio-inline label {
  color: #8a6d3b;
}

.has-warning .form-control {
  border-color: #8a6d3b;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}

.has-warning .form-control:focus {
  border-color: #66512c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
}

.has-warning .input-group-addon {
  color: #8a6d3b;
  background-color: #fcf8e3;
  border-color: #8a6d3b;
}

.has-error .checkbox,
.has-error .checkbox-inline,
.has-error .control-label,
.has-error .form-control-feedback,
.has-error .help-block,
.has-error .radio,
.has-error .radio-inline,
.has-error.checkbox label,
.has-error.checkbox-inline label,
.has-error.radio label,
.has-error.radio-inline label {
  color: #a94442;
}

.has-error .form-control {
  border-color: #a94442;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}

.has-error .form-control:focus {
  border-color: #843534;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
}

.has-error .input-group-addon {
  color: #a94442;
  background-color: #f2dede;
  border-color: #a94442;
}

.has-feedback label ~ .form-control-feedback {
  top: 25px;
}

.has-feedback label.sr-only ~ .form-control-feedback {
  top: 0;
}

.help-block {
  display: block;
  margin-top: 5px;
  margin-bottom: 10px;
  color: #737373;
}

@media (min-width: 768px) {
  .form-inline .form-control-static,
  .form-inline .form-group {
    display: inline-block;
  }

  .form-inline .control-label,
  .form-inline .form-group {
    margin-bottom: 0;
    vertical-align: middle;
  }

  .form-inline .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }

  .form-inline .input-group {
    display: inline-table;
    vertical-align: middle;
  }

  .form-inline .input-group .form-control,
  .form-inline .input-group .input-group-addon,
  .form-inline .input-group .input-group-btn {
    width: auto;
  }

  .form-inline .input-group > .form-control {
    width: 100%;
  }

  .form-inline .checkbox,
  .form-inline .radio {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }

  .form-inline .checkbox label,
  .form-inline .radio label {
    padding-left: 0;
  }

  .form-inline .checkbox input[type="checkbox"],
  .form-inline .radio input[type="radio"] {
    position: relative;
    margin-left: 0;
  }

  .form-inline .has-feedback .form-control-feedback {
    top: 0;
  }

  .form-horizontal .control-label {
    padding-top: 7px;
    margin-bottom: 0;
    text-align: right;
  }
}

.form-horizontal .checkbox,
.form-horizontal .checkbox-inline,
.form-horizontal .radio,
.form-horizontal .radio-inline {
  padding-top: 7px;
  margin-top: 0;
  margin-bottom: 0;
}

.form-horizontal .checkbox,
.form-horizontal .radio {
  min-height: 27px;
}

.form-horizontal .form-group {
  margin-right: -15px;
  margin-left: -15px;
}

.form-horizontal .has-feedback .form-control-feedback {
  right: 15px;
}

@media (min-width: 768px) {
  .form-horizontal .form-group-lg .control-label {
    padding-top: 14.33px;
    font-size: 18px;
  }

  .form-horizontal .form-group-sm .control-label {
    padding-top: 6px;
    font-size: 12px;
  }
}

.btn {
  display: inline-block;
  padding: 6px 12px;
  margin-bottom: 0;
  font-size: 14px;
  font-weight: 400;
  line-height: 1.42857143;
  text-align: center;
  white-space: nowrap;
  -ms-touch-action: manipulation;
  touch-action: manipulation;
  cursor: pointer;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  border: 1px solid transparent;
  border-radius: 4px;
}

.btn.active.focus,
.btn.active:focus,
.btn.focus,
.btn:active.focus,
.btn:active:focus,
.btn:focus {
  outline: dotted thin;
  outline: -webkit-focus-ring-color auto 5px;
  outline-offset: -2px;
}

.btn.focus,
.btn:focus,
.btn:hover {
  color: #333;
  text-decoration: none;
}

.btn.active,
.btn:active {
  outline: 0;
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}

.btn.disabled,
.btn[disabled],
fieldset[disabled] .btn {
  cursor: not-allowed;
  filter: alpha(opacity=65);
  -webkit-box-shadow: none;
  box-shadow: none;
  opacity: 0.65;
}

a.btn.disabled,
fieldset[disabled] a.btn {
  pointer-events: none;
}

.btn-default {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}

.btn-default.focus,
.btn-default:focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}

.btn-default.active,
.btn-default:active,
.btn-default:hover,
.open > .dropdown-toggle.btn-default {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}

.btn-default.active.focus,
.btn-default.active:focus,
.btn-default.active:hover,
.btn-default:active.focus,
.btn-default:active:focus,
.btn-default:active:hover,
.open > .dropdown-toggle.btn-default.focus,
.open > .dropdown-toggle.btn-default:focus,
.open > .dropdown-toggle.btn-default:hover {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}

.btn-default.disabled,
.btn-default.disabled.active,
.btn-default.disabled.focus,
.btn-default.disabled:active,
.btn-default.disabled:focus,
.btn-default.disabled:hover,
.btn-default[disabled],
.btn-default[disabled].active,
.btn-default[disabled].focus,
.btn-default[disabled]:active,
.btn-default[disabled]:focus,
.btn-default[disabled]:hover,
fieldset[disabled] .btn-default,
fieldset[disabled] .btn-default.active,
fieldset[disabled] .btn-default.focus,
fieldset[disabled] .btn-default:active,
fieldset[disabled] .btn-default:focus,
fieldset[disabled] .btn-default:hover {
  background-color: #fff;
  border-color: #ccc;
}

.btn-default .badge {
  color: #fff;
  background-color: #333;
}

.btn-primary {
  color: #fff;
  background-color: #337ab7;
  border-color: #2e6da4;
}

.btn-primary.focus,
.btn-primary:focus {
  color: #fff;
  background-color: #286090;
  border-color: #122b40;
}

.btn-primary.active,
.btn-primary:active,
.btn-primary:hover,
.open > .dropdown-toggle.btn-primary {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}

.btn-primary.active.focus,
.btn-primary.active:focus,
.btn-primary.active:hover,
.btn-primary:active.focus,
.btn-primary:active:focus,
.btn-primary:active:hover,
.open > .dropdown-toggle.btn-primary.focus,
.open > .dropdown-toggle.btn-primary:focus,
.open > .dropdown-toggle.btn-primary:hover {
  color: #fff;
  background-color: #204d74;
  border-color: #122b40;
}

.btn-primary.disabled,
.btn-primary.disabled.active,
.btn-primary.disabled.focus,
.btn-primary.disabled:active,
.btn-primary.disabled:focus,
.btn-primary.disabled:hover,
.btn-primary[disabled],
.btn-primary[disabled].active,
.btn-primary[disabled].focus,
.btn-primary[disabled]:active,
.btn-primary[disabled]:focus,
.btn-primary[disabled]:hover,
fieldset[disabled] .btn-primary,
fieldset[disabled] .btn-primary.active,
fieldset[disabled] .btn-primary.focus,
fieldset[disabled] .btn-primary:active,
fieldset[disabled] .btn-primary:focus,
fieldset[disabled] .btn-primary:hover {
  background-color: #337ab7;
  border-color: #2e6da4;
}

.btn-primary .badge {
  color: #337ab7;
  background-color: #fff;
}

.btn-success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}

.btn-success.focus,
.btn-success:focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}

.btn-success.active,
.btn-success:active,
.btn-success:hover,
.open > .dropdown-toggle.btn-success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}

.btn-success.active.focus,
.btn-success.active:focus,
.btn-success.active:hover,
.btn-success:active.focus,
.btn-success:active:focus,
.btn-success:active:hover,
.open > .dropdown-toggle.btn-success.focus,
.open > .dropdown-toggle.btn-success:focus,
.open > .dropdown-toggle.btn-success:hover {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}

.btn-success.active,
.btn-success:active,
.open > .dropdown-toggle.btn-success {
  background-image: none;
}

.btn-success.disabled,
.btn-success.disabled.active,
.btn-success.disabled.focus,
.btn-success.disabled:active,
.btn-success.disabled:focus,
.btn-success.disabled:hover,
.btn-success[disabled],
.btn-success[disabled].active,
.btn-success[disabled].focus,
.btn-success[disabled]:active,
.btn-success[disabled]:focus,
.btn-success[disabled]:hover,
fieldset[disabled] .btn-success,
fieldset[disabled] .btn-success.active,
fieldset[disabled] .btn-success.focus,
fieldset[disabled] .btn-success:active,
fieldset[disabled] .btn-success:focus,
fieldset[disabled] .btn-success:hover {
  background-color: #5cb85c;
  border-color: #4cae4c;
}

.btn-success .badge {
  color: #5cb85c;
  background-color: #fff;
}

.btn-info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}

.btn-info.focus,
.btn-info:focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}

.btn-info.active,
.btn-info:active,
.btn-info:hover,
.open > .dropdown-toggle.btn-info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}

.btn-info.active.focus,
.btn-info.active:focus,
.btn-info.active:hover,
.btn-info:active.focus,
.btn-info:active:focus,
.btn-info:active:hover,
.open > .dropdown-toggle.btn-info.focus,
.open > .dropdown-toggle.btn-info:focus,
.open > .dropdown-toggle.btn-info:hover {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}

.btn-info.disabled,
.btn-info.disabled.active,
.btn-info.disabled.focus,
.btn-info.disabled:active,
.btn-info.disabled:focus,
.btn-info.disabled:hover,
.btn-info[disabled],
.btn-info[disabled].active,
.btn-info[disabled].focus,
.btn-info[disabled]:active,
.btn-info[disabled]:focus,
.btn-info[disabled]:hover,
fieldset[disabled] .btn-info,
fieldset[disabled] .btn-info.active,
fieldset[disabled] .btn-info.focus,
fieldset[disabled] .btn-info:active,
fieldset[disabled] .btn-info:focus,
fieldset[disabled] .btn-info:hover {
  background-color: #5bc0de;
  border-color: #46b8da;
}

.btn-info .badge {
  color: #5bc0de;
  background-color: #fff;
}

.btn-warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}

.btn-warning.focus,
.btn-warning:focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}

.btn-warning.active,
.btn-warning:active,
.btn-warning:hover,
.open > .dropdown-toggle.btn-warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}

.btn-warning.active.focus,
.btn-warning.active:focus,
.btn-warning.active:hover,
.btn-warning:active.focus,
.btn-warning:active:focus,
.btn-warning:active:hover,
.open > .dropdown-toggle.btn-warning.focus,
.open > .dropdown-toggle.btn-warning:focus,
.open > .dropdown-toggle.btn-warning:hover {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}

.btn-warning.disabled,
.btn-warning.disabled.active,
.btn-warning.disabled.focus,
.btn-warning.disabled:active,
.btn-warning.disabled:focus,
.btn-warning.disabled:hover,
.btn-warning[disabled],
.btn-warning[disabled].active,
.btn-warning[disabled].focus,
.btn-warning[disabled]:active,
.btn-warning[disabled]:focus,
.btn-warning[disabled]:hover,
fieldset[disabled] .btn-warning,
fieldset[disabled] .btn-warning.active,
fieldset[disabled] .btn-warning.focus,
fieldset[disabled] .btn-warning:active,
fieldset[disabled] .btn-warning:focus,
fieldset[disabled] .btn-warning:hover {
  background-color: #f0ad4e;
  border-color: #eea236;
}

.btn-warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}

.btn-danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}

.btn-danger.focus,
.btn-danger:focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}

.btn-danger.active,
.btn-danger:active,
.btn-danger:hover,
.open > .dropdown-toggle.btn-danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}

.btn-danger.active.focus,
.btn-danger.active:focus,
.btn-danger.active:hover,
.btn-danger:active.focus,
.btn-danger:active:focus,
.btn-danger:active:hover,
.open > .dropdown-toggle.btn-danger.focus,
.open > .dropdown-toggle.btn-danger:focus,
.open > .dropdown-toggle.btn-danger:hover {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}

.btn-danger.disabled,
.btn-danger.disabled.active,
.btn-danger.disabled.focus,
.btn-danger.disabled:active,
.btn-danger.disabled:focus,
.btn-danger.disabled:hover,
.btn-danger[disabled],
.btn-danger[disabled].active,
.btn-danger[disabled].focus,
.btn-danger[disabled]:active,
.btn-danger[disabled]:focus,
.btn-danger[disabled]:hover,
fieldset[disabled] .btn-danger,
fieldset[disabled] .btn-danger.active,
fieldset[disabled] .btn-danger.focus,
fieldset[disabled] .btn-danger:active,
fieldset[disabled] .btn-danger:focus,
fieldset[disabled] .btn-danger:hover {
  background-color: #d9534f;
  border-color: #d43f3a;
}

.btn-danger .badge {
  color: #d9534f;
  background-color: #fff;
}

.btn-link {
  font-weight: 400;
  color: #337ab7;
  border-radius: 0;
}

.btn-link,
.btn-link.active,
.btn-link:active,
.btn-link[disabled],
fieldset[disabled] .btn-link {
  background-color: transparent;
  -webkit-box-shadow: none;
  box-shadow: none;
}

.btn-link,
.btn-link:active,
.btn-link:focus,
.btn-link:hover {
  border-color: transparent;
}

.btn-link:focus,
.btn-link:hover {
  color: #23527c;
  text-decoration: underline;
  background-color: transparent;
}

.btn-link[disabled]:focus,
.btn-link[disabled]:hover,
fieldset[disabled] .btn-link:focus,
fieldset[disabled] .btn-link:hover {
  color: #777;
  text-decoration: none;
}

.btn-group-lg > .btn,
.btn-lg {
  padding: 10px 16px;
  font-size: 18px;
  line-height: 1.3333333;
  border-radius: 6px;
}

.btn-group-sm > .btn,
.btn-sm {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 3px;
}

.btn-group-xs > .btn,
.btn-xs {
  padding: 1px 5px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 3px;
}

.btn-block {
  display: block;
  width: 100%;
}

.btn-block + .btn-block {
  margin-top: 5px;
}

input[type="button"].btn-block,
input[type="reset"].btn-block,
input[type="submit"].btn-block {
  width: 100%;
}

.fade {
  opacity: 0;
  -webkit-transition: opacity 0.15s linear;
  -o-transition: opacity 0.15s linear;
  transition: opacity 0.15s linear;
}

.fade.in {
  opacity: 1;
}

.collapse {
  display: none;
}

.collapse.in {
  display: block;
}

tr.collapse.in {
  display: table-row;
}

tbody.collapse.in {
  display: table-row-group;
}

.collapsing {
  height: 0;
  overflow: hidden;
  -webkit-transition-timing-function: ease;
  -o-transition-timing-function: ease;
  transition-timing-function: ease;
  -webkit-transition-duration: 0.35s;
  -o-transition-duration: 0.35s;
  transition-duration: 0.35s;
  -webkit-transition-property: height, visibility;
  -o-transition-property: height, visibility;
  transition-property: height, visibility;
}

.caret {
  display: inline-block;
  width: 0;
  height: 0;
  margin-left: 2px;
  border-top: 4px dashed;
  border-top: 4px solid\9;
  border-right: 4px solid transparent;
  border-left: 4px solid transparent;
}

.dropdown-toggle:focus {
  outline: 0;
}

.dropdown-menu {
  position: absolute;
  top: 100%;
  left: 0;
  z-index: 1000;
  display: none;
  min-width: 160px;
  padding: 5px 0;
  margin: 2px 0 0;
  font-size: 14px;
  text-align: left;
  list-style: none;
  background-color: #fff;
  background-clip: padding-box;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.15);
  border-radius: 4px;
  -webkit-box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
}

.dropdown-menu-right,
.dropdown-menu.pull-right {
  right: 0;
  left: auto;
}

.dropdown-header,
.dropdown-menu > li > a {
  display: block;
  padding: 3px 20px;
  line-height: 1.42857143;
  white-space: nowrap;
}

.btn-group-vertical > .btn:not(:first-child):not(:last-child),
.btn-group > .btn-group:not(:first-child):not(:last-child) > .btn,
.btn-group > .btn:not(:first-child):not(:last-child):not(.dropdown-toggle) {
  border-radius: 0;
}

.dropdown-menu .divider {
  height: 1px;
  margin: 9px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}

.dropdown-menu > li > a {
  clear: both;
  font-weight: 400;
  color: #333;
}

.dropdown-menu > li > a:focus,
.dropdown-menu > li > a:hover {
  color: #262626;
  text-decoration: none;
  background-color: #f5f5f5;
}

.dropdown-menu > .active > a,
.dropdown-menu > .active > a:focus,
.dropdown-menu > .active > a:hover {
  color: #fff;
  text-decoration: none;
  background-color: #337ab7;
  outline: 0;
}

.dropdown-menu > .disabled > a,
.dropdown-menu > .disabled > a:focus,
.dropdown-menu > .disabled > a:hover {
  color: #777;
}

.dropdown-menu > .disabled > a:focus,
.dropdown-menu > .disabled > a:hover {
  text-decoration: none;
  cursor: not-allowed;
  background-color: transparent;
  filter: progid:DXImageTransform.Microsoft.gradient(enabled=false);
}

.open > .dropdown-menu {
  display: block;
}

.open > a {
  outline: 0;
}

.dropdown-menu-left {
  right: auto;
  left: 0;
}

.dropdown-header {
  font-size: 12px;
  color: #777;
}

.dropdown-backdrop {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 990;
}

.nav-justified > .dropdown .dropdown-menu,
.nav-tabs.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}

.pull-right > .dropdown-menu {
  right: 0;
  left: auto;
}

.dropup .caret,
.navbar-fixed-bottom .dropdown .caret {
  content: "";
  border-top: 0;
  border-bottom: 4px dashed;
  border-bottom: 4px solid\9;
}

.dropup .dropdown-menu,
.navbar-fixed-bottom .dropdown .dropdown-menu {
  top: auto;
  bottom: 100%;
  margin-bottom: 2px;
}

@media (min-width: 768px) {
  .navbar-right .dropdown-menu {
    right: 0;
    left: auto;
  }

  .navbar-right .dropdown-menu-left {
    right: auto;
    left: 0;
  }
}

.btn-group,
.btn-group-vertical {
  position: relative;
  display: inline-block;
}

.btn-group-vertical > .btn,
.btn-group > .btn {
  position: relative;
  float: left;
}

.btn-group-vertical > .btn.active,
.btn-group-vertical > .btn:active,
.btn-group-vertical > .btn:focus,
.btn-group-vertical > .btn:hover,
.btn-group > .btn.active,
.btn-group > .btn:active,
.btn-group > .btn:focus,
.btn-group > .btn:hover {
  z-index: 2;
}

.btn-group .btn + .btn,
.btn-group .btn + .btn-group,
.btn-group .btn-group + .btn,
.btn-group .btn-group + .btn-group {
  margin-left: -1px;
}

.btn-toolbar {
  margin-left: -5px;
}

.btn-toolbar > .btn,
.btn-toolbar > .btn-group,
.btn-toolbar > .input-group {
  margin-left: 5px;
}

.btn .caret,
.btn-group > .btn:first-child {
  margin-left: 0;
}

.btn-group > .btn:first-child:not(:last-child):not(.dropdown-toggle) {
  border-top-right-radius: 0;
  border-bottom-right-radius: 0;
}

.btn-group > .btn:last-child:not(:first-child),
.btn-group > .dropdown-toggle:not(:first-child) {
  border-top-left-radius: 0;
  border-bottom-left-radius: 0;
}

.btn-group > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-top-right-radius: 0;
  border-bottom-right-radius: 0;
}

.btn-group > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-top-left-radius: 0;
  border-bottom-left-radius: 0;
}

.btn-group .dropdown-toggle:active,
.btn-group.open .dropdown-toggle {
  outline: 0;
}

.btn-group > .btn + .dropdown-toggle {
  padding-right: 8px;
  padding-left: 8px;
}

.btn-group > .btn-lg + .dropdown-toggle {
  padding-right: 12px;
  padding-left: 12px;
}

.btn-group.open .dropdown-toggle {
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}

.btn-group.open .dropdown-toggle.btn-link {
  -webkit-box-shadow: none;
  box-shadow: none;
}

.btn-lg .caret {
  border-width: 5px 5px 0;
}

.dropup .btn-lg .caret {
  border-width: 0 5px 5px;
}

.btn-group-vertical > .btn,
.btn-group-vertical > .btn-group,
.btn-group-vertical > .btn-group > .btn {
  display: block;
  float: none;
  width: 100%;
  max-width: 100%;
}

.btn-group-vertical > .btn-group > .btn {
  float: none;
}

.btn-group-vertical > .btn + .btn,
.btn-group-vertical > .btn + .btn-group,
.btn-group-vertical > .btn-group + .btn,
.btn-group-vertical > .btn-group + .btn-group {
  margin-top: -1px;
  margin-left: 0;
}

.btn-group-vertical > .btn:first-child:not(:last-child) {
  border-top-right-radius: 4px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}

.btn-group-vertical > .btn:last-child:not(:first-child) {
  border-top-left-radius: 0;
  border-top-right-radius: 0;
  border-bottom-left-radius: 4px;
}

.btn-group-vertical > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}

.btn-group-vertical > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group-vertical
  > .btn-group:first-child:not(:last-child)
  > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}

.btn-group-vertical
  > .btn-group:last-child:not(:first-child)
  > .btn:first-child {
  border-top-left-radius: 0;
  border-top-right-radius: 0;
}

.btn-group-justified {
  display: table;
  width: 100%;
  table-layout: fixed;
  border-collapse: separate;
}

.btn-group-justified > .btn,
.btn-group-justified > .btn-group {
  display: table-cell;
  float: none;
  width: 1%;
}

.btn-group-justified > .btn-group .btn {
  width: 100%;
}

.btn-group-justified > .btn-group .dropdown-menu {
  left: auto;
}

[data-toggle="buttons"] > .btn input[type="checkbox"],
[data-toggle="buttons"] > .btn input[type="radio"],
[data-toggle="buttons"] > .btn-group > .btn input[type="checkbox"],
[data-toggle="buttons"] > .btn-group > .btn input[type="radio"] {
  position: absolute;
  clip: rect(0, 0, 0, 0);
  pointer-events: none;
}

.input-group {
  position: relative;
  display: table;
  border-collapse: separate;
}

.input-group[class*="col-"] {
  float: none;
  padding-right: 0;
  padding-left: 0;
}

.input-group .form-control {
  position: relative;
  z-index: 2;
  float: left;
  width: 100%;
  margin-bottom: 0;
}

.input-group-lg > .form-control,
.input-group-lg > .input-group-addon,
.input-group-lg > .input-group-btn > .btn {
  height: 46px;
  padding: 10px 16px;
  font-size: 18px;
  line-height: 1.3333333;
  border-radius: 6px;
}

select.input-group-lg > .form-control,
select.input-group-lg > .input-group-addon,
select.input-group-lg > .input-group-btn > .btn {
  height: 46px;
  line-height: 46px;
}

select[multiple].input-group-lg > .form-control,
select[multiple].input-group-lg > .input-group-addon,
select[multiple].input-group-lg > .input-group-btn > .btn,
textarea.input-group-lg > .form-control,
textarea.input-group-lg > .input-group-addon,
textarea.input-group-lg > .input-group-btn > .btn {
  height: auto;
}

.input-group-sm > .form-control,
.input-group-sm > .input-group-addon,
.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 3px;
}

select.input-group-sm > .form-control,
select.input-group-sm > .input-group-addon,
select.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  line-height: 30px;
}

select[multiple].input-group-sm > .form-control,
select[multiple].input-group-sm > .input-group-addon,
select[multiple].input-group-sm > .input-group-btn > .btn,
textarea.input-group-sm > .form-control,
textarea.input-group-sm > .input-group-addon,
textarea.input-group-sm > .input-group-btn > .btn {
  height: auto;
}

.input-group .form-control,
.input-group-addon,
.input-group-btn {
  display: table-cell;
}

.nav > li,
.nav > li > a {
  display: block;
  position: relative;
}

.input-group .form-control:not(:first-child):not(:last-child),
.input-group-addon:not(:first-child):not(:last-child),
.input-group-btn:not(:first-child):not(:last-child) {
  border-radius: 0;
}

.input-group-addon,
.input-group-btn {
  width: 1%;
  white-space: nowrap;
  vertical-align: middle;
}

.input-group-addon {
  padding: 6px 12px;
  font-size: 14px;
  font-weight: 400;
  line-height: 1;
  color: #555;
  text-align: center;
  background-color: #eee;
  border: 1px solid #ccc;
  border-radius: 4px;
}

.input-group-addon.input-sm {
  padding: 5px 10px;
  font-size: 12px;
  border-radius: 3px;
}

.input-group-addon.input-lg {
  padding: 10px 16px;
  font-size: 18px;
  border-radius: 6px;
}

.input-group-addon input[type="checkbox"],
.input-group-addon input[type="radio"] {
  margin-top: 0;
}

.input-group .form-control:first-child,
.input-group-addon:first-child,
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group > .btn,
.input-group-btn:first-child > .dropdown-toggle,
.input-group-btn:last-child > .btn-group:not(:last-child) > .btn,
.input-group-btn:last-child > .btn:not(:last-child):not(.dropdown-toggle) {
  border-top-right-radius: 0;
  border-bottom-right-radius: 0;
}

.input-group-addon:first-child {
  border-right: 0;
}

.input-group .form-control:last-child,
.input-group-addon:last-child,
.input-group-btn:first-child > .btn-group:not(:first-child) > .btn,
.input-group-btn:first-child > .btn:not(:first-child),
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group > .btn,
.input-group-btn:last-child > .dropdown-toggle {
  border-top-left-radius: 0;
  border-bottom-left-radius: 0;
}

.input-group-addon:last-child {
  border-left: 0;
}

.input-group-btn {
  position: relative;
  font-size: 0;
  white-space: nowrap;
}

.input-group-btn > .btn {
  position: relative;
}

.input-group-btn > .btn + .btn {
  margin-left: -1px;
}

.input-group-btn > .btn:active,
.input-group-btn > .btn:focus,
.input-group-btn > .btn:hover {
  z-index: 2;
}

.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group {
  margin-right: -1px;
}

.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group {
  z-index: 2;
  margin-left: -1px;
}

.nav {
  padding-left: 0;
  margin-bottom: 0;
  list-style: none;
}

.nav > li > a {
  padding: 10px 15px;
}

.nav > li > a:focus,
.nav > li > a:hover {
  text-decoration: none;
  background-color: #eee;
}

.nav > li.disabled > a {
  color: #777;
}

.nav > li.disabled > a:focus,
.nav > li.disabled > a:hover {
  color: #777;
  text-decoration: none;
  cursor: not-allowed;
  background-color: transparent;
}

.nav .open > a,
.nav .open > a:focus,
.nav .open > a:hover {
  background-color: #eee;
  border-color: #337ab7;
}

.nav .nav-divider {
  height: 1px;
  margin: 9px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}

.nav > li > a > img {
  max-width: none;
}

.nav-tabs {
  border-bottom: 1px solid #ddd;
}

.nav-tabs > li {
  float: left;
  margin-bottom: -1px;
}

.nav-tabs > li > a {
  margin-right: 2px;
  line-height: 1.42857143;
  border: 1px solid transparent;
  border-radius: 4px 4px 0 0;
}

.nav-tabs > li > a:hover {
  border-color: #eee #eee #ddd;
}

.nav-tabs > li.active > a,
.nav-tabs > li.active > a:focus,
.nav-tabs > li.active > a:hover {
  color: #555;
  cursor: default;
  background-color: #fff;
  border: 1px solid #ddd;
  border-bottom-color: transparent;
}

.nav-tabs.nav-justified {
  width: 100%;
  border-bottom: 0;
}

.nav-tabs.nav-justified > li {
  float: none;
}

.nav-tabs.nav-justified > li > a {
  margin-bottom: 5px;
  text-align: center;
  margin-right: 0;
  border-radius: 4px;
}

.nav-tabs.nav-justified > .active > a,
.nav-tabs.nav-justified > .active > a:focus,
.nav-tabs.nav-justified > .active > a:hover {
  border: 1px solid #ddd;
}

@media (min-width: 768px) {
  .nav-tabs.nav-justified > li {
    display: table-cell;
    width: 1%;
  }

  .nav-tabs.nav-justified > li > a {
    margin-bottom: 0;
    border-bottom: 1px solid #ddd;
    border-radius: 4px 4px 0 0;
  }

  .nav-tabs.nav-justified > .active > a,
  .nav-tabs.nav-justified > .active > a:focus,
  .nav-tabs.nav-justified > .active > a:hover {
    border-bottom-color: #fff;
  }
}

.nav-pills > li {
  float: left;
}

.nav-justified > li,
.nav-stacked > li {
  float: none;
}

.nav-pills > li > a {
  border-radius: 4px;
}

.nav-pills > li + li {
  margin-left: 2px;
}

.nav-pills > li.active > a,
.nav-pills > li.active > a:focus,
.nav-pills > li.active > a:hover {
  color: #fff;
  background-color: #337ab7;
}

.nav-stacked > li + li {
  margin-top: 2px;
  margin-left: 0;
}

.nav-justified {
  width: 100%;
}

.nav-justified > li > a {
  margin-bottom: 5px;
  text-align: center;
}

.nav-tabs-justified {
  border-bottom: 0;
}

.nav-tabs-justified > li > a {
  margin-right: 0;
  border-radius: 4px;
}

.nav-tabs-justified > .active > a,
.nav-tabs-justified > .active > a:focus,
.nav-tabs-justified > .active > a:hover {
  border: 1px solid #ddd;
}

@media (min-width: 768px) {
  .nav-justified > li {
    display: table-cell;
    width: 1%;
  }

  .nav-justified > li > a {
    margin-bottom: 0;
  }

  .nav-tabs-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 4px 4px 0 0;
  }

  .nav-tabs-justified > .active > a,
  .nav-tabs-justified > .active > a:focus,
  .nav-tabs-justified > .active > a:hover {
    border-bottom-color: #fff;
  }
}

.tab-content > .tab-pane {
  display: none;
}

.tab-content > .active {
  display: block;
}

.nav-tabs .dropdown-menu {
  margin-top: -1px;
  border-top-left-radius: 0;
  border-top-right-radius: 0;
}

.navbar {
  position: relative;
  min-height: 50px;
  margin-bottom: 20px;
  border: 1px solid transparent;
}

.navbar-collapse {
  padding-right: 15px;
  padding-left: 15px;
  overflow-x: visible;
  -webkit-overflow-scrolling: touch;
  border-top: 1px solid transparent;
  -webkit-box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1);
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1);
}

.navbar-collapse.in {
  overflow-y: auto;
}

@media (min-width: 768px) {
  .navbar {
    border-radius: 4px;
  }

  .navbar-header {
    float: left;
  }

  .navbar-collapse {
    width: auto;
    border-top: 0;
    -webkit-box-shadow: none;
    box-shadow: none;
  }

  .navbar-collapse.collapse {
    display: block !important;
    height: auto !important;
    padding-bottom: 0;
    overflow: visible !important;
  }

  .navbar-collapse.in {
    overflow-y: visible;
  }

  .navbar-fixed-bottom .navbar-collapse,
  .navbar-fixed-top .navbar-collapse,
  .navbar-static-top .navbar-collapse {
    padding-right: 0;
    padding-left: 0;
  }
}

.embed-responsive,
.modal,
.modal-open,
.progress {
  overflow: hidden;
}

@media (max-device-width: 480px) and (orientation: landscape) {
  .navbar-fixed-bottom .navbar-collapse,
  .navbar-fixed-top .navbar-collapse {
    max-height: 200px;
  }
}

.container-fluid > .navbar-collapse,
.container-fluid > .navbar-header,
.container > .navbar-collapse,
.container > .navbar-header {
  margin-right: -15px;
  margin-left: -15px;
}

.navbar-static-top {
  z-index: 1000;
  border-width: 0 0 1px;
}

.navbar-fixed-bottom,
.navbar-fixed-top {
  position: fixed;
  right: 0;
  left: 0;
  z-index: 1030;
}

.navbar-fixed-top {
  top: 0;
  border-width: 0 0 1px;
}

.navbar-fixed-bottom {
  bottom: 0;
  margin-bottom: 0;
  border-width: 1px 0 0;
}

.navbar-brand {
  float: left;
  height: 50px;
  padding: 15px;
  font-size: 18px;
  line-height: 20px;
}

.navbar-brand:focus,
.navbar-brand:hover {
  text-decoration: none;
}

.navbar-brand > img {
  display: block;
}

@media (min-width: 768px) {
  .container-fluid > .navbar-collapse,
  .container-fluid > .navbar-header,
  .container > .navbar-collapse,
  .container > .navbar-header {
    margin-right: 0;
    margin-left: 0;
  }

  .navbar-fixed-bottom,
  .navbar-fixed-top,
  .navbar-static-top {
    border-radius: 0;
  }

  .navbar > .container .navbar-brand,
  .navbar > .container-fluid .navbar-brand {
    margin-left: -15px;
  }
}

.navbar-toggle {
  position: relative;
  float: right;
  padding: 9px 10px;
  margin-top: 8px;
  margin-right: 15px;
  margin-bottom: 8px;
  background-color: transparent;
  border: 1px solid transparent;
  border-radius: 4px;
}

.navbar-toggle:focus {
  outline: 0;
}

.navbar-toggle .icon-bar {
  display: block;
  width: 22px;
  height: 2px;
  border-radius: 1px;
}

.navbar-toggle .icon-bar + .icon-bar {
  margin-top: 4px;
}

.navbar-nav {
  margin: 7.5px -15px;
}

.navbar-nav > li > a {
  padding-top: 10px;
  padding-bottom: 10px;
  line-height: 20px;
}

@media (max-width: 767px) {
  .navbar-nav .open .dropdown-menu {
    position: static;
    float: none;
    width: auto;
    margin-top: 0;
    background-color: transparent;
    border: 0;
    -webkit-box-shadow: none;
    box-shadow: none;
  }

  .navbar-nav .open .dropdown-menu .dropdown-header,
  .navbar-nav .open .dropdown-menu > li > a {
    padding: 5px 15px 5px 25px;
  }

  .navbar-nav .open .dropdown-menu > li > a {
    line-height: 20px;
  }

  .navbar-nav .open .dropdown-menu > li > a:focus,
  .navbar-nav .open .dropdown-menu > li > a:hover {
    background-image: none;
  }
}

.progress-bar-striped,
.progress-striped .progress-bar,
.progress-striped .progress-bar-success {
  background-image: -webkit-linear-gradient(
    45deg,
    rgba(255, 255, 255, 0.15) 25%,
    transparent 25%,
    transparent 50%,
    rgba(255, 255, 255, 0.15) 50%,
    rgba(255, 255, 255, 0.15) 75%,
    transparent 75%,
    transparent
  );
  background-image: -o-linear-gradient(
    45deg,
    rgba(255, 255, 255, 0.15) 25%,
    transparent 25%,
    transparent 50%,
    rgba(255, 255, 255, 0.15) 50%,
    rgba(255, 255, 255, 0.15) 75%,
    transparent 75%,
    transparent
  );
}

@media (min-width: 768px) {
  .navbar-toggle {
    display: none;
  }

  .navbar-nav {
    float: left;
    margin: 0;
  }

  .navbar-nav > li {
    float: left;
  }

  .navbar-nav > li > a {
    padding-top: 15px;
    padding-bottom: 15px;
  }
}

.navbar-form {
  padding: 10px 15px;
  border-top: 1px solid transparent;
  border-bottom: 1px solid transparent;
  -webkit-box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1),
    0 1px 0 rgba(255, 255, 255, 0.1);
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1),
    0 1px 0 rgba(255, 255, 255, 0.1);
  margin: 8px -15px;
}

@media (min-width: 768px) {
  .navbar-form .form-control-static,
  .navbar-form .form-group {
    display: inline-block;
  }

  .navbar-form .control-label,
  .navbar-form .form-group {
    margin-bottom: 0;
    vertical-align: middle;
  }

  .navbar-form .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }

  .navbar-form .input-group {
    display: inline-table;
    vertical-align: middle;
  }

  .navbar-form .input-group .form-control,
  .navbar-form .input-group .input-group-addon,
  .navbar-form .input-group .input-group-btn {
    width: auto;
  }

  .navbar-form .input-group > .form-control {
    width: 100%;
  }

  .navbar-form .checkbox,
  .navbar-form .radio {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }

  .navbar-form .checkbox label,
  .navbar-form .radio label {
    padding-left: 0;
  }

  .navbar-form .checkbox input[type="checkbox"],
  .navbar-form .radio input[type="radio"] {
    position: relative;
    margin-left: 0;
  }

  .navbar-form .has-feedback .form-control-feedback {
    top: 0;
  }

  .navbar-form {
    width: auto;
    padding-top: 0;
    padding-bottom: 0;
    margin-right: 0;
    margin-left: 0;
    border: 0;
    -webkit-box-shadow: none;
    box-shadow: none;
  }
}

.breadcrumb > li,
.pagination {
  display: inline-block;
}

.btn .badge,
.btn .label {
  top: -1px;
  position: relative;
}

@media (max-width: 767px) {
  .navbar-form .form-group {
    margin-bottom: 5px;
  }

  .navbar-form .form-group:last-child {
    margin-bottom: 0;
  }
}

.navbar-nav > li > .dropdown-menu {
  margin-top: 0;
  border-top-left-radius: 0;
  border-top-right-radius: 0;
}

.navbar-fixed-bottom .navbar-nav > li > .dropdown-menu {
  margin-bottom: 0;
  border-radius: 4px 4px 0 0;
}

.navbar-btn {
  margin-top: 8px;
  margin-bottom: 8px;
}

.navbar-btn.btn-sm {
  margin-top: 10px;
  margin-bottom: 10px;
}

.navbar-btn.btn-xs {
  margin-top: 14px;
  margin-bottom: 14px;
}

.media,
.navbar-text {
  margin-top: 15px;
}

.navbar-text {
  margin-bottom: 15px;
}

@media (min-width: 768px) {
  .navbar-text {
    float: left;
    margin-right: 15px;
    margin-left: 15px;
  }

  .navbar-left {
    float: left !important;
  }

  .navbar-right {
    float: right !important;
    margin-right: -15px;
  }

  .navbar-right ~ .navbar-right {
    margin-right: 0;
  }
}

.navbar-default {
  background-color: #f8f8f8;
  border-color: #e7e7e7;
}

.navbar-default .navbar-brand {
  color: #777;
}

.navbar-default .navbar-brand:focus,
.navbar-default .navbar-brand:hover {
  color: #5e5e5e;
  background-color: transparent;
}

.navbar-default .navbar-nav > li > a,
.navbar-default .navbar-text {
  color: #777;
}

.navbar-default .navbar-nav > li > a:focus,
.navbar-default .navbar-nav > li > a:hover {
  color: #333;
  background-color: transparent;
}

.navbar-default .navbar-nav > .active > a,
.navbar-default .navbar-nav > .active > a:focus,
.navbar-default .navbar-nav > .active > a:hover {
  color: #555;
  background-color: #e7e7e7;
}

.navbar-default .navbar-nav > .disabled > a,
.navbar-default .navbar-nav > .disabled > a:focus,
.navbar-default .navbar-nav > .disabled > a:hover {
  color: #ccc;
  background-color: transparent;
}

.navbar-default .navbar-toggle {
  border-color: #ddd;
}

.navbar-default .navbar-toggle:focus,
.navbar-default .navbar-toggle:hover {
  background-color: #ddd;
}

.navbar-default .navbar-toggle .icon-bar {
  background-color: #888;
}

.navbar-default .navbar-collapse,
.navbar-default .navbar-form {
  border-color: #e7e7e7;
}

.navbar-default .navbar-nav > .open > a,
.navbar-default .navbar-nav > .open > a:focus,
.navbar-default .navbar-nav > .open > a:hover {
  color: #555;
  background-color: #e7e7e7;
}

@media (max-width: 767px) {
  .navbar-default .navbar-nav .open .dropdown-menu > li > a {
    color: #777;
  }

  .navbar-default .navbar-nav .open .dropdown-menu > li > a:focus,
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:hover {
    color: #333;
    background-color: transparent;
  }

  .navbar-default .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:focus,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:hover {
    color: #555;
    background-color: #e7e7e7;
  }

  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:focus,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:hover {
    color: #ccc;
    background-color: transparent;
  }
}

.navbar-default .navbar-link {
  color: #777;
}

.navbar-default .navbar-link:hover {
  color: #333;
}

.navbar-default .btn-link {
  color: #777;
}

.navbar-default .btn-link:focus,
.navbar-default .btn-link:hover {
  color: #333;
}

.navbar-default .btn-link[disabled]:focus,
.navbar-default .btn-link[disabled]:hover,
fieldset[disabled] .navbar-default .btn-link:focus,
fieldset[disabled] .navbar-default .btn-link:hover {
  color: #ccc;
}

.navbar-inverse {
  background-color: #222;
  border-color: #080808;
}

.navbar-inverse .navbar-brand {
  color: #9d9d9d;
}

.navbar-inverse .navbar-brand:focus,
.navbar-inverse .navbar-brand:hover {
  color: #fff;
  background-color: transparent;
}

.navbar-inverse .navbar-nav > li > a,
.navbar-inverse .navbar-text {
  color: #9d9d9d;
}

.navbar-inverse .navbar-nav > li > a:focus,
.navbar-inverse .navbar-nav > li > a:hover {
  color: #fff;
  background-color: transparent;
}

.navbar-inverse .navbar-nav > .active > a,
.navbar-inverse .navbar-nav > .active > a:focus,
.navbar-inverse .navbar-nav > .active > a:hover {
  color: #fff;
  background-color: #080808;
}

.navbar-inverse .navbar-nav > .disabled > a,
.navbar-inverse .navbar-nav > .disabled > a:focus,
.navbar-inverse .navbar-nav > .disabled > a:hover {
  color: #444;
  background-color: transparent;
}

.navbar-inverse .navbar-toggle {
  border-color: #333;
}

.navbar-inverse .navbar-toggle:focus,
.navbar-inverse .navbar-toggle:hover {
  background-color: #333;
}

.navbar-inverse .navbar-toggle .icon-bar {
  background-color: #fff;
}

.navbar-inverse .navbar-collapse,
.navbar-inverse .navbar-form {
  border-color: #101010;
}

.navbar-inverse .navbar-nav > .open > a,
.navbar-inverse .navbar-nav > .open > a:focus,
.navbar-inverse .navbar-nav > .open > a:hover {
  color: #fff;
  background-color: #080808;
}

@media (max-width: 767px) {
  .navbar-inverse .navbar-nav .open .dropdown-menu > .dropdown-header {
    border-color: #080808;
  }

  .navbar-inverse .navbar-nav .open .dropdown-menu .divider {
    background-color: #080808;
  }

  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a {
    color: #9d9d9d;
  }

  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:focus,
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:hover {
    color: #fff;
    background-color: transparent;
  }

  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:focus,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:hover {
    color: #fff;
    background-color: #080808;
  }

  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:focus,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:hover {
    color: #444;
    background-color: transparent;
  }
}

.navbar-inverse .navbar-link {
  color: #9d9d9d;
}

.navbar-inverse .navbar-link:hover {
  color: #fff;
}

.navbar-inverse .btn-link {
  color: #9d9d9d;
}

.navbar-inverse .btn-link:focus,
.navbar-inverse .btn-link:hover {
  color: #fff;
}

.navbar-inverse .btn-link[disabled]:focus,
.navbar-inverse .btn-link[disabled]:hover,
fieldset[disabled] .navbar-inverse .btn-link:focus,
fieldset[disabled] .navbar-inverse .btn-link:hover {
  color: #444;
}

.breadcrumb {
  padding: 8px 15px;
  margin-bottom: 20px;
  list-style: none;
  background-color: #f5f5f5;
  border-radius: 4px;
}

.breadcrumb > li + li:before {
  padding: 0 5px;
  color: #ccc;
  content: "/\00a0";
}

.breadcrumb > .active {
  color: #777;
}

.pagination {
  padding-left: 0;
  margin: 20px 0;
  border-radius: 4px;
}

.pager li,
.pagination > li {
  display: inline;
}

.pagination > li > a,
.pagination > li > span {
  position: relative;
  float: left;
  padding: 6px 12px;
  margin-left: -1px;
  line-height: 1.42857143;
  color: #337ab7;
  text-decoration: none;
  background-color: #fff;
  border: 1px solid #ddd;
}

.pagination > li:first-child > a,
.pagination > li:first-child > span {
  margin-left: 0;
  border-top-left-radius: 4px;
  border-bottom-left-radius: 4px;
}

.pagination > li:last-child > a,
.pagination > li:last-child > span {
  border-top-right-radius: 4px;
  border-bottom-right-radius: 4px;
}

.pagination > li > a:focus,
.pagination > li > a:hover,
.pagination > li > span:focus,
.pagination > li > span:hover {
  z-index: 3;
  color: #23527c;
  background-color: #eee;
  border-color: #ddd;
}

.pagination > .active > a,
.pagination > .active > a:focus,
.pagination > .active > a:hover,
.pagination > .active > span,
.pagination > .active > span:focus,
.pagination > .active > span:hover {
  z-index: 2;
  color: #fff;
  cursor: default;
  background-color: #337ab7;
  border-color: #337ab7;
}

.pagination > .disabled > a,
.pagination > .disabled > a:focus,
.pagination > .disabled > a:hover,
.pagination > .disabled > span,
.pagination > .disabled > span:focus,
.pagination > .disabled > span:hover {
  color: #777;
  cursor: not-allowed;
  background-color: #fff;
  border-color: #ddd;
}

.pagination-lg > li > a,
.pagination-lg > li > span {
  padding: 10px 16px;
  font-size: 18px;
  line-height: 1.3333333;
}

.pagination-lg > li:first-child > a,
.pagination-lg > li:first-child > span {
  border-top-left-radius: 6px;
  border-bottom-left-radius: 6px;
}

.pagination-lg > li:last-child > a,
.pagination-lg > li:last-child > span {
  border-top-right-radius: 6px;
  border-bottom-right-radius: 6px;
}

.pagination-sm > li > a,
.pagination-sm > li > span {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
}

.badge,
.label {
  font-weight: 700;
  line-height: 1;
  white-space: nowrap;
  text-align: center;
}

.pagination-sm > li:first-child > a,
.pagination-sm > li:first-child > span {
  border-top-left-radius: 3px;
  border-bottom-left-radius: 3px;
}

.pagination-sm > li:last-child > a,
.pagination-sm > li:last-child > span {
  border-top-right-radius: 3px;
  border-bottom-right-radius: 3px;
}

.pager {
  padding-left: 0;
  margin: 20px 0;
  text-align: center;
  list-style: none;
}

.pager li > a,
.pager li > span {
  display: inline-block;
  padding: 5px 14px;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 15px;
}

.pager li > a:focus,
.pager li > a:hover {
  text-decoration: none;
  background-color: #eee;
}

.pager .next > a,
.pager .next > span {
  float: right;
}

.pager .previous > a,
.pager .previous > span {
  float: left;
}

.pager .disabled > a,
.pager .disabled > a:focus,
.pager .disabled > a:hover,
.pager .disabled > span {
  color: #777;
  cursor: not-allowed;
  background-color: #fff;
}

.label {
  display: inline;
  padding: 0.2em 0.6em 0.3em;
  font-size: 75%;
  color: #fff;
  border-radius: 0.25em;
}

a.label:focus,
a.label:hover {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}

.label:empty {
  display: none;
}

.label-default {
  background-color: #777;
}

.label-default[href]:focus,
.label-default[href]:hover {
  background-color: #5e5e5e;
}

.label-primary {
  background-color: #337ab7;
}

.label-primary[href]:focus,
.label-primary[href]:hover {
  background-color: #286090;
}

.label-success {
  background-color: #5cb85c;
}

.label-success[href]:focus,
.label-success[href]:hover {
  background-color: #449d44;
}

.label-info {
  background-color: #5bc0de;
}

.label-info[href]:focus,
.label-info[href]:hover {
  background-color: #31b0d5;
}

.label-warning {
  background-color: #f0ad4e;
}

.label-warning[href]:focus,
.label-warning[href]:hover {
  background-color: #ec971f;
}

.label-danger {
  background-color: #d9534f;
}

.label-danger[href]:focus,
.label-danger[href]:hover {
  background-color: #c9302c;
}

.badge {
  display: inline-block;
  min-width: 10px;
  padding: 3px 7px;
  font-size: 12px;
  color: #fff;
  vertical-align: middle;
  background-color: #777;
  border-radius: 10px;
}

.badge:empty {
  display: none;
}

.media-object,
.thumbnail {
  display: block;
}

.btn-group-xs > .btn .badge,
.btn-xs .badge {
  top: 0;
  padding: 1px 5px;
}

a.badge:focus,
a.badge:hover {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}

.list-group-item.active > .badge,
.nav-pills > .active > a > .badge {
  color: #337ab7;
  background-color: #fff;
}

.jumbotron,
.jumbotron .h1,
.jumbotron h1 {
  color: inherit;
}

.list-group-item > .badge {
  float: right;
}

.list-group-item > .badge + .badge {
  margin-right: 5px;
}

.nav-pills > li > a > .badge {
  margin-left: 3px;
}

.jumbotron {
  padding-top: 30px;
  padding-bottom: 30px;
  margin-bottom: 30px;
  background-color: #eee;
}

.jumbotron p {
  margin-bottom: 15px;
  font-size: 21px;
  font-weight: 200;
}

.alert,
.thumbnail {
  margin-bottom: 20px;
}

.alert .alert-link,
.close {
  font-weight: 700;
}

.jumbotron > hr {
  border-top-color: #d5d5d5;
}

.container .jumbotron,
.container-fluid .jumbotron {
  border-radius: 6px;
}

.jumbotron .container {
  max-width: 100%;
}

@media screen and (min-width: 768px) {
  .jumbotron {
    padding-top: 48px;
    padding-bottom: 48px;
  }

  .container .jumbotron,
  .container-fluid .jumbotron {
    padding-right: 60px;
    padding-left: 60px;
  }

  .jumbotron .h1,
  .jumbotron h1 {
    font-size: 63px;
  }
}

.thumbnail {
  padding: 4px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 4px;
  -webkit-transition: border 0.2s ease-in-out;
  -o-transition: border 0.2s ease-in-out;
  transition: border 0.2s ease-in-out;
}

.thumbnail a > img,
.thumbnail > img {
  margin-right: auto;
  margin-left: auto;
}

a.thumbnail.active,
a.thumbnail:focus,
a.thumbnail:hover {
  border-color: #337ab7;
}

.thumbnail .caption {
  padding: 9px;
  color: #333;
}

.alert {
  padding: 15px;
  border: 1px solid transparent;
  border-radius: 4px;
}

.alert h4 {
  margin-top: 0;
  color: inherit;
}

.alert > p,
.alert > ul {
  margin-bottom: 0;
}

.alert > p + p {
  margin-top: 5px;
}

.alert-dismissable,
.alert-dismissible {
  padding-right: 35px;
}

.alert-dismissable .close,
.alert-dismissible .close {
  position: relative;
  top: -2px;
  right: -21px;
  color: inherit;
}

.modal,
.modal-backdrop {
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
}

.alert-success {
  color: #3c763d;
  background-color: #dff0d8;
  border-color: #d6e9c6;
}

.alert-success hr {
  border-top-color: #c9e2b3;
}

.alert-success .alert-link {
  color: #2b542c;
}

.alert-info {
  color: #31708f;
  background-color: #d9edf7;
  border-color: #bce8f1;
}

.alert-info hr {
  border-top-color: #a6e1ec;
}

.alert-info .alert-link {
  color: #245269;
}

.alert-warning {
  color: #8a6d3b;
  background-color: #fcf8e3;
  border-color: #faebcc;
}

.alert-warning hr {
  border-top-color: #f7e1b5;
}

.alert-warning .alert-link {
  color: #66512c;
}

.alert-danger {
  color: #a94442;
  background-color: #f2dede;
  border-color: #ebccd1;
}

.alert-danger hr {
  border-top-color: #e4b9c0;
}

.alert-danger .alert-link {
  color: #843534;
}

@-webkit-keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }

  to {
    background-position: 0 0;
  }
}

@-o-keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }

  to {
    background-position: 0 0;
  }
}

@keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }

  to {
    background-position: 0 0;
  }
}

.progress {
  height: 20px;
  margin-bottom: 20px;
  background-color: #f5f5f5;
  border-radius: 4px;
  -webkit-box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
  box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
}

.progress-bar {
  float: left;
  width: 0;
  height: 100%;
  font-size: 12px;
  line-height: 20px;
  color: #fff;
  text-align: center;
  background-color: #337ab7;
  -webkit-box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  -webkit-transition: width 0.6s ease;
  -o-transition: width 0.6s ease;
  transition: width 0.6s ease;
}

.progress-bar-striped,
.progress-striped .progress-bar {
  background-image: linear-gradient(
    45deg,
    rgba(255, 255, 255, 0.15) 25%,
    transparent 25%,
    transparent 50%,
    rgba(255, 255, 255, 0.15) 50%,
    rgba(255, 255, 255, 0.15) 75%,
    transparent 75%,
    transparent
  );
  -webkit-background-size: 40px 40px;
  background-size: 40px 40px;
}

.progress-bar.active,
.progress.active .progress-bar {
  -webkit-animation: progress-bar-stripes 2s linear infinite;
  -o-animation: progress-bar-stripes 2s linear infinite;
  animation: progress-bar-stripes 2s linear infinite;
}

.progress-bar-success {
  background-color: #5cb85c;
}

.progress-striped .progress-bar-success {
  background-image: linear-gradient(
    45deg,
    rgba(255, 255, 255, 0.15) 25%,
    transparent 25%,
    transparent 50%,
    rgba(255, 255, 255, 0.15) 50%,
    rgba(255, 255, 255, 0.15) 75%,
    transparent 75%,
    transparent
  );
}

.progress-striped .progress-bar-info,
.progress-striped .progress-bar-warning {
  background-image: -webkit-linear-gradient(
    45deg,
    rgba(255, 255, 255, 0.15) 25%,
    transparent 25%,
    transparent 50%,
    rgba(255, 255, 255, 0.15) 50%,
    rgba(255, 255, 255, 0.15) 75%,
    transparent 75%,
    transparent
  );
  background-image: -o-linear-gradient(
    45deg,
    rgba(255, 255, 255, 0.15) 25%,
    transparent 25%,
    transparent 50%,
    rgba(255, 255, 255, 0.15) 50%,
    rgba(255, 255, 255, 0.15) 75%,
    transparent 75%,
    transparent
  );
}

.progress-bar-info {
  background-color: #5bc0de;
}

.progress-striped .progress-bar-info {
  background-image: linear-gradient(
    45deg,
    rgba(255, 255, 255, 0.15) 25%,
    transparent 25%,
    transparent 50%,
    rgba(255, 255, 255, 0.15) 50%,
    rgba(255, 255, 255, 0.15) 75%,
    transparent 75%,
    transparent
  );
}

.progress-bar-warning {
  background-color: #f0ad4e;
}

.progress-striped .progress-bar-warning {
  background-image: linear-gradient(
    45deg,
    rgba(255, 255, 255, 0.15) 25%,
    transparent 25%,
    transparent 50%,
    rgba(255, 255, 255, 0.15) 50%,
    rgba(255, 255, 255, 0.15) 75%,
    transparent 75%,
    transparent
  );
}

.progress-bar-danger {
  background-color: #d9534f;
}

.progress-striped .progress-bar-danger {
  background-image: -webkit-linear-gradient(
    45deg,
    rgba(255, 255, 255, 0.15) 25%,
    transparent 25%,
    transparent 50%,
    rgba(255, 255, 255, 0.15) 50%,
    rgba(255, 255, 255, 0.15) 75%,
    transparent 75%,
    transparent
  );
  background-image: -o-linear-gradient(
    45deg,
    rgba(255, 255, 255, 0.15) 25%,
    transparent 25%,
    transparent 50%,
    rgba(255, 255, 255, 0.15) 50%,
    rgba(255, 255, 255, 0.15) 75%,
    transparent 75%,
    transparent
  );
  background-image: linear-gradient(
    45deg,
    rgba(255, 255, 255, 0.15) 25%,
    transparent 25%,
    transparent 50%,
    rgba(255, 255, 255, 0.15) 50%,
    rgba(255, 255, 255, 0.15) 75%,
    transparent 75%,
    transparent
  );
}

.media:first-child {
  margin-top: 0;
}

.media,
.media-body {
  overflow: hidden;
  zoom: 1;
}

.media-body {
  width: 10000px;
}

.media-object.img-thumbnail {
  max-width: none;
}

.media-right,
.media > .pull-right {
  padding-left: 10px;
}

.media-left,
.media > .pull-left {
  padding-right: 10px;
}

.media-body,
.media-left,
.media-right {
  display: table-cell;
  vertical-align: top;
}

.media-middle {
  vertical-align: middle;
}

.media-bottom {
  vertical-align: bottom;
}

.media-heading {
  margin-top: 0;
  margin-bottom: 5px;
}

.media-list {
  padding-left: 0;
  list-style: none;
}

.list-group {
  padding-left: 0;
  margin-bottom: 20px;
}

.list-group-item {
  position: relative;
  display: block;
  padding: 10px 15px;
  margin-bottom: -1px;
  background-color: #fff;
  border: 1px solid #ddd;
}

.list-group-item:first-child {
  border-top-left-radius: 4px;
  border-top-right-radius: 4px;
}

.list-group-item:last-child {
  margin-bottom: 0;
  border-bottom-right-radius: 4px;
  border-bottom-left-radius: 4px;
}

a.list-group-item,
button.list-group-item {
  color: #555;
}

a.list-group-item .list-group-item-heading,
button.list-group-item .list-group-item-heading {
  color: #333;
}

a.list-group-item:focus,
a.list-group-item:hover,
button.list-group-item:focus,
button.list-group-item:hover {
  color: #555;
  text-decoration: none;
  background-color: #f5f5f5;
}

button.list-group-item {
  width: 100%;
  text-align: left;
}

.list-group-item.disabled,
.list-group-item.disabled:focus,
.list-group-item.disabled:hover {
  color: #777;
  cursor: not-allowed;
  background-color: #eee;
}

.list-group-item.disabled .list-group-item-heading,
.list-group-item.disabled:focus .list-group-item-heading,
.list-group-item.disabled:hover .list-group-item-heading {
  color: inherit;
}

.list-group-item.disabled .list-group-item-text,
.list-group-item.disabled:focus .list-group-item-text,
.list-group-item.disabled:hover .list-group-item-text {
  color: #777;
}

.list-group-item.active,
.list-group-item.active:focus,
.list-group-item.active:hover {
  z-index: 2;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}

.list-group-item.active .list-group-item-heading,
.list-group-item.active .list-group-item-heading > .small,
.list-group-item.active .list-group-item-heading > small,
.list-group-item.active:focus .list-group-item-heading,
.list-group-item.active:focus .list-group-item-heading > .small,
.list-group-item.active:focus .list-group-item-heading > small,
.list-group-item.active:hover .list-group-item-heading,
.list-group-item.active:hover .list-group-item-heading > .small,
.list-group-item.active:hover .list-group-item-heading > small {
  color: inherit;
}

.list-group-item.active .list-group-item-text,
.list-group-item.active:focus .list-group-item-text,
.list-group-item.active:hover .list-group-item-text {
  color: #c7ddef;
}

.list-group-item-success {
  color: #3c763d;
  background-color: #dff0d8;
}

a.list-group-item-success,
button.list-group-item-success {
  color: #3c763d;
}

a.list-group-item-success .list-group-item-heading,
button.list-group-item-success .list-group-item-heading {
  color: inherit;
}

a.list-group-item-success:focus,
a.list-group-item-success:hover,
button.list-group-item-success:focus,
button.list-group-item-success:hover {
  color: #3c763d;
  background-color: #d0e9c6;
}

a.list-group-item-success.active,
a.list-group-item-success.active:focus,
a.list-group-item-success.active:hover,
button.list-group-item-success.active,
button.list-group-item-success.active:focus,
button.list-group-item-success.active:hover {
  color: #fff;
  background-color: #3c763d;
  border-color: #3c763d;
}

.list-group-item-info {
  color: #31708f;
  background-color: #d9edf7;
}

a.list-group-item-info,
button.list-group-item-info {
  color: #31708f;
}

a.list-group-item-info .list-group-item-heading,
button.list-group-item-info .list-group-item-heading {
  color: inherit;
}

a.list-group-item-info:focus,
a.list-group-item-info:hover,
button.list-group-item-info:focus,
button.list-group-item-info:hover {
  color: #31708f;
  background-color: #c4e3f3;
}

a.list-group-item-info.active,
a.list-group-item-info.active:focus,
a.list-group-item-info.active:hover,
button.list-group-item-info.active,
button.list-group-item-info.active:focus,
button.list-group-item-info.active:hover {
  color: #fff;
  background-color: #31708f;
  border-color: #31708f;
}

.list-group-item-warning {
  color: #8a6d3b;
  background-color: #fcf8e3;
}

a.list-group-item-warning,
button.list-group-item-warning {
  color: #8a6d3b;
}

a.list-group-item-warning .list-group-item-heading,
button.list-group-item-warning .list-group-item-heading {
  color: inherit;
}

a.list-group-item-warning:focus,
a.list-group-item-warning:hover,
button.list-group-item-warning:focus,
button.list-group-item-warning:hover {
  color: #8a6d3b;
  background-color: #faf2cc;
}

a.list-group-item-warning.active,
a.list-group-item-warning.active:focus,
a.list-group-item-warning.active:hover,
button.list-group-item-warning.active,
button.list-group-item-warning.active:focus,
button.list-group-item-warning.active:hover {
  color: #fff;
  background-color: #8a6d3b;
  border-color: #8a6d3b;
}

.list-group-item-danger {
  color: #a94442;
  background-color: #f2dede;
}

a.list-group-item-danger,
button.list-group-item-danger {
  color: #a94442;
}

a.list-group-item-danger .list-group-item-heading,
button.list-group-item-danger .list-group-item-heading {
  color: inherit;
}

a.list-group-item-danger:focus,
a.list-group-item-danger:hover,
button.list-group-item-danger:focus,
button.list-group-item-danger:hover {
  color: #a94442;
  background-color: #ebcccc;
}

a.list-group-item-danger.active,
a.list-group-item-danger.active:focus,
a.list-group-item-danger.active:hover,
button.list-group-item-danger.active,
button.list-group-item-danger.active:focus,
button.list-group-item-danger.active:hover {
  color: #fff;
  background-color: #a94442;
  border-color: #a94442;
}

.panel-heading > .dropdown .dropdown-toggle,
.panel-title,
.panel-title > .small,
.panel-title > .small > a,
.panel-title > a,
.panel-title > small,
.panel-title > small > a {
  color: inherit;
}

.list-group-item-heading {
  margin-top: 0;
  margin-bottom: 5px;
}

.list-group-item-text {
  margin-bottom: 0;
  line-height: 1.3;
}

.carousel-inner > .item > a > img,
.carousel-inner > .item > img,
.close {
  line-height: 1;
}

.panel {
  margin-bottom: 20px;
  background-color: #fff;
  border: 1px solid transparent;
  border-radius: 4px;
  -webkit-box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
}

.panel-title,
.panel > .list-group,
.panel > .panel-collapse > .list-group,
.panel > .panel-collapse > .table,
.panel > .table,
.panel > .table-responsive > .table {
  margin-bottom: 0;
}

.panel-body {
  padding: 15px;
}

.panel-heading {
  padding: 10px 15px;
  border-bottom: 1px solid transparent;
  border-top-left-radius: 3px;
  border-top-right-radius: 3px;
}

.panel-title {
  margin-top: 0;
  font-size: 16px;
}

.panel-footer {
  padding: 10px 15px;
  background-color: #f5f5f5;
  border-top: 1px solid #ddd;
  border-bottom-right-radius: 3px;
  border-bottom-left-radius: 3px;
}

.panel > .list-group .list-group-item,
.panel > .panel-collapse > .list-group .list-group-item {
  border-width: 1px 0;
  border-radius: 0;
}

.panel-group .panel-heading,
.panel > .table-bordered > tbody > tr:first-child > td,
.panel > .table-bordered > tbody > tr:first-child > th,
.panel > .table-bordered > tbody > tr:last-child > td,
.panel > .table-bordered > tbody > tr:last-child > th,
.panel > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-bordered > tfoot > tr:last-child > th,
.panel > .table-bordered > thead > tr:first-child > td,
.panel > .table-bordered > thead > tr:first-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > th,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > td,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > th {
  border-bottom: 0;
}

.panel > .list-group:first-child .list-group-item:first-child,
.panel
  > .panel-collapse
  > .list-group:first-child
  .list-group-item:first-child {
  border-top: 0;
  border-top-left-radius: 3px;
  border-top-right-radius: 3px;
}

.panel > .list-group:last-child .list-group-item:last-child,
.panel > .panel-collapse > .list-group:last-child .list-group-item:last-child {
  border-bottom: 0;
  border-bottom-right-radius: 3px;
  border-bottom-left-radius: 3px;
}

.panel
  > .panel-heading
  + .panel-collapse
  > .list-group
  .list-group-item:first-child {
  border-top-left-radius: 0;
  border-top-right-radius: 0;
}

.list-group + .panel-footer,
.panel-heading + .list-group .list-group-item:first-child {
  border-top-width: 0;
}

.panel > .panel-collapse > .table caption,
.panel > .table caption,
.panel > .table-responsive > .table caption {
  padding-right: 15px;
  padding-left: 15px;
}

.panel > .table-responsive:first-child > .table:first-child,
.panel
  > .table-responsive:first-child
  > .table:first-child
  > tbody:first-child
  > tr:first-child,
.panel
  > .table-responsive:first-child
  > .table:first-child
  > thead:first-child
  > tr:first-child,
.panel > .table:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child,
.panel > .table:first-child > thead:first-child > tr:first-child {
  border-top-left-radius: 3px;
  border-top-right-radius: 3px;
}

.panel
  > .table-responsive:first-child
  > .table:first-child
  > tbody:first-child
  > tr:first-child
  td:first-child,
.panel
  > .table-responsive:first-child
  > .table:first-child
  > tbody:first-child
  > tr:first-child
  th:first-child,
.panel
  > .table-responsive:first-child
  > .table:first-child
  > thead:first-child
  > tr:first-child
  td:first-child,
.panel
  > .table-responsive:first-child
  > .table:first-child
  > thead:first-child
  > tr:first-child
  th:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:first-child,
.panel > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel
  > .table:first-child
  > thead:first-child
  > tr:first-child
  th:first-child {
  border-top-left-radius: 3px;
}

.panel
  > .table-responsive:first-child
  > .table:first-child
  > tbody:first-child
  > tr:first-child
  td:last-child,
.panel
  > .table-responsive:first-child
  > .table:first-child
  > tbody:first-child
  > tr:first-child
  th:last-child,
.panel
  > .table-responsive:first-child
  > .table:first-child
  > thead:first-child
  > tr:first-child
  td:last-child,
.panel
  > .table-responsive:first-child
  > .table:first-child
  > thead:first-child
  > tr:first-child
  th:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:last-child,
.panel > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:last-child {
  border-top-right-radius: 3px;
}

.panel > .table-responsive:last-child > .table:last-child,
.panel
  > .table-responsive:last-child
  > .table:last-child
  > tbody:last-child
  > tr:last-child,
.panel
  > .table-responsive:last-child
  > .table:last-child
  > tfoot:last-child
  > tr:last-child,
.panel > .table:last-child,
.panel > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child {
  border-bottom-right-radius: 3px;
  border-bottom-left-radius: 3px;
}

.panel
  > .table-responsive:last-child
  > .table:last-child
  > tbody:last-child
  > tr:last-child
  td:first-child,
.panel
  > .table-responsive:last-child
  > .table:last-child
  > tbody:last-child
  > tr:last-child
  th:first-child,
.panel
  > .table-responsive:last-child
  > .table:last-child
  > tfoot:last-child
  > tr:last-child
  td:first-child,
.panel
  > .table-responsive:last-child
  > .table:last-child
  > tfoot:last-child
  > tr:last-child
  th:first-child,
.panel > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:first-child {
  border-bottom-left-radius: 3px;
}

.panel
  > .table-responsive:last-child
  > .table:last-child
  > tbody:last-child
  > tr:last-child
  td:last-child,
.panel
  > .table-responsive:last-child
  > .table:last-child
  > tbody:last-child
  > tr:last-child
  th:last-child,
.panel
  > .table-responsive:last-child
  > .table:last-child
  > tfoot:last-child
  > tr:last-child
  td:last-child,
.panel
  > .table-responsive:last-child
  > .table:last-child
  > tfoot:last-child
  > tr:last-child
  th:last-child,
.panel > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:last-child {
  border-bottom-right-radius: 3px;
}

.panel > .panel-body + .table,
.panel > .panel-body + .table-responsive,
.panel > .table + .panel-body,
.panel > .table-responsive + .panel-body {
  border-top: 1px solid #ddd;
}

.panel > .table > tbody:first-child > tr:first-child td,
.panel > .table > tbody:first-child > tr:first-child th {
  border-top: 0;
}

.panel > .table-bordered,
.panel > .table-responsive > .table-bordered {
  border: 0;
}

.panel > .table-bordered > tbody > tr > td:first-child,
.panel > .table-bordered > tbody > tr > th:first-child,
.panel > .table-bordered > tfoot > tr > td:first-child,
.panel > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-bordered > thead > tr > td:first-child,
.panel > .table-bordered > thead > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:first-child {
  border-left: 0;
}

.panel > .table-bordered > tbody > tr > td:last-child,
.panel > .table-bordered > tbody > tr > th:last-child,
.panel > .table-bordered > tfoot > tr > td:last-child,
.panel > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-bordered > thead > tr > td:last-child,
.panel > .table-bordered > thead > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:last-child {
  border-right: 0;
}

.panel > .table-responsive {
  margin-bottom: 0;
  border: 0;
}

.panel-group {
  margin-bottom: 20px;
}

.panel-group .panel {
  margin-bottom: 0;
  border-radius: 4px;
}

.panel-group .panel + .panel {
  margin-top: 5px;
}

.panel-group .panel-heading + .panel-collapse > .list-group,
.panel-group .panel-heading + .panel-collapse > .panel-body {
  border-top: 1px solid #ddd;
}

.panel-group .panel-footer {
  border-top: 0;
}

.panel-group .panel-footer + .panel-collapse .panel-body {
  border-bottom: 1px solid #ddd;
}

.panel-default {
  border-color: #ddd;
}

.panel-default > .panel-heading {
  color: #333;
  background-color: #f5f5f5;
  border-color: #ddd;
}

.panel-default > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ddd;
}

.panel-default > .panel-heading .badge {
  color: #f5f5f5;
  background-color: #333;
}

.panel-default > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ddd;
}

.panel-primary {
  border-color: #337ab7;
}

.panel-primary > .panel-heading {
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}

.panel-primary > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #337ab7;
}

.panel-primary > .panel-heading .badge {
  color: #337ab7;
  background-color: #fff;
}

.panel-primary > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #337ab7;
}

.panel-success {
  border-color: #d6e9c6;
}

.panel-success > .panel-heading {
  color: #3c763d;
  background-color: #dff0d8;
  border-color: #d6e9c6;
}

.panel-success > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #d6e9c6;
}

.panel-success > .panel-heading .badge {
  color: #dff0d8;
  background-color: #3c763d;
}

.panel-success > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #d6e9c6;
}

.panel-info {
  border-color: #bce8f1;
}

.panel-info > .panel-heading {
  color: #31708f;
  background-color: #d9edf7;
  border-color: #bce8f1;
}

.panel-info > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #bce8f1;
}

.panel-info > .panel-heading .badge {
  color: #d9edf7;
  background-color: #31708f;
}

.panel-info > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #bce8f1;
}

.panel-warning {
  border-color: #faebcc;
}

.panel-warning > .panel-heading {
  color: #8a6d3b;
  background-color: #fcf8e3;
  border-color: #faebcc;
}

.panel-warning > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #faebcc;
}

.panel-warning > .panel-heading .badge {
  color: #fcf8e3;
  background-color: #8a6d3b;
}

.panel-warning > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #faebcc;
}

.panel-danger {
  border-color: #ebccd1;
}

.panel-danger > .panel-heading {
  color: #a94442;
  background-color: #f2dede;
  border-color: #ebccd1;
}

.panel-danger > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ebccd1;
}

.panel-danger > .panel-heading .badge {
  color: #f2dede;
  background-color: #a94442;
}

.panel-danger > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ebccd1;
}

.embed-responsive {
  position: relative;
  display: block;
  height: 0;
  padding: 0;
}

.embed-responsive .embed-responsive-item,
.embed-responsive embed,
.embed-responsive iframe,
.embed-responsive object,
.embed-responsive video {
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border: 0;
}

.embed-responsive-16by9 {
  padding-bottom: 56.25%;
}

.embed-responsive-4by3 {
  padding-bottom: 75%;
}

.well {
  min-height: 20px;
  padding: 19px;
  margin-bottom: 20px;
  background-color: #f5f5f5;
  border: 1px solid #e3e3e3;
  border-radius: 4px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
}

.well blockquote {
  border-color: #ddd;
  border-color: rgba(0, 0, 0, 0.15);
}

.well-lg {
  padding: 24px;
  border-radius: 6px;
}

.well-sm {
  padding: 9px;
  border-radius: 3px;
}

.close {
  float: right;
  font-size: 21px;
  color: #000;
  text-shadow: 0 1px 0 #fff;
  filter: alpha(opacity=20);
  opacity: 0.2;
}

.popover,
.tooltip {
  font-style: normal;
  font-weight: 400;
  line-height: 1.42857143;
  text-shadow: none;
  text-transform: none;
  letter-spacing: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  white-space: normal;
  line-break: auto;
  text-decoration: none;
}

.close:focus,
.close:hover {
  color: #000;
  text-decoration: none;
  cursor: pointer;
  filter: alpha(opacity=50);
  opacity: 0.5;
}

button.close {
  -webkit-appearance: none;
  padding: 0;
  cursor: pointer;
  background: 0 0;
  border: 0;
}

.modal {
  position: fixed;
  z-index: 1050;
  display: none;
  -webkit-overflow-scrolling: touch;
  outline: 0;
}

.modal.fade .modal-dialog {
  -webkit-transition: -webkit-transform 0.3s ease-out;
  -o-transition: -o-transform 0.3s ease-out;
  transition: transform 0.3s ease-out;
  -webkit-transform: translate(0, -25%);
  -ms-transform: translate(0, -25%);
  -o-transform: translate(0, -25%);
  transform: translate(0, -25%);
}

.modal.in .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}

.modal-open .modal {
  overflow-x: hidden;
  overflow-y: auto;
}

.modal-dialog {
  position: relative;
  width: auto;
  margin: 10px;
}

.modal-content {
  position: relative;
  background-color: #fff;
  background-clip: padding-box;
  border: 1px solid #999;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 6px;
  outline: 0;
  -webkit-box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
}

.modal-backdrop {
  position: fixed;
  z-index: 1040;
  background-color: #000;
}

.modal-backdrop.fade {
  filter: alpha(opacity=0);
  opacity: 0;
}

.carousel-control,
.modal-backdrop.in {
  filter: alpha(opacity=50);
  opacity: 0.5;
}

.modal-header {
  min-height: 16.43px;
  padding: 15px;
  border-bottom: 1px solid #e5e5e5;
}

.modal-header .close {
  margin-top: -2px;
}

.modal-title {
  margin: 0;
  line-height: 1.42857143;
}

.modal-body {
  position: relative;
  padding: 15px;
}

.modal-footer {
  padding: 15px;
  text-align: right;
  border-top: 1px solid #e5e5e5;
}

.modal-footer .btn + .btn {
  margin-bottom: 0;
  margin-left: 5px;
}

.modal-footer .btn-group .btn + .btn {
  margin-left: -1px;
}

.modal-footer .btn-block + .btn-block {
  margin-left: 0;
}

.modal-scrollbar-measure {
  position: absolute;
  top: -9999px;
  width: 50px;
  height: 50px;
  overflow: scroll;
}

@media (min-width: 768px) {
  .modal-dialog {
    width: 600px;
    margin: 30px auto;
  }

  .modal-content {
    -webkit-box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
  }

  .modal-sm {
    width: 300px;
  }
}

.tooltip.top-left .tooltip-arrow,
.tooltip.top-right .tooltip-arrow {
  bottom: 0;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}

@media (min-width: 992px) {
  .modal-lg {
    width: 900px;
  }
}

.tooltip {
  position: absolute;
  z-index: 1070;
  display: block;
  font-size: 12px;
  text-align: left;
  text-align: start;
  filter: alpha(opacity=0);
  opacity: 0;
}

.tooltip.in {
  filter: alpha(opacity=90);
  opacity: 0.9;
}

.tooltip.top {
  padding: 5px 0;
  margin-top: -3px;
}

.tooltip.right {
  padding: 0 5px;
  margin-left: 3px;
}

.tooltip.bottom {
  padding: 5px 0;
  margin-top: 3px;
}

.tooltip.left {
  padding: 0 5px;
  margin-left: -3px;
}

.tooltip-inner {
  max-width: 200px;
  padding: 3px 8px;
  color: #fff;
  text-align: center;
  background-color: #000;
  border-radius: 4px;
}

.tooltip-arrow {
  position: absolute;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}

.tooltip.top .tooltip-arrow {
  bottom: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}

.tooltip.top-left .tooltip-arrow {
  right: 5px;
}

.tooltip.top-right .tooltip-arrow {
  left: 5px;
}

.tooltip.right .tooltip-arrow {
  top: 50%;
  left: 0;
  margin-top: -5px;
  border-width: 5px 5px 5px 0;
  border-right-color: #000;
}

.tooltip.left .tooltip-arrow {
  top: 50%;
  right: 0;
  margin-top: -5px;
  border-width: 5px 0 5px 5px;
  border-left-color: #000;
}

.tooltip.bottom .tooltip-arrow,
.tooltip.bottom-left .tooltip-arrow,
.tooltip.bottom-right .tooltip-arrow {
  border-width: 0 5px 5px;
  border-bottom-color: #000;
  top: 0;
}

.tooltip.bottom .tooltip-arrow {
  left: 50%;
  margin-left: -5px;
}

.tooltip.bottom-left .tooltip-arrow {
  right: 5px;
  margin-top: -5px;
}

.tooltip.bottom-right .tooltip-arrow {
  left: 5px;
  margin-top: -5px;
}

.popover {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 1060;
  display: none;
  max-width: 276px;
  padding: 1px;
  font-size: 14px;
  text-align: left;
  text-align: start;
  background-color: #fff;
  -webkit-background-clip: padding-box;
  background-clip: padding-box;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 6px;
  -webkit-box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
}

.carousel-caption,
.carousel-control {
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
}

.popover.top {
  margin-top: -10px;
}

.popover.right {
  margin-left: 10px;
}

.popover.bottom {
  margin-top: 10px;
}

.popover.left {
  margin-left: -10px;
}

.popover-title {
  padding: 8px 14px;
  margin: 0;
  font-size: 14px;
  background-color: #f7f7f7;
  border-bottom: 1px solid #ebebeb;
  border-radius: 5px 5px 0 0;
}

.popover-content {
  padding: 9px 14px;
}

.popover > .arrow,
.popover > .arrow:after {
  position: absolute;
  display: block;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}

.carousel,
.carousel-inner {
  position: relative;
}

.popover > .arrow {
  border-width: 11px;
}

.popover > .arrow:after {
  content: "";
  border-width: 10px;
}

.popover.top > .arrow {
  bottom: -11px;
  left: 50%;
  margin-left: -11px;
  border-top-color: #999;
  border-top-color: rgba(0, 0, 0, 0.25);
  border-bottom-width: 0;
}

.popover.top > .arrow:after {
  bottom: 1px;
  margin-left: -10px;
  content: " ";
  border-top-color: #fff;
  border-bottom-width: 0;
}

.popover.left > .arrow:after,
.popover.right > .arrow:after {
  bottom: -10px;
  content: " ";
}

.popover.right > .arrow {
  top: 50%;
  left: -11px;
  margin-top: -11px;
  border-right-color: #999;
  border-right-color: rgba(0, 0, 0, 0.25);
  border-left-width: 0;
}

.popover.right > .arrow:after {
  left: 1px;
  border-right-color: #fff;
  border-left-width: 0;
}

.popover.bottom > .arrow {
  top: -11px;
  left: 50%;
  margin-left: -11px;
  border-top-width: 0;
  border-bottom-color: #999;
  border-bottom-color: rgba(0, 0, 0, 0.25);
}

.popover.bottom > .arrow:after {
  top: 1px;
  margin-left: -10px;
  content: " ";
  border-top-width: 0;
  border-bottom-color: #fff;
}

.popover.left > .arrow {
  top: 50%;
  right: -11px;
  margin-top: -11px;
  border-right-width: 0;
  border-left-color: #999;
  border-left-color: rgba(0, 0, 0, 0.25);
}

.popover.left > .arrow:after {
  right: 1px;
  border-right-width: 0;
  border-left-color: #fff;
}

.carousel-inner {
  width: 100%;
  overflow: hidden;
}

.carousel-inner > .item {
  position: relative;
  display: none;
  -webkit-transition: 0.6s ease-in-out left;
  -o-transition: 0.6s ease-in-out left;
  transition: 0.6s ease-in-out left;
}

@media all and (transform-3d), (-webkit-transform-3d) {
  .carousel-inner > .item {
    -webkit-transition: -webkit-transform 0.6s ease-in-out;
    -o-transition: -o-transform 0.6s ease-in-out;
    transition: transform 0.6s ease-in-out;
    -webkit-backface-visibility: hidden;
    backface-visibility: hidden;
    -webkit-perspective: 1000px;
    perspective: 1000px;
  }

  .carousel-inner > .item.active.right,
  .carousel-inner > .item.next {
    left: 0;
    -webkit-transform: translate3d(100%, 0, 0);
    transform: translate3d(100%, 0, 0);
  }

  .carousel-inner > .item.active.left,
  .carousel-inner > .item.prev {
    left: 0;
    -webkit-transform: translate3d(-100%, 0, 0);
    transform: translate3d(-100%, 0, 0);
  }

  .carousel-inner > .item.active,
  .carousel-inner > .item.next.left,
  .carousel-inner > .item.prev.right {
    left: 0;
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
  }
}

.carousel-inner > .active,
.carousel-inner > .next,
.carousel-inner > .prev {
  display: block;
}

.carousel-inner > .active {
  left: 0;
}

.carousel-inner > .next,
.carousel-inner > .prev {
  position: absolute;
  top: 0;
  width: 100%;
}

.carousel-inner > .next {
  left: 100%;
}

.carousel-inner > .prev {
  left: -100%;
}

.carousel-inner > .next.left,
.carousel-inner > .prev.right {
  left: 0;
}

.carousel-inner > .active.left {
  left: -100%;
}

.carousel-inner > .active.right {
  left: 100%;
}

.carousel-control {
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  width: 15%;
  font-size: 20px;
}

.carousel-control.left {
  background-image: -webkit-linear-gradient(
    left,
    rgba(0, 0, 0, 0.5) 0,
    rgba(0, 0, 0, 0.0001) 100%
  );
  background-image: -o-linear-gradient(
    left,
    rgba(0, 0, 0, 0.5) 0,
    rgba(0, 0, 0, 0.0001) 100%
  );
  background-image: -webkit-gradient(
    linear,
    left top,
    right top,
    from(rgba(0, 0, 0, 0.5)),
    to(rgba(0, 0, 0, 0.0001))
  );
  background-image: linear-gradient(
    to right,
    rgba(0, 0, 0, 0.5) 0,
    rgba(0, 0, 0, 0.0001) 100%
  );
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#80000000', endColorstr='#00000000', GradientType=1);
  background-repeat: repeat-x;
}

.carousel-control.right {
  right: 0;
  left: auto;
  background-image: -webkit-linear-gradient(
    left,
    rgba(0, 0, 0, 0.0001) 0,
    rgba(0, 0, 0, 0.5) 100%
  );
  background-image: -o-linear-gradient(
    left,
    rgba(0, 0, 0, 0.0001) 0,
    rgba(0, 0, 0, 0.5) 100%
  );
  background-image: -webkit-gradient(
    linear,
    left top,
    right top,
    from(rgba(0, 0, 0, 0.0001)),
    to(rgba(0, 0, 0, 0.5))
  );
  background-image: linear-gradient(
    to right,
    rgba(0, 0, 0, 0.0001) 0,
    rgba(0, 0, 0, 0.5) 100%
  );
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#00000000', endColorstr='#80000000', GradientType=1);
  background-repeat: repeat-x;
}

.carousel-control:focus,
.carousel-control:hover {
  color: #fff;
  text-decoration: none;
  filter: alpha(opacity=90);
  outline: 0;
  opacity: 0.9;
}

.carousel-control .glyphicon-chevron-left,
.carousel-control .glyphicon-chevron-right,
.carousel-control .icon-next,
.carousel-control .icon-prev {
  position: absolute;
  top: 50%;
  z-index: 5;
  display: inline-block;
  margin-top: -10px;
}

.carousel-control .glyphicon-chevron-left,
.carousel-control .icon-prev {
  left: 50%;
  margin-left: -10px;
}

.carousel-control .glyphicon-chevron-right,
.carousel-control .icon-next {
  right: 50%;
  margin-right: -10px;
}

.carousel-control .icon-next,
.carousel-control .icon-prev {
  width: 20px;
  height: 20px;
  font-family: serif;
  line-height: 1;
}

.carousel-control .icon-prev:before {
  content: "\2039";
}

.carousel-control .icon-next:before {
  content: "\203a";
}

.carousel-indicators {
  position: absolute;
  bottom: 10px;
  left: 50%;
  z-index: 15;
  width: 60%;
  padding-left: 0;
  margin-left: -30%;
  text-align: center;
  list-style: none;
}

.carousel-indicators li {
  display: inline-block;
  width: 10px;
  height: 10px;
  margin: 1px;
  text-indent: -999px;
  cursor: pointer;
  background-color: #000\9;
  background-color: transparent;
  border: 1px solid #fff;
  border-radius: 10px;
}

.carousel-indicators .active {
  width: 12px;
  height: 12px;
  margin: 0;
  background-color: #fff;
}

.carousel-caption {
  position: absolute;
  right: 15%;
  bottom: 20px;
  left: 15%;
  z-index: 10;
  padding-top: 20px;
  padding-bottom: 20px;
}

.carousel-caption .btn,
.text-hide {
  text-shadow: none;
}

@media screen and (min-width: 768px) {
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-next,
  .carousel-control .icon-prev {
    width: 30px;
    height: 30px;
    margin-top: -15px;
    font-size: 30px;
  }

  .carousel-control .glyphicon-chevron-left,
  .carousel-control .icon-prev {
    margin-left: -15px;
  }

  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-next {
    margin-right: -15px;
  }

  .carousel-caption {
    right: 20%;
    left: 20%;
    padding-bottom: 30px;
  }

  .carousel-indicators {
    bottom: 20px;
  }
}

.btn-group-vertical > .btn-group:after,
.btn-group-vertical > .btn-group:before,
.btn-toolbar:after,
.btn-toolbar:before,
.clearfix:after,
.clearfix:before,
.container-fluid:after,
.container-fluid:before,
.container:after,
.container:before,
.dl-horizontal dd:after,
.dl-horizontal dd:before,
.form-horizontal .form-group:after,
.form-horizontal .form-group:before,
.modal-footer:after,
.modal-footer:before,
.nav:after,
.nav:before,
.navbar-collapse:after,
.navbar-collapse:before,
.navbar-header:after,
.navbar-header:before,
.navbar:after,
.navbar:before,
.pager:after,
.pager:before,
.panel-body:after,
.panel-body:before,
.row:after,
.row:before {
  display: table;
  content: " ";
}

.btn-group-vertical > .btn-group:after,
.btn-toolbar:after,
.clearfix:after,
.container-fluid:after,
.container:after,
.dl-horizontal dd:after,
.form-horizontal .form-group:after,
.modal-footer:after,
.nav:after,
.navbar-collapse:after,
.navbar-header:after,
.navbar:after,
.pager:after,
.panel-body:after,
.row:after {
  clear: both;
}

.center-block {
  display: block;
  margin-right: auto;
  margin-left: auto;
}

.pull-right {
  float: right !important;
}

.pull-left {
  float: left !important;
}

.hide {
  display: none !important;
}

.show {
  display: block !important;
}

.hidden,
.visible-lg,
.visible-lg-block,
.visible-lg-inline,
.visible-lg-inline-block,
.visible-md,
.visible-md-block,
.visible-md-inline,
.visible-md-inline-block,
.visible-sm,
.visible-sm-block,
.visible-sm-inline,
.visible-sm-inline-block,
.visible-xs,
.visible-xs-block,
.visible-xs-inline,
.visible-xs-inline-block {
  display: none !important;
}

.invisible {
  visibility: hidden;
}

.text-hide {
  font: 0/0 a;
  color: transparent;
  background-color: transparent;
  border: 0;
}

.affix {
  position: fixed;
}

@-ms-viewport {
  width: device-width;
}

@media (max-width: 767px) {
  .visible-xs {
    display: block !important;
  }

  table.visible-xs {
    display: table !important;
  }

  tr.visible-xs {
    display: table-row !important;
  }

  td.visible-xs,
  th.visible-xs {
    display: table-cell !important;
  }

  .visible-xs-block {
    display: block !important;
  }

  .visible-xs-inline {
    display: inline !important;
  }

  .visible-xs-inline-block {
    display: inline-block !important;
  }
}

@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm {
    display: block !important;
  }

  table.visible-sm {
    display: table !important;
  }

  tr.visible-sm {
    display: table-row !important;
  }

  td.visible-sm,
  th.visible-sm {
    display: table-cell !important;
  }

  .visible-sm-block {
    display: block !important;
  }

  .visible-sm-inline {
    display: inline !important;
  }

  .visible-sm-inline-block {
    display: inline-block !important;
  }
}

@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md {
    display: block !important;
  }

  table.visible-md {
    display: table !important;
  }

  tr.visible-md {
    display: table-row !important;
  }

  td.visible-md,
  th.visible-md {
    display: table-cell !important;
  }

  .visible-md-block {
    display: block !important;
  }

  .visible-md-inline {
    display: inline !important;
  }

  .visible-md-inline-block {
    display: inline-block !important;
  }
}

@media (min-width: 1200px) {
  .visible-lg {
    display: block !important;
  }

  table.visible-lg {
    display: table !important;
  }

  tr.visible-lg {
    display: table-row !important;
  }

  td.visible-lg,
  th.visible-lg {
    display: table-cell !important;
  }

  .visible-lg-block {
    display: block !important;
  }

  .visible-lg-inline {
    display: inline !important;
  }

  .visible-lg-inline-block {
    display: inline-block !important;
  }

  .hidden-lg {
    display: none !important;
  }
}

@media (max-width: 767px) {
  .hidden-xs {
    display: none !important;
  }
}

@media (min-width: 768px) and (max-width: 991px) {
  .hidden-sm {
    display: none !important;
  }
}

@media (min-width: 992px) and (max-width: 1199px) {
  .hidden-md {
    display: none !important;
  }
}

.visible-print {
  display: none !important;
}

@media print {
  .visible-print {
    display: block !important;
  }

  table.visible-print {
    display: table !important;
  }

  tr.visible-print {
    display: table-row !important;
  }

  td.visible-print,
  th.visible-print {
    display: table-cell !important;
  }
}

.visible-print-block {
  display: none !important;
}

@media print {
  .visible-print-block {
    display: block !important;
  }
}

.visible-print-inline {
  display: none !important;
}

@media print {
  .visible-print-inline {
    display: inline !important;
  }
}

.visible-print-inline-block {
  display: none !important;
}

@media print {
  .visible-print-inline-block {
    display: inline-block !important;
  }

  .hidden-print {
    display: none !important;
  }
}

/*!
* Launchframe v1.0.0 by @Whiteboardis dev team
* Copyright 2015 Whiteboard
*
* Designed and built for developers by developers.
*/
/*
* Based somewhat on Skeleton
* www.getskeleton.com

Less version credit: https://github.com/thatericsmith/Skeleton
Extended to be dynamic based on variables defined above
*/

/*
	Default grid: mobile FIRST!
	Note: This will be implicit for @tiny and @small widths
*/

.columns,
.column {
  margin: 0;
}

.container {
  position: relative;
  width: 90%;
  padding: 0;
  margin: 0 auto;
}

.container.plusfour,
.container.pluseight {
  width: 100%;
}

.container .column.one-third,
.container .column.two-thirds,
.container .column.one {
  width: 100%;
}

.container .columns.two,
.container .columns.three,
.container .columns.four,
.container .columns.five,
.container .columns.six,
.container .columns.seven,
.container .columns.eight,
.container .columns.nine,
.container .columns.ten,
.container .columns.eleven,
.container .columns.twelve,
.container .columns.thirteen,
.container .columns.fourteen,
.container .columns.fifteen,
.container .columns.sixteen,
.container .columns.twenty,
.container .columns.twentyfour {
  width: 100%;
}

/* Offsets */

.container .offset-by-one,
.container .offset-by-two,
.container .offset-by-three,
.container .offset-by-four,
.container .offset-by-five,
.container .offset-by-six,
.container .offset-by-seven,
.container .offset-by-eight,
.container .offset-by-nine,
.container .offset-by-ten,
.container .offset-by-eleven,
.container .offset-by-twelve,
.container .offset-by-thirteen,
.container .offset-by-fourteen,
.container .offset-by-fifteen {
  padding-left: 0;
}

@media only screen and (min-width: 720px) {
   {
    /* Nested Column Classes */
  }
  .container {
    position: relative;
    width: 720px;
    padding: 0;
    margin: 0 auto;
  }
  .container.plusfour {
    width: 960px;
  }
  .container.pluseight {
    width: 1200px;
  }
  .column,
  .columns {
    display: inline;
    float: left;
    margin-right: 13.333333333333334px !important;
    margin-left: 13.333333333333334px !important;
  }
  .row {
    margin-bottom: 6.666666666666667px;
  }
  .column.alpha,
  .columns.alpha {
    margin-left: 0 !important;
  }
  .column.omega,
  .columns.omega {
    margin-right: 0 !important;
  }
  .column.alpha.omega,
  .columns.alpha.omega {
    margin: 0 !important;
  }
  .container {
    /* Base Grid */

    /* Offsets */
  }
  .container .one.column {
    width: 33.333333333333336px;
  }
  .container .columns.two {
    width: 93.33333333333334px;
  }
  .container .columns.three {
    width: 153.33333333333334px;
  }
  .container .columns.four {
    width: 213.33333333333334px;
  }
  .container .columns.five {
    width: 273.33333333333337px;
  }
  .container .columns.six {
    width: 333.33333333333337px;
  }
  .container .columns.seven {
    width: 393.33333333333337px;
  }
  .container .columns.eight {
    width: 453.33333333333337px;
  }
  .container .columns.nine {
    width: 513.3333333333334px;
  }
  .container .columns.ten {
    width: 573.3333333333334px;
  }
  .container .columns.eleven {
    width: 633.3333333333334px;
  }
  .container .columns.twelve {
    width: 693.3333333333334px;
  }
  .container .columns.thirteen {
    width: 753.3333333333334px;
  }
  .container .columns.fourteen {
    width: 813.3333333333334px;
  }
  .container .columns.fifteen {
    width: 873.3333333333335px;
  }
  .container .columns.sixteen {
    width: 933.3333333333334px;
  }
  .container .one-third.column {
    width: 220px;
  }
  .container .two-thirds.column {
    width: 466.6666666666667px;
  }
  .container .offset-by-one {
    padding-left: 60px;
  }
  .container .offset-by-two {
    padding-left: 120px;
  }
  .container .offset-by-three {
    padding-left: 180px;
  }
  .container .offset-by-four {
    padding-left: 240px;
  }
  .container .offset-by-five {
    padding-left: 300px;
  }
  .container .offset-by-six {
    padding-left: 360px;
  }
  .container .offset-by-seven {
    padding-left: 420px;
  }
  .container .offset-by-eight {
    padding-left: 480px;
  }
  .container .offset-by-nine {
    padding-left: 540px;
  }
  .container .offset-by-ten {
    padding-left: 600px;
  }
  .container .offset-by-eleven {
    padding-left: 660px;
  }
  .container .offset-by-twelve {
    padding-left: 720px;
  }
  .container .offset-by-thirteen {
    padding-left: 780px;
  }
  .container .offset-by-fourteen {
    padding-left: 840px;
  }
  .container .offset-by-fifteen {
    padding-left: 900px;
  }
}

@media only screen and (min-width: 940px) {
   {
    /* Nested Column Classes */
  }
  .container {
    position: relative;
    width: 940.0000000000001px;
    padding: 0;
    margin: 0 auto;
  }
  .container.plusfour {
    width: 1253.3333333333335px;
  }
  .container.pluseight {
    width: 1566.666666666667px;
  }
  .column,
  .columns {
    display: inline;
    float: left;
    margin-right: 17.40740740740741px !important;
    margin-left: 17.40740740740741px !important;
  }
  .row {
    margin-bottom: 8.703703703703704px;
  }
  .column.alpha,
  .columns.alpha {
    margin-left: 0 !important;
  }
  .column.omega,
  .columns.omega {
    margin-right: 0 !important;
  }
  .column.alpha.omega,
  .columns.alpha.omega {
    margin: 0 !important;
  }
  .container {
    /* Base Grid */

    /* Offsets */
  }
  .container .one.column {
    width: 43.51851851851852px;
  }
  .container .columns.two {
    width: 121.85185185185185px;
  }
  .container .columns.three {
    width: 200.18518518518516px;
  }
  .container .columns.four {
    width: 278.51851851851853px;
  }
  .container .columns.five {
    width: 356.85185185185185px;
  }
  .container .columns.six {
    width: 435.18518518518516px;
  }
  .container .columns.seven {
    width: 513.5185185185185px;
  }
  .container .columns.eight {
    width: 591.8518518518518px;
  }
  .container .columns.nine {
    width: 670.1851851851852px;
  }
  .container .columns.ten {
    width: 748.5185185185186px;
  }
  .container .columns.eleven {
    width: 826.8518518518518px;
  }
  .container .columns.twelve {
    width: 905.1851851851852px;
  }
  .container .columns.thirteen {
    width: 983.5185185185186px;
  }
  .container .columns.fourteen {
    width: 1061.8518518518517px;
  }
  .container .columns.fifteen {
    width: 1140.1851851851852px;
  }
  .container .columns.sixteen {
    width: 1218.5185185185187px;
  }
  .container .one-third.column {
    width: 287.22222222222223px;
  }
  .container .two-thirds.column {
    width: 609.2592592592592px;
  }
  .container .offset-by-one {
    padding-left: 78.33333333333334px;
  }
  .container .offset-by-two {
    padding-left: 156.66666666666669px;
  }
  .container .offset-by-three {
    padding-left: 235.00000000000003px;
  }
  .container .offset-by-four {
    padding-left: 313.33333333333337px;
  }
  .container .offset-by-five {
    padding-left: 391.66666666666674px;
  }
  .container .offset-by-six {
    padding-left: 470.00000000000006px;
  }
  .container .offset-by-seven {
    padding-left: 548.3333333333334px;
  }
  .container .offset-by-eight {
    padding-left: 626.6666666666667px;
  }
  .container .offset-by-nine {
    padding-left: 705.0000000000001px;
  }
  .container .offset-by-ten {
    padding-left: 783.3333333333335px;
  }
  .container .offset-by-eleven {
    padding-left: 861.6666666666667px;
  }
  .container .offset-by-twelve {
    padding-left: 940.0000000000001px;
  }
  .container .offset-by-thirteen {
    padding-left: 1018.3333333333335px;
  }
  .container .offset-by-fourteen {
    padding-left: 1096.6666666666667px;
  }
  .container .offset-by-fifteen {
    padding-left: 1175.0000000000002px;
  }
}

@media only screen and (min-width: 1100px) {
   {
    /* Nested Column Classes */
  }
  .container {
    position: relative;
    width: 1100px;
    padding: 0;
    margin: 0 auto;
  }
  .container.plusfour {
    width: 1466.6666666666665px;
  }
  .container.pluseight {
    width: 1833.333333333333px;
  }
  .column,
  .columns {
    display: inline;
    float: left;
    margin-right: 20.37037037037037px !important;
    margin-left: 20.37037037037037px !important;
  }
  .row {
    margin-bottom: 10.185185185185185px;
  }
  .column.alpha,
  .columns.alpha {
    margin-left: 0 !important;
  }
  .column.omega,
  .columns.omega {
    margin-right: 0 !important;
  }
  .column.alpha.omega,
  .columns.alpha.omega {
    margin: 0 !important;
  }
  .container {
    /* Base Grid */

    /* Offsets */
  }
  .container .one.column {
    width: 50.925925925925924px;
  }
  .container .columns.two {
    width: 142.59259259259258px;
  }
  .container .columns.three {
    width: 234.25925925925924px;
  }
  .container .columns.four {
    width: 325.9259259259259px;
  }
  .container .columns.five {
    width: 417.5925925925926px;
  }
  .container .columns.six {
    width: 509.25925925925924px;
  }
  .container .columns.seven {
    width: 600.9259259259259px;
  }
  .container .columns.eight {
    width: 692.5925925925926px;
  }
  .container .columns.nine {
    width: 784.2592592592592px;
  }
  .container .columns.ten {
    width: 875.9259259259259px;
  }
  .container .columns.eleven {
    width: 967.5925925925926px;
  }
  .container .columns.twelve {
    width: 1059.2592592592591px;
  }
  .container .columns.thirteen {
    width: 1150.9259259259259px;
  }
  .container .columns.fourteen {
    width: 1242.5925925925926px;
  }
  .container .columns.fifteen {
    width: 1334.2592592592591px;
  }
  .container .columns.sixteen {
    width: 1425.9259259259259px;
  }
  .container .one-third.column {
    width: 336.1111111111111px;
  }
  .container .two-thirds.column {
    width: 712.9629629629629px;
  }
  .container .offset-by-one {
    padding-left: 91.66666666666666px;
  }
  .container .offset-by-two {
    padding-left: 183.33333333333331px;
  }
  .container .offset-by-three {
    padding-left: 275px;
  }
  .container .offset-by-four {
    padding-left: 366.66666666666663px;
  }
  .container .offset-by-five {
    padding-left: 458.33333333333326px;
  }
  .container .offset-by-six {
    padding-left: 550px;
  }
  .container .offset-by-seven {
    padding-left: 641.6666666666666px;
  }
  .container .offset-by-eight {
    padding-left: 733.3333333333333px;
  }
  .container .offset-by-nine {
    padding-left: 824.9999999999999px;
  }
  .container .offset-by-ten {
    padding-left: 916.6666666666665px;
  }
  .container .offset-by-eleven {
    padding-left: 1008.3333333333333px;
  }
  .container .offset-by-twelve {
    padding-left: 1100px;
  }
  .container .offset-by-thirteen {
    padding-left: 1191.6666666666665px;
  }
  .container .offset-by-fourteen {
    padding-left: 1283.3333333333333px;
  }
  .container .offset-by-fifteen {
    padding-left: 1374.9999999999998px;
  }
}

@media only screen and (min-width: 1240px) {
   {
    /* Nested Column Classes */
  }
  .container {
    position: relative;
    width: 1240px;
    padding: 0;
    margin: 0 auto;
  }
  .container.plusfour {
    width: 1653.3333333333333px;
  }
  .container.pluseight {
    width: 2066.6666666666665px;
  }
  .column,
  .columns {
    display: inline;
    float: left;
    margin-right: 22.962962962962962px !important;
    margin-left: 22.962962962962962px !important;
  }
  .row {
    margin-bottom: 11.481481481481481px;
  }
  .column.alpha,
  .columns.alpha {
    margin-left: 0 !important;
  }
  .column.omega,
  .columns.omega {
    margin-right: 0 !important;
  }
  .column.alpha.omega,
  .columns.alpha.omega {
    margin: 0 !important;
  }
  .container {
    /* Base Grid */

    /* Offsets */
  }
  .container .one.column {
    width: 57.407407407407405px;
  }
  .container .columns.two {
    width: 160.74074074074073px;
  }
  .container .columns.three {
    width: 264.0740740740741px;
  }
  .container .columns.four {
    width: 367.4074074074074px;
  }
  .container .columns.five {
    width: 470.7407407407407px;
  }
  .container .columns.six {
    width: 574.0740740740741px;
  }
  .container .columns.seven {
    width: 677.4074074074074px;
  }
  .container .columns.eight {
    width: 780.7407407407406px;
  }
  .container .columns.nine {
    width: 884.074074074074px;
  }
  .container .columns.ten {
    width: 987.4074074074074px;
  }
  .container .columns.eleven {
    width: 1090.7407407407406px;
  }
  .container .columns.twelve {
    width: 1194.0740740740741px;
  }
  .container .columns.thirteen {
    width: 1297.4074074074074px;
  }
  .container .columns.fourteen {
    width: 1400.7407407407406px;
  }
  .container .columns.fifteen {
    width: 1504.074074074074px;
  }
  .container .columns.sixteen {
    width: 1607.4074074074074px;
  }
  .container .one-third.column {
    width: 378.88888888888886px;
  }
  .container .two-thirds.column {
    width: 803.7037037037037px;
  }
  .container .offset-by-one {
    padding-left: 103.33333333333333px;
  }
  .container .offset-by-two {
    padding-left: 206.66666666666666px;
  }
  .container .offset-by-three {
    padding-left: 310px;
  }
  .container .offset-by-four {
    padding-left: 413.3333333333333px;
  }
  .container .offset-by-five {
    padding-left: 516.6666666666666px;
  }
  .container .offset-by-six {
    padding-left: 620px;
  }
  .container .offset-by-seven {
    padding-left: 723.3333333333333px;
  }
  .container .offset-by-eight {
    padding-left: 826.6666666666666px;
  }
  .container .offset-by-nine {
    padding-left: 930px;
  }
  .container .offset-by-ten {
    padding-left: 1033.3333333333333px;
  }
  .container .offset-by-eleven {
    padding-left: 1136.6666666666665px;
  }
  .container .offset-by-twelve {
    padding-left: 1240px;
  }
  .container .offset-by-thirteen {
    padding-left: 1343.3333333333333px;
  }
  .container .offset-by-fourteen {
    padding-left: 1446.6666666666665px;
  }
  .container .offset-by-fifteen {
    padding-left: 1550px;
  }
}

.floatright {
  float: right;
}

.floatleft {
  float: left;
}

/* #Clearing
================================================== */

/* Self Clearing Goodness */

.container:after {
  display: block;
  height: 0;
  clear: both;
  content: "\0020";
  visibility: hidden;
}

/* Use clearfix class on parent to clear nested columns,
    or wrap each row of columns in a <div class="row"> */

.clearfix:before,
.clearfix:after,
.row:before,
.row:after {
  display: block;
  width: 0;
  height: 0;
  overflow: hidden;
  content: "\0020";
  visibility: hidden;
}

.row:after,
.clearfix:after {
  clear: both;
}

.row,
.clearfix {
  zoom: 1;
}

.clear {
  display: block;
  width: 0;
  height: 0;
  overflow: hidden;
  clear: both;
  visibility: hidden;
}

/*  Font Awesome
    the iconic font designed for use with Twitter Bootstrap
    -------------------------------------------------------
    The full suite of pictographic icons, examples, and documentation
    can be found at: http://fortawesome.github.com/Font-Awesome/

    License
    -------------------------------------------------------
    The Font Awesome webfont, CSS, and LESS files are licensed under CC BY 3.0:
    http://creativecommons.org/licenses/by/3.0/ A mention of
    'Font Awesome - http://fortawesome.github.com/Font-Awesome' in human-readable
    source code is considered acceptable attribution (most common on the web).
    If human readable source code is not available to the end user, a mention in
    an 'About' or 'Credits' screen is considered acceptable (most common in desktop
    or mobile software).

    Contact
    -------------------------------------------------------
    Email: dave@davegandy.com
    Twitter: http://twitter.com/fortaweso_me
    Work: Lead Product Designer @ http://kyruus.com

    */

/*  Font Awesome styles
    ------------------------------------------------------- */

[class^="icon-"]:before,
[class*=" icon-"]:before {
  display: inline-block;
  font-family: FontAwesome;
  font-style: normal;
  font-weight: normal;
  text-decoration: inherit;
}

a [class^="icon-"],
a [class*=" icon-"] {
  display: inline-block;
  text-decoration: inherit;
}

/* makes the font 33% larger relative to the icon container */

.icon-large:before {
  font-size: 1.3333333333333333em;
  vertical-align: middle;
}

.btn [class^="icon-"],
.nav-tabs [class^="icon-"],
.btn [class*=" icon-"],
.nav-tabs [class*=" icon-"] {
  /* keeps button heights with and without icons the same */

  line-height: 0.9em;
}

li [class^="icon-"],
li [class*=" icon-"] {
  display: inline-block;
  width: 1.25em;
  text-align: center;
}

li .icon-large:before,
li .icon-large:before {
  /* 1.5 increased font size for icon-large * 1.25 width */

  width: 1.875em;
}

ul.icons {
  margin-left: 2em;
  text-indent: -0.8em;
  list-style-type: none;
}

ul.icons li [class^="icon-"],
ul.icons li [class*=" icon-"] {
  width: 0.8em;
}

ul.icons li .icon-large:before,
ul.icons li .icon-large:before {
  /* 1.5 increased font size for icon-large * 1.25 width */

  vertical-align: initial;
}

/*  Font Awesome uses the Unicode Private Use Area (PUA) to ensure screen
    readers do not read off random characters that represent icons */

.icon-glass:before {
  content: "\f000";
}

.icon-music:before {
  content: "\f001";
}

.icon-search:before {
  content: "\f002";
}

.icon-envelope:before {
  content: "\f003";
}

.icon-heart:before {
  content: "\f004";
}

.icon-star:before {
  content: "\f005";
}

.icon-star-empty:before {
  content: "\f006";
}

.icon-user:before {
  content: "\f007";
}

.icon-film:before {
  content: "\f008";
}

.icon-th-large:before {
  content: "\f009";
}

.icon-th:before {
  content: "\f00a";
}

.icon-th-list:before {
  content: "\f00b";
}

.icon-ok:before {
  content: "\f00c";
}

.icon-remove:before {
  content: "\f00d";
}

.icon-zoom-in:before {
  content: "\f00e";
}

.icon-zoom-out:before {
  content: "\f010";
}

.icon-off:before {
  content: "\f011";
}

.icon-signal:before {
  content: "\f012";
}

.icon-cog:before {
  content: "\f013";
}

.icon-trash:before {
  content: "\f014";
}

.icon-home:before {
  content: "\f015";
}

.icon-file:before {
  content: "\f016";
}

.icon-time:before {
  content: "\f017";
}

.icon-road:before {
  content: "\f018";
}

.icon-download-alt:before {
  content: "\f019";
}

.icon-download:before {
  content: "\f01a";
}

.icon-upload:before {
  content: "\f01b";
}

.icon-inbox:before {
  content: "\f01c";
}

.icon-play-circle:before {
  content: "\f01d";
}

.icon-repeat:before {
  content: "\f01e";
}

/* \f020 is not a valid unicode character. all shifted one down */

.icon-refresh:before {
  content: "\f021";
}

.icon-list-alt:before {
  content: "\f022";
}

.icon-lock:before {
  content: "\f023";
}

.icon-flag:before {
  content: "\f024";
}

.icon-headphones:before {
  content: "\f025";
}

.icon-volume-off:before {
  content: "\f026";
}

.icon-volume-down:before {
  content: "\f027";
}

.icon-volume-up:before {
  content: "\f028";
}

.icon-qrcode:before {
  content: "\f029";
}

.icon-barcode:before {
  content: "\f02a";
}

.icon-tag:before {
  content: "\f02b";
}

.icon-tags:before {
  content: "\f02c";
}

.icon-book:before {
  content: "\f02d";
}

.icon-bookmark:before {
  content: "\f02e";
}

.icon-print:before {
  content: "\f02f";
}

.icon-camera:before {
  content: "\f030";
}

.icon-font:before {
  content: "\f031";
}

.icon-bold:before {
  content: "\f032";
}

.icon-italic:before {
  content: "\f033";
}

.icon-text-height:before {
  content: "\f034";
}

.icon-text-width:before {
  content: "\f035";
}

.icon-align-left:before {
  content: "\f036";
}

.icon-align-center:before {
  content: "\f037";
}

.icon-align-right:before {
  content: "\f038";
}

.icon-align-justify:before {
  content: "\f039";
}

.icon-list:before {
  content: "\f03a";
}

.icon-indent-left:before {
  content: "\f03b";
}

.icon-indent-right:before {
  content: "\f03c";
}

.icon-facetime-video:before {
  content: "\f03d";
}

.icon-picture:before {
  content: "\f03e";
}

.icon-pencil:before {
  content: "\f040";
}

.icon-map-marker:before {
  content: "\f041";
}

.icon-adjust:before {
  content: "\f042";
}

.icon-tint:before {
  content: "\f043";
}

.icon-edit:before {
  content: "\f044";
}

.icon-share:before {
  content: "\f045";
}

.icon-check:before {
  content: "\f046";
}

.icon-move:before {
  content: "\f047";
}

.icon-step-backward:before {
  content: "\f048";
}

.icon-fast-backward:before {
  content: "\f049";
}

.icon-backward:before {
  content: "\f04a";
}

.icon-play:before {
  content: "\f04b";
}

.icon-pause:before {
  content: "\f04c";
}

.icon-stop:before {
  content: "\f04d";
}

.icon-forward:before {
  content: "\f04e";
}

.icon-fast-forward:before {
  content: "\f050";
}

.icon-step-forward:before {
  content: "\f051";
}

.icon-eject:before {
  content: "\f052";
}

.icon-chevron-left:before {
  content: "\f053";
}

.icon-chevron-right:before {
  content: "\f054";
}

.icon-plus-sign:before {
  content: "\f055";
}

.icon-minus-sign:before {
  content: "\f056";
}

.icon-remove-sign:before {
  content: "\f057";
}

.icon-ok-sign:before {
  content: "\f058";
}

.icon-question-sign:before {
  content: "\f059";
}

.icon-info-sign:before {
  content: "\f05a";
}

.icon-screenshot:before {
  content: "\f05b";
}

.icon-remove-circle:before {
  content: "\f05c";
}

.icon-ok-circle:before {
  content: "\f05d";
}

.icon-ban-circle:before {
  content: "\f05e";
}

.icon-arrow-left:before {
  content: "\f060";
}

.icon-arrow-right:before {
  content: "\f061";
}

.icon-arrow-up:before {
  content: "\f062";
}

.icon-arrow-down:before {
  content: "\f063";
}

.icon-share-alt:before {
  content: "\f064";
}

.icon-resize-full:before {
  content: "\f065";
}

.icon-resize-small:before {
  content: "\f066";
}

.icon-plus:before {
  content: "\f067";
}

.icon-minus:before {
  content: "\f068";
}

.icon-asterisk:before {
  content: "\f069";
}

.icon-exclamation-sign:before {
  content: "\f06a";
}

.icon-gift:before {
  content: "\f06b";
}

.icon-leaf:before {
  content: "\f06c";
}

.icon-fire:before {
  content: "\f06d";
}

.icon-eye-open:before {
  content: "\f06e";
}

.icon-eye-close:before {
  content: "\f070";
}

.icon-warning-sign:before {
  content: "\f071";
}

.icon-plane:before {
  content: "\f072";
}

.icon-calendar:before {
  content: "\f073";
}

.icon-random:before {
  content: "\f074";
}

.icon-comment:before {
  content: "\f075";
}

.icon-magnet:before {
  content: "\f076";
}

.icon-chevron-up:before {
  content: "\f077";
}

.icon-chevron-down:before {
  content: "\f078";
}

.icon-retweet:before {
  content: "\f079";
}

.icon-shopping-cart:before {
  content: "\f07a";
}

.icon-folder-close:before {
  content: "\f07b";
}

.icon-folder-open:before {
  content: "\f07c";
}

.icon-resize-vertical:before {
  content: "\f07d";
}

.icon-resize-horizontal:before {
  content: "\f07e";
}

.icon-bar-chart:before {
  content: "\f080";
}

.icon-twitter-sign:before {
  content: "\f081";
}

.icon-facebook-sign:before {
  content: "\f082";
}

.icon-camera-retro:before {
  content: "\f083";
}

.icon-key:before {
  content: "\f084";
}

.icon-cogs:before {
  content: "\f085";
}

.icon-comments:before {
  content: "\f086";
}

.icon-thumbs-up:before {
  content: "\f087";
}

.icon-thumbs-down:before {
  content: "\f088";
}

.icon-star-half:before {
  content: "\f089";
}

.icon-heart-empty:before {
  content: "\f08a";
}

.icon-signout:before {
  content: "\f08b";
}

.icon-linkedin-sign:before {
  content: "\f08c";
}

.icon-pushpin:before {
  content: "\f08d";
}

.icon-external-link:before {
  content: "\f08e";
}

.icon-signin:before {
  content: "\f090";
}

.icon-trophy:before {
  content: "\f091";
}

.icon-github-sign:before {
  content: "\f092";
}

.icon-upload-alt:before {
  content: "\f093";
}

.icon-lemon:before {
  content: "\f094";
}

.icon-phone:before {
  content: "\f095";
}

.icon-check-empty:before {
  content: "\f096";
}

.icon-bookmark-empty:before {
  content: "\f097";
}

.icon-phone-sign:before {
  content: "\f098";
}

.icon-twitter:before {
  content: "\f099";
}

.icon-facebook:before {
  content: "\f09a";
}

.icon-github:before {
  content: "\f09b";
}

.icon-unlock:before {
  content: "\f09c";
}

.icon-credit-card:before {
  content: "\f09d";
}

.icon-rss:before {
  content: "\f09e";
}

.icon-hdd:before {
  content: "\f0a0";
}

.icon-bullhorn:before {
  content: "\f0a1";
}

.icon-bell:before {
  content: "\f0a2";
}

.icon-certificate:before {
  content: "\f0a3";
}

.icon-hand-right:before {
  content: "\f0a4";
}

.icon-hand-left:before {
  content: "\f0a5";
}

.icon-hand-up:before {
  content: "\f0a6";
}

.icon-hand-down:before {
  content: "\f0a7";
}

.icon-circle-arrow-left:before {
  content: "\f0a8";
}

.icon-circle-arrow-right:before {
  content: "\f0a9";
}

.icon-circle-arrow-up:before {
  content: "\f0aa";
}

.icon-circle-arrow-down:before {
  content: "\f0ab";
}

.icon-globe:before {
  content: "\f0ac";
}

.icon-wrench:before {
  content: "\f0ad";
}

.icon-tasks:before {
  content: "\f0ae";
}

.icon-filter:before {
  content: "\f0b0";
}

.icon-briefcase:before {
  content: "\f0b1";
}

.icon-fullscreen:before {
  content: "\f0b2";
}

.icon-group:before {
  content: "\f0c0";
}

.icon-link:before {
  content: "\f0c1";
}

.icon-cloud:before {
  content: "\f0c2";
}

.icon-beaker:before {
  content: "\f0c3";
}

.icon-cut:before {
  content: "\f0c4";
}

.icon-copy:before {
  content: "\f0c5";
}

.icon-paper-clip:before {
  content: "\f0c6";
}

.icon-save:before {
  content: "\f0c7";
}

.icon-sign-blank:before {
  content: "\f0c8";
}

.icon-reorder:before {
  content: "\f0c9";
}

.icon-list-ul:before {
  content: "\f0ca";
}

.icon-list-ol:before {
  content: "\f0cb";
}

.icon-strikethrough:before {
  content: "\f0cc";
}

.icon-underline:before {
  content: "\f0cd";
}

.icon-table:before {
  content: "\f0ce";
}

.icon-table:before {
  content: "\f0ce";
}

.icon-magic:before {
  content: "\f0d0";
}

.icon-truck:before {
  content: "\f0d1";
}

.icon-pinterest:before {
  content: "\f0d2";
}

.icon-pinterest-sign:before {
  content: "\f0d3";
}

.icon-google-plus-sign:before {
  content: "\f0d4";
}

.icon-google-plus:before {
  content: "\f0d5";
}

.icon-money:before {
  content: "\f0d6";
}

.icon-caret-down:before {
  content: "\f0d7";
}

.icon-caret-up:before {
  content: "\f0d8";
}

.icon-caret-left:before {
  content: "\f0d9";
}

.icon-caret-right:before {
  content: "\f0da";
}

.icon-columns:before {
  content: "\f0db";
}

.icon-sort:before {
  content: "\f0dc";
}

.icon-sort-down:before {
  content: "\f0dd";
}

.icon-sort-up:before {
  content: "\f0de";
}

.icon-envelope-alt:before {
  content: "\f0e0";
}

.icon-linkedin:before {
  content: "\f0e1";
}

.icon-undo:before {
  content: "\f0e2";
}

.icon-legal:before {
  content: "\f0e3";
}

.icon-dashboard:before {
  content: "\f0e4";
}

.icon-comment-alt:before {
  content: "\f0e5";
}

.icon-comments-alt:before {
  content: "\f0e6";
}

.icon-bolt:before {
  content: "\f0e7";
}

.icon-sitemap:before {
  content: "\f0e8";
}

.icon-umbrella:before {
  content: "\f0e9";
}

.icon-paste:before {
  content: "\f0ea";
}

.icon-user-md:before {
  content: "\f200";
}

.icon-apple-logo:before {
  content: "\f500";
}

.icon-windows-8:before {
  content: "\f501";
}

.icon-js-fiddle:before {
  content: "\f502";
}

.icon-skype:before {
  content: "\f503";
}

.icon-youtube-sign:before {
  content: "\f504";
}

.icon-youtube:before {
  content: "\f505";
}

.icon-vimeo-sign:before {
  content: "\f506";
}

.icon-vimeo:before {
  content: "\f507";
}

.icon-lastfm-sign:before {
  content: "\f508";
}

.icon-lastfm:before {
  content: "\f509";
}

.icon-rss-sign:before {
  content: "\f50a";
}

.icon-reddit:before {
  content: "\f50b";
}

.icon-delicious-sign:before {
  content: "\f50c";
}

.icon-wordpress-sign:before {
  content: "\f50d";
}

.icon-wordpress:before {
  content: "\f50e";
}

.icon-git-fork:before {
  content: "\f50f";
}

.icon-blogger-sign:before {
  content: "\f510";
}

.icon-blogger:before {
  content: "\f511";
}

.icon-tumblr-sign:before {
  content: "\f512";
}

.icon-tumblr:before {
  content: "\f513";
}

.icon-flickr-sign:before {
  content: "\f514";
}

.icon-flickr:before {
  content: "\f515";
}

.icon-picasa-sign:before {
  content: "\f516";
}

.icon-picasa:before {
  content: "\f517";
}

.icon-amazon-sign:before {
  content: "\f518";
}

.icon-amazon:before {
  content: "\f519";
}

.icon-yelp-sign:before {
  content: "\f51a";
}

.icon-yelp:before {
  content: "\f51b";
}

.icon-soundcloud:before {
  content: "\f51c";
}

.icon-spotify:before {
  content: "\f51d";
}

.icon-yahoo-sign:before {
  content: "\f520";
}

.icon-yahoo:before {
  content: "\f521";
}

.icon-evernote-sign:before {
  content: "\f522";
}

.icon-evernote:before {
  content: "\f523";
}

.icon-google-sign:before {
  content: "\f524";
}

.icon-google:before {
  content: "\f525";
}

.icon-hacker-news:before {
  content: "\f526";
}

.icon-map:before {
  content: "\f529";
}

.icon-bus-sign:before {
  content: "\f52a";
}

.icon-bike-sign:before {
  content: "\f52b";
}

.icon-car-sign:before {
  content: "\f52c";
}

.icon-taxi-sign:before {
  content: "\f52d";
}

.icon-truck-sign:before {
  content: "\f52e";
}

.icon-handicap-sign:before {
  content: "\f52f";
}

/*! normalize.css v2.0.1 | MIT License | git.io/normalize */

/* ==========================================================================
   HTML5 display definitions
   ========================================================================== */

/**
 * Correct `block` display not defined in IE 8/9.
 */

article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
main,
nav,
section,
summary {
  display: block;
}

/**
 * Correct `inline-block` display not defined in IE 8/9.
 */

audio,
canvas,
video {
  display: inline-block;
}

/**
 * Prevent modern browsers from displaying `audio` without controls.
 * Remove excess height in iOS 5 devices.
 */

audio:not([controls]) {
  display: none;
  height: 0;
}

/**
 * Address styling not present in IE 8/9.
 */

[hidden] {
  display: none;
}

/* ==========================================================================
   Base
   ========================================================================== */

/**
 * 1. Set default font family to sans-serif.
 * 2. Prevent iOS text size adjust after orientation change, without disabling
 *    user zoom.
 */

html {
  font-family: "Avenir Next", sans-serif;
  /* 1 */

  -webkit-text-size-adjust: 100%;
  -ms-text-size-adjust: 100%;
  /* 2 */
}

/**
 * Remove default margin.
 */

body {
  margin: 0;
}

/* ==========================================================================
   Links
   ========================================================================== */

/**
 * Address `outline` inconsistency between Chrome and other browsers.
 */

a:focus {
  outline: thin dotted;
}

/**
 * Improve readability when focused and also mouse hovered in all browsers.
 */

a:active,
a:hover {
  outline: 0;
}

/* ==========================================================================
   Typography
   ========================================================================== */

/**
 * Address variable `h1` font size within `section` and `article` contexts in
 * Firefox 4+, Safari 5, and Chrome.
 */

h1 {
  font-size: 96px;
}

/**
 * Address styling not present in IE 8/9, Safari 5, and Chrome.
 */

abbr[title] {
  border-bottom: 1px dotted;
}

/**
 * Address style set to `bolder` in Firefox 4+, Safari 5, and Chrome.
 */

b,
strong {
  font-weight: bold;
}

/**
 * Address styling not present in Safari 5 and Chrome.
 */

dfn {
  font-style: italic;
}

/**
 * Address styling not present in IE 8/9.
 */

mark {
  color: #000;
  background: #ff0;
}

/**
 * Correct font family set oddly in Safari 5 and Chrome.
 */

code,
kbd,
pre,
samp {
  font-family: monospace, serif;
  font-size: 1em;
}

/**
 * Improve readability of pre-formatted text in all browsers.
 */

pre {
  word-wrap: break-word;
  white-space: pre;
  white-space: pre-wrap;
}

/**
 * Set consistent quote types.
 */

q {
  quotes: "\201C""\201D""\2018""\2019";
}

/**
 * Address inconsistent and variable font size in all browsers.
 */

small {
  font-size: 80%;
}

/**
 * Prevent `sub` and `sup` affecting `line-height` in all browsers.
 */

sub,
sup {
  position: relative;
  font-size: 75%;
  line-height: 0;
  vertical-align: baseline;
}

sup {
  top: -0.5em;
}

sub {
  bottom: -0.25em;
}

/* ==========================================================================
   Embedded content
   ========================================================================== */

/**
 * Remove border when inside `a` element in IE 8/9.
 */

img {
  border: 0;
}

/**
 * Correct overflow displayed oddly in IE 9.
 */

svg:not(:root) {
  overflow: hidden;
}

/* ==========================================================================
   Figures
   ========================================================================== */

/**
 * Address margin not present in IE 8/9 and Safari 5.
 */

figure {
  margin: 0;
}

/* ==========================================================================
   Forms
   ========================================================================== */

/**
 * Define consistent border, margin, and padding.
 */

fieldset {
  padding: 0.35em 0.625em 0.75em;
  margin: 0 2px;
  border: 1px solid #c0c0c0;
}

/**
 * 1. Correct `color` not being inherited in IE 8/9.
 * 2. Remove padding so people aren't caught out if they zero out fieldsets.
 */

legend {
  padding: 0;
  border: 0;
}

/**
 * 1. Correct font family not being inherited in all browsers.
 * 2. Correct font size not being inherited in all browsers.
 * 3. Address margins set differently in Firefox 4+, Safari 5, and Chrome.
 */

button,
input,
select,
textarea {
  margin: 0;
  font-family: inherit;
  font-size: 100%;
}

/**
 * Address Firefox 4+ setting `line-height` on `input` using `!important` in
 * the UA stylesheet.
 */

button,
input {
  line-height: normal;
}

/**
 * 1. Avoid the WebKit bug in Android 4.0.* where (2) destroys native `audio`
 *    and `video` controls.
 * 2. Correct inability to style clickable `input` types in iOS.
 * 3. Improve usability and consistency of cursor style between image-type
 *    `input` and others.
 */

button,
html input[type="button"],
input[type="reset"],
input[type="submit"] {
  cursor: pointer;
  -webkit-appearance: button;
}

/**
 * Re-set default cursor for disabled elements.
 */

button[disabled],
html input[disabled] {
  cursor: default;
}

/**
 * 1. Address box sizing set to `content-box` in IE 8/9.
 * 2. Remove excess padding in IE 8/9.
 */

input[type="checkbox"],
input[type="radio"] {
  padding: 0;
  box-sizing: border-box;
}

/**
 * 1. Address `appearance` set to `searchfield` in Safari 5 and Chrome.
 * 2. Address `box-sizing` set to `border-box` in Safari 5 and Chrome
 *    (include `-moz` to future-proof).
 */

input[type="search"] {
  -webkit-box-sizing: content-box;
  -moz-box-sizing: content-box;
  box-sizing: content-box;
  -webkit-appearance: textfield;
}

/**
 * Remove inner padding and search cancel button in Safari 5 and Chrome
 * on OS X.
 */

input[type="search"]::-webkit-search-cancel-button,
input[type="search"]::-webkit-search-decoration {
  -webkit-appearance: none;
}

/**
 * Remove inner padding and border in Firefox 4+.
 */

button::-moz-focus-inner,
input::-moz-focus-inner {
  padding: 0;
  border: 0;
}

/**
 * 1. Remove default vertical scrollbar in IE 8/9.
 * 2. Improve readability and alignment in all browsers.
 */

textarea {
  overflow: auto;
  /* 1 */

  vertical-align: top;
  /* 2 */
}

/* ==========================================================================
   Tables
   ========================================================================== */

/**
 * Remove most spacing between table cells.
 */

table {
  border-collapse: collapse;
  border-spacing: 0;
}

html,
button,
input,
select,
textarea {
  color: #222;
}

body {
  font-family: "Sentinel SSm A", "Sentinel SSm B", serif;
  font-size: 1em;
  line-height: 1.4;
  color: #17333a;
  background: #fffefa;
}

/*
 * Remove text-shadow in selection highlight: h5bp.com/i
 * These selection declarations have to be separate.
 * Customize the background color to match your design.
 */

::-moz-selection {
  text-shadow: none;
  background: #b3d4fc;
}

::selection {
  text-shadow: none;
  background: #b3d4fc;
}

/*
 * A better looking default horizontal rule
 */

hr {
  display: block;
  height: 1px;
  padding: 0;
  margin: 1em 0;
  border: 0;
  border-top: 1px solid #ccc;
}

/* ==========================================================================
   Chrome Frame prompt
   ========================================================================== */

.chromeframe {
  padding: 0.2em 0;
  margin: 0.2em 0;
  color: #000;
  background: #ccc;
}

.serif,
h1,
h2,
h3 {
  font-family: "Sentinel SSm A", "Sentinel SSm B", serif;
}

.sans-serif {
  font-family: "Avenir Next", sans-serif;
}

.sans-serif-cond {
  font-family: "Avenir Next Condensed", sans-serif;
}

.demi {
  font-weight: 600;
}

.whitetext {
  color: #fff;
}

.orangetext {
  color: #ffaa00;
}

.uc {
  text-transform: uppercase;
}

.text-spacing {
  letter-spacing: 0.1em;
}

/* Borrowed from:
	http://css-tricks.com/snippets/css/useful-css3-less-mixins/
	https://github.com/owzzz/Useful-Less-Mixins/blob/master/mixins.less

*/

/* Alignment */

.alignleft {
  display: inline;
  float: left;
  margin-right: 1.5em;
}

.alignright {
  display: inline;
  float: right;
  margin-left: 1.5em;
}

.aligncenter {
  display: block;
  margin: 0 auto;
  clear: both;
}

/* Text meant only for screen readers */

.screen-reader-text {
  position: absolute !important;
  clip: rect(1px, 1px, 1px, 1px);
}

.screen-reader-text:hover,
.screen-reader-text:active,
.screen-reader-text:focus {
  top: 5px;
  left: 5px;
  z-index: 100000;
  display: block;
  width: auto;
  height: auto;
  padding: 15px 23px 14px;
  clip: auto !important;
  font-size: 14px;
  font-weight: bold;
  line-height: normal;
  color: #21759b;
  text-decoration: none;
  background-color: #f1f1f1;
  border-radius: 3px;
  box-shadow: 0 0 2px 2px rgba(0, 0, 0, 0.6);
}

/* Clearing */

.clear:before,
.clear:after,
.entry-content:before,
.entry-content:after,
.comment-content:before,
.comment-content:after,
.site-header:before,
.site-header:after,
.site-content:before,
.site-content:after,
.site-footer:before,
.site-footer:after {
  display: table;
  content: "";
}

.clear:after,
.entry-content:after,
.comment-content:after,
.site-header:after,
.site-content:after,
.site-footer:after {
  clear: both;
}

/* =Menu
----------------------------------------------- */

.main-navigation {
  display: block;
  float: left;
  width: 100%;
  clear: both;
}

.main-navigation ul {
  padding-left: 0;
  margin: 0;
  list-style: none;
}

.main-navigation li {
  position: relative;
  float: left;
}

.main-navigation a {
  display: block;
  text-decoration: none;
}

.main-navigation ul ul {
  position: absolute;
  top: 1.5em;
  left: 0;
  z-index: 99999;
  display: none;
  float: left;
  box-shadow: 0 3px 3px rgba(0, 0, 0, 0.2);
}

.main-navigation ul ul ul {
  top: 0;
  left: 100%;
}

.main-navigation ul ul a {
  width: 200px;
}

.main-navigation ul li:hover > ul {
  display: block;
}

/* Small menu */

/* =Content
----------------------------------------------- */

.hentry {
  margin: 0 0 1.5em;
}

.byline,
.updated {
  display: none;
}

.single .byline,
.group-blog .byline {
  display: inline;
}

.page-content,
.entry-content,
.entry-summary {
  margin: 1.5em 0 0;
}

.page-links {
  margin: 0 0 1.5em;
  clear: both;
}

/* =Asides
----------------------------------------------- */

.blog .format-aside .entry-title,
.archive .format-aside .entry-title {
  display: none;
}

/* =Media
----------------------------------------------- */

.page-content img.wp-smiley,
.entry-content img.wp-smiley,
.comment-content img.wp-smiley {
  padding: 0;
  margin-top: 0;
  margin-bottom: 0;
  border: none;
}

.wp-caption {
  max-width: 100%;
  margin-bottom: 1.5em;
  border: 1px solid #ccc;
}

.wp-caption img[class*="wp-image-"] {
  display: block;
  max-width: 98%;
  margin: 1.2% auto 0;
}

.wp-caption-text {
  text-align: center;
}

.wp-caption .wp-caption-text {
  margin: 0.8075em 0;
}

.site-main .gallery {
  margin-bottom: 1.5em;
}

.site-main .gallery a img {
  height: auto;
  max-width: 90%;
  border: none;
}

.site-main .gallery dd {
  margin: 0;
}

/* Make sure embeds and iframes fit their containers */

embed,
iframe,
object {
  max-width: 100%;
}

/* =Navigation
----------------------------------------------- */

.site-main [class*="navigation"] {
  margin: 0 0 1.5em;
  overflow: hidden;
}

[class*="navigation"] .nav-previous {
  float: left;
  width: 50%;
}

[class*="navigation"] .nav-next {
  float: right;
  width: 50%;
  text-align: right;
}

/* =Comments
----------------------------------------------- */

.comment-content a {
  word-wrap: break-word;
}

/* =Widgets
----------------------------------------------- */

.widget {
  margin: 0 0 1.5em;
}

/* Make sure select elements fit in widgets */

.widget select {
  max-width: 100%;
}

/* Search widget */

.widget_search .search-submit {
  display: none;
}

/* =Infinite Scroll
----------------------------------------------- */

/* Globally hidden elements when Infinite Scroll is supported and in use. */

.infinite-scroll .paging-navigation,
.infinite-scroll.neverending .site-footer {
  /* Theme Footer (when set to scrolling) */

  display: none;
}

/* When Infinite Scroll has reached its end we need to re-display elements that were hidden (via .neverending) before */

.infinity-end.neverending .site-footer {
  display: block;
}

/*

All site-specific styles go here.

Some rules and guidelines:
	classes are better than IDs
	don't specify font-sizes more than once
	avoid making classes for one rule
	avoid using pixels for font-sizes except on body
	don't abuse less nesting

*/

body {
  -webkit-font-smoothing: antialiased;
}

p {
  color: #67818f;
}

.italic {
  font-style: italic;
}

* {
  transition: all 0.13s ease-in-out;
}

.whitetext.sans-serif-cond.uc a {
  color: #fff;
  text-decoration: none;
}

.whitetext.sans-serif-cond.uc a:hover {
  opacity: 0.7;
}

.whitetext.sans-serif-cond.uc a:hover i {
  margin-left: 10px;
}

.gradient-bg {
  background-color: rgba(0, 0, 0, 0);
  background-image: -webkit-gradient(
    linear,
    0 0%,
    0% 100%,
    from(rgba(0, 0, 0, 0.4)),
    to(rgba(0, 0, 0, 0))
  );
  background-image: -webkit-linear-gradient(
    top,
    rgba(0, 0, 0, 0.4),
    rgba(0, 0, 0, 0)
  );
  background-image: -moz-linear-gradient(
    top,
    rgba(0, 0, 0, 0.4),
    rgba(0, 0, 0, 0)
  );
  background-image: -ms-linear-gradient(
    top,
    rgba(0, 0, 0, 0.4),
    rgba(0, 0, 0, 0)
  );
  background-image: -o-linear-gradient(
    top,
    rgba(0, 0, 0, 0.4),
    rgba(0, 0, 0, 0)
  );
}

.site-header {
  position: relative;
  background-position: bottom center;
  background-size: cover;
  border-bottom: 4px solid #b2cc49;
}

.site-header .bg-image {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  -webkit-transition: top 0;
  -moz-transition: top 0;
  -ms-transition: top 0;
  -o-transition: top 0;
  transition: top 0;
  background-image: url(../img/home_img.jpg);
}

.site-header .bg-image:after {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 1;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0);
  background-image: -webkit-gradient(
    linear,
    0 0%,
    0% 100%,
    from(rgba(0, 0, 0, 0.4)),
    to(rgba(0, 0, 0, 0))
  );
  background-image: -webkit-linear-gradient(
    top,
    rgba(0, 0, 0, 0.4),
    rgba(0, 0, 0, 0)
  );
  background-image: -moz-linear-gradient(
    top,
    rgba(0, 0, 0, 0.4),
    rgba(0, 0, 0, 0)
  );
  background-image: -ms-linear-gradient(
    top,
    rgba(0, 0, 0, 0.4),
    rgba(0, 0, 0, 0)
  );
  background-image: -o-linear-gradient(
    top,
    rgba(0, 0, 0, 0.4),
    rgba(0, 0, 0, 0)
  );
  content: "";
}

.site-header .container {
  z-index: 1;
}

@media only screen and (min-width: 940px) {
}

.site-header .page-title {
  color: #fff;
  text-align: center;
}

.site-header .page-title h1 {
  margin: 0;
}

@media only screen and (min-width: 940px) {
  .site-header .page-title {
    font-size: 3em;
  }
}

.site-header .container.wide {
  padding: 3em 0;
}

@media only screen and (min-width: 940px) {
  .site-header .container.wide {
    padding: 160px 0 224px 0;
  }
}

.site-header .curtain {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 1;
  width: 100%;
  height: 100%;
  background-color: rgba(37, 83, 95, 0.5);
}

body.show-mnav {
  background-color: #102328 !important;
  -webkit-transition: none;
  -moz-transition: none;
  -ms-transition: none;
  -o-transition: none;
  transition: none;
}

body.show-mnav .main-navigation .menu-toggle i.icon-align-justify {
  display: none;
}

body.show-mnav .main-navigation .menu-toggle i.icon-chevron-right {
  display: block;
}

#page {
  background-color: #fff;
}

.panel {
  position: relative;
}

@media only screen and (min-width: 940px) {
  .panel {
    padding: 60px 0 0;
  }
}

.panel .panel-label {
  position: absolute;
  top: 0;
  left: 0;
  width: 5%;
  height: 100%;
  font-family: "Avenir Next", sans-serif;
  font-weight: 600;
  letter-spacing: 0.1em;
  text-transform: uppercase;
}

.panel .panel-label span {
  position: absolute;
  top: 70%;
  left: 50%;
  display: block;
  height: auto;
  line-height: 30px;
  text-align: center;
  white-space: nowrap;
  -webkit-transform: rotate(-90deg);
  -moz-transform: rotate(-90deg);
  -ms-transform: rotate(-90deg);
  -o-transform: rotate(-90deg);
  transform: rotate(-90deg);
  -webkit-transform-origin: top left;
  -moz-transform-origin: top left;
  -ms-transform-origin: top left;
  -o-transform-origin: top left;
  transform-origin: top left;
}

.panel .panel-content {
  font-size: 1.4em;
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}

@media only screen and (min-width: 940px) {
  .panel .panel-content {
    font-size: 1.7em;
  }
}

@media only screen and (min-width: 1100px) {
  .panel .panel-content {
    font-size: 2em;
  }
}

@media only screen and (min-width: 1240px) {
}

.home .site-header {
  overflow: hidden;
  -webkit-transform: translate3d(0, 0, 0, 0);
}

.home .nav-wrap {
  background-color: transparent;
}

.home .video-container {
  position: absolute;
  top: 0;
  right: 0 !important;
  bottom: 0 !important;
  left: 0;
  display: none;
  width: 100%;
  height: 100% !important;
  padding: 0 !important;
  -webkit-transition: top 0;
  -moz-transition: top 0;
  -ms-transition: top 0;
  -o-transition: top 0;
  transition: top 0;
}

.home .video-container video {
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  width: 100%;
}

@media only screen and (min-width: 1100px) {
  .home .video-container {
    display: block;
  }
}

.home .panel .panel-content {
  font-weight: 200;
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}

@media only screen and (min-width: 940px) {
  .home .panel .panel-content {
    font-size: 1em;
  }
}

.home .panel .container {
  padding-bottom: 40px;
}

.home .panel-1 {
  border-bottom: 4px solid #ffaa00;
}

.home .panel-1 .panel-bg {
  width: 100%;
  background-image: url(../img/ttt.jpg);
  background-position: bottom left;
  background-repeat: no-repeat;
  background-size: cover;
}

.home .panel-2 {
  padding: 2em 0 0 0;
  background: #17333a;
}

@media only screen and (min-width: 940px) {
  .home .panel-2 {
    padding: 6em 0 0 0;
  }
}

.home .panel-2 h2 {
  margin: 0;
}

.home .panel-2 h3 {
  margin: 0;
  margin-bottom: 0;
  font-size: 1.7em;
  letter-spacing: 0.1em;
}

.home .panel-2 .description {
  line-height: 1.6em;
  color: #ffffff;
}

@media only screen and (min-width: 940px) {
  .home .panel-2 .description {
    padding-left: 1em;
    margin-top: 0;
    font-size: 1.5em;
    border-left: 1px solid #ffaa00;
  }
}

.home .panel .no-padding {
  padding-bottom: 0 !important;
}

.home .panel .panel-action {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  font-family: "Avenir Next Condensed", sans-serif;
  font-size: 1.6em;
  font-weight: 600;
  line-height: 3em;
  text-align: center;
  text-transform: uppercase;
  cursor: pointer;
}

.home .panel .panel-action.white {
  color: #b2cc49;
  background-color: #faf9f5;
}

.home .panel .panel-action.white span {
  border-color: #b2cc49;
}

.home .panel .panel-action.white:hover {
  color: #657d0f;
  background-color: #b2cc49;
}

.home .panel .panel-action.blue {
  z-index: 999;
  color: #fff;
  background-color: #102328;
}

.home .panel .panel-action.blue span {
  border-color: #fff;
}

.home .panel .panel-action.blue:hover {
  background-color: #25535f;
}

@media only screen and (min-width: 1100px) {
  .home .panel .panel-action {
    position: absolute;
    top: 0;
    right: 0;
    left: auto;
    display: block;
    width: 8%;
    height: 100%;
  }
  .home .panel .panel-action span {
    position: absolute;
    top: 55%;
    left: 50%;
    display: block;
    width: auto;
    height: auto;
    margin-left: -15px;
    line-height: 30px;
    text-align: center;
    white-space: nowrap;
    border-bottom: 2px solid;
    -webkit-transform: rotate(-90deg);
    -moz-transform: rotate(-90deg);
    -ms-transform: rotate(-90deg);
    -o-transform: rotate(-90deg);
    transform: rotate(-90deg);
    -webkit-transform-origin: top left;
    -moz-transform-origin: top left;
    -ms-transform-origin: top left;
    -o-transform-origin: top left;
    transform-origin: top left;
  }
}

.half-boxes {
  position: relative;
  display: block;
  overflow: hidden;
  text-decoration: none;
  cursor: pointer;
  background-position: center;
  background-size: cover;
  background-size: 130%;
}

@media only screen and (min-width: 940px) {
  .half-boxes {
    display: inline;
    height: 0;
    padding-bottom: 20%;
  }
}

.half-boxes .acquired-banner {
  position: absolute;
  top: 10px;
  right: -55px;
  width: 200px;
  padding: 10px;
  font-family: "Avenir Next", sans-serif;
  font-size: 1.25em;
  font-weight: 600;
  color: white;
  text-align: center;
  text-transform: uppercase;
  background: #b2cc49;
  transform: rotate(30deg);
}

.half-boxes .investment-title {
  display: inline-block;
  font-family: "Sentinel SSm A", "Sentinel SSm B", serif;
  font-size: 1.5em;
  font-weight: bold;
  color: #ffffff;
  border-bottom: 2px solid #b2cc49;
}

.half-boxes .investment-title a {
  color: #ffffff;
  text-decoration: none;
}

@media only screen and (min-width: 940px) {
  .half-boxes .investment-title {
    font-size: 2em;
  }
}

.half-boxes .investment-description {
  min-height: 5em;
  padding-bottom: 2em;
  margin-top: 1em;
  font-family: "Avenir Next", sans-serif;
  font-weight: normal;
  line-height: 1.3em;
  color: #ffffff;
}

@media only screen and (min-width: 940px) {
  .half-boxes .investment-description {
    margin-top: 5em;
  }
}

.half-boxes .content-wrap {
  left: 5%;
  width: 90%;
  padding-top: 30px;
}

@media only screen and (min-width: 940px) {
  .half-boxes .content-wrap {
    position: absolute;
    top: 15em;
    left: 10%;
    width: 80%;
    padding-top: 0;
  }
}

.half-boxes p {
  font-size: 1em;
}

@media only screen and (min-width: 940px) {
  .half-boxes p {
    font-size: 1.2em;
  }
}

.half-boxes:hover {
  background-size: 120%;
}

.half-boxes:hover p {
  color: #fff;
}

.half-boxes:hover:after {
  background-color: rgba(204, 136, 0, 0.85);
}

.half-boxes:hover .content-wrap {
  top: 2em;
}

.half-boxes:hover .investment-title {
  border-bottom: 2px solid rgba(255, 255, 255, 0.5);
}

.half-boxes:hover .investment-description {
  margin-top: 1em;
}

.half-boxes:hover.more {
  color: #ffffff;
}

.half-boxes > * {
  position: relative;
  z-index: 101;
}

.half-boxes:after {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 100;
  display: block;
  width: 100%;
  height: 100%;
  background-color: rgba(37, 83, 95, 0.4);
  content: "";
  -webkit-transition: all, 0.3s;
  -moz-transition: all, 0.3s;
  -ms-transition: all, 0.3s;
  -o-transition: all, 0.3s;
  transition: all, 0.3s;
}

.half-boxes.more {
  position: relative;
  background-color: #17333a;
}

.half-boxes.more i {
  position: absolute;
  top: 50%;
  left: 50%;
  margin-top: -40px;
  margin-left: -40px;
  font-size: 80px;
  color: #3b8395;
}

.half-boxes.more:hover i {
  color: #ffffff;
}

.display-table {
  display: table;
  width: 100%;
  height: 100%;
}

.display-table-cell {
  display: table-cell;
}

.vmiddle {
  vertical-align: middle;
}

.w100 {
  width: 100%;
}

.h100 {
  height: 100%;
}

.pos-absolute {
  position: absolute;
}

.site-header.sub {
  background-image: url("../img/ttt.jpg");
  background-position: center;
  background-size: cover;
}

.sub .site-description {
  font-size: 4em;
  text-align: center;
}

.left-panel {
  z-index: 5;
}

@media only screen and (min-width: 940px) {
  .left-panel {
    position: absolute;
    top: 0;
    right: auto;
    left: 0;
    display: block;
    width: 8%;
    height: 100%;
    padding: 60px 0;
    border-right: 1px solid #d2d8d7;
  }
  .left-panel span {
    position: absolute;
    top: 70%;
    left: 70%;
    display: block;
    width: auto;
    height: auto;
    margin-left: -35px;
    font-family: "Avenir Next", sans-serif;
    font-size: 0.5em;
    font-weight: 500;
    line-height: 30px;
    color: #17333a;
    text-align: center;
    text-transform: uppercase;
    white-space: nowrap;
    -webkit-transform: rotate(-90deg);
    -moz-transform: rotate(-90deg);
    -ms-transform: rotate(-90deg);
    -o-transform: rotate(-90deg);
    transform: rotate(-90deg);
    -webkit-transform-origin: top left;
    -moz-transform-origin: top left;
    -ms-transform-origin: top left;
    -o-transform-origin: top left;
    transform-origin: top left;
  }
}

.tan {
  background-color: #fffefa;
}

@media only screen and (min-width: 940px) {
  .lighttan {
    background-color: lighttan;
  }
}

.content-right p {
  font-weight: 200;
}

@media only screen and (min-width: 940px) {
  .content-right {
    padding-bottom: 80px;
    padding-left: 140px;
    font-size: 20.8px;
  }
}

.historical-context {
  max-width: 515px;
  margin: 0 auto;
}

@media only screen and (min-width: 1100px) {
  .historical-context {
    max-width: 800px;
  }
}

.panel-2.bio-container {
  padding: 0;
  overflow: hidden;
}

@media only screen and (min-width: 1100px) {
  .panel-2.bio-container .left-panel span {
    top: 60%;
    color: #fff;
  }
}

.panel-2.bio-container h3 {
  padding-top: 70px;
  margin-bottom: 0;
  font-size: 1em;
  font-weight: 400;
  color: #fff;
}

.panel-2.bio-container .bio-bgs {
  position: relative;
  display: block;
}

.panel-2.bio-container .bio-bgs .bio-bg {
  display: none;
  width: 100%;
  height: 0;
  padding-bottom: 46.25%;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

.panel-2.bio-container .bio-bgs .bio-bg.show {
  display: block;
}

@media only screen and (min-width: 1100px) {
  .panel-2.bio-container .bio-bgs .bio-bg {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    padding-bottom: 0;
  }
}

@media only screen and (min-width: 1100px) {
  .panel-2.bio-container .bio-bgs {
    position: absolute;
    top: 0;
    left: 0;
    z-index: 1;
    width: 100%;
    height: 100%;
  }
}

.panel-2.bio-container .bio-content {
  position: relative;
  z-index: 2;
}

.panel-2.bio-container .bio-content-wrap {
  padding: 0 0 4em 0;
  overflow: auto;
  background-color: #17333a;
}

@media only screen and (min-width: 1100px) {
  .panel-2.bio-container .bio-content-wrap {
    padding: 0;
    background-color: transparent;
  }
}

.panel-2.bio-container .panel-content.about {
  max-width: 500px;
  margin: 0 auto;
  margin-left: 100px;
}

.panel-2.bio-container .panel-content.about p {
  padding-bottom: 1em;
  font-size: 0.5em;
  line-height: 1.8em;
  color: #fff;
}

@media only screen and (min-width: 1100px) {
  .panel-2.bio-container .panel-content.about {
    float: left;
    padding: 100px 50px;
    background-color: rgba(23, 51, 58, 0.8);
    -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
    box-sizing: border-box;
  }
}

.panel-2.bio-container .thumbs {
  float: left;
  height: 50px;
  padding-left: 0 !important;
  margin-left: 0 !important;
  text-decoration: none;
  list-style: none;
  cursor: pointer;
}

.panel-2.bio-container .thumbs li {
  float: left;
  width: 50px;
  height: 50px;
  margin-right: 7px;
  overflow: hidden;
}

@media only screen and (min-width: 1100px) {
  .panel-2.bio-container .thumbs li {
    margin-right: 20px;
  }
}

.panel-2.bio-container .thumbs li a.bio.thumb {
  display: block;
  width: 50px !important;
  height: 50px !important;
  background-position: center;
  background-repeat: no-repeat;
  background-size: 100%;
  transition: all 0.13s ease-in-out;
}

.panel-2.bio-container .thumbs li a.bio.thumb:hover {
  background-color: transparent;
  background-image: url("../img/ttt.jpg") !important;
  background-size: 40%;
}

.panel-2.bio-container .thumbs .current {
  background-image: url("../img/ttt.jpg");
  background-position: center;
  background-repeat: no-repeat;
  background-size: 40%;
}

.panel-2.bio-container .thumbs .current li:hover {
  opacity: 0;
}

.social-link {
  display: none;
  padding: 10px 40px;
  font-family: "Avenir Next", sans-serif;
  font-size: 0.4em;
  font-weight: 600;
  line-height: 1em;
  letter-spacing: 0.08em;
  color: #fff;
  text-decoration: none;
  text-transform: uppercase;
  border: 2px solid #fff;
  border-radius: 22px;
}

.social-link.show {
  display: inline-block;
  margin: 0 auto;
}

.social-link:hover {
  background-color: #b2cc49;
}

.social-link i {
  padding: 0 10px;
}

.investments.container.wide {
  padding: 0;
}

.investments {
  padding-bottom: 60px;
  margin-right: 0 !important;
  margin-left: 0 !important;
}

@media only screen and (min-width: 940px) {
  .investments {
    padding: 60px 100px;
  }
}

.investments-grid {
  overflow: auto;
  background-color: #17333a;
}

.opportunities .startups {
  background-image: url("../img/ui.jpg");
  background-position: center;
  background-size: cover;
}

.opportunities .investors {
  background-image: url("../img/ttt.jpg");
  background-position: center;
  background-size: cover;
}

.opportunities .thirdparties {
  background-image: url("../img/mi.jpg");
  background-position: center;
  background-size: cover;
}

.opportunities .celik {
  background-image: url("../img/celik.jpg");
  background-position: center;
  background-size: cover;
}

.opportunities .container.wide {
  width: 90% !important;
}

@media only screen and (min-width: 940px) {
  .opportunities .container.wide {
    width: 100% !important;
  }
}

@media only screen and (min-width: 940px) {
  .opportunities .container.wide .panel-content h2 {
    padding-top: 5px;
  }
}

.opportunities .container.wide .panel-content p {
  font-size: 19.2px;
  font-weight: 200;
}

.opportunities .container.wide .panel-content li {
  font-size: 15.2px;
  font-weight: 200;
}

ul.ul-two {
  columns: 2;
  -webkit-columns: 2;
  -moz-columns: 2;
}

ul.ul-one {
  columns: 1;
  -webkit-columns: 1;
  -moz-columns: 1;
}

@media only screen and (min-width: 940px) {
  .custom-margin {
    margin-top: 30px;
    margin-bottom: 20px;
  }
  .panel-content.first-one {
    margin-top: 15px !important;
  }
}

.opportunities .image-left {
  width: 111% !important;
  height: 15%;
  min-width: 300px;
  min-height: 280px;
  padding: 1px;
  margin-left: -6%;
}

@media only screen and (min-width: 720px) {
  .opportunities .image-left {
    width: 30% !important;
    margin-left: -15px !important;
  }
}

.opportunities .panel-action {
  position: relative;
  bottom: 0;
  left: 0;
  display: inline-block;
  width: 100%;
  margin-bottom: 2em;
  font-family: "Avenir Next Condensed", sans-serif;
  font-size: 1.3em;
  font-weight: 600;
  line-height: 3em;
  text-align: center;
  text-transform: uppercase;
  cursor: pointer;
  background-color: #eee;
  -webkit-border-radius: 3px;
  -moz-border-radius: 3px;
  border-radius: 3px;
  -webkit-background-clip: padding-box;
  -moz-background-clip: padding;
  background-clip: padding-box;
}

.opportunities .panel-action.white {
  color: #b2cc49;
  background-color: #faf9f5;
}

.opportunities .panel-action.white span {
  border-color: #b2cc49;
}

.opportunities .panel-action.white:hover {
  color: #657d0f;
  background-color: #b2cc49;
}

.opportunities .panel-action.tan {
  color: #b2cc49;
}

.opportunities .panel-action.tan span {
  border-color: #b2cc49;
}

.opportunities .panel-action.tan:hover {
  color: #657d0f;
  background-color: #b2cc49;
}

.opportunities .panel-action.lighttan {
  color: #b2cc49;
}

.opportunities .panel-action.lighttan span {
  border-color: #b2cc49;
}

.opportunities .panel-action.lighttan:hover {
  color: #657d0f;
  background-color: #b2cc49;
}

@media only screen and (min-width: 940px) {
  .opportunities .panel-action {
    position: absolute;
    top: 0;
    right: 0;
    left: auto;
    display: block;
    width: 8%;
    height: 100%;
    margin-bottom: none;
    background-color: transparent;
    -webkit-border-radius: 0;
    -moz-border-radius: 0;
    border-radius: 0;
    -webkit-background-clip: padding-box;
    -moz-background-clip: padding;
    background-clip: padding-box;
  }
  .opportunities .panel-action span {
    position: absolute;
    top: 65%;
    left: 50%;
    display: block;
    width: auto;
    height: auto;
    margin-left: -15px;
    line-height: 30px;
    text-align: center;
    white-space: nowrap;
    border-bottom: 2px solid;
    -webkit-transform: rotate(-90deg);
    -moz-transform: rotate(-90deg);
    -ms-transform: rotate(-90deg);
    -o-transform: rotate(-90deg);
    transform: rotate(-90deg);
    -webkit-transform-origin: top left;
    -moz-transform-origin: top left;
    -ms-transform-origin: top left;
    -o-transform-origin: top left;
    transform-origin: top left;
  }
}

div.panel-action span {
  display: block;
  padding: 1em 0;
  color: #17333a;
  text-align: center;
  background-color: #eee;
}

@media only screen and (min-width: 940px) {
  div.panel-action span {
    display: inline;
    padding: 0;
    text-align: inherit;
    background-color: transparent;
  }
}

@media only screen and (min-width: 1100px) {
  div.panel-action span {
    margin-bottom: 1em;
  }
}

.category.panel-2 .left-panel span {
  top: 60%;
  color: #17333a;
}

.category.panel-2 h3 {
  color: #17333a;
}

.category {
  color: #58666e;
}

.category p {
  font-weight: 200;
}

.category ul.columnize li {
  padding: 10px 0;
  font-size: 80%;
  font-weight: 500;
}

.container.wide {
  width: 100% !important;
  padding-bottom: 0;
  padding-left: 0;
}

.bg-blue-case {
  background-color: #193f49;
}

.case-study.panel.first {
  padding: 4em 0;
  font-family: "Avenir Next", sans-serif;
  font-size: 1.2em;
  line-height: 1.6em;
  color: #ffffff;
}

.case-study.panel.first p {
  color: #ffffff;
  text-align: left;
}

.case-study.panel.first .half-boxes {
  float: none;
  width: 90%;
  height: auto;
  padding: 4em 0;
  margin: 0 auto;
  color: #ffffff;
  text-align: center;
}

@media only screen and (min-width: 720px) {
  .case-study.panel.first .half-boxes {
    float: left;
    width: 50%;
  }
}

@media only screen and (min-width: 720px) {
  .container.wide {
    width: 100vw !important;
  }
}

.case-study.panel.first .half-boxes:after {
  background-color: transparent;
}

.case-study.panel.first .half-boxes:hover:after {
  background-color: transparent;
}

.case-study.panel.first .half-boxes p {
  margin-top: 0;
  font-size: 1.24em;
  line-height: 1.7em;
  color: #ddd;
}

.case-study.panel.first .half-boxes .quote {
  font-size: 2em;
  font-style: italic;
  font-weight: 600;
  line-height: 1.4em;
  color: #d2d8d7;
  text-align: center;
}

.case-study.panel.first .half-boxes .quote:before {
  content: "\201C";
}

.case-study.panel.first .half-boxes .quote:after {
  content: "\201D";
}

.case-study.panel.first .half-boxes .author {
  display: inline-block;
  min-width: 140px;
  padding: 15px 0;
  margin: 0 auto;
  margin-top: 40px;
  clear: both;
  font-size: 0.9em;
  color: #d2d8d7;
  text-align: center;
  white-space: nowrap;
  border-top: 2px solid #04aec3;
  border-bottom: 2px solid #04aec3;
}

@media only screen and (min-width: 720px) {
  .case-study.panel.first .half-boxes.left {
    border-right: 1px solid rgba(88, 102, 110, 0.75);
  }
}

.case-study.panel-2 .four.columns {
  width: 33.333% !important;
  margin: 0 !important;
}

.case-study.panel-2 h2 {
  padding-top: 50px;
  margin-bottom: -10px;
  font-size: 3.5em;
  color: #fff;
  text-align: center;
}

.case-study.panel-2 .graph {
  margin-top: 0;
  margin-bottom: 100px;
  font-size: 0.8em;
  color: #58666e;
  text-align: center;
}

.case-study.panel-2 .graph:after {
  padding-left: 10px;
  content: url("../img/ttt.jpg");
}

.orange {
  background-color: #ffaa00;
}

.orange-light {
  background-color: #ffbb33;
}

.case-study-body {
  padding: 120px 60px;
}

.case-study.founders {
  padding-bottom: 80px;
}

.case-study.founders .profile-image {
  display: block;
  width: 100%;
  height: 0;
  min-width: 200px;
  padding-bottom: 100%;
  background-color: #d2d8d7;
  background-position: center;
  background-size: 100%;
  background-size: cover;
}

.case-study.founders h4,
.case-study.founders p {
  text-align: center;
}

.case-study.founders h2 {
  padding-bottom: 60px;
  text-align: center;
}

.case-study.founders h4 {
  margin-bottom: -10px;
  font-size: 1em;
  color: #58666e;
}

.case-study.founders p {
  font-size: 0.6em;
  color: #8a99a2;
}

.case-study.founders .three.columns {
  padding-bottom: 20px !important;
}

main {
  border-bottom: 1px solid rgba(88, 102, 110, 0.5);
}

.panel.contact {
  max-width: 600px;
  margin: 0 auto;
}

.blog-post {
  padding: 20px;
  margin: 30px 0;
}

.blog-post .entry-image {
  float: left;
}

.blog-post .entry-meta a {
  line-height: 3em;
  color: #58666e;
  text-decoration: none;
}

.blog-post .entry-content {
  margin-top: 0;
}

.blog-post .entry-content p {
  font-size: 0.9em;
  font-weight: 200;
}

.blog-post .blog-content-wrap {
  max-width: 600px;
}

.blog-post h2 {
  margin-top: 0;
  margin-bottom: 6px;
}

.blog-post h2 a {
  overflow: hidden;
  font-size: 1.2em;
  font-weight: 600;
  color: #17333a;
  text-decoration: none;
  border-left: 1px solid #fff;
  transition: all 0.3s ease-in-out;
}

.blog-post h2 a:hover {
  padding-left: 10px;
  border-left: 8px solid #b2cc49;
}

.author-image {
  display: inline;
  float: left;
  width: 50px;
  height: 50px;
  margin: 0 15px;
  margin-left: 0;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  border-radius: 50%;
}

@media only screen and (min-width: 940px) {
}

.blog .site-header {
  min-height: 80px;
  background-image: none !important;
  border-bottom: 1px solid #58666e;
}

.blog .site-header .container.wide {
  background-color: rgba(0, 0, 0, 0);
  background-image: none;
}

.blog .site-header .container.wide .site-branding {
  color: #58666e;
}

.blog .site-header .container.wide .site-branding .main-navigation {
  margin-bottom: 25px;
}

.blog .site-header .container.wide .site-branding .main-navigation .logo,
.blog .site-header .container.wide .site-branding .main-navigation .menu-toggle,
.blog .site-header .container.wide .site-branding .main-navigation .menu-item {
  color: #58666e;
}

.blog .site-header .container.wide .site-branding .main-navigation .logo svg {
  fill: #58666e;
}

.blog .site-header .container.wide .site-branding .main-navigation .menu a {
  color: #58666e;
}

.blog
  .site-header
  .container.wide
  .site-branding
  .main-navigation
  .nav-contact
  a {
  padding: 0 10px;
  border: 2px solid rgba(255, 255, 255, 0.5);
  border-radius: 5px;
}

.blog
  .site-header
  .container.wide
  .site-branding
  .main-navigation
  .nav-contact
  a:hover {
  color: #fff;
  background-color: #b2cc49;
}

.blog .site-header .container.wide .row.page-title {
  display: none;
}

.footer-help {
  padding-top: 1em;
  font-family: "Avenir Next", sans-serif;
}

@media only screen and (min-width: 940px) {
  .footer-help {
    padding-top: 3em;
  }
}

.footer-help p {
  margin-bottom: 2em;
  font-size: 0.9em;
  color: #222;
}

@media only screen and (min-width: 940px) {
  .footer-help p {
    margin-bottom: 0.5em;
    font-size: 1.1em;
    line-height: 1.6em;
  }
}

.footer-help h3 {
  margin-top: 0;
  margin-bottom: 0.3em;
  font-family: "Avenir Next", sans-serif;
  font-size: 1.2em;
  font-weight: bold;
}

@media only screen and (min-width: 940px) {
  .footer-help h3 {
    font-size: 2em;
  }
}

.footer-help .cta-button {
  display: block;
  padding: 0.6em 1em 0.5em 1em;
  margin-bottom: 1em;
  font-family: "Avenir Next", sans-serif;
  font-size: 1.2em;
  font-weight: 400;
  color: #222;
  text-align: center;
  text-decoration: none;
  text-transform: uppercase;
  border: 2px solid rgba(23, 51, 58, 0.09999999999999998);
  -webkit-border-radius: 30px;
  -moz-border-radius: 30px;
  border-radius: 30px;
  -webkit-background-clip: padding-box;
  -moz-background-clip: padding;
  background-clip: padding-box;
}

.footer-help .cta-button:hover {
  border: 2px solid #b2cc49;
}

.panel .icon-chevron-right {
  position: relative;
  top: -2px;
  left: 4px;
  display: inline-block;
  width: 18px;
  height: 18px;
  font-size: 14px;
  line-height: 19px;
  letter-spacing: 0;
  text-align: center;
  text-indent: 1px;
  border: 2px solid #ffaa00;
  border-radius: 50%;
}

.panel-3 {
  padding: 30px 0 0 0;
  padding-bottom: 0;
}

@media only screen and (min-width: 940px) {
  .panel-3 {
    padding: 0;
  }
}

.panel-3 h2 {
  color: #17333a;
}

.panel-3 .panel-bg {
  width: 100%;
  height: 0;
  padding-bottom: 41.40625%;
  background-image: url(../img/ttt.jpg);
  background-position: bottom center;
  background-repeat: no-repeat;
  background-size: 100%;
}

.footer-bottom {
  position: relative;
  padding: 30px 0 30px 0;
  color: #ffffff;
  background-image: url(../img/ttt.jpg);
  background-position: top center;
  background-repeat: no-repeat;
  background-size: cover;
}

@media only screen and (min-width: 940px) {
  .footer-bottom {
    padding: 300px 0 30px 0;
  }
}

.footer-bottom .curtain {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 1;
  width: 100%;
  height: 100%;
  background: -moz-linear-gradient(
    top,
    rgba(51, 51, 51, 0) 0,
    rgba(51, 51, 51, 0) 34%,
    rgba(51, 51, 51, 0.6) 100%
  );
  background: -webkit-gradient(
    linear,
    left top,
    left bottom,
    color-stop(0, rgba(51, 51, 51, 0)),
    color-stop(34%, rgba(51, 51, 51, 0)),
    color-stop(100%, rgba(51, 51, 51, 0.6))
  );
  background: -webkit-linear-gradient(
    top,
    rgba(51, 51, 51, 0) 0,
    rgba(51, 51, 51, 0) 34%,
    rgba(51, 51, 51, 0.6) 100%
  );
  background: -o-linear-gradient(
    top,
    rgba(51, 51, 51, 0) 0,
    rgba(51, 51, 51, 0) 34%,
    rgba(51, 51, 51, 0.6) 100%
  );
  background: -ms-linear-gradient(
    top,
    rgba(51, 51, 51, 0) 0,
    rgba(51, 51, 51, 0) 34%,
    rgba(51, 51, 51, 0.6) 100%
  );
  background: linear-gradient(
    to bottom,
    rgba(51, 51, 51, 0) 0,
    rgba(51, 51, 51, 0) 34%,
    rgba(51, 51, 51, 0.6) 100%
  );
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#00333333', endColorstr='#99333333', GradientType=0);
}

.footer-bottom .menu {
  display: none;
}

@media only screen and (min-width: 940px) {
  .footer-bottom .menu {
    display: inline;
  }
}

.footer-bottom .menu li a {
  text-decoration: none;
  border-bottom: none;
}

.footer-bottom .container {
  position: relative;
  z-index: 2;
}

.footer-bottom a {
  color: #fff;
  text-decoration: none;
  border-bottom: 1px dotted #fff;
}

.footer-bottom ul {
  padding: 0;
  margin: 0;
}

.footer-bottom ul li {
  margin-bottom: 0.7em;
  list-style-type: none;
}

.footer-bottom ul li a {
  font-family: "Avenir Next", sans-serif;
  font-size: 1.2em;
  font-weight: bold;
  color: #ffffff;
  text-decoration: none;
  text-transform: uppercase;
}

.footer-bottom .border-top {
  text-align: center;
  border-top: 1px solid rgba(255, 255, 255, 0.19999999999999996);
}

@media only screen and (min-width: 940px) {
  .footer-bottom .border-top {
    text-align: none;
  }
}

.footer-bottom .copyright,
.footer-bottom .flag {
  margin-top: 3em;
  font-family: "Avenir Next", sans-serif;
  font-size: 0.8em;
  text-align: center;
}

@media only screen and (min-width: 940px) {
  .footer-bottom .copyright,
  .footer-bottom .flag {
    text-align: left;
  }
}

.footer-bottom .copyright a,
.footer-bottom .flag a {
  text-decoration: none;
  border-bottom: none;
}

.footer-bottom .flag {
  text-align: center;
}

@media only screen and (min-width: 940px) {
  .footer-bottom .flag {
    text-align: right;
  }
}

.footer-bottom h3 {
  margin: 0 0 1em 0;
  font-family: "Avenir Next", sans-serif;
  text-transform: uppercase;
}

.footer-bottom .border-left {
  padding: 2em 0;
  margin: 3em 0;
  border-top: 1px solid rgba(255, 255, 255, 0.19999999999999996);
  border-bottom: 1px solid rgba(255, 255, 255, 0.19999999999999996);
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}

@media only screen and (min-width: 940px) {
  .footer-bottom .border-left {
    min-height: 300px;
    padding: 0 4em;
    margin: 0;
    border-top: none;
    border-right: 1px solid rgba(255, 255, 255, 0.19999999999999996);
    border-bottom: none;
    border-left: 1px solid rgba(255, 255, 255, 0.19999999999999996);
  }
}

.footer-bottom .tweets {
  padding: 0;
  margin: 0;
}

.footer-bottom .tweets li {
  margin-bottom: 2em;
  font-family: "Avenir Next", sans-serif;
  font-size: 0.9em;
  list-style-type: none;
}

.footer-bottom .tweets li a {
  font-size: 1em;
  font-weight: normal;
  color: #fff;
  text-transform: none;
  border-bottom: 1px dotted #fff;
}

.footer-bottom .twitter-link {
  display: inline-block;
  padding-bottom: 3px;
  font-family: "Avenir Next", sans-serif;
  font-weight: bold;
  color: #ffffff;
  text-decoration: none;
  border-bottom: 2px solid #ffffff;
}

[class^="ratio-"] {
  position: relative;
  display: block;
  width: 100%;
  height: 0;
  background-color: #eee;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

[class^="ratio-"] iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100% !important;
  height: 100% !important;
}

.ratio-sixteen-nine {
  padding-bottom: 56.25%;
}

.ratio-three-one {
  padding-bottom: 33.33%;
}

.ratio-square,
.ratio-1-1 {
  padding-bottom: 100%;
}

.ratio-two-one {
  padding-bottom: 50%;
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}

.panel-bg.home-quote {
  padding: 5em 0 6em 0;
}

.panel-bg.home-quote .quote {
  line-height: 1.6em;
}

.panel-bg.home-quote .quote:before {
  margin-left: -0.45em;
  font-size: 1em;
  content: "\201C";
}

.panel-bg.home-quote .quote:after {
  margin-right: -1em;
  font-size: 1em;
  content: "\201D";
}

@media only screen and (min-width: 940px) {
  .panel-bg.home-quote .quote {
    font-size: 1.5em;
  }
}

.panel-bg.home-quote .attribution {
  margin-top: 2em;
  font-family: "Avenir Next", sans-serif;
  font-weight: bold;
  text-transform: uppercase;
}

.cta {
  display: block;
  padding: 20px;
  margin-bottom: 12px;
  font-family: "Avenir Next Condensed", sans-serif;
  font-size: 2em;
  font-weight: 600;
  letter-spacing: 0.06em;
  color: #fff;
  text-align: center;
  text-transform: uppercase;
  cursor: pointer;
  background-color: #b2cc49;
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}

.cta:hover {
  background-color: #17333a;
}

.cta:hover i {
  color: #ffaa00;
  border-color: #ffaa00;
}

.cta .icon-chevron-right {
  top: -5px;
  color: #fff;
  border-color: #fff;
}

.cta-desc {
  font-family: "Avenir Next", sans-serif;
  font-size: 80%;
  font-weight: 600;
  line-height: 1.2;
  letter-spacing: 0.1em;
  color: #67818f;
  text-transform: uppercase;
}

.half-boxes {
  font-size: 75%;
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}

@media only screen and (min-width: 940px) {
  .half-boxes {
    float: left;
    width: 33.33%;
  }
  .half-boxes p {
    padding-right: 20px;
  }
}

.site-description {
  margin: 0 0 0.5em 0;
  font-size: 1.6em;
  line-height: 1;
  color: #fff;
}

@media only screen and (min-width: 720px) {
  .site-description {
    margin: 0;
    font-size: 4em;
  }
}

@media only screen and (min-width: 940px) {
  .site-description {
    font-size: 6em;
  }
}

.long-site-description {
  margin-bottom: 6em;
  font-size: 1em;
  color: #fff;
}

@media only screen and (min-width: 940px) {
  .long-site-description {
    font-size: 1.8em;
  }
}

.home-intro {
  font-weight: 300;
  line-height: 1.6em;
}

.home-intro h2 {
  margin: 1.5em 0 0 0;
  font-family: "Avenir Next", sans-serif;
  font-size: 1.8em;
  text-transform: uppercase;
}

@media only screen and (min-width: 940px) {
  .home-intro h2 {
    margin: 0.83em 0;
    font-size: 2.2em;
  }
}

.home-intro a {
  padding-bottom: 3px;
  font-family: "Avenir Next", sans-serif;
  font-weight: bold;
  color: #b2cc49;
  text-decoration: none;
  text-transform: uppercase;
  border-bottom: 2px solid #b2cc49;
}

.home-intro p.big {
  font-size: 2em;
  line-height: 1.4em;
  color: #b2cc49;
}

@media (min-width: 1325px) and (max-width: 1450px) {
  .home-intro .six.columns {
    width: 550px;
  }
}

@media (min-width: 1240px) and (max-width: 1324px) {
  .home-intro .six.columns {
    width: 525px;
  }
}

@media (min-width: 1100px) and (max-width: 1239px) {
  .home-intro .six.columns {
    width: 465px;
  }
}

.nav-wrap {
  position: relative;
  top: 0;
  left: 0;
  z-index: 1000;
  width: 100%;
  -webkit-transition: background-color 0.5s;
  -moz-transition: background-color 0.5s;
  -ms-transition: background-color 0.5s;
  -o-transition: background-color 0.5s;
  transition: background-color 0.5s;
}

.nav-wrap.fix {
  position: fixed;
  padding-top: 0;
  border-bottom: none;
}

.nav-wrap.fix .logo {
  opacity: 0;
}

@media only screen and (min-width: 940px) {
  .nav-wrap.fix {
    background-color: rgba(23, 51, 58, 0.95);
    box-shadow: 0 0px 15px rgba(0, 0, 0, 0.5);
  }
  .nav-wrap.fix .logo {
    opacity: 1;
  }
}

@media only screen and (min-width: 940px) {
  .nav-wrap {
    padding-top: 1.5em;
  }
}

.main-navigation {
  position: relative;
  margin-top: 25px;
  margin-bottom: 25px;
}

@media only screen and (min-width: 940px) {
  .main-navigation {
    margin-top: 25px;
  }
}

.main-navigation .logo {
  position: relative;
  display: block;
  float: left;
  width: 120px;
  height: 0;
  padding: 0;
  padding-bottom: 37px;
  padding-left: 55px;
  font-size: 0.5em;
  font-weight: 600;
  line-height: 1.35;
  letter-spacing: 0.1em;
  color: #fff;
  text-transform: uppercase;
}

.main-navigation .logo svg {
  position: absolute;
  top: 0;
  left: 0;
  width: 50px;
  height: 22px;
  fill: #fff;
}

@media only screen and (min-width: 940px) {
  .main-navigation .logo {
    width: 200px;
    padding-left: 100px;
    font-size: 1em;
  }
  .main-navigation .logo svg {
    width: 90px;
    height: 37px;
  }
}

.main-navigation .menu-toggle {
  position: absolute;
  top: -10px;
  right: 0;
  z-index: 999;
  display: block;
  width: 30px;
  height: 30px;
  margin: 0;
  line-height: 1em;
  color: #aaa;
  background-color: #eee;
  -webkit-border-radius: 3px;
  -moz-border-radius: 3px;
  border-radius: 3px;
  -webkit-background-clip: padding-box;
  -moz-background-clip: padding;
  background-clip: padding-box;
}

.main-navigation .menu-toggle i.icon-align-justify {
  position: absolute;
  top: -15%;
  left: 57%;
  margin-top: -15px;
  margin-left: -9px;
  font-size: 20px;
  color: #aaa;
}

.main-navigation .menu-toggle i.icon-chevron-right {
  position: absolute;
  top: 50%;
  left: 50%;
  display: none;
  margin-top: -15px;
  margin-left: -4px;
  font-size: 20px;
  color: #aaa;
}

@media only screen and (min-width: 940px) {
  .main-navigation .menu-toggle {
    display: none;
  }
}

.main-navigation.toggled .nav-menu {
  right: 0;
  box-shadow: 0 0px 25px rgba(0, 0, 0, 0.5);
}

.main-navigation .nav-menu {
  position: fixed;
  top: 0;
  right: -100%;
  display: block;
  width: 80%;
  height: 100%;
  padding-top: 20px;
  padding-left: 20px;
  text-align: left;
  background-color: rgba(16, 35, 40, 0.95);
  border-left: 1px solid #666;
  -webkit-transition: all 0.25s;
  -moz-transition: all 0.25s;
  -ms-transition: all 0.25s;
  -o-transition: all 0.25s;
  transition: all 0.25s;
}

.main-navigation .nav-menu a {
  display: block;
  padding: 16px 8px;
  font-family: "Avenir Next", sans-serif;
  color: #ffffff;
  border-bottom: 1px solid rgba(255, 255, 255, 0.09999999999999998);
}

@media only screen and (min-width: 940px) {
  .main-navigation .nav-menu {
    position: relative;
    top: auto;
    right: auto;
    left: auto;
    display: inherit;
    width: auto;
    height: auto;
    padding-top: 0;
    padding-left: 0;
    margin-top: 0;
    text-align: none;
    background: none;
    background-color: none;
    border-left: 0;
  }
}

.main-navigation ul {
  display: none;
}

@media only screen and (min-width: 940px) {
  .main-navigation ul {
    display: block;
  }
}

.main-navigation .menu li {
  display: block;
  float: none;
}

@media only screen and (min-width: 940px) {
  .main-navigation .menu {
    float: right;
    line-height: 37px;
  }
  .main-navigation .menu li {
    float: left;
    margin-left: 15px;
  }
  .main-navigation .menu a {
    padding: 1em 0 0.9em 0;
    font-family: "Avenir Next", sans-serif;
    font-size: 14px;
    font-weight: 600;
    line-height: 1em;
    letter-spacing: 0.1em;
    color: #fff;
    text-transform: uppercase;
    border-top: 2px solid transparent;
    border-bottom: 2px solid transparent;
  }
  .main-navigation .menu a:hover {
    border-bottom: 2px solid rgba(255, 255, 255, 0.5);
  }
  .main-navigation .menu .current_page_item a {
    border-bottom: 2px solid #fff;
  }
  .main-navigation .menu .nav-contact a {
    padding: 1em 1.5em 0.9em 1.5em;
    line-height: 1em;
    border: 2px solid rgba(255, 255, 255, 0.3);
    border-radius: 5px;
  }
  .main-navigation .menu .nav-contact a:hover {
    background-color: #b2cc49;
    border: 2px solid #b2cc49;
  }
}

@media only screen and (min-width: 1100px) {
  .main-navigation .menu li {
    margin-left: 35px;
  }
}

.more-link,
.close-alert {
  display: block;
  padding: 0 6px;
  line-height: 3;
  cursor: pointer;
  background: #9eb834;
}

@media only screen and (min-width: 940px) {
  .more-link,
  .close-alert {
    display: inline-block;
    line-height: 1;
    background-color: transparent;
  }
  .more-link:hover,
  .close-alert:hover {
    background: #9eb834;
  }
}

.more-link:hover,
.close-alert:hover {
  color: #c6d979;
  background: #90a92f;
}

@media only screen and (min-width: 300px) {
  .close-alert i {
    display: none;
  }
}

@media only screen and (min-width: 940px) {
  .close-alert {
    display: block;
    float: right;
    padding: 0 20px;
    margin-right: -2%;
    line-height: 4em;
  }
  .close-alert span {
    display: none;
  }
  .close-alert i {
    display: inline;
  }
}

@media only screen and (min-width: 1100px) {
  .close-alert span {
    display: inline;
  }
}

.more-link {
  text-decoration: none;
}

@media only screen and (min-width: 300px) {
  .more-link i {
    display: none;
  }
}

@media only screen and (min-width: 940px) {
  .more-link {
    display: inline;
    float: right;
    padding: 0 20px;
    line-height: 4em;
    border-right: 1px solid rgba(255, 255, 255, 0.4);
    border-left: 1px solid rgba(255, 255, 255, 0.4);
  }
  .more-link span {
    display: none;
  }
  .more-link i {
    display: inline;
  }
}

@media only screen and (min-width: 1100px) {
  .more-link span {
    display: inline;
  }
}

.nav-placeholder {
  display: none;
}

.show {
  display: block;
}

.hide {
  display: none;
}

.sitewide-alert {
  position: relative;
  z-index: 1000;
  display: block;
  overflow: auto;
  font-family: "Avenir Next", sans-serif;
  font-size: 0.85em;
  font-weight: 300;
  font-weight: 600;
  color: #657d0f;
  text-align: center;
  background-color: #b2cc49;
}

@media only screen and (min-width: 940px) {
  .sitewide-alert {
    text-align: left;
  }
}

@media only screen and (min-width: 720px) {
  .sitewide-alert {
    line-height: 4em;
  }
}

.sitewide-alert a {
  color: #657d0f;
}

.sitewide-alert span {
  font-family: "Avenir Next Condensed", sans-serif;
  font-size: 1.2em;
}

@media only screen and (min-width: 940px) {
  .columnize {
    -moz-column-count: 2;
    -moz-column-gap: 40px;
    -webkit-column-count: 2;
    -webkit-column-gap: 40px;
  }
}

#main.investments-index .panel-1 .content-right {
  padding-bottom: 60px;
}

/* Wufoo Stuff */

.info {
  display: inline-block;
  padding: 0 1% 1.1em 1%;
  margin: 0 0 5px 0;
  clear: both;
}

.info[class] {
  display: block;
}

.hideHeader .info,
#payment.hideHeader li.first {
  display: none;
}

.info h2 {
  margin: 1em 0 5px 0;
  clear: left;
  font-family: "Avenir Next", sans-serif;
  font-size: 120%;
  font-weight: normal;
  font-weight: bold;
  text-align: center;
}

@media only screen and (min-width: 940px) {
  .info h2 {
    font-size: 200%;
  }
}

.info div {
  font-size: 95%;
  line-height: 135%;
  color: #555555;
}

form ul {
  padding: 0;
  margin: 0;
  list-style-type: none;
}

form ul span {
  width: 48%;
}

* html form ul {
  width: 99%;
  zoom: 1;
}

form li {
  position: relative;
  padding: 6px 1% 9px 1%;
  margin: 0;
  clear: both;
  background-color: transparent;
  -webkit-transition: background-color 350ms ease-out;
  -moz-transition: background-color 350ms ease-out;
  -o-transition: background-color 350ms ease-out;
  transition: background-color 350ms ease-out;
}

form ul:after,
form li:after,
form li div:after {
  display: block;
  height: 0;
  clear: both;
  content: ".";
  visibility: hidden;
}

* html form li {
  height: 1%;
  margin-bottom: -3px;
}

* + html form li {
  height: 1%;
  margin-bottom: -3px;
}

* html form li div {
  display: inline-block;
}

* + html form ul,
* + html form li div {
  display: inline-block;
}

form li div {
  padding: 0;
  margin: 0;
  color: #444444;
}

form li span {
  float: left;
  padding: 0;
  margin: 0 0.3em 0 0;
  color: #444444;
}

form li div span {
  display: block;
  float: left;
  width: 100%;
  margin: 0;
}

li.twoColumns div span {
  width: 48%;
  margin: 0 5px 0 0;
}

li.threeColumns div span {
  width: 30%;
  margin: 0 5px 0 0;
}

li.notStacked div span {
  width: auto;
  margin: 0 7px 0 0;
}

form li.complex {
  padding-bottom: 0;
}

form li.complex div span {
  width: auto;
  padding-bottom: 12px;
  margin: 0 0.3em 0 0;
}

form li.complex div span.full {
  margin: 0;
}

form li.complex div span.left,
form li.complex div span.right {
  width: 48%;
  margin: 0;
}

form li.complex div span.full input,
form li.complex div span.full select,
form li.complex div span.left input,
form li.complex div span.right input,
form li.complex div span.left select,
form li.complex div span.right select {
  width: 100%;
}

.left {
  float: left;
}

.right {
  float: right;
}

.clear {
  clear: both !important;
}

label span,
.section span,
p span,
.likert span {
  display: inline !important;
  float: none !important;
}

form li div label,
form li span label {
  display: block;
  padding-top: 3px;
  margin: 0;
  clear: both;
  font-size: 85%;
  line-height: 160%;
  color: #444;
}

fieldset {
  display: block;
  padding: 0;
  margin: 0;
  border: none;
}

label.desc,
legend.desc {
  display: block;
  width: 100%;
  padding: 0 0 3px 0;
  margin: 0;
  font-family: "Avenir Next", sans-serif;
  font-size: 95%;
  font-size: 1.1em;
  font-weight: normal;
  line-height: 150%;
  color: #222;
  white-space: normal;
  border: none;
}

label.choice {
  display: block;
  width: 88%;
  padding: 0 0 5px 0;
  margin: -17px 0 0 23px;
  font-size: 100%;
  line-height: 150%;
  color: #222;
  cursor: pointer;
}

.safari label.choice {
  margin-top: -16px;
}

form.rightLabel .desc {
  padding-top: 2px;
}

span.symbol {
  font-size: 120%;
  line-height: 135%;
}

form li .datepicker {
  float: left;
  width: 16px;
  height: 16px;
  padding: 0;
  margin: 0.19em 5px 0 0;
  cursor: pointer !important;
}

form span.req {
  display: inline;
  float: none;
  padding: 0;
  margin: 0;
  font-weight: bold;
  color: red !important;
}

form li div label var {
  font-style: normal;
  font-weight: bold;
}

form li div label .currently {
  display: none;
}

input.text,
input.search,
input.file,
textarea.textarea,
select.select {
  padding: 2px 0;
  margin: 0;
  font-size: 100%;
  color: #333;
}

input.text,
input.search,
textarea.textarea {
  width: 100%;
  padding: 0.5em;
  border: 1px solid #ccc;
  -webkit-border-radius: 10px;
  -moz-border-radius: 10px;
  border-radius: 10px;
  -webkit-box-shadow: none;
  -moz-box-shadow: none;
  box-shadow: none;
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
  -webkit-background-clip: padding-box;
  -moz-background-clip: padding;
  background-clip: padding-box;
}

input.nospin::-webkit-inner-spin-button,
input.nospin::-webkit-outer-spin-button {
  margin: 0;
  -webkit-appearance: none;
}

select.select {
  padding: 1px 0 0 0;
}

input.search {
  padding-left: 6px;
  -webkit-border-radius: 10px;
  -moz-border-radius: 10px;
  border-radius: 10px;
}

input.checkbox,
input.radio {
  display: block;
  width: 13px;
  height: 13px;
  padding: 0;
  margin: 4px 0 0 0;
}

input.other {
  margin: 0 0 8px 25px;
}

.safari select.select {
  margin: 0 0 1px 0;
  font-size: 120% !important;
}

* html select.select {
  margin: 1px 0;
}

* + html select.select {
  margin: 1px 0;
}

.center,
form li span.center input.text,
form li span.center label,
form li.name span label,
form li.date input.text,
form li.date span label,
form li.phone input.text,
form li.phone span label,
form li.time input.text,
form li.time span label {
  text-align: center;
}

form li.time select.select {
  margin-left: 5px;
}

form li.price .right {
  text-align: right;
}

.third {
  width: 32% !important;
}

.half {
  width: 48% !important;
}

.full {
  width: 100% !important;
}

input.small,
select.small {
  width: 25%;
}

input.medium,
select.medium {
  display: block;
}

input.large,
select.large {
  width: 100%;
}

.msie[class] select.ieSelectFix {
  width: auto;
}

.msie[class] select.ieSelectFix.small {
  min-width: 25%;
}

.msie[class] select.ieSelectFix.medium {
  min-width: 50%;
}

.msie[class] select.ieSelectFix.large {
  width: 100%;
}

textarea.textarea {
  width: 293px;
  max-width: 100%;
  min-width: 100%;
}

textarea.small {
  height: 5.5em;
}

textarea.medium {
  height: 10em;
}

textarea.large {
  height: 20em;
}

li.file a {
  color: #222;
  text-decoration: none;
}

li.file span {
  display: inline;
  float: none;
}

li.file img {
  display: block;
  float: left;
  padding: 5px 5px 7px 5px;
  margin: 0 0 0 -10px;
}

li.file .file-size,
li.file .file-type {
  font-size: 85%;
  color: #666;
  text-transform: uppercase;
}

li.file .file-name {
  display: block;
  padding: 14px 0 0 0;
  color: blue;
  text-decoration: underline;
}

li.file .file-delete {
  font-size: 85%;
  color: red !important;
  text-decoration: underline;
}

li.file a:hover .file-name {
  color: #008000 !important;
}

li.file a:hover .file-name {
  color: #008000 !important;
}

form li.likert {
  float: none !important;
  width: auto !important;
  padding: 6px 1% 5px 1%;
  margin: 0;
  clear: both !important;
}

.likert table {
  width: 100%;
  margin: 0 0 0.9em 0;
  background: #fff;
  border: 1px solid #dedede;
  border-bottom: none;
}

.likert caption {
  padding: 5px 0 0.5em 0;
  font-size: 95%;
  line-height: 135%;
  color: #222;
  text-align: left;
}

.likert input {
  padding: 0;
  margin: 2px 0;
}

.likert tbody td label {
  display: block;
  font-size: 85%;
  color: #565656;
}

.likert thead td,
.likert thead th {
  background-color: #e6e6e6;
}

.likert td {
  padding: 4px 6px;
  text-align: center;
  border-left: 1px solid #ccc;
}

.likert thead td {
  padding: 10px 6px;
  font-size: 85%;
}

.likert th,
.likert td {
  border-bottom: 1px solid #dedede;
}

.likert tbody th {
  padding: 8px 8px;
  text-align: left;
}

.likert tbody th label {
  font-size: 95%;
  font-weight: bold;
  color: #222;
}

.likert tbody tr.alt td,
.likert tbody tr.alt th {
  background-color: #f5f5f5;
}

.likert tbody tr:hover td,
.likert tbody tr:hover th {
  background-color: #ffffcf;
}

.col1 td {
  width: 30%;
}

.col2 td {
  width: 25%;
}

.col3 td {
  width: 18%;
}

.col4 td {
  width: 14.5%;
}

.col5 td {
  width: 12%;
}

.col6 td,
.col7 td {
  width: 10%;
}

.col8 td,
.col9 td,
.col10 td {
  width: 6.5%;
}

.col11 {
  width: 6%;
}

.hideNumbers tbody td label {
  display: none;
}

form li.buttons {
  position: relative;
  width: auto !important;
  padding: 10px 1% 10px 1%;
  clear: both;
}

form li.buttons input {
  margin-right: 5px;
  font-size: 100%;
}

input.btTxt {
  display: block;
  width: auto;
  width: 100%;
  padding: 0 7px;
  padding: 1em 0;
  margin-bottom: 2em;
  overflow: visible;
  font-family: "Avenir Next Condensed", sans-serif;
  font-size: 1.5em !important;
  font-weight: bold;
  color: #ffffff;
  text-align: center;
  text-transform: uppercase;
  background-color: orange;
  border: none;
  -webkit-box-shadow: none;
  -moz-box-shadow: none;
  box-shadow: none;
}

.safari input.btTxt {
  font-size: 120%;
}

.buttons .marker {
  position: absolute;
  top: 0;
  right: 0;
  width: auto;
  padding: 15px 10px 0 0;
  color: #000;
}

button.link {
  display: inline-block;
  padding: 0;
  font-size: 100%;
  color: blue;
  text-decoration: underline;
  cursor: pointer;
  background: none;
  border: none;
}

button.link:hover {
  color: #008000;
}

.leftLabel li,
.rightLabel li {
  width: 74% !important;
  padding-top: 9px;
}

.leftLabel .desc,
.rightLabel .desc {
  float: left;
  width: 31%;
  margin: 0 15px 0 0;
}

.rightLabel .desc {
  text-align: right;
}

.leftLabel li div,
.rightLabel li div {
  float: left;
  width: 65%;
}

* html .leftLabel li fieldset div,
* html .rightLabel li fieldset div {
  float: right;
}

* + html .leftLabel li fieldset div,
* + html .rightLabel li fieldset div {
  float: right;
}

.leftLabel .buttons,
.rightLabel .buttons {
  padding-left: 23%;
}

.leftLabel .buttons div,
.rightLabel .buttons div {
  float: none;
  margin: 0 0 0 20px;
}

.leftLabel p.instruct,
.rightLabel p.instruct {
  width: 28%;
  margin-left: 5px;
}

.leftLabel .altInstruct .instruct,
.rightLabel .altInstruct .instruct {
  width: 65%;
  padding-left: 15px;
  margin-left: 31% !important;
}

.noI form li,
.altInstruct form li {
  width: auto !important;
}

.noI .leftLabel .buttons,
.noI .rightLabel .buttons {
  padding-left: 31%;
}

.noI .leftLabel .buttons div,
.noI .rightLabel .buttons div {
  margin: 0 0 0 17px;
}

form li.leftHalf,
form li.rightHalf {
  width: 47% !important;
}

form li.leftThird,
form li.middleThird,
form li.rightThird {
  width: 30% !important;
}

form li.leftFourth,
form li.middleFourth,
form li.rightFourth {
  width: 23% !important;
  _width: 22% !important;
}

form li.leftFifth,
form li.middleFifth,
form li.rightFifth {
  width: 18% !important;
  _width: 17% !important;
}

form li.middleThird {
  float: left;
  margin-left: 2% !important;
  clear: none !important;
}

form li.leftFourth,
form li.middleFourth,
form li.leftFifth,
form li.middleFifth {
  float: left;
  clear: none !important;
}

form li.rightHalf,
form li.rightThird,
form li.rightFourth,
form li.rightFifth {
  float: right;
  clear: none !important;
}

li.leftHalf .small,
li.rightHalf .small,
li.leftHalf .medium,
li.rightHalf .medium,
li.leftThird .small,
li.middleThird .small,
li.rightThird .small,
li.leftThird .medium,
li.middleThird .medium,
li.rightThird .medium,
li.leftFourth .medium,
li.middleFourth .medium,
li.rightFourth .medium,
li.leftFourth .small,
li.middleFourth .small,
li.rightFourth .small,
li.leftFifth .medium,
li.middleFifth .medium,
li.rightFifth .medium,
li.leftFifth .small,
li.middleFifth .small,
li.rightFifth .small {
  width: 100% !important;
}

form li.leftHalf,
form li.leftThird,
form li.leftFourth,
form li.leftFifth {
  float: left;
  clear: left !important;
}

* html form li.middleFourth {
  margin-left: 1% !important;
}

* html form li.middleFifth {
  margin-left: 1% !important;
}

form li.focused {
  background-color: #fff7c0;
}

form .instruct {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 1000;
  width: 45%;
  padding: 8px 10px 10px 10px;
  margin: 0 0 0 8px;
  font-size: 105%;
  background: #f5f5f5;
  border: 1px solid #e6e6e6;
  opacity: 0;
  visibility: hidden;
  -webkit-transition: opacity 350ms ease-out;
  -moz-transition: opacity 350ms ease-out;
  -o-transition: opacity 350ms ease-out;
  transition: opacity 350ms ease-out;
}

form .instruct small {
  font-size: 80%;
  line-height: 120%;
  color: #444444;
}

form li.focused .instruct,
form li:hover .instruct {
  left: 100%;
  opacity: 1;
  visibility: visible;
}

.altInstruct .instruct,
li.leftHalf .instruct,
li.rightHalf .instruct,
li.leftThird .instruct,
li.middleThird .instruct,
li.rightThird .instruct,
li.leftFourth .instruct,
li.middleFourth .instruct,
li.rightFourth .instruct,
li.leftFifth .instruct,
li.middleFifth .instruct,
li.rightFifth .instruct,
.iphone .instruct {
  position: static;
  width: 100%;
  padding: 6px 0 0 0;
  margin: 0;
  clear: left;
  font-style: italic;
  background: none !important;
  border: none !important;
  opacity: 1;
  visibility: visible;
}

.altInstruct p.complex,
li.leftHalf p.complex,
li.rightHalf p.complex,
li.leftThird p.complex,
li.middleThird p.complex,
li.rightThird p.complex,
.iphone p.complex {
  padding: 0 0 9px 0;
}

.hideSeconds .seconds,
.hideAMPM .ampm,
.hideAddr2 .addr2,
.hideSecondary #previousPageButton,
.hideCents .radix,
.hideCents .cents,
.hideState .state {
  display: none;
}

form li.section {
  position: static;
  width: auto !important;
  padding: 7px 0 0 0;
  margin: 0;
  clear: both;
}

form li.section h3 {
  width: auto;
  padding: 12px 1% 0 1%;
  margin: 0 0 3px 0;
  font-weight: normal;
  line-height: 135%;
  border-top: 1px dotted #cccccc;
}

form li.first {
  padding: 0;
}

form li.first h3 {
  padding: 8px 1% 0 1%;
  border-top: none !important;
}

form li.section div {
  display: block;
  float: none;
  width: auto;
  padding: 0 1% 0 1%;
  margin: 0 0 1em 0;
  font-size: 85%;
  line-height: 160%;
}

form li.section.scrollText {
  height: 150px;
  padding: 10px;
  margin-bottom: 10px;
  overflow: auto;
  border: 1px solid #dedede;
  -webkit-box-shadow: rgba(0, 0, 0, 0.15) 0 0 3px;
  -moz-box-shadow: rgba(0, 0, 0, 0.15) 0 0 3px;
  -o-box-shadow: rgba(0, 0, 0, 0.15) 0 0 3px;
  box-shadow: rgba(0, 0, 0, 0.15) 0 0 3px;
}

form li.section.scrollText h3 {
  padding-top: 8px;
  border: none;
}

form li.captcha {
  position: static;
  width: auto !important;
  padding: 1.1em 1% 9px 1%;
  margin-top: 5px;
  clear: both;
  border-top: 1px dotted #ccc;
}

form li.captcha label.desc {
  float: none;
  width: auto !important;
  margin-bottom: 4px;
}

* + html #recaptcha_area,
* + html #recaptcha_table {
  min-width: 450px !important;
}

* html #recaptcha_area,
* html #recaptcha_table {
  width: 450px !important;
}

#recaptcha_widget_div table {
  background: #ffffff;
}

form li.captcha .noscript iframe {
  padding: 0;
  margin: 0;
  overflow: hidden;
  border: none;
}

form li.captcha .noscript label.desc {
  display: block !important;
}

form li.captcha .noscript textarea {
  margin-left: 12px;
}

iframe[src="about:blank"] {
  display: none;
}

form li.paging-context {
  position: static;
  width: auto !important;
  padding: 5px 1% 10px 1%;
  margin: 0 0 7px 0;
  clear: both;
  border-bottom: 1px dotted #ccc;
}

.paging-context table {
  width: 100%;
}

.pgStyle1 td {
  text-align: left;
  vertical-align: middle;
}

.pgStyle1 td.c {
  width: 22px;
}

form li {
  margin-bottom: 1em;
}

.pgStyle1 td.t {
  padding: 0 1%;
}

.pgStyle1 var {
  display: block;
  float: left;
  width: 20px;
  height: 20px;
  font-size: 85%;
  font-style: normal;
  line-height: 19px;
  color: #000;
  text-align: center;
  background: none;
  border: 1px solid #ccc;
  -webkit-border-radius: 10px;
  -moz-border-radius: 10px;
  border-radius: 10px;
  -webkit-box-shadow: rgba(0, 0, 0, 0.15) 0 1px 2px;
  -moz-box-shadow: rgba(0, 0, 0, 0.15) 0 1px 2px;
  -o-box-shadow: rgba(0, 0, 0, 0.15) 0 1px 2px;
  box-shadow: rgba(0, 0, 0, 0.15) 0 1px 2px;
}

.pgStyle1 .done var {
  background: #cccccc;
}

.pgStyle1 .selected var {
  font-weight: bold;
  color: #000;
  background: #fff7c0;
  border: 1px solid #e6dead;
}

.pgStyle1 b {
  font-size: 85%;
  font-weight: normal;
  color: #000000;
}

.pgStyle1 .selected b {
  font-weight: bold;
}

.circle6 td,
.circle7 td {
  text-align: center;
  vertical-align: top;
}

.nopagelabel td.t {
  display: none;
}

.nopagelabel .pgStyle1 var,
.circle6 var,
.circle7 var {
  float: none;
  width: 24px;
  height: 24px;
  margin: 0 auto 7px auto;
  font-size: 90%;
  line-height: 24px;
  -webkit-border-radius: 12px;
  -moz-border-radius: 12px;
  border-radius: 12px;
}

.nopagelabel .pgStyle1 var {
  margin-bottom: 0;
}

.circle6 b,
.circle7 b {
  padding: 0;
}

.circle2 td {
  width: 50%;
}

.circle3 td {
  width: 33%;
}

.circle4 td {
  width: 25%;
}

.circle5 td {
  width: 20%;
}

.circle6 td {
  width: 16.6%;
}

.circle7 td {
  width: 14.2%;
}

.pgStyle2 td {
  position: relative;
  height: 25px;
  padding: 2px;
  vertical-align: middle;
  border: 1px solid #ccc;
  -webkit-border-radius: 14px;
  -moz-border-radius: 14px;
  border-radius: 14px;
  -webkit-box-shadow: rgba(0, 0, 0, 0.1) 1px 1px 1px;
  -moz-box-shadow: rgba(0, 0, 0, 0.1) 1px 1px 1px;
  -o-box-shadow: rgba(0, 0, 0, 0.1) 1px 1px 1px;
  box-shadow: rgba(0, 0, 0, 0.1) 1px 1px 1px;
}

.pgStyle2 var {
  display: block;
  float: left;
  height: 26px;
  font-style: normal;
  color: #000;
  text-align: right;
  background: #fff7c0;
  -webkit-border-radius: 12px;
  -moz-border-radius: 12px;
  border-radius: 12px;
  -webkit-box-shadow: rgba(0, 0, 0, 0.15) 1px 0 0;
  -moz-box-shadow: rgba(0, 0, 0, 0.15) 1px 0 0;
  -o-box-shadow: rgba(0, 0, 0, 0.15) 1px 0 0;
  box-shadow: rgba(0, 0, 0, 0.15) 1px 0 0;
}

.pgStyle2 var b {
  display: block;
  float: right;
  padding: 3px 10px 3px 3px;
  font-size: 100%;
  line-height: 19px;
}

.pgStyle2 em {
  display: inline-block;
  padding: 4px 0;
  margin: 0 0 0 9px;
  font-size: 85%;
  font-style: normal;
  line-height: 18px;
}

.pgStyle2 var em {
  padding: 4px 5px 3px 0;
}

.page1 .pgStyle2 var {
  padding-left: 7px;
  text-align: left;
  background: none;
  -webkit-box-shadow: none;
  -moz-box-shadow: none;
  -o-box-shadow: none;
  box-shadow: none;
}

.page1 .pgStyle2 b {
  float: none;
  padding-right: 0;
}

.hideMarkers .marker,
.nopagelabel .pgStyle1 b,
.nopagelabel .pgStyle2 em {
  display: none !important;
}

#errorLi {
  width: 99%;
  padding: 1em 0 1em 0;
  margin: 15px auto 15px auto;
  text-align: center;
  background: #fff !important;
  border: 1px solid red;
  -webkit-border-radius: 20px;
  -moz-border-radius: 20px;
  border-radius: 20px;
}

#errorMsgLbl {
  padding: 0;
  margin: 0 0 5px 0;
  font-size: 125%;
  color: #df0000 !important;
}

#errorMsg {
  margin: 0 0 2px 0;
  font-size: 100%;
  color: #000 !important;
}

#errorMsg b {
  padding: 2px 8px;
  color: red !important;
  background-color: #ffdfdf !important;
  -webkit-border-radius: 10px;
  -moz-border-radius: 10px;
  border-radius: 10px;
}

form li.error {
  display: block !important;
  margin-bottom: 3px !important;
  background-color: #ffdfdf !important;
}

form li label.error,
form li input.error {
  font-weight: bold !important;
  color: #df0000 !important;
}

form li input.error {
  background: #fff !important;
  border: 2px solid #df0000 !important;
}

form li.error label,
form li.error span.symbol {
  color: #000000 !important;
}

form li.error .desc {
  color: #df0000 !important;
}

form p.error {
  display: none;
  padding: 7px 0 0 0 !important;
  margin: 0 !important;
  clear: both;
  font-size: 11px;
  font-weight: bold;
  line-height: 10px !important;
  color: #df0000 !important;
}

form li.error p.error {
  display: block;
}

form li.complex p.error {
  padding: 0 0 9px 0 !important;
}

.rtl h1,
.rtl form * {
  text-align: right;
  direction: rtl;
}

.rtl li span {
  float: right;
}

.rtl .right {
  float: left;
}

.rtl #logo a {
  background-position: right top;
}

.rtl label.choice {
  margin: -17px 23px 0 0;
}

.rtl .leftLabel .desc,
.rtl .rightLabel .desc {
  float: right;
  margin: 0 0 0 15px;
}

.rtl .leftLabel li div,
.rtl .rightLabel li div {
  float: right;
}

.rtl .leftLabel .desc {
  text-align: left;
}

.rtl li.focused .instruct,
.rtl li:hover .instruct {
  right: 100%;
  left: auto;
}

.rtl .leftLabel p.instruct,
.rtl .rightLabel p.instruct {
  margin-right: 5px;
}

.rtl .leftLabel .altInstruct .instruct,
.rtl .rightLabel .altInstruct .instruct {
  padding-right: 15px;
  margin-right: 31% !important;
}

.rtl .leftLabel .buttons,
.rtl .rightLabel .buttons {
  padding-right: 23%;
}

.rtl .leftLabel .buttons div,
.rtl .rightLabel .buttons div {
  float: none;
  margin: 0 20px 0 0;
}

.noI .rtl .leftLabel .buttons,
.noI .rtl .rightLabel .buttons {
  padding-right: 31%;
}

.noI .rtl .leftLabel .buttons div,
.noI .rtl .rightLabel .buttons div {
  margin: 0 17px 0 0;
}

.rtl .likert td label {
  text-align: center;
}

.rtl .likert caption,
.rtl .likert tbody th {
  text-align: right;
}

.rtl .likert td {
  text-align: center;
  border-right: 1px solid #cccccc;
  border-left: none;
}

.rtl .pgStyle1 var {
  text-align: center;
}

.rtl .pgStyle1 td {
  text-align: right;
}

.rtl .pgStyle2 var {
  float: right;
}

.rtl .pgStyle2 var b {
  float: left;
  padding: 3px 3px 3px 10px;
}

.rtl .pgStyle2 em {
  margin: 0 9px 0 0;
}

.rtl .pgStyle2 var em {
  padding: 4px 0 3px 5px;
}

.rtl .page1 .pgStyle2 var {
  padding-right: 7px;
}

.rtl .page1 .pgStyle2 b {
  padding-left: 0;
}

.rtl .buttons .marker {
  right: auto;
  left: 0;
  padding: 15px 0 0 10px;
}

.rtl #errorLi * {
  text-align: center;
}

.investment-blogs-wrap {
  padding: 50px 0;
  background: #f0f0f0;
}

.investment-blogs-wrap h1 {
  margin-top: 0;
  font-family: "Avenir Next", sans-serif;
  text-align: center;
  text-transform: uppercase;
}

.investment-blog {
  display: block;
  height: 400px;
  color: #17333a;
  text-decoration: none;
  background: white;
  box-sizing: border-box;
}

.investment-blog > div {
  display: block;
  height: 200px;
  background-size: cover;
}

.blog-wrap-content {
  padding: 15px;
}

.investments-container {
  padding-top: 10px;
  background: #17333a;
  border-top: 1px solid #67818f;
}

.investment-grid-controller {
  display: block;
  width: 100%;
  font-family: "Avenir Next", sans-serif;
  font-size: 0.75em;
  text-transform: uppercase;
}

.investment-grid-controller .controller-btn {
  display: inline-block;
  padding: 0 15px;
  font-size: 1.5em;
  font-weight: 600;
  color: #ffaa00;
}

.investment-grid-controller .controller-btn:hover {
  text-decoration: underline;
  cursor: pointer;
}

.statistic-wrap .statistic-box {
  display: block;
  float: auto;
  width: 100%;
  padding: 75px 0;
  font-family: "Avenir Next", sans-serif;
  text-align: center;
  background: rgba(255, 170, 0, 0.8);
}

.statistic-wrap .statistic-box:nth-child(2) {
  background: #ffaa00;
}

@media only screen and (min-width: 720px) {
  .statistic-wrap .statistic-box {
    display: inline-block;
    float: left;
    width: 33.33%;
  }
}

.statistic-wrap h2,
.statistic-wrap p {
  margin: 0;
}

.statistic-wrap h2 {
  font-family: "Avenir Next", sans-serif;
  font-size: 4em;
  color: white;
}

.statistic-wrap p {
  font-weight: 600;
  color: #4c4c4c;
}

@media only screen and (min-width: 720px) {
  .statistic-wrap {
    overflow: auto;
  }
}

.case-study.founders {
  padding-bottom: 10px;
  overflow: auto;
  text-align: center;
}

.case-study.founders h2 {
  padding-top: 20px;
  padding-bottom: 20px;
}

@media only screen and (min-width: 720px) {
  .case-study.founders {
    padding-bottom: 80px;
  }
}

.individual-founder {
  display: inline-block;
  float: left;
  width: 50%;
}

@media only screen and (min-width: 720px) {
  .individual-founder {
    display: inline-block;
    float: none;
    width: 20%;
    margin: 2%;
  }
}

.home header .header-content {
  padding-top: 100px;
}

.home header .long-site-description {
  padding-bottom: 100px;
  margin-bottom: 0;
}

.blog-landing-wrap {
  display: block;
  width: 90%;
  margin: 0 auto;
  overflow: auto;
  font-family: "Avenir Next", sans-serif;
}

.blog-landing-wrap .blog-landing-individual {
  display: block;
  margin-top: 25px;
  color: #4c4c4c;
  text-decoration: none;
}

.blog-landing-wrap img {
  width: 100%;
  height: 250px;
  margin-right: 25px;
}

.blog-landing-wrap h1 {
  margin: 10px 0 -10px;
  font-family: "Avenir Next", sans-serif;
}

.blog-landing-wrap .read-more {
  padding-bottom: 5px;
  font-weight: 600;
  color: #ffaa00;
  text-decoration: none;
  text-transform: uppercase;
  border-bottom: 2px solid #ffaa00;
}

.blog-landing-wrap .row {
  margin-bottom: 30px;
}

.blog-landing-wrap .row:first-child {
  margin-top: 30px;
}

@media only screen and (min-width: 720px) {
  .blog-landing-wrap .blog-landing-individual {
    max-width: 1400px;
    overflow: auto;
  }
  .blog-landing-wrap img {
    display: inline-block;
    float: left;
    width: 300px;
    height: 250px;
  }
  .blog-landing-wrap .blog-landing-content {
    display: inline-block;
    float: left;
  }
}

.single p {
  font-family: "Avenir Next", sans-serif;
}

.single-wrap {
  padding: 50px 0;
}

/*
 * Image replacement
 */

.ir {
  overflow: hidden;
  *text-indent: -9999px;
  background-color: transparent;
  border: 0;
}

.ir:before {
  display: block;
  width: 0;
  height: 150%;
  content: "";
}

/*
 * Hide from both screenreaders and browsers: h5bp.com/u
 */

.hidden {
  display: none !important;
  visibility: hidden;
}

/*
 * Hide only visually, but have it available for screenreaders: h5bp.com/v
 */

.visuallyhidden {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0 0 0 0);
  border: 0;
}

/*
 * Extends the .visuallyhidden class to allow the element to be focusable
 * when navigated to via the keyboard: h5bp.com/p
 */

.visuallyhidden.focusable:active,
.visuallyhidden.focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}

/*
 * Hide visually and from screenreaders, but maintain layout
 */

.invisible {
  visibility: hidden;
}

@media print,
  (-o-min-device-pixel-ratio: 5/4),
  (-webkit-min-device-pixel-ratio: 1.25),
  (min-resolution: 120dpi) {
   {
    /* Style adjustments for high resolution devices */
  }
}

/* ==========================================================================
   Print styles.
   Inlined to avoid required HTTP connection: h5bp.com/r
   ========================================================================== */

@media print {
   {
    /*
         * Don't show links for images, or javascript/internal links
         */
  }
  * {
    color: #000 !important;
    text-shadow: none !important;
    background: transparent !important;
    box-shadow: none !important;
  }
  a,
  a:visited {
    text-decoration: underline;
  }
  a[href]:after {
    content: " (" attr(href) ")";
  }
  abbr[title]:after {
    content: " (" attr(title) ")";
  }
  .ir a:after,
  a[href^="javascript:"]:after,
  a[href^="#"]:after {
    content: "";
  }
  pre,
  blockquote {
    border: 1px solid #999;
    page-break-inside: avoid;
  }
  thead {
    display: table-header-group;
    /* h5bp.com/t */
  }
  tr,
  img {
    page-break-inside: avoid;
  }
  img {
    max-width: 100% !important;
  }
  @page {
    margin: 0.5cm;
  }
  p,
  h2,
  h3 {
    orphans: 3;
    widows: 3;
  }
  h2,
  h3 {
    page-break-after: avoid;
  }
}
</style>
