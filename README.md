<!DOCTYPE html>
<html>
<head><meta charset="utf-8" />
<title>TomoPy</title><script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.0.3/jquery.min.js"></script>

<style type="text/css">
    /*!
*
* Twitter Bootstrap
*
*/
/*!
 * Bootstrap v3.3.7 (http://getbootstrap.com)
 * Copyright 2011-2016 Twitter, Inc.
 * Licensed under MIT (https://github.com/twbs/bootstrap/blob/master/LICENSE)
 */
/*! normalize.css v3.0.3 | MIT License | github.com/necolas/normalize.css */
html {
  font-family: sans-serif;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
}
body {
  margin: 0;
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
abbr[title] {
  border-bottom: 1px dotted;
}
b,
strong {
  font-weight: bold;
}
dfn {
  font-style: italic;
}
h1 {
  font-size: 2em;
  margin: 0.67em 0;
}
mark {
  background: #ff0;
  color: #000;
}
small {
  font-size: 80%;
}
sub,
sup {
  font-size: 75%;
  line-height: 0;
  position: relative;
  vertical-align: baseline;
}
sup {
  top: -0.5em;
}
sub {
  bottom: -0.25em;
}
img {
  border: 0;
}
svg:not(:root) {
  overflow: hidden;
}
figure {
  margin: 1em 40px;
}
hr {
  box-sizing: content-box;
  height: 0;
}
pre {
  overflow: auto;
}
code,
kbd,
pre,
samp {
  font-family: monospace, monospace;
  font-size: 1em;
}
button,
input,
optgroup,
select,
textarea {
  color: inherit;
  font: inherit;
  margin: 0;
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
  border: 0;
  padding: 0;
}
input {
  line-height: normal;
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
input[type="search"] {
  -webkit-appearance: textfield;
  box-sizing: content-box;
}
input[type="search"]::-webkit-search-cancel-button,
input[type="search"]::-webkit-search-decoration {
  -webkit-appearance: none;
}
fieldset {
  border: 1px solid #c0c0c0;
  margin: 0 2px;
  padding: 0.35em 0.625em 0.75em;
}
legend {
  border: 0;
  padding: 0;
}
textarea {
  overflow: auto;
}
optgroup {
  font-weight: bold;
}
table {
  border-collapse: collapse;
  border-spacing: 0;
}
td,
th {
  padding: 0;
}
/*! Source: https://github.com/h5bp/html5-boilerplate/blob/master/src/css/main.css */
@media print {
  *,
  *:before,
  *:after {
    background: transparent !important;
    color: #000 !important;
    box-shadow: none !important;
    text-shadow: none !important;
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
  a[href^="#"]:after,
  a[href^="javascript:"]:after {
    content: "";
  }
  pre,
  blockquote {
    border: 1px solid #999;
    page-break-inside: avoid;
  }
  thead {
    display: table-header-group;
  }
  tr,
  img {
    page-break-inside: avoid;
  }
  img {
    max-width: 100% !important;
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
  .table-bordered th,
  .table-bordered td {
    border: 1px solid #ddd !important;
  }
}
@font-face {
  font-family: 'Glyphicons Halflings';
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot');
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot?#iefix') format('embedded-opentype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff2') format('woff2'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff') format('woff'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.ttf') format('truetype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.svg#glyphicons_halflingsregular') format('svg');
}
.glyphicon {
  position: relative;
  top: 1px;
  display: inline-block;
  font-family: 'Glyphicons Halflings';
  font-style: normal;
  font-weight: normal;
  line-height: 1;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.glyphicon-asterisk:before {
  content: "\002a";
}
.glyphicon-plus:before {
  content: "\002b";
}
.glyphicon-euro:before,
.glyphicon-eur:before {
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
.glyphicon-bitcoin:before {
  content: "\e227";
}
.glyphicon-btc:before {
  content: "\e227";
}
.glyphicon-xbt:before {
  content: "\e227";
}
.glyphicon-yen:before {
  content: "\00a5";
}
.glyphicon-jpy:before {
  content: "\00a5";
}
.glyphicon-ruble:before {
  content: "\20bd";
}
.glyphicon-rub:before {
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
* {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
*:before,
*:after {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
html {
  font-size: 10px;
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
}
body {
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 13px;
  line-height: 1.42857143;
  color: #000;
  background-color: #fff;
}
input,
button,
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
a:hover,
a:focus {
  color: #23527c;
  text-decoration: underline;
}
a:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
figure {
  margin: 0;
}
img {
  vertical-align: middle;
}
.img-responsive,
.thumbnail > img,
.thumbnail a > img,
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  display: block;
  max-width: 100%;
  height: auto;
}
.img-rounded {
  border-radius: 3px;
}
.img-thumbnail {
  padding: 4px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: all 0.2s ease-in-out;
  -o-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  display: inline-block;
  max-width: 100%;
  height: auto;
}
.img-circle {
  border-radius: 50%;
}
hr {
  margin-top: 18px;
  margin-bottom: 18px;
  border: 0;
  border-top: 1px solid #eeeeee;
}
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  margin: -1px;
  padding: 0;
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
h1,
h2,
h3,
h4,
h5,
h6,
.h1,
.h2,
.h3,
.h4,
.h5,
.h6 {
  font-family: inherit;
  font-weight: 500;
  line-height: 1.1;
  color: inherit;
}
h1 small,
h2 small,
h3 small,
h4 small,
h5 small,
h6 small,
.h1 small,
.h2 small,
.h3 small,
.h4 small,
.h5 small,
.h6 small,
h1 .small,
h2 .small,
h3 .small,
h4 .small,
h5 .small,
h6 .small,
.h1 .small,
.h2 .small,
.h3 .small,
.h4 .small,
.h5 .small,
.h6 .small {
  font-weight: normal;
  line-height: 1;
  color: #777777;
}
h1,
.h1,
h2,
.h2,
h3,
.h3 {
  margin-top: 18px;
  margin-bottom: 9px;
}
h1 small,
.h1 small,
h2 small,
.h2 small,
h3 small,
.h3 small,
h1 .small,
.h1 .small,
h2 .small,
.h2 .small,
h3 .small,
.h3 .small {
  font-size: 65%;
}
h4,
.h4,
h5,
.h5,
h6,
.h6 {
  margin-top: 9px;
  margin-bottom: 9px;
}
h4 small,
.h4 small,
h5 small,
.h5 small,
h6 small,
.h6 small,
h4 .small,
.h4 .small,
h5 .small,
.h5 .small,
h6 .small,
.h6 .small {
  font-size: 75%;
}
h1,
.h1 {
  font-size: 33px;
}
h2,
.h2 {
  font-size: 27px;
}
h3,
.h3 {
  font-size: 23px;
}
h4,
.h4 {
  font-size: 17px;
}
h5,
.h5 {
  font-size: 13px;
}
h6,
.h6 {
  font-size: 12px;
}
p {
  margin: 0 0 9px;
}
.lead {
  margin-bottom: 18px;
  font-size: 14px;
  font-weight: 300;
  line-height: 1.4;
}
@media (min-width: 768px) {
  .lead {
    font-size: 19.5px;
  }
}
small,
.small {
  font-size: 92%;
}
mark,
.mark {
  background-color: #fcf8e3;
  padding: .2em;
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
  color: #777777;
}
.text-primary {
  color: #337ab7;
}
a.text-primary:hover,
a.text-primary:focus {
  color: #286090;
}
.text-success {
  color: #3c763d;
}
a.text-success:hover,
a.text-success:focus {
  color: #2b542c;
}
.text-info {
  color: #31708f;
}
a.text-info:hover,
a.text-info:focus {
  color: #245269;
}
.text-warning {
  color: #8a6d3b;
}
a.text-warning:hover,
a.text-warning:focus {
  color: #66512c;
}
.text-danger {
  color: #a94442;
}
a.text-danger:hover,
a.text-danger:focus {
  color: #843534;
}
.bg-primary {
  color: #fff;
  background-color: #337ab7;
}
a.bg-primary:hover,
a.bg-primary:focus {
  background-color: #286090;
}
.bg-success {
  background-color: #dff0d8;
}
a.bg-success:hover,
a.bg-success:focus {
  background-color: #c1e2b3;
}
.bg-info {
  background-color: #d9edf7;
}
a.bg-info:hover,
a.bg-info:focus {
  background-color: #afd9ee;
}
.bg-warning {
  background-color: #fcf8e3;
}
a.bg-warning:hover,
a.bg-warning:focus {
  background-color: #f7ecb5;
}
.bg-danger {
  background-color: #f2dede;
}
a.bg-danger:hover,
a.bg-danger:focus {
  background-color: #e4b9b9;
}
.page-header {
  padding-bottom: 8px;
  margin: 36px 0 18px;
  border-bottom: 1px solid #eeeeee;
}
ul,
ol {
  margin-top: 0;
  margin-bottom: 9px;
}
ul ul,
ol ul,
ul ol,
ol ol {
  margin-bottom: 0;
}
.list-unstyled {
  padding-left: 0;
  list-style: none;
}
.list-inline {
  padding-left: 0;
  list-style: none;
  margin-left: -5px;
}
.list-inline > li {
  display: inline-block;
  padding-left: 5px;
  padding-right: 5px;
}
dl {
  margin-top: 0;
  margin-bottom: 18px;
}
dt,
dd {
  line-height: 1.42857143;
}
dt {
  font-weight: bold;
}
dd {
  margin-left: 0;
}
@media (min-width: 541px) {
  .dl-horizontal dt {
    float: left;
    width: 160px;
    clear: left;
    text-align: right;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }
  .dl-horizontal dd {
    margin-left: 180px;
  }
}
abbr[title],
abbr[data-original-title] {
  cursor: help;
  border-bottom: 1px dotted #777777;
}
.initialism {
  font-size: 90%;
  text-transform: uppercase;
}
blockquote {
  padding: 9px 18px;
  margin: 0 0 18px;
  font-size: inherit;
  border-left: 5px solid #eeeeee;
}
blockquote p:last-child,
blockquote ul:last-child,
blockquote ol:last-child {
  margin-bottom: 0;
}
blockquote footer,
blockquote small,
blockquote .small {
  display: block;
  font-size: 80%;
  line-height: 1.42857143;
  color: #777777;
}
blockquote footer:before,
blockquote small:before,
blockquote .small:before {
  content: '\2014 \00A0';
}
.blockquote-reverse,
blockquote.pull-right {
  padding-right: 15px;
  padding-left: 0;
  border-right: 5px solid #eeeeee;
  border-left: 0;
  text-align: right;
}
.blockquote-reverse footer:before,
blockquote.pull-right footer:before,
.blockquote-reverse small:before,
blockquote.pull-right small:before,
.blockquote-reverse .small:before,
blockquote.pull-right .small:before {
  content: '';
}
.blockquote-reverse footer:after,
blockquote.pull-right footer:after,
.blockquote-reverse small:after,
blockquote.pull-right small:after,
.blockquote-reverse .small:after,
blockquote.pull-right .small:after {
  content: '\00A0 \2014';
}
address {
  margin-bottom: 18px;
  font-style: normal;
  line-height: 1.42857143;
}
code,
kbd,
pre,
samp {
  font-family: monospace;
}
code {
  padding: 2px 4px;
  font-size: 90%;
  color: #c7254e;
  background-color: #f9f2f4;
  border-radius: 2px;
}
kbd {
  padding: 2px 4px;
  font-size: 90%;
  color: #888;
  background-color: transparent;
  border-radius: 1px;
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.25);
}
kbd kbd {
  padding: 0;
  font-size: 100%;
  font-weight: bold;
  box-shadow: none;
}
pre {
  display: block;
  padding: 8.5px;
  margin: 0 0 9px;
  font-size: 12px;
  line-height: 1.42857143;
  word-break: break-all;
  word-wrap: break-word;
  color: #333333;
  background-color: #f5f5f5;
  border: 1px solid #ccc;
  border-radius: 2px;
}
pre code {
  padding: 0;
  font-size: inherit;
  color: inherit;
  white-space: pre-wrap;
  background-color: transparent;
  border-radius: 0;
}
.pre-scrollable {
  max-height: 340px;
  overflow-y: scroll;
}
.container {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
@media (min-width: 768px) {
  .container {
    width: 768px;
  }
}
@media (min-width: 992px) {
  .container {
    width: 940px;
  }
}
@media (min-width: 1200px) {
  .container {
    width: 1140px;
  }
}
.container-fluid {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
.row {
  margin-left: 0px;
  margin-right: 0px;
}
.col-xs-1, .col-sm-1, .col-md-1, .col-lg-1, .col-xs-2, .col-sm-2, .col-md-2, .col-lg-2, .col-xs-3, .col-sm-3, .col-md-3, .col-lg-3, .col-xs-4, .col-sm-4, .col-md-4, .col-lg-4, .col-xs-5, .col-sm-5, .col-md-5, .col-lg-5, .col-xs-6, .col-sm-6, .col-md-6, .col-lg-6, .col-xs-7, .col-sm-7, .col-md-7, .col-lg-7, .col-xs-8, .col-sm-8, .col-md-8, .col-lg-8, .col-xs-9, .col-sm-9, .col-md-9, .col-lg-9, .col-xs-10, .col-sm-10, .col-md-10, .col-lg-10, .col-xs-11, .col-sm-11, .col-md-11, .col-lg-11, .col-xs-12, .col-sm-12, .col-md-12, .col-lg-12 {
  position: relative;
  min-height: 1px;
  padding-left: 0px;
  padding-right: 0px;
}
.col-xs-1, .col-xs-2, .col-xs-3, .col-xs-4, .col-xs-5, .col-xs-6, .col-xs-7, .col-xs-8, .col-xs-9, .col-xs-10, .col-xs-11, .col-xs-12 {
  float: left;
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
  margin-left: 0%;
}
@media (min-width: 768px) {
  .col-sm-1, .col-sm-2, .col-sm-3, .col-sm-4, .col-sm-5, .col-sm-6, .col-sm-7, .col-sm-8, .col-sm-9, .col-sm-10, .col-sm-11, .col-sm-12 {
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
    margin-left: 0%;
  }
}
@media (min-width: 992px) {
  .col-md-1, .col-md-2, .col-md-3, .col-md-4, .col-md-5, .col-md-6, .col-md-7, .col-md-8, .col-md-9, .col-md-10, .col-md-11, .col-md-12 {
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
    margin-left: 0%;
  }
}
@media (min-width: 1200px) {
  .col-lg-1, .col-lg-2, .col-lg-3, .col-lg-4, .col-lg-5, .col-lg-6, .col-lg-7, .col-lg-8, .col-lg-9, .col-lg-10, .col-lg-11, .col-lg-12 {
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
    margin-left: 0%;
  }
}
table {
  background-color: transparent;
}
caption {
  padding-top: 8px;
  padding-bottom: 8px;
  color: #777777;
  text-align: left;
}
th {
  text-align: left;
}
.table {
  width: 100%;
  max-width: 100%;
  margin-bottom: 18px;
}
.table > thead > tr > th,
.table > tbody > tr > th,
.table > tfoot > tr > th,
.table > thead > tr > td,
.table > tbody > tr > td,
.table > tfoot > tr > td {
  padding: 8px;
  line-height: 1.42857143;
  vertical-align: top;
  border-top: 1px solid #ddd;
}
.table > thead > tr > th {
  vertical-align: bottom;
  border-bottom: 2px solid #ddd;
}
.table > caption + thead > tr:first-child > th,
.table > colgroup + thead > tr:first-child > th,
.table > thead:first-child > tr:first-child > th,
.table > caption + thead > tr:first-child > td,
.table > colgroup + thead > tr:first-child > td,
.table > thead:first-child > tr:first-child > td {
  border-top: 0;
}
.table > tbody + tbody {
  border-top: 2px solid #ddd;
}
.table .table {
  background-color: #fff;
}
.table-condensed > thead > tr > th,
.table-condensed > tbody > tr > th,
.table-condensed > tfoot > tr > th,
.table-condensed > thead > tr > td,
.table-condensed > tbody > tr > td,
.table-condensed > tfoot > tr > td {
  padding: 5px;
}
.table-bordered {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > tbody > tr > th,
.table-bordered > tfoot > tr > th,
.table-bordered > thead > tr > td,
.table-bordered > tbody > tr > td,
.table-bordered > tfoot > tr > td {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > thead > tr > td {
  border-bottom-width: 2px;
}
.table-striped > tbody > tr:nth-of-type(odd) {
  background-color: #f9f9f9;
}
.table-hover > tbody > tr:hover {
  background-color: #f5f5f5;
}
table col[class*="col-"] {
  position: static;
  float: none;
  display: table-column;
}
table td[class*="col-"],
table th[class*="col-"] {
  position: static;
  float: none;
  display: table-cell;
}
.table > thead > tr > td.active,
.table > tbody > tr > td.active,
.table > tfoot > tr > td.active,
.table > thead > tr > th.active,
.table > tbody > tr > th.active,
.table > tfoot > tr > th.active,
.table > thead > tr.active > td,
.table > tbody > tr.active > td,
.table > tfoot > tr.active > td,
.table > thead > tr.active > th,
.table > tbody > tr.active > th,
.table > tfoot > tr.active > th {
  background-color: #f5f5f5;
}
.table-hover > tbody > tr > td.active:hover,
.table-hover > tbody > tr > th.active:hover,
.table-hover > tbody > tr.active:hover > td,
.table-hover > tbody > tr:hover > .active,
.table-hover > tbody > tr.active:hover > th {
  background-color: #e8e8e8;
}
.table > thead > tr > td.success,
.table > tbody > tr > td.success,
.table > tfoot > tr > td.success,
.table > thead > tr > th.success,
.table > tbody > tr > th.success,
.table > tfoot > tr > th.success,
.table > thead > tr.success > td,
.table > tbody > tr.success > td,
.table > tfoot > tr.success > td,
.table > thead > tr.success > th,
.table > tbody > tr.success > th,
.table > tfoot > tr.success > th {
  background-color: #dff0d8;
}
.table-hover > tbody > tr > td.success:hover,
.table-hover > tbody > tr > th.success:hover,
.table-hover > tbody > tr.success:hover > td,
.table-hover > tbody > tr:hover > .success,
.table-hover > tbody > tr.success:hover > th {
  background-color: #d0e9c6;
}
.table > thead > tr > td.info,
.table > tbody > tr > td.info,
.table > tfoot > tr > td.info,
.table > thead > tr > th.info,
.table > tbody > tr > th.info,
.table > tfoot > tr > th.info,
.table > thead > tr.info > td,
.table > tbody > tr.info > td,
.table > tfoot > tr.info > td,
.table > thead > tr.info > th,
.table > tbody > tr.info > th,
.table > tfoot > tr.info > th {
  background-color: #d9edf7;
}
.table-hover > tbody > tr > td.info:hover,
.table-hover > tbody > tr > th.info:hover,
.table-hover > tbody > tr.info:hover > td,
.table-hover > tbody > tr:hover > .info,
.table-hover > tbody > tr.info:hover > th {
  background-color: #c4e3f3;
}
.table > thead > tr > td.warning,
.table > tbody > tr > td.warning,
.table > tfoot > tr > td.warning,
.table > thead > tr > th.warning,
.table > tbody > tr > th.warning,
.table > tfoot > tr > th.warning,
.table > thead > tr.warning > td,
.table > tbody > tr.warning > td,
.table > tfoot > tr.warning > td,
.table > thead > tr.warning > th,
.table > tbody > tr.warning > th,
.table > tfoot > tr.warning > th {
  background-color: #fcf8e3;
}
.table-hover > tbody > tr > td.warning:hover,
.table-hover > tbody > tr > th.warning:hover,
.table-hover > tbody > tr.warning:hover > td,
.table-hover > tbody > tr:hover > .warning,
.table-hover > tbody > tr.warning:hover > th {
  background-color: #faf2cc;
}
.table > thead > tr > td.danger,
.table > tbody > tr > td.danger,
.table > tfoot > tr > td.danger,
.table > thead > tr > th.danger,
.table > tbody > tr > th.danger,
.table > tfoot > tr > th.danger,
.table > thead > tr.danger > td,
.table > tbody > tr.danger > td,
.table > tfoot > tr.danger > td,
.table > thead > tr.danger > th,
.table > tbody > tr.danger > th,
.table > tfoot > tr.danger > th {
  background-color: #f2dede;
}
.table-hover > tbody > tr > td.danger:hover,
.table-hover > tbody > tr > th.danger:hover,
.table-hover > tbody > tr.danger:hover > td,
.table-hover > tbody > tr:hover > .danger,
.table-hover > tbody > tr.danger:hover > th {
  background-color: #ebcccc;
}
.table-responsive {
  overflow-x: auto;
  min-height: 0.01%;
}
@media screen and (max-width: 767px) {
  .table-responsive {
    width: 100%;
    margin-bottom: 13.5px;
    overflow-y: hidden;
    -ms-overflow-style: -ms-autohiding-scrollbar;
    border: 1px solid #ddd;
  }
  .table-responsive > .table {
    margin-bottom: 0;
  }
  .table-responsive > .table > thead > tr > th,
  .table-responsive > .table > tbody > tr > th,
  .table-responsive > .table > tfoot > tr > th,
  .table-responsive > .table > thead > tr > td,
  .table-responsive > .table > tbody > tr > td,
  .table-responsive > .table > tfoot > tr > td {
    white-space: nowrap;
  }
  .table-responsive > .table-bordered {
    border: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:first-child,
  .table-responsive > .table-bordered > tbody > tr > th:first-child,
  .table-responsive > .table-bordered > tfoot > tr > th:first-child,
  .table-responsive > .table-bordered > thead > tr > td:first-child,
  .table-responsive > .table-bordered > tbody > tr > td:first-child,
  .table-responsive > .table-bordered > tfoot > tr > td:first-child {
    border-left: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:last-child,
  .table-responsive > .table-bordered > tbody > tr > th:last-child,
  .table-responsive > .table-bordered > tfoot > tr > th:last-child,
  .table-responsive > .table-bordered > thead > tr > td:last-child,
  .table-responsive > .table-bordered > tbody > tr > td:last-child,
  .table-responsive > .table-bordered > tfoot > tr > td:last-child {
    border-right: 0;
  }
  .table-responsive > .table-bordered > tbody > tr:last-child > th,
  .table-responsive > .table-bordered > tfoot > tr:last-child > th,
  .table-responsive > .table-bordered > tbody > tr:last-child > td,
  .table-responsive > .table-bordered > tfoot > tr:last-child > td {
    border-bottom: 0;
  }
}
fieldset {
  padding: 0;
  margin: 0;
  border: 0;
  min-width: 0;
}
legend {
  display: block;
  width: 100%;
  padding: 0;
  margin-bottom: 18px;
  font-size: 19.5px;
  line-height: inherit;
  color: #333333;
  border: 0;
  border-bottom: 1px solid #e5e5e5;
}
label {
  display: inline-block;
  max-width: 100%;
  margin-bottom: 5px;
  font-weight: bold;
}
input[type="search"] {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
input[type="radio"],
input[type="checkbox"] {
  margin: 4px 0 0;
  margin-top: 1px \9;
  line-height: normal;
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
input[type="file"]:focus,
input[type="radio"]:focus,
input[type="checkbox"]:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
output {
  display: block;
  padding-top: 7px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
}
.form-control {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
}
.form-control:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
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
.form-control::-ms-expand {
  border: 0;
  background-color: transparent;
}
.form-control[disabled],
.form-control[readonly],
fieldset[disabled] .form-control {
  background-color: #eeeeee;
  opacity: 1;
}
.form-control[disabled],
fieldset[disabled] .form-control {
  cursor: not-allowed;
}
textarea.form-control {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: none;
}
@media screen and (-webkit-min-device-pixel-ratio: 0) {
  input[type="date"].form-control,
  input[type="time"].form-control,
  input[type="datetime-local"].form-control,
  input[type="month"].form-control {
    line-height: 32px;
  }
  input[type="date"].input-sm,
  input[type="time"].input-sm,
  input[type="datetime-local"].input-sm,
  input[type="month"].input-sm,
  .input-group-sm input[type="date"],
  .input-group-sm input[type="time"],
  .input-group-sm input[type="datetime-local"],
  .input-group-sm input[type="month"] {
    line-height: 30px;
  }
  input[type="date"].input-lg,
  input[type="time"].input-lg,
  input[type="datetime-local"].input-lg,
  input[type="month"].input-lg,
  .input-group-lg input[type="date"],
  .input-group-lg input[type="time"],
  .input-group-lg input[type="datetime-local"],
  .input-group-lg input[type="month"] {
    line-height: 45px;
  }
}
.form-group {
  margin-bottom: 15px;
}
.radio,
.checkbox {
  position: relative;
  display: block;
  margin-top: 10px;
  margin-bottom: 10px;
}
.radio label,
.checkbox label {
  min-height: 18px;
  padding-left: 20px;
  margin-bottom: 0;
  font-weight: normal;
  cursor: pointer;
}
.radio input[type="radio"],
.radio-inline input[type="radio"],
.checkbox input[type="checkbox"],
.checkbox-inline input[type="checkbox"] {
  position: absolute;
  margin-left: -20px;
  margin-top: 4px \9;
}
.radio + .radio,
.checkbox + .checkbox {
  margin-top: -5px;
}
.radio-inline,
.checkbox-inline {
  position: relative;
  display: inline-block;
  padding-left: 20px;
  margin-bottom: 0;
  vertical-align: middle;
  font-weight: normal;
  cursor: pointer;
}
.radio-inline + .radio-inline,
.checkbox-inline + .checkbox-inline {
  margin-top: 0;
  margin-left: 10px;
}
input[type="radio"][disabled],
input[type="checkbox"][disabled],
input[type="radio"].disabled,
input[type="checkbox"].disabled,
fieldset[disabled] input[type="radio"],
fieldset[disabled] input[type="checkbox"] {
  cursor: not-allowed;
}
.radio-inline.disabled,
.checkbox-inline.disabled,
fieldset[disabled] .radio-inline,
fieldset[disabled] .checkbox-inline {
  cursor: not-allowed;
}
.radio.disabled label,
.checkbox.disabled label,
fieldset[disabled] .radio label,
fieldset[disabled] .checkbox label {
  cursor: not-allowed;
}
.form-control-static {
  padding-top: 7px;
  padding-bottom: 7px;
  margin-bottom: 0;
  min-height: 31px;
}
.form-control-static.input-lg,
.form-control-static.input-sm {
  padding-left: 0;
  padding-right: 0;
}
.input-sm {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-sm {
  height: 30px;
  line-height: 30px;
}
textarea.input-sm,
select[multiple].input-sm {
  height: auto;
}
.form-group-sm .form-control {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.form-group-sm select.form-control {
  height: 30px;
  line-height: 30px;
}
.form-group-sm textarea.form-control,
.form-group-sm select[multiple].form-control {
  height: auto;
}
.form-group-sm .form-control-static {
  height: 30px;
  min-height: 30px;
  padding: 6px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.input-lg {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-lg {
  height: 45px;
  line-height: 45px;
}
textarea.input-lg,
select[multiple].input-lg {
  height: auto;
}
.form-group-lg .form-control {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.form-group-lg select.form-control {
  height: 45px;
  line-height: 45px;
}
.form-group-lg textarea.form-control,
.form-group-lg select[multiple].form-control {
  height: auto;
}
.form-group-lg .form-control-static {
  height: 45px;
  min-height: 35px;
  padding: 11px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.has-feedback {
  position: relative;
}
.has-feedback .form-control {
  padding-right: 40px;
}
.form-control-feedback {
  position: absolute;
  top: 0;
  right: 0;
  z-index: 2;
  display: block;
  width: 32px;
  height: 32px;
  line-height: 32px;
  text-align: center;
  pointer-events: none;
}
.input-lg + .form-control-feedback,
.input-group-lg + .form-control-feedback,
.form-group-lg .form-control + .form-control-feedback {
  width: 45px;
  height: 45px;
  line-height: 45px;
}
.input-sm + .form-control-feedback,
.input-group-sm + .form-control-feedback,
.form-group-sm .form-control + .form-control-feedback {
  width: 30px;
  height: 30px;
  line-height: 30px;
}
.has-success .help-block,
.has-success .control-label,
.has-success .radio,
.has-success .checkbox,
.has-success .radio-inline,
.has-success .checkbox-inline,
.has-success.radio label,
.has-success.checkbox label,
.has-success.radio-inline label,
.has-success.checkbox-inline label {
  color: #3c763d;
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
  border-color: #3c763d;
  background-color: #dff0d8;
}
.has-success .form-control-feedback {
  color: #3c763d;
}
.has-warning .help-block,
.has-warning .control-label,
.has-warning .radio,
.has-warning .checkbox,
.has-warning .radio-inline,
.has-warning .checkbox-inline,
.has-warning.radio label,
.has-warning.checkbox label,
.has-warning.radio-inline label,
.has-warning.checkbox-inline label {
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
  border-color: #8a6d3b;
  background-color: #fcf8e3;
}
.has-warning .form-control-feedback {
  color: #8a6d3b;
}
.has-error .help-block,
.has-error .control-label,
.has-error .radio,
.has-error .checkbox,
.has-error .radio-inline,
.has-error .checkbox-inline,
.has-error.radio label,
.has-error.checkbox label,
.has-error.radio-inline label,
.has-error.checkbox-inline label {
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
  border-color: #a94442;
  background-color: #f2dede;
}
.has-error .form-control-feedback {
  color: #a94442;
}
.has-feedback label ~ .form-control-feedback {
  top: 23px;
}
.has-feedback label.sr-only ~ .form-control-feedback {
  top: 0;
}
.help-block {
  display: block;
  margin-top: 5px;
  margin-bottom: 10px;
  color: #404040;
}
@media (min-width: 768px) {
  .form-inline .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .form-inline .form-control-static {
    display: inline-block;
  }
  .form-inline .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .form-inline .input-group .input-group-addon,
  .form-inline .input-group .input-group-btn,
  .form-inline .input-group .form-control {
    width: auto;
  }
  .form-inline .input-group > .form-control {
    width: 100%;
  }
  .form-inline .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio,
  .form-inline .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio label,
  .form-inline .checkbox label {
    padding-left: 0;
  }
  .form-inline .radio input[type="radio"],
  .form-inline .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .form-inline .has-feedback .form-control-feedback {
    top: 0;
  }
}
.form-horizontal .radio,
.form-horizontal .checkbox,
.form-horizontal .radio-inline,
.form-horizontal .checkbox-inline {
  margin-top: 0;
  margin-bottom: 0;
  padding-top: 7px;
}
.form-horizontal .radio,
.form-horizontal .checkbox {
  min-height: 25px;
}
.form-horizontal .form-group {
  margin-left: 0px;
  margin-right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .control-label {
    text-align: right;
    margin-bottom: 0;
    padding-top: 7px;
  }
}
.form-horizontal .has-feedback .form-control-feedback {
  right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .form-group-lg .control-label {
    padding-top: 11px;
    font-size: 17px;
  }
}
@media (min-width: 768px) {
  .form-horizontal .form-group-sm .control-label {
    padding-top: 6px;
    font-size: 12px;
  }
}
.btn {
  display: inline-block;
  margin-bottom: 0;
  font-weight: normal;
  text-align: center;
  vertical-align: middle;
  touch-action: manipulation;
  cursor: pointer;
  background-image: none;
  border: 1px solid transparent;
  white-space: nowrap;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  border-radius: 2px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
.btn:focus,
.btn:active:focus,
.btn.active:focus,
.btn.focus,
.btn:active.focus,
.btn.active.focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
.btn:hover,
.btn:focus,
.btn.focus {
  color: #333;
  text-decoration: none;
}
.btn:active,
.btn.active {
  outline: 0;
  background-image: none;
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn.disabled,
.btn[disabled],
fieldset[disabled] .btn {
  cursor: not-allowed;
  opacity: 0.65;
  filter: alpha(opacity=65);
  -webkit-box-shadow: none;
  box-shadow: none;
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
.btn-default:focus,
.btn-default.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.btn-default:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active:hover,
.btn-default.active:hover,
.open > .dropdown-toggle.btn-default:hover,
.btn-default:active:focus,
.btn-default.active:focus,
.open > .dropdown-toggle.btn-default:focus,
.btn-default:active.focus,
.btn-default.active.focus,
.open > .dropdown-toggle.btn-default.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  background-image: none;
}
.btn-default.disabled:hover,
.btn-default[disabled]:hover,
fieldset[disabled] .btn-default:hover,
.btn-default.disabled:focus,
.btn-default[disabled]:focus,
fieldset[disabled] .btn-default:focus,
.btn-default.disabled.focus,
.btn-default[disabled].focus,
fieldset[disabled] .btn-default.focus {
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
.btn-primary:focus,
.btn-primary.focus {
  color: #fff;
  background-color: #286090;
  border-color: #122b40;
}
.btn-primary:hover {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active:hover,
.btn-primary.active:hover,
.open > .dropdown-toggle.btn-primary:hover,
.btn-primary:active:focus,
.btn-primary.active:focus,
.open > .dropdown-toggle.btn-primary:focus,
.btn-primary:active.focus,
.btn-primary.active.focus,
.open > .dropdown-toggle.btn-primary.focus {
  color: #fff;
  background-color: #204d74;
  border-color: #122b40;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  background-image: none;
}
.btn-primary.disabled:hover,
.btn-primary[disabled]:hover,
fieldset[disabled] .btn-primary:hover,
.btn-primary.disabled:focus,
.btn-primary[disabled]:focus,
fieldset[disabled] .btn-primary:focus,
.btn-primary.disabled.focus,
.btn-primary[disabled].focus,
fieldset[disabled] .btn-primary.focus {
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
.btn-success:focus,
.btn-success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.btn-success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active:hover,
.btn-success.active:hover,
.open > .dropdown-toggle.btn-success:hover,
.btn-success:active:focus,
.btn-success.active:focus,
.open > .dropdown-toggle.btn-success:focus,
.btn-success:active.focus,
.btn-success.active.focus,
.open > .dropdown-toggle.btn-success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  background-image: none;
}
.btn-success.disabled:hover,
.btn-success[disabled]:hover,
fieldset[disabled] .btn-success:hover,
.btn-success.disabled:focus,
.btn-success[disabled]:focus,
fieldset[disabled] .btn-success:focus,
.btn-success.disabled.focus,
.btn-success[disabled].focus,
fieldset[disabled] .btn-success.focus {
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
.btn-info:focus,
.btn-info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.btn-info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active:hover,
.btn-info.active:hover,
.open > .dropdown-toggle.btn-info:hover,
.btn-info:active:focus,
.btn-info.active:focus,
.open > .dropdown-toggle.btn-info:focus,
.btn-info:active.focus,
.btn-info.active.focus,
.open > .dropdown-toggle.btn-info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  background-image: none;
}
.btn-info.disabled:hover,
.btn-info[disabled]:hover,
fieldset[disabled] .btn-info:hover,
.btn-info.disabled:focus,
.btn-info[disabled]:focus,
fieldset[disabled] .btn-info:focus,
.btn-info.disabled.focus,
.btn-info[disabled].focus,
fieldset[disabled] .btn-info.focus {
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
.btn-warning:focus,
.btn-warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.btn-warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active:hover,
.btn-warning.active:hover,
.open > .dropdown-toggle.btn-warning:hover,
.btn-warning:active:focus,
.btn-warning.active:focus,
.open > .dropdown-toggle.btn-warning:focus,
.btn-warning:active.focus,
.btn-warning.active.focus,
.open > .dropdown-toggle.btn-warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  background-image: none;
}
.btn-warning.disabled:hover,
.btn-warning[disabled]:hover,
fieldset[disabled] .btn-warning:hover,
.btn-warning.disabled:focus,
.btn-warning[disabled]:focus,
fieldset[disabled] .btn-warning:focus,
.btn-warning.disabled.focus,
.btn-warning[disabled].focus,
fieldset[disabled] .btn-warning.focus {
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
.btn-danger:focus,
.btn-danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.btn-danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active:hover,
.btn-danger.active:hover,
.open > .dropdown-toggle.btn-danger:hover,
.btn-danger:active:focus,
.btn-danger.active:focus,
.open > .dropdown-toggle.btn-danger:focus,
.btn-danger:active.focus,
.btn-danger.active.focus,
.open > .dropdown-toggle.btn-danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  background-image: none;
}
.btn-danger.disabled:hover,
.btn-danger[disabled]:hover,
fieldset[disabled] .btn-danger:hover,
.btn-danger.disabled:focus,
.btn-danger[disabled]:focus,
fieldset[disabled] .btn-danger:focus,
.btn-danger.disabled.focus,
.btn-danger[disabled].focus,
fieldset[disabled] .btn-danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger .badge {
  color: #d9534f;
  background-color: #fff;
}
.btn-link {
  color: #337ab7;
  font-weight: normal;
  border-radius: 0;
}
.btn-link,
.btn-link:active,
.btn-link.active,
.btn-link[disabled],
fieldset[disabled] .btn-link {
  background-color: transparent;
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn-link,
.btn-link:hover,
.btn-link:focus,
.btn-link:active {
  border-color: transparent;
}
.btn-link:hover,
.btn-link:focus {
  color: #23527c;
  text-decoration: underline;
  background-color: transparent;
}
.btn-link[disabled]:hover,
fieldset[disabled] .btn-link:hover,
.btn-link[disabled]:focus,
fieldset[disabled] .btn-link:focus {
  color: #777777;
  text-decoration: none;
}
.btn-lg,
.btn-group-lg > .btn {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.btn-sm,
.btn-group-sm > .btn {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-xs,
.btn-group-xs > .btn {
  padding: 1px 5px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-block {
  display: block;
  width: 100%;
}
.btn-block + .btn-block {
  margin-top: 5px;
}
input[type="submit"].btn-block,
input[type="reset"].btn-block,
input[type="button"].btn-block {
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
  position: relative;
  height: 0;
  overflow: hidden;
  -webkit-transition-property: height, visibility;
  transition-property: height, visibility;
  -webkit-transition-duration: 0.35s;
  transition-duration: 0.35s;
  -webkit-transition-timing-function: ease;
  transition-timing-function: ease;
}
.caret {
  display: inline-block;
  width: 0;
  height: 0;
  margin-left: 2px;
  vertical-align: middle;
  border-top: 4px dashed;
  border-top: 4px solid \9;
  border-right: 4px solid transparent;
  border-left: 4px solid transparent;
}
.dropup,
.dropdown {
  position: relative;
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
  float: left;
  min-width: 160px;
  padding: 5px 0;
  margin: 2px 0 0;
  list-style: none;
  font-size: 13px;
  text-align: left;
  background-color: #fff;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.15);
  border-radius: 2px;
  -webkit-box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  background-clip: padding-box;
}
.dropdown-menu.pull-right {
  right: 0;
  left: auto;
}
.dropdown-menu .divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.dropdown-menu > li > a {
  display: block;
  padding: 3px 20px;
  clear: both;
  font-weight: normal;
  line-height: 1.42857143;
  color: #333333;
  white-space: nowrap;
}
.dropdown-menu > li > a:hover,
.dropdown-menu > li > a:focus {
  text-decoration: none;
  color: #262626;
  background-color: #f5f5f5;
}
.dropdown-menu > .active > a,
.dropdown-menu > .active > a:hover,
.dropdown-menu > .active > a:focus {
  color: #fff;
  text-decoration: none;
  outline: 0;
  background-color: #337ab7;
}
.dropdown-menu > .disabled > a,
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  color: #777777;
}
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  text-decoration: none;
  background-color: transparent;
  background-image: none;
  filter: progid:DXImageTransform.Microsoft.gradient(enabled = false);
  cursor: not-allowed;
}
.open > .dropdown-menu {
  display: block;
}
.open > a {
  outline: 0;
}
.dropdown-menu-right {
  left: auto;
  right: 0;
}
.dropdown-menu-left {
  left: 0;
  right: auto;
}
.dropdown-header {
  display: block;
  padding: 3px 20px;
  font-size: 12px;
  line-height: 1.42857143;
  color: #777777;
  white-space: nowrap;
}
.dropdown-backdrop {
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  top: 0;
  z-index: 990;
}
.pull-right > .dropdown-menu {
  right: 0;
  left: auto;
}
.dropup .caret,
.navbar-fixed-bottom .dropdown .caret {
  border-top: 0;
  border-bottom: 4px dashed;
  border-bottom: 4px solid \9;
  content: "";
}
.dropup .dropdown-menu,
.navbar-fixed-bottom .dropdown .dropdown-menu {
  top: auto;
  bottom: 100%;
  margin-bottom: 2px;
}
@media (min-width: 541px) {
  .navbar-right .dropdown-menu {
    left: auto;
    right: 0;
  }
  .navbar-right .dropdown-menu-left {
    left: 0;
    right: auto;
  }
}
.btn-group,
.btn-group-vertical {
  position: relative;
  display: inline-block;
  vertical-align: middle;
}
.btn-group > .btn,
.btn-group-vertical > .btn {
  position: relative;
  float: left;
}
.btn-group > .btn:hover,
.btn-group-vertical > .btn:hover,
.btn-group > .btn:focus,
.btn-group-vertical > .btn:focus,
.btn-group > .btn:active,
.btn-group-vertical > .btn:active,
.btn-group > .btn.active,
.btn-group-vertical > .btn.active {
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
.btn-toolbar .btn,
.btn-toolbar .btn-group,
.btn-toolbar .input-group {
  float: left;
}
.btn-toolbar > .btn,
.btn-toolbar > .btn-group,
.btn-toolbar > .input-group {
  margin-left: 5px;
}
.btn-group > .btn:not(:first-child):not(:last-child):not(.dropdown-toggle) {
  border-radius: 0;
}
.btn-group > .btn:first-child {
  margin-left: 0;
}
.btn-group > .btn:first-child:not(:last-child):not(.dropdown-toggle) {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn:last-child:not(:first-child),
.btn-group > .dropdown-toggle:not(:first-child) {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group > .btn-group {
  float: left;
}
.btn-group > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group .dropdown-toggle:active,
.btn-group.open .dropdown-toggle {
  outline: 0;
}
.btn-group > .btn + .dropdown-toggle {
  padding-left: 8px;
  padding-right: 8px;
}
.btn-group > .btn-lg + .dropdown-toggle {
  padding-left: 12px;
  padding-right: 12px;
}
.btn-group.open .dropdown-toggle {
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn-group.open .dropdown-toggle.btn-link {
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn .caret {
  margin-left: 0;
}
.btn-lg .caret {
  border-width: 5px 5px 0;
  border-bottom-width: 0;
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
.btn-group-vertical > .btn:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.btn-group-vertical > .btn:first-child:not(:last-child) {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn:last-child:not(:first-child) {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
.btn-group-vertical > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.btn-group-justified {
  display: table;
  width: 100%;
  table-layout: fixed;
  border-collapse: separate;
}
.btn-group-justified > .btn,
.btn-group-justified > .btn-group {
  float: none;
  display: table-cell;
  width: 1%;
}
.btn-group-justified > .btn-group .btn {
  width: 100%;
}
.btn-group-justified > .btn-group .dropdown-menu {
  left: auto;
}
[data-toggle="buttons"] > .btn input[type="radio"],
[data-toggle="buttons"] > .btn-group > .btn input[type="radio"],
[data-toggle="buttons"] > .btn input[type="checkbox"],
[data-toggle="buttons"] > .btn-group > .btn input[type="checkbox"] {
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
  padding-left: 0;
  padding-right: 0;
}
.input-group .form-control {
  position: relative;
  z-index: 2;
  float: left;
  width: 100%;
  margin-bottom: 0;
}
.input-group .form-control:focus {
  z-index: 3;
}
.input-group-lg > .form-control,
.input-group-lg > .input-group-addon,
.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-group-lg > .form-control,
select.input-group-lg > .input-group-addon,
select.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  line-height: 45px;
}
textarea.input-group-lg > .form-control,
textarea.input-group-lg > .input-group-addon,
textarea.input-group-lg > .input-group-btn > .btn,
select[multiple].input-group-lg > .form-control,
select[multiple].input-group-lg > .input-group-addon,
select[multiple].input-group-lg > .input-group-btn > .btn {
  height: auto;
}
.input-group-sm > .form-control,
.input-group-sm > .input-group-addon,
.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-group-sm > .form-control,
select.input-group-sm > .input-group-addon,
select.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  line-height: 30px;
}
textarea.input-group-sm > .form-control,
textarea.input-group-sm > .input-group-addon,
textarea.input-group-sm > .input-group-btn > .btn,
select[multiple].input-group-sm > .form-control,
select[multiple].input-group-sm > .input-group-addon,
select[multiple].input-group-sm > .input-group-btn > .btn {
  height: auto;
}
.input-group-addon,
.input-group-btn,
.input-group .form-control {
  display: table-cell;
}
.input-group-addon:not(:first-child):not(:last-child),
.input-group-btn:not(:first-child):not(:last-child),
.input-group .form-control:not(:first-child):not(:last-child) {
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
  font-size: 13px;
  font-weight: normal;
  line-height: 1;
  color: #555555;
  text-align: center;
  background-color: #eeeeee;
  border: 1px solid #ccc;
  border-radius: 2px;
}
.input-group-addon.input-sm {
  padding: 5px 10px;
  font-size: 12px;
  border-radius: 1px;
}
.input-group-addon.input-lg {
  padding: 10px 16px;
  font-size: 17px;
  border-radius: 3px;
}
.input-group-addon input[type="radio"],
.input-group-addon input[type="checkbox"] {
  margin-top: 0;
}
.input-group .form-control:first-child,
.input-group-addon:first-child,
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group > .btn,
.input-group-btn:first-child > .dropdown-toggle,
.input-group-btn:last-child > .btn:not(:last-child):not(.dropdown-toggle),
.input-group-btn:last-child > .btn-group:not(:last-child) > .btn {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.input-group-addon:first-child {
  border-right: 0;
}
.input-group .form-control:last-child,
.input-group-addon:last-child,
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group > .btn,
.input-group-btn:last-child > .dropdown-toggle,
.input-group-btn:first-child > .btn:not(:first-child),
.input-group-btn:first-child > .btn-group:not(:first-child) > .btn {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
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
.input-group-btn > .btn:hover,
.input-group-btn > .btn:focus,
.input-group-btn > .btn:active {
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
  margin-bottom: 0;
  padding-left: 0;
  list-style: none;
}
.nav > li {
  position: relative;
  display: block;
}
.nav > li > a {
  position: relative;
  display: block;
  padding: 10px 15px;
}
.nav > li > a:hover,
.nav > li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.nav > li.disabled > a {
  color: #777777;
}
.nav > li.disabled > a:hover,
.nav > li.disabled > a:focus {
  color: #777777;
  text-decoration: none;
  background-color: transparent;
  cursor: not-allowed;
}
.nav .open > a,
.nav .open > a:hover,
.nav .open > a:focus {
  background-color: #eeeeee;
  border-color: #337ab7;
}
.nav .nav-divider {
  height: 1px;
  margin: 8px 0;
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
  border-radius: 2px 2px 0 0;
}
.nav-tabs > li > a:hover {
  border-color: #eeeeee #eeeeee #ddd;
}
.nav-tabs > li.active > a,
.nav-tabs > li.active > a:hover,
.nav-tabs > li.active > a:focus {
  color: #555555;
  background-color: #fff;
  border: 1px solid #ddd;
  border-bottom-color: transparent;
  cursor: default;
}
.nav-tabs.nav-justified {
  width: 100%;
  border-bottom: 0;
}
.nav-tabs.nav-justified > li {
  float: none;
}
.nav-tabs.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-tabs.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-tabs.nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs.nav-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs.nav-justified > .active > a,
.nav-tabs.nav-justified > .active > a:hover,
.nav-tabs.nav-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs.nav-justified > .active > a,
  .nav-tabs.nav-justified > .active > a:hover,
  .nav-tabs.nav-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.nav-pills > li {
  float: left;
}
.nav-pills > li > a {
  border-radius: 2px;
}
.nav-pills > li + li {
  margin-left: 2px;
}
.nav-pills > li.active > a,
.nav-pills > li.active > a:hover,
.nav-pills > li.active > a:focus {
  color: #fff;
  background-color: #337ab7;
}
.nav-stacked > li {
  float: none;
}
.nav-stacked > li + li {
  margin-top: 2px;
  margin-left: 0;
}
.nav-justified {
  width: 100%;
}
.nav-justified > li {
  float: none;
}
.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs-justified {
  border-bottom: 0;
}
.nav-tabs-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs-justified > .active > a,
.nav-tabs-justified > .active > a:hover,
.nav-tabs-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs-justified > .active > a,
  .nav-tabs-justified > .active > a:hover,
  .nav-tabs-justified > .active > a:focus {
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
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar {
  position: relative;
  min-height: 30px;
  margin-bottom: 18px;
  border: 1px solid transparent;
}
@media (min-width: 541px) {
  .navbar {
    border-radius: 2px;
  }
}
@media (min-width: 541px) {
  .navbar-header {
    float: left;
  }
}
.navbar-collapse {
  overflow-x: visible;
  padding-right: 0px;
  padding-left: 0px;
  border-top: 1px solid transparent;
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1);
  -webkit-overflow-scrolling: touch;
}
.navbar-collapse.in {
  overflow-y: auto;
}
@media (min-width: 541px) {
  .navbar-collapse {
    width: auto;
    border-top: 0;
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
  .navbar-fixed-top .navbar-collapse,
  .navbar-static-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    padding-left: 0;
    padding-right: 0;
  }
}
.navbar-fixed-top .navbar-collapse,
.navbar-fixed-bottom .navbar-collapse {
  max-height: 340px;
}
@media (max-device-width: 540px) and (orientation: landscape) {
  .navbar-fixed-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    max-height: 200px;
  }
}
.container > .navbar-header,
.container-fluid > .navbar-header,
.container > .navbar-collapse,
.container-fluid > .navbar-collapse {
  margin-right: 0px;
  margin-left: 0px;
}
@media (min-width: 541px) {
  .container > .navbar-header,
  .container-fluid > .navbar-header,
  .container > .navbar-collapse,
  .container-fluid > .navbar-collapse {
    margin-right: 0;
    margin-left: 0;
  }
}
.navbar-static-top {
  z-index: 1000;
  border-width: 0 0 1px;
}
@media (min-width: 541px) {
  .navbar-static-top {
    border-radius: 0;
  }
}
.navbar-fixed-top,
.navbar-fixed-bottom {
  position: fixed;
  right: 0;
  left: 0;
  z-index: 1030;
}
@media (min-width: 541px) {
  .navbar-fixed-top,
  .navbar-fixed-bottom {
    border-radius: 0;
  }
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
  padding: 6px 0px;
  font-size: 17px;
  line-height: 18px;
  height: 30px;
}
.navbar-brand:hover,
.navbar-brand:focus {
  text-decoration: none;
}
.navbar-brand > img {
  display: block;
}
@media (min-width: 541px) {
  .navbar > .container .navbar-brand,
  .navbar > .container-fluid .navbar-brand {
    margin-left: 0px;
  }
}
.navbar-toggle {
  position: relative;
  float: right;
  margin-right: 0px;
  padding: 9px 10px;
  margin-top: -2px;
  margin-bottom: -2px;
  background-color: transparent;
  background-image: none;
  border: 1px solid transparent;
  border-radius: 2px;
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
@media (min-width: 541px) {
  .navbar-toggle {
    display: none;
  }
}
.navbar-nav {
  margin: 3px 0px;
}
.navbar-nav > li > a {
  padding-top: 10px;
  padding-bottom: 10px;
  line-height: 18px;
}
@media (max-width: 540px) {
  .navbar-nav .open .dropdown-menu {
    position: static;
    float: none;
    width: auto;
    margin-top: 0;
    background-color: transparent;
    border: 0;
    box-shadow: none;
  }
  .navbar-nav .open .dropdown-menu > li > a,
  .navbar-nav .open .dropdown-menu .dropdown-header {
    padding: 5px 15px 5px 25px;
  }
  .navbar-nav .open .dropdown-menu > li > a {
    line-height: 18px;
  }
  .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-nav .open .dropdown-menu > li > a:focus {
    background-image: none;
  }
}
@media (min-width: 541px) {
  .navbar-nav {
    float: left;
    margin: 0;
  }
  .navbar-nav > li {
    float: left;
  }
  .navbar-nav > li > a {
    padding-top: 6px;
    padding-bottom: 6px;
  }
}
.navbar-form {
  margin-left: 0px;
  margin-right: 0px;
  padding: 10px 0px;
  border-top: 1px solid transparent;
  border-bottom: 1px solid transparent;
  -webkit-box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  margin-top: -1px;
  margin-bottom: -1px;
}
@media (min-width: 768px) {
  .navbar-form .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .navbar-form .form-control-static {
    display: inline-block;
  }
  .navbar-form .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .navbar-form .input-group .input-group-addon,
  .navbar-form .input-group .input-group-btn,
  .navbar-form .input-group .form-control {
    width: auto;
  }
  .navbar-form .input-group > .form-control {
    width: 100%;
  }
  .navbar-form .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio,
  .navbar-form .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio label,
  .navbar-form .checkbox label {
    padding-left: 0;
  }
  .navbar-form .radio input[type="radio"],
  .navbar-form .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .navbar-form .has-feedback .form-control-feedback {
    top: 0;
  }
}
@media (max-width: 540px) {
  .navbar-form .form-group {
    margin-bottom: 5px;
  }
  .navbar-form .form-group:last-child {
    margin-bottom: 0;
  }
}
@media (min-width: 541px) {
  .navbar-form {
    width: auto;
    border: 0;
    margin-left: 0;
    margin-right: 0;
    padding-top: 0;
    padding-bottom: 0;
    -webkit-box-shadow: none;
    box-shadow: none;
  }
}
.navbar-nav > li > .dropdown-menu {
  margin-top: 0;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar-fixed-bottom .navbar-nav > li > .dropdown-menu {
  margin-bottom: 0;
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.navbar-btn {
  margin-top: -1px;
  margin-bottom: -1px;
}
.navbar-btn.btn-sm {
  margin-top: 0px;
  margin-bottom: 0px;
}
.navbar-btn.btn-xs {
  margin-top: 4px;
  margin-bottom: 4px;
}
.navbar-text {
  margin-top: 6px;
  margin-bottom: 6px;
}
@media (min-width: 541px) {
  .navbar-text {
    float: left;
    margin-left: 0px;
    margin-right: 0px;
  }
}
@media (min-width: 541px) {
  .navbar-left {
    float: left !important;
    float: left;
  }
  .navbar-right {
    float: right !important;
    float: right;
    margin-right: 0px;
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
.navbar-default .navbar-brand:hover,
.navbar-default .navbar-brand:focus {
  color: #5e5e5e;
  background-color: transparent;
}
.navbar-default .navbar-text {
  color: #777;
}
.navbar-default .navbar-nav > li > a {
  color: #777;
}
.navbar-default .navbar-nav > li > a:hover,
.navbar-default .navbar-nav > li > a:focus {
  color: #333;
  background-color: transparent;
}
.navbar-default .navbar-nav > .active > a,
.navbar-default .navbar-nav > .active > a:hover,
.navbar-default .navbar-nav > .active > a:focus {
  color: #555;
  background-color: #e7e7e7;
}
.navbar-default .navbar-nav > .disabled > a,
.navbar-default .navbar-nav > .disabled > a:hover,
.navbar-default .navbar-nav > .disabled > a:focus {
  color: #ccc;
  background-color: transparent;
}
.navbar-default .navbar-toggle {
  border-color: #ddd;
}
.navbar-default .navbar-toggle:hover,
.navbar-default .navbar-toggle:focus {
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
.navbar-default .navbar-nav > .open > a:hover,
.navbar-default .navbar-nav > .open > a:focus {
  background-color: #e7e7e7;
  color: #555;
}
@media (max-width: 540px) {
  .navbar-default .navbar-nav .open .dropdown-menu > li > a {
    color: #777;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #333;
    background-color: transparent;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #555;
    background-color: #e7e7e7;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:focus {
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
.navbar-default .btn-link:hover,
.navbar-default .btn-link:focus {
  color: #333;
}
.navbar-default .btn-link[disabled]:hover,
fieldset[disabled] .navbar-default .btn-link:hover,
.navbar-default .btn-link[disabled]:focus,
fieldset[disabled] .navbar-default .btn-link:focus {
  color: #ccc;
}
.navbar-inverse {
  background-color: #222;
  border-color: #080808;
}
.navbar-inverse .navbar-brand {
  color: #9d9d9d;
}
.navbar-inverse .navbar-brand:hover,
.navbar-inverse .navbar-brand:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-text {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a:hover,
.navbar-inverse .navbar-nav > li > a:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-nav > .active > a,
.navbar-inverse .navbar-nav > .active > a:hover,
.navbar-inverse .navbar-nav > .active > a:focus {
  color: #fff;
  background-color: #080808;
}
.navbar-inverse .navbar-nav > .disabled > a,
.navbar-inverse .navbar-nav > .disabled > a:hover,
.navbar-inverse .navbar-nav > .disabled > a:focus {
  color: #444;
  background-color: transparent;
}
.navbar-inverse .navbar-toggle {
  border-color: #333;
}
.navbar-inverse .navbar-toggle:hover,
.navbar-inverse .navbar-toggle:focus {
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
.navbar-inverse .navbar-nav > .open > a:hover,
.navbar-inverse .navbar-nav > .open > a:focus {
  background-color: #080808;
  color: #fff;
}
@media (max-width: 540px) {
  .navbar-inverse .navbar-nav .open .dropdown-menu > .dropdown-header {
    border-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu .divider {
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a {
    color: #9d9d9d;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #fff;
    background-color: transparent;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #fff;
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:focus {
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
.navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link:focus {
  color: #fff;
}
.navbar-inverse .btn-link[disabled]:hover,
fieldset[disabled] .navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link[disabled]:focus,
fieldset[disabled] .navbar-inverse .btn-link:focus {
  color: #444;
}
.breadcrumb {
  padding: 8px 15px;
  margin-bottom: 18px;
  list-style: none;
  background-color: #f5f5f5;
  border-radius: 2px;
}
.breadcrumb > li {
  display: inline-block;
}
.breadcrumb > li + li:before {
  content: "/\00a0";
  padding: 0 5px;
  color: #5e5e5e;
}
.breadcrumb > .active {
  color: #777777;
}
.pagination {
  display: inline-block;
  padding-left: 0;
  margin: 18px 0;
  border-radius: 2px;
}
.pagination > li {
  display: inline;
}
.pagination > li > a,
.pagination > li > span {
  position: relative;
  float: left;
  padding: 6px 12px;
  line-height: 1.42857143;
  text-decoration: none;
  color: #337ab7;
  background-color: #fff;
  border: 1px solid #ddd;
  margin-left: -1px;
}
.pagination > li:first-child > a,
.pagination > li:first-child > span {
  margin-left: 0;
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.pagination > li:last-child > a,
.pagination > li:last-child > span {
  border-bottom-right-radius: 2px;
  border-top-right-radius: 2px;
}
.pagination > li > a:hover,
.pagination > li > span:hover,
.pagination > li > a:focus,
.pagination > li > span:focus {
  z-index: 2;
  color: #23527c;
  background-color: #eeeeee;
  border-color: #ddd;
}
.pagination > .active > a,
.pagination > .active > span,
.pagination > .active > a:hover,
.pagination > .active > span:hover,
.pagination > .active > a:focus,
.pagination > .active > span:focus {
  z-index: 3;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
  cursor: default;
}
.pagination > .disabled > span,
.pagination > .disabled > span:hover,
.pagination > .disabled > span:focus,
.pagination > .disabled > a,
.pagination > .disabled > a:hover,
.pagination > .disabled > a:focus {
  color: #777777;
  background-color: #fff;
  border-color: #ddd;
  cursor: not-allowed;
}
.pagination-lg > li > a,
.pagination-lg > li > span {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.pagination-lg > li:first-child > a,
.pagination-lg > li:first-child > span {
  border-bottom-left-radius: 3px;
  border-top-left-radius: 3px;
}
.pagination-lg > li:last-child > a,
.pagination-lg > li:last-child > span {
  border-bottom-right-radius: 3px;
  border-top-right-radius: 3px;
}
.pagination-sm > li > a,
.pagination-sm > li > span {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.pagination-sm > li:first-child > a,
.pagination-sm > li:first-child > span {
  border-bottom-left-radius: 1px;
  border-top-left-radius: 1px;
}
.pagination-sm > li:last-child > a,
.pagination-sm > li:last-child > span {
  border-bottom-right-radius: 1px;
  border-top-right-radius: 1px;
}
.pager {
  padding-left: 0;
  margin: 18px 0;
  list-style: none;
  text-align: center;
}
.pager li {
  display: inline;
}
.pager li > a,
.pager li > span {
  display: inline-block;
  padding: 5px 14px;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 15px;
}
.pager li > a:hover,
.pager li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
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
.pager .disabled > a:hover,
.pager .disabled > a:focus,
.pager .disabled > span {
  color: #777777;
  background-color: #fff;
  cursor: not-allowed;
}
.label {
  display: inline;
  padding: .2em .6em .3em;
  font-size: 75%;
  font-weight: bold;
  line-height: 1;
  color: #fff;
  text-align: center;
  white-space: nowrap;
  vertical-align: baseline;
  border-radius: .25em;
}
a.label:hover,
a.label:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.label:empty {
  display: none;
}
.btn .label {
  position: relative;
  top: -1px;
}
.label-default {
  background-color: #777777;
}
.label-default[href]:hover,
.label-default[href]:focus {
  background-color: #5e5e5e;
}
.label-primary {
  background-color: #337ab7;
}
.label-primary[href]:hover,
.label-primary[href]:focus {
  background-color: #286090;
}
.label-success {
  background-color: #5cb85c;
}
.label-success[href]:hover,
.label-success[href]:focus {
  background-color: #449d44;
}
.label-info {
  background-color: #5bc0de;
}
.label-info[href]:hover,
.label-info[href]:focus {
  background-color: #31b0d5;
}
.label-warning {
  background-color: #f0ad4e;
}
.label-warning[href]:hover,
.label-warning[href]:focus {
  background-color: #ec971f;
}
.label-danger {
  background-color: #d9534f;
}
.label-danger[href]:hover,
.label-danger[href]:focus {
  background-color: #c9302c;
}
.badge {
  display: inline-block;
  min-width: 10px;
  padding: 3px 7px;
  font-size: 12px;
  font-weight: bold;
  color: #fff;
  line-height: 1;
  vertical-align: middle;
  white-space: nowrap;
  text-align: center;
  background-color: #777777;
  border-radius: 10px;
}
.badge:empty {
  display: none;
}
.btn .badge {
  position: relative;
  top: -1px;
}
.btn-xs .badge,
.btn-group-xs > .btn .badge {
  top: 0;
  padding: 1px 5px;
}
a.badge:hover,
a.badge:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.list-group-item.active > .badge,
.nav-pills > .active > a > .badge {
  color: #337ab7;
  background-color: #fff;
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
  color: inherit;
  background-color: #eeeeee;
}
.jumbotron h1,
.jumbotron .h1 {
  color: inherit;
}
.jumbotron p {
  margin-bottom: 15px;
  font-size: 20px;
  font-weight: 200;
}
.jumbotron > hr {
  border-top-color: #d5d5d5;
}
.container .jumbotron,
.container-fluid .jumbotron {
  border-radius: 3px;
  padding-left: 0px;
  padding-right: 0px;
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
    padding-left: 60px;
    padding-right: 60px;
  }
  .jumbotron h1,
  .jumbotron .h1 {
    font-size: 59px;
  }
}
.thumbnail {
  display: block;
  padding: 4px;
  margin-bottom: 18px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: border 0.2s ease-in-out;
  -o-transition: border 0.2s ease-in-out;
  transition: border 0.2s ease-in-out;
}
.thumbnail > img,
.thumbnail a > img {
  margin-left: auto;
  margin-right: auto;
}
a.thumbnail:hover,
a.thumbnail:focus,
a.thumbnail.active {
  border-color: #337ab7;
}
.thumbnail .caption {
  padding: 9px;
  color: #000;
}
.alert {
  padding: 15px;
  margin-bottom: 18px;
  border: 1px solid transparent;
  border-radius: 2px;
}
.alert h4 {
  margin-top: 0;
  color: inherit;
}
.alert .alert-link {
  font-weight: bold;
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
.alert-success {
  background-color: #dff0d8;
  border-color: #d6e9c6;
  color: #3c763d;
}
.alert-success hr {
  border-top-color: #c9e2b3;
}
.alert-success .alert-link {
  color: #2b542c;
}
.alert-info {
  background-color: #d9edf7;
  border-color: #bce8f1;
  color: #31708f;
}
.alert-info hr {
  border-top-color: #a6e1ec;
}
.alert-info .alert-link {
  color: #245269;
}
.alert-warning {
  background-color: #fcf8e3;
  border-color: #faebcc;
  color: #8a6d3b;
}
.alert-warning hr {
  border-top-color: #f7e1b5;
}
.alert-warning .alert-link {
  color: #66512c;
}
.alert-danger {
  background-color: #f2dede;
  border-color: #ebccd1;
  color: #a94442;
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
@keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
.progress {
  overflow: hidden;
  height: 18px;
  margin-bottom: 18px;
  background-color: #f5f5f5;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
  box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
}
.progress-bar {
  float: left;
  width: 0%;
  height: 100%;
  font-size: 12px;
  line-height: 18px;
  color: #fff;
  text-align: center;
  background-color: #337ab7;
  -webkit-box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  -webkit-transition: width 0.6s ease;
  -o-transition: width 0.6s ease;
  transition: width 0.6s ease;
}
.progress-striped .progress-bar,
.progress-bar-striped {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-size: 40px 40px;
}
.progress.active .progress-bar,
.progress-bar.active {
  -webkit-animation: progress-bar-stripes 2s linear infinite;
  -o-animation: progress-bar-stripes 2s linear infinite;
  animation: progress-bar-stripes 2s linear infinite;
}
.progress-bar-success {
  background-color: #5cb85c;
}
.progress-striped .progress-bar-success {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-info {
  background-color: #5bc0de;
}
.progress-striped .progress-bar-info {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-warning {
  background-color: #f0ad4e;
}
.progress-striped .progress-bar-warning {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-danger {
  background-color: #d9534f;
}
.progress-striped .progress-bar-danger {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.media {
  margin-top: 15px;
}
.media:first-child {
  margin-top: 0;
}
.media,
.media-body {
  zoom: 1;
  overflow: hidden;
}
.media-body {
  width: 10000px;
}
.media-object {
  display: block;
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
.media-left,
.media-right,
.media-body {
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
  margin-bottom: 20px;
  padding-left: 0;
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
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
}
.list-group-item:last-child {
  margin-bottom: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
a.list-group-item,
button.list-group-item {
  color: #555;
}
a.list-group-item .list-group-item-heading,
button.list-group-item .list-group-item-heading {
  color: #333;
}
a.list-group-item:hover,
button.list-group-item:hover,
a.list-group-item:focus,
button.list-group-item:focus {
  text-decoration: none;
  color: #555;
  background-color: #f5f5f5;
}
button.list-group-item {
  width: 100%;
  text-align: left;
}
.list-group-item.disabled,
.list-group-item.disabled:hover,
.list-group-item.disabled:focus {
  background-color: #eeeeee;
  color: #777777;
  cursor: not-allowed;
}
.list-group-item.disabled .list-group-item-heading,
.list-group-item.disabled:hover .list-group-item-heading,
.list-group-item.disabled:focus .list-group-item-heading {
  color: inherit;
}
.list-group-item.disabled .list-group-item-text,
.list-group-item.disabled:hover .list-group-item-text,
.list-group-item.disabled:focus .list-group-item-text {
  color: #777777;
}
.list-group-item.active,
.list-group-item.active:hover,
.list-group-item.active:focus {
  z-index: 2;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.list-group-item.active .list-group-item-heading,
.list-group-item.active:hover .list-group-item-heading,
.list-group-item.active:focus .list-group-item-heading,
.list-group-item.active .list-group-item-heading > small,
.list-group-item.active:hover .list-group-item-heading > small,
.list-group-item.active:focus .list-group-item-heading > small,
.list-group-item.active .list-group-item-heading > .small,
.list-group-item.active:hover .list-group-item-heading > .small,
.list-group-item.active:focus .list-group-item-heading > .small {
  color: inherit;
}
.list-group-item.active .list-group-item-text,
.list-group-item.active:hover .list-group-item-text,
.list-group-item.active:focus .list-group-item-text {
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
a.list-group-item-success:hover,
button.list-group-item-success:hover,
a.list-group-item-success:focus,
button.list-group-item-success:focus {
  color: #3c763d;
  background-color: #d0e9c6;
}
a.list-group-item-success.active,
button.list-group-item-success.active,
a.list-group-item-success.active:hover,
button.list-group-item-success.active:hover,
a.list-group-item-success.active:focus,
button.list-group-item-success.active:focus {
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
a.list-group-item-info:hover,
button.list-group-item-info:hover,
a.list-group-item-info:focus,
button.list-group-item-info:focus {
  color: #31708f;
  background-color: #c4e3f3;
}
a.list-group-item-info.active,
button.list-group-item-info.active,
a.list-group-item-info.active:hover,
button.list-group-item-info.active:hover,
a.list-group-item-info.active:focus,
button.list-group-item-info.active:focus {
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
a.list-group-item-warning:hover,
button.list-group-item-warning:hover,
a.list-group-item-warning:focus,
button.list-group-item-warning:focus {
  color: #8a6d3b;
  background-color: #faf2cc;
}
a.list-group-item-warning.active,
button.list-group-item-warning.active,
a.list-group-item-warning.active:hover,
button.list-group-item-warning.active:hover,
a.list-group-item-warning.active:focus,
button.list-group-item-warning.active:focus {
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
a.list-group-item-danger:hover,
button.list-group-item-danger:hover,
a.list-group-item-danger:focus,
button.list-group-item-danger:focus {
  color: #a94442;
  background-color: #ebcccc;
}
a.list-group-item-danger.active,
button.list-group-item-danger.active,
a.list-group-item-danger.active:hover,
button.list-group-item-danger.active:hover,
a.list-group-item-danger.active:focus,
button.list-group-item-danger.active:focus {
  color: #fff;
  background-color: #a94442;
  border-color: #a94442;
}
.list-group-item-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.list-group-item-text {
  margin-bottom: 0;
  line-height: 1.3;
}
.panel {
  margin-bottom: 18px;
  background-color: #fff;
  border: 1px solid transparent;
  border-radius: 2px;
  -webkit-box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
}
.panel-body {
  padding: 15px;
}
.panel-heading {
  padding: 10px 15px;
  border-bottom: 1px solid transparent;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel-heading > .dropdown .dropdown-toggle {
  color: inherit;
}
.panel-title {
  margin-top: 0;
  margin-bottom: 0;
  font-size: 15px;
  color: inherit;
}
.panel-title > a,
.panel-title > small,
.panel-title > .small,
.panel-title > small > a,
.panel-title > .small > a {
  color: inherit;
}
.panel-footer {
  padding: 10px 15px;
  background-color: #f5f5f5;
  border-top: 1px solid #ddd;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .list-group,
.panel > .panel-collapse > .list-group {
  margin-bottom: 0;
}
.panel > .list-group .list-group-item,
.panel > .panel-collapse > .list-group .list-group-item {
  border-width: 1px 0;
  border-radius: 0;
}
.panel > .list-group:first-child .list-group-item:first-child,
.panel > .panel-collapse > .list-group:first-child .list-group-item:first-child {
  border-top: 0;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .list-group:last-child .list-group-item:last-child,
.panel > .panel-collapse > .list-group:last-child .list-group-item:last-child {
  border-bottom: 0;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .panel-heading + .panel-collapse > .list-group .list-group-item:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.panel-heading + .list-group .list-group-item:first-child {
  border-top-width: 0;
}
.list-group + .panel-footer {
  border-top-width: 0;
}
.panel > .table,
.panel > .table-responsive > .table,
.panel > .panel-collapse > .table {
  margin-bottom: 0;
}
.panel > .table caption,
.panel > .table-responsive > .table caption,
.panel > .panel-collapse > .table caption {
  padding-left: 15px;
  padding-right: 15px;
}
.panel > .table:first-child,
.panel > .table-responsive:first-child > .table:first-child {
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child {
  border-top-left-radius: 1px;
  border-top-right-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:first-child {
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:last-child {
  border-top-right-radius: 1px;
}
.panel > .table:last-child,
.panel > .table-responsive:last-child > .table:last-child {
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child {
  border-bottom-left-radius: 1px;
  border-bottom-right-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:first-child {
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:last-child {
  border-bottom-right-radius: 1px;
}
.panel > .panel-body + .table,
.panel > .panel-body + .table-responsive,
.panel > .table + .panel-body,
.panel > .table-responsive + .panel-body {
  border-top: 1px solid #ddd;
}
.panel > .table > tbody:first-child > tr:first-child th,
.panel > .table > tbody:first-child > tr:first-child td {
  border-top: 0;
}
.panel > .table-bordered,
.panel > .table-responsive > .table-bordered {
  border: 0;
}
.panel > .table-bordered > thead > tr > th:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:first-child,
.panel > .table-bordered > tbody > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:first-child,
.panel > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-bordered > thead > tr > td:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:first-child,
.panel > .table-bordered > tbody > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:first-child,
.panel > .table-bordered > tfoot > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:first-child {
  border-left: 0;
}
.panel > .table-bordered > thead > tr > th:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:last-child,
.panel > .table-bordered > tbody > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:last-child,
.panel > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-bordered > thead > tr > td:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:last-child,
.panel > .table-bordered > tbody > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:last-child,
.panel > .table-bordered > tfoot > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:last-child {
  border-right: 0;
}
.panel > .table-bordered > thead > tr:first-child > td,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > td,
.panel > .table-bordered > tbody > tr:first-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > td,
.panel > .table-bordered > thead > tr:first-child > th,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > th,
.panel > .table-bordered > tbody > tr:first-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > th {
  border-bottom: 0;
}
.panel > .table-bordered > tbody > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > td,
.panel > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-bordered > tbody > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > th,
.panel > .table-bordered > tfoot > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > th {
  border-bottom: 0;
}
.panel > .table-responsive {
  border: 0;
  margin-bottom: 0;
}
.panel-group {
  margin-bottom: 18px;
}
.panel-group .panel {
  margin-bottom: 0;
  border-radius: 2px;
}
.panel-group .panel + .panel {
  margin-top: 5px;
}
.panel-group .panel-heading {
  border-bottom: 0;
}
.panel-group .panel-heading + .panel-collapse > .panel-body,
.panel-group .panel-heading + .panel-collapse > .list-group {
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
  color: #333333;
  background-color: #f5f5f5;
  border-color: #ddd;
}
.panel-default > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ddd;
}
.panel-default > .panel-heading .badge {
  color: #f5f5f5;
  background-color: #333333;
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
  overflow: hidden;
}
.embed-responsive .embed-responsive-item,
.embed-responsive iframe,
.embed-responsive embed,
.embed-responsive object,
.embed-responsive video {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  height: 100%;
  width: 100%;
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
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
}
.well blockquote {
  border-color: #ddd;
  border-color: rgba(0, 0, 0, 0.15);
}
.well-lg {
  padding: 24px;
  border-radius: 3px;
}
.well-sm {
  padding: 9px;
  border-radius: 1px;
}
.close {
  float: right;
  font-size: 19.5px;
  font-weight: bold;
  line-height: 1;
  color: #000;
  text-shadow: 0 1px 0 #fff;
  opacity: 0.2;
  filter: alpha(opacity=20);
}
.close:hover,
.close:focus {
  color: #000;
  text-decoration: none;
  cursor: pointer;
  opacity: 0.5;
  filter: alpha(opacity=50);
}
button.close {
  padding: 0;
  cursor: pointer;
  background: transparent;
  border: 0;
  -webkit-appearance: none;
}
.modal-open {
  overflow: hidden;
}
.modal {
  display: none;
  overflow: hidden;
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1050;
  -webkit-overflow-scrolling: touch;
  outline: 0;
}
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, -25%);
  -ms-transform: translate(0, -25%);
  -o-transform: translate(0, -25%);
  transform: translate(0, -25%);
  -webkit-transition: -webkit-transform 0.3s ease-out;
  -moz-transition: -moz-transform 0.3s ease-out;
  -o-transition: -o-transform 0.3s ease-out;
  transition: transform 0.3s ease-out;
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
  border: 1px solid #999;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  background-clip: padding-box;
  outline: 0;
}
.modal-backdrop {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1040;
  background-color: #000;
}
.modal-backdrop.fade {
  opacity: 0;
  filter: alpha(opacity=0);
}
.modal-backdrop.in {
  opacity: 0.5;
  filter: alpha(opacity=50);
}
.modal-header {
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
  margin-left: 5px;
  margin-bottom: 0;
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
@media (min-width: 992px) {
  .modal-lg {
    width: 900px;
  }
}
.tooltip {
  position: absolute;
  z-index: 1070;
  display: block;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 12px;
  opacity: 0;
  filter: alpha(opacity=0);
}
.tooltip.in {
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.tooltip.top {
  margin-top: -3px;
  padding: 5px 0;
}
.tooltip.right {
  margin-left: 3px;
  padding: 0 5px;
}
.tooltip.bottom {
  margin-top: 3px;
  padding: 5px 0;
}
.tooltip.left {
  margin-left: -3px;
  padding: 0 5px;
}
.tooltip-inner {
  max-width: 200px;
  padding: 3px 8px;
  color: #fff;
  text-align: center;
  background-color: #000;
  border-radius: 2px;
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
  bottom: 0;
  right: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-right .tooltip-arrow {
  bottom: 0;
  left: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
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
.tooltip.bottom .tooltip-arrow {
  top: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-left .tooltip-arrow {
  top: 0;
  right: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-right .tooltip-arrow {
  top: 0;
  left: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.popover {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 1060;
  display: none;
  max-width: 276px;
  padding: 1px;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 13px;
  background-color: #fff;
  background-clip: padding-box;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
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
  margin: 0;
  padding: 8px 14px;
  font-size: 13px;
  background-color: #f7f7f7;
  border-bottom: 1px solid #ebebeb;
  border-radius: 2px 2px 0 0;
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
.popover > .arrow {
  border-width: 11px;
}
.popover > .arrow:after {
  border-width: 10px;
  content: "";
}
.popover.top > .arrow {
  left: 50%;
  margin-left: -11px;
  border-bottom-width: 0;
  border-top-color: #999999;
  border-top-color: rgba(0, 0, 0, 0.25);
  bottom: -11px;
}
.popover.top > .arrow:after {
  content: " ";
  bottom: 1px;
  margin-left: -10px;
  border-bottom-width: 0;
  border-top-color: #fff;
}
.popover.right > .arrow {
  top: 50%;
  left: -11px;
  margin-top: -11px;
  border-left-width: 0;
  border-right-color: #999999;
  border-right-color: rgba(0, 0, 0, 0.25);
}
.popover.right > .arrow:after {
  content: " ";
  left: 1px;
  bottom: -10px;
  border-left-width: 0;
  border-right-color: #fff;
}
.popover.bottom > .arrow {
  left: 50%;
  margin-left: -11px;
  border-top-width: 0;
  border-bottom-color: #999999;
  border-bottom-color: rgba(0, 0, 0, 0.25);
  top: -11px;
}
.popover.bottom > .arrow:after {
  content: " ";
  top: 1px;
  margin-left: -10px;
  border-top-width: 0;
  border-bottom-color: #fff;
}
.popover.left > .arrow {
  top: 50%;
  right: -11px;
  margin-top: -11px;
  border-right-width: 0;
  border-left-color: #999999;
  border-left-color: rgba(0, 0, 0, 0.25);
}
.popover.left > .arrow:after {
  content: " ";
  right: 1px;
  border-right-width: 0;
  border-left-color: #fff;
  bottom: -10px;
}
.carousel {
  position: relative;
}
.carousel-inner {
  position: relative;
  overflow: hidden;
  width: 100%;
}
.carousel-inner > .item {
  display: none;
  position: relative;
  -webkit-transition: 0.6s ease-in-out left;
  -o-transition: 0.6s ease-in-out left;
  transition: 0.6s ease-in-out left;
}
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  line-height: 1;
}
@media all and (transform-3d), (-webkit-transform-3d) {
  .carousel-inner > .item {
    -webkit-transition: -webkit-transform 0.6s ease-in-out;
    -moz-transition: -moz-transform 0.6s ease-in-out;
    -o-transition: -o-transform 0.6s ease-in-out;
    transition: transform 0.6s ease-in-out;
    -webkit-backface-visibility: hidden;
    -moz-backface-visibility: hidden;
    backface-visibility: hidden;
    -webkit-perspective: 1000px;
    -moz-perspective: 1000px;
    perspective: 1000px;
  }
  .carousel-inner > .item.next,
  .carousel-inner > .item.active.right {
    -webkit-transform: translate3d(100%, 0, 0);
    transform: translate3d(100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.prev,
  .carousel-inner > .item.active.left {
    -webkit-transform: translate3d(-100%, 0, 0);
    transform: translate3d(-100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.next.left,
  .carousel-inner > .item.prev.right,
  .carousel-inner > .item.active {
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
    left: 0;
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
  left: 0;
  bottom: 0;
  width: 15%;
  opacity: 0.5;
  filter: alpha(opacity=50);
  font-size: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
  background-color: rgba(0, 0, 0, 0);
}
.carousel-control.left {
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#80000000', endColorstr='#00000000', GradientType=1);
}
.carousel-control.right {
  left: auto;
  right: 0;
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#00000000', endColorstr='#80000000', GradientType=1);
}
.carousel-control:hover,
.carousel-control:focus {
  outline: 0;
  color: #fff;
  text-decoration: none;
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.carousel-control .icon-prev,
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-left,
.carousel-control .glyphicon-chevron-right {
  position: absolute;
  top: 50%;
  margin-top: -10px;
  z-index: 5;
  display: inline-block;
}
.carousel-control .icon-prev,
.carousel-control .glyphicon-chevron-left {
  left: 50%;
  margin-left: -10px;
}
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-right {
  right: 50%;
  margin-right: -10px;
}
.carousel-control .icon-prev,
.carousel-control .icon-next {
  width: 20px;
  height: 20px;
  line-height: 1;
  font-family: serif;
}
.carousel-control .icon-prev:before {
  content: '\2039';
}
.carousel-control .icon-next:before {
  content: '\203a';
}
.carousel-indicators {
  position: absolute;
  bottom: 10px;
  left: 50%;
  z-index: 15;
  width: 60%;
  margin-left: -30%;
  padding-left: 0;
  list-style: none;
  text-align: center;
}
.carousel-indicators li {
  display: inline-block;
  width: 10px;
  height: 10px;
  margin: 1px;
  text-indent: -999px;
  border: 1px solid #fff;
  border-radius: 10px;
  cursor: pointer;
  background-color: #000 \9;
  background-color: rgba(0, 0, 0, 0);
}
.carousel-indicators .active {
  margin: 0;
  width: 12px;
  height: 12px;
  background-color: #fff;
}
.carousel-caption {
  position: absolute;
  left: 15%;
  right: 15%;
  bottom: 20px;
  z-index: 10;
  padding-top: 20px;
  padding-bottom: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
}
.carousel-caption .btn {
  text-shadow: none;
}
@media screen and (min-width: 768px) {
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-prev,
  .carousel-control .icon-next {
    width: 30px;
    height: 30px;
    margin-top: -10px;
    font-size: 30px;
  }
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .icon-prev {
    margin-left: -10px;
  }
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-next {
    margin-right: -10px;
  }
  .carousel-caption {
    left: 20%;
    right: 20%;
    padding-bottom: 30px;
  }
  .carousel-indicators {
    bottom: 20px;
  }
}
.clearfix:before,
.clearfix:after,
.dl-horizontal dd:before,
.dl-horizontal dd:after,
.container:before,
.container:after,
.container-fluid:before,
.container-fluid:after,
.row:before,
.row:after,
.form-horizontal .form-group:before,
.form-horizontal .form-group:after,
.btn-toolbar:before,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:before,
.btn-group-vertical > .btn-group:after,
.nav:before,
.nav:after,
.navbar:before,
.navbar:after,
.navbar-header:before,
.navbar-header:after,
.navbar-collapse:before,
.navbar-collapse:after,
.pager:before,
.pager:after,
.panel-body:before,
.panel-body:after,
.modal-header:before,
.modal-header:after,
.modal-footer:before,
.modal-footer:after,
.item_buttons:before,
.item_buttons:after {
  content: " ";
  display: table;
}
.clearfix:after,
.dl-horizontal dd:after,
.container:after,
.container-fluid:after,
.row:after,
.form-horizontal .form-group:after,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:after,
.nav:after,
.navbar:after,
.navbar-header:after,
.navbar-collapse:after,
.pager:after,
.panel-body:after,
.modal-header:after,
.modal-footer:after,
.item_buttons:after {
  clear: both;
}
.center-block {
  display: block;
  margin-left: auto;
  margin-right: auto;
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
.invisible {
  visibility: hidden;
}
.text-hide {
  font: 0/0 a;
  color: transparent;
  text-shadow: none;
  background-color: transparent;
  border: 0;
}
.hidden {
  display: none !important;
}
.affix {
  position: fixed;
}
@-ms-viewport {
  width: device-width;
}
.visible-xs,
.visible-sm,
.visible-md,
.visible-lg {
  display: none !important;
}
.visible-xs-block,
.visible-xs-inline,
.visible-xs-inline-block,
.visible-sm-block,
.visible-sm-inline,
.visible-sm-inline-block,
.visible-md-block,
.visible-md-inline,
.visible-md-inline-block,
.visible-lg-block,
.visible-lg-inline,
.visible-lg-inline-block {
  display: none !important;
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
  th.visible-xs,
  td.visible-xs {
    display: table-cell !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-block {
    display: block !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline {
    display: inline !important;
  }
}
@media (max-width: 767px) {
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
  th.visible-sm,
  td.visible-sm {
    display: table-cell !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-block {
    display: block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline {
    display: inline !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
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
  th.visible-md,
  td.visible-md {
    display: table-cell !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-block {
    display: block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline {
    display: inline !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
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
  th.visible-lg,
  td.visible-lg {
    display: table-cell !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-block {
    display: block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline {
    display: inline !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline-block {
    display: inline-block !important;
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
@media (min-width: 1200px) {
  .hidden-lg {
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
  th.visible-print,
  td.visible-print {
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
}
@media print {
  .hidden-print {
    display: none !important;
  }
}
/*!
*
* Font Awesome
*
*/
/*!
 *  Font Awesome 4.2.0 by @davegandy - http://fontawesome.io - @fontawesome
 *  License - http://fontawesome.io/license (Font: SIL OFL 1.1, CSS: MIT License)
 */
/* FONT PATH
 * -------------------------- */
@font-face {
  font-family: 'FontAwesome';
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?v=4.2.0');
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?#iefix&v=4.2.0') format('embedded-opentype'), url('../components/font-awesome/fonts/fontawesome-webfont.woff?v=4.2.0') format('woff'), url('../components/font-awesome/fonts/fontawesome-webfont.ttf?v=4.2.0') format('truetype'), url('../components/font-awesome/fonts/fontawesome-webfont.svg?v=4.2.0#fontawesomeregular') format('svg');
  font-weight: normal;
  font-style: normal;
}
.fa {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
/* makes the font 33% larger relative to the icon container */
.fa-lg {
  font-size: 1.33333333em;
  line-height: 0.75em;
  vertical-align: -15%;
}
.fa-2x {
  font-size: 2em;
}
.fa-3x {
  font-size: 3em;
}
.fa-4x {
  font-size: 4em;
}
.fa-5x {
  font-size: 5em;
}
.fa-fw {
  width: 1.28571429em;
  text-align: center;
}
.fa-ul {
  padding-left: 0;
  margin-left: 2.14285714em;
  list-style-type: none;
}
.fa-ul > li {
  position: relative;
}
.fa-li {
  position: absolute;
  left: -2.14285714em;
  width: 2.14285714em;
  top: 0.14285714em;
  text-align: center;
}
.fa-li.fa-lg {
  left: -1.85714286em;
}
.fa-border {
  padding: .2em .25em .15em;
  border: solid 0.08em #eee;
  border-radius: .1em;
}
.pull-right {
  float: right;
}
.pull-left {
  float: left;
}
.fa.pull-left {
  margin-right: .3em;
}
.fa.pull-right {
  margin-left: .3em;
}
.fa-spin {
  -webkit-animation: fa-spin 2s infinite linear;
  animation: fa-spin 2s infinite linear;
}
@-webkit-keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
@keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
.fa-rotate-90 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=1);
  -webkit-transform: rotate(90deg);
  -ms-transform: rotate(90deg);
  transform: rotate(90deg);
}
.fa-rotate-180 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=2);
  -webkit-transform: rotate(180deg);
  -ms-transform: rotate(180deg);
  transform: rotate(180deg);
}
.fa-rotate-270 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=3);
  -webkit-transform: rotate(270deg);
  -ms-transform: rotate(270deg);
  transform: rotate(270deg);
}
.fa-flip-horizontal {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=0, mirror=1);
  -webkit-transform: scale(-1, 1);
  -ms-transform: scale(-1, 1);
  transform: scale(-1, 1);
}
.fa-flip-vertical {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=2, mirror=1);
  -webkit-transform: scale(1, -1);
  -ms-transform: scale(1, -1);
  transform: scale(1, -1);
}
:root .fa-rotate-90,
:root .fa-rotate-180,
:root .fa-rotate-270,
:root .fa-flip-horizontal,
:root .fa-flip-vertical {
  filter: none;
}
.fa-stack {
  position: relative;
  display: inline-block;
  width: 2em;
  height: 2em;
  line-height: 2em;
  vertical-align: middle;
}
.fa-stack-1x,
.fa-stack-2x {
  position: absolute;
  left: 0;
  width: 100%;
  text-align: center;
}
.fa-stack-1x {
  line-height: inherit;
}
.fa-stack-2x {
  font-size: 2em;
}
.fa-inverse {
  color: #fff;
}
/* Font Awesome uses the Unicode Private Use Area (PUA) to ensure screen
   readers do not read off random characters that represent icons */
.fa-glass:before {
  content: "\f000";
}
.fa-music:before {
  content: "\f001";
}
.fa-search:before {
  content: "\f002";
}
.fa-envelope-o:before {
  content: "\f003";
}
.fa-heart:before {
  content: "\f004";
}
.fa-star:before {
  content: "\f005";
}
.fa-star-o:before {
  content: "\f006";
}
.fa-user:before {
  content: "\f007";
}
.fa-film:before {
  content: "\f008";
}
.fa-th-large:before {
  content: "\f009";
}
.fa-th:before {
  content: "\f00a";
}
.fa-th-list:before {
  content: "\f00b";
}
.fa-check:before {
  content: "\f00c";
}
.fa-remove:before,
.fa-close:before,
.fa-times:before {
  content: "\f00d";
}
.fa-search-plus:before {
  content: "\f00e";
}
.fa-search-minus:before {
  content: "\f010";
}
.fa-power-off:before {
  content: "\f011";
}
.fa-signal:before {
  content: "\f012";
}
.fa-gear:before,
.fa-cog:before {
  content: "\f013";
}
.fa-trash-o:before {
  content: "\f014";
}
.fa-home:before {
  content: "\f015";
}
.fa-file-o:before {
  content: "\f016";
}
.fa-clock-o:before {
  content: "\f017";
}
.fa-road:before {
  content: "\f018";
}
.fa-download:before {
  content: "\f019";
}
.fa-arrow-circle-o-down:before {
  content: "\f01a";
}
.fa-arrow-circle-o-up:before {
  content: "\f01b";
}
.fa-inbox:before {
  content: "\f01c";
}
.fa-play-circle-o:before {
  content: "\f01d";
}
.fa-rotate-right:before,
.fa-repeat:before {
  content: "\f01e";
}
.fa-refresh:before {
  content: "\f021";
}
.fa-list-alt:before {
  content: "\f022";
}
.fa-lock:before {
  content: "\f023";
}
.fa-flag:before {
  content: "\f024";
}
.fa-headphones:before {
  content: "\f025";
}
.fa-volume-off:before {
  content: "\f026";
}
.fa-volume-down:before {
  content: "\f027";
}
.fa-volume-up:before {
  content: "\f028";
}
.fa-qrcode:before {
  content: "\f029";
}
.fa-barcode:before {
  content: "\f02a";
}
.fa-tag:before {
  content: "\f02b";
}
.fa-tags:before {
  content: "\f02c";
}
.fa-book:before {
  content: "\f02d";
}
.fa-bookmark:before {
  content: "\f02e";
}
.fa-print:before {
  content: "\f02f";
}
.fa-camera:before {
  content: "\f030";
}
.fa-font:before {
  content: "\f031";
}
.fa-bold:before {
  content: "\f032";
}
.fa-italic:before {
  content: "\f033";
}
.fa-text-height:before {
  content: "\f034";
}
.fa-text-width:before {
  content: "\f035";
}
.fa-align-left:before {
  content: "\f036";
}
.fa-align-center:before {
  content: "\f037";
}
.fa-align-right:before {
  content: "\f038";
}
.fa-align-justify:before {
  content: "\f039";
}
.fa-list:before {
  content: "\f03a";
}
.fa-dedent:before,
.fa-outdent:before {
  content: "\f03b";
}
.fa-indent:before {
  content: "\f03c";
}
.fa-video-camera:before {
  content: "\f03d";
}
.fa-photo:before,
.fa-image:before,
.fa-picture-o:before {
  content: "\f03e";
}
.fa-pencil:before {
  content: "\f040";
}
.fa-map-marker:before {
  content: "\f041";
}
.fa-adjust:before {
  content: "\f042";
}
.fa-tint:before {
  content: "\f043";
}
.fa-edit:before,
.fa-pencil-square-o:before {
  content: "\f044";
}
.fa-share-square-o:before {
  content: "\f045";
}
.fa-check-square-o:before {
  content: "\f046";
}
.fa-arrows:before {
  content: "\f047";
}
.fa-step-backward:before {
  content: "\f048";
}
.fa-fast-backward:before {
  content: "\f049";
}
.fa-backward:before {
  content: "\f04a";
}
.fa-play:before {
  content: "\f04b";
}
.fa-pause:before {
  content: "\f04c";
}
.fa-stop:before {
  content: "\f04d";
}
.fa-forward:before {
  content: "\f04e";
}
.fa-fast-forward:before {
  content: "\f050";
}
.fa-step-forward:before {
  content: "\f051";
}
.fa-eject:before {
  content: "\f052";
}
.fa-chevron-left:before {
  content: "\f053";
}
.fa-chevron-right:before {
  content: "\f054";
}
.fa-plus-circle:before {
  content: "\f055";
}
.fa-minus-circle:before {
  content: "\f056";
}
.fa-times-circle:before {
  content: "\f057";
}
.fa-check-circle:before {
  content: "\f058";
}
.fa-question-circle:before {
  content: "\f059";
}
.fa-info-circle:before {
  content: "\f05a";
}
.fa-crosshairs:before {
  content: "\f05b";
}
.fa-times-circle-o:before {
  content: "\f05c";
}
.fa-check-circle-o:before {
  content: "\f05d";
}
.fa-ban:before {
  content: "\f05e";
}
.fa-arrow-left:before {
  content: "\f060";
}
.fa-arrow-right:before {
  content: "\f061";
}
.fa-arrow-up:before {
  content: "\f062";
}
.fa-arrow-down:before {
  content: "\f063";
}
.fa-mail-forward:before,
.fa-share:before {
  content: "\f064";
}
.fa-expand:before {
  content: "\f065";
}
.fa-compress:before {
  content: "\f066";
}
.fa-plus:before {
  content: "\f067";
}
.fa-minus:before {
  content: "\f068";
}
.fa-asterisk:before {
  content: "\f069";
}
.fa-exclamation-circle:before {
  content: "\f06a";
}
.fa-gift:before {
  content: "\f06b";
}
.fa-leaf:before {
  content: "\f06c";
}
.fa-fire:before {
  content: "\f06d";
}
.fa-eye:before {
  content: "\f06e";
}
.fa-eye-slash:before {
  content: "\f070";
}
.fa-warning:before,
.fa-exclamation-triangle:before {
  content: "\f071";
}
.fa-plane:before {
  content: "\f072";
}
.fa-calendar:before {
  content: "\f073";
}
.fa-random:before {
  content: "\f074";
}
.fa-comment:before {
  content: "\f075";
}
.fa-magnet:before {
  content: "\f076";
}
.fa-chevron-up:before {
  content: "\f077";
}
.fa-chevron-down:before {
  content: "\f078";
}
.fa-retweet:before {
  content: "\f079";
}
.fa-shopping-cart:before {
  content: "\f07a";
}
.fa-folder:before {
  content: "\f07b";
}
.fa-folder-open:before {
  content: "\f07c";
}
.fa-arrows-v:before {
  content: "\f07d";
}
.fa-arrows-h:before {
  content: "\f07e";
}
.fa-bar-chart-o:before,
.fa-bar-chart:before {
  content: "\f080";
}
.fa-twitter-square:before {
  content: "\f081";
}
.fa-facebook-square:before {
  content: "\f082";
}
.fa-camera-retro:before {
  content: "\f083";
}
.fa-key:before {
  content: "\f084";
}
.fa-gears:before,
.fa-cogs:before {
  content: "\f085";
}
.fa-comments:before {
  content: "\f086";
}
.fa-thumbs-o-up:before {
  content: "\f087";
}
.fa-thumbs-o-down:before {
  content: "\f088";
}
.fa-star-half:before {
  content: "\f089";
}
.fa-heart-o:before {
  content: "\f08a";
}
.fa-sign-out:before {
  content: "\f08b";
}
.fa-linkedin-square:before {
  content: "\f08c";
}
.fa-thumb-tack:before {
  content: "\f08d";
}
.fa-external-link:before {
  content: "\f08e";
}
.fa-sign-in:before {
  content: "\f090";
}
.fa-trophy:before {
  content: "\f091";
}
.fa-github-square:before {
  content: "\f092";
}
.fa-upload:before {
  content: "\f093";
}
.fa-lemon-o:before {
  content: "\f094";
}
.fa-phone:before {
  content: "\f095";
}
.fa-square-o:before {
  content: "\f096";
}
.fa-bookmark-o:before {
  content: "\f097";
}
.fa-phone-square:before {
  content: "\f098";
}
.fa-twitter:before {
  content: "\f099";
}
.fa-facebook:before {
  content: "\f09a";
}
.fa-github:before {
  content: "\f09b";
}
.fa-unlock:before {
  content: "\f09c";
}
.fa-credit-card:before {
  content: "\f09d";
}
.fa-rss:before {
  content: "\f09e";
}
.fa-hdd-o:before {
  content: "\f0a0";
}
.fa-bullhorn:before {
  content: "\f0a1";
}
.fa-bell:before {
  content: "\f0f3";
}
.fa-certificate:before {
  content: "\f0a3";
}
.fa-hand-o-right:before {
  content: "\f0a4";
}
.fa-hand-o-left:before {
  content: "\f0a5";
}
.fa-hand-o-up:before {
  content: "\f0a6";
}
.fa-hand-o-down:before {
  content: "\f0a7";
}
.fa-arrow-circle-left:before {
  content: "\f0a8";
}
.fa-arrow-circle-right:before {
  content: "\f0a9";
}
.fa-arrow-circle-up:before {
  content: "\f0aa";
}
.fa-arrow-circle-down:before {
  content: "\f0ab";
}
.fa-globe:before {
  content: "\f0ac";
}
.fa-wrench:before {
  content: "\f0ad";
}
.fa-tasks:before {
  content: "\f0ae";
}
.fa-filter:before {
  content: "\f0b0";
}
.fa-briefcase:before {
  content: "\f0b1";
}
.fa-arrows-alt:before {
  content: "\f0b2";
}
.fa-group:before,
.fa-users:before {
  content: "\f0c0";
}
.fa-chain:before,
.fa-link:before {
  content: "\f0c1";
}
.fa-cloud:before {
  content: "\f0c2";
}
.fa-flask:before {
  content: "\f0c3";
}
.fa-cut:before,
.fa-scissors:before {
  content: "\f0c4";
}
.fa-copy:before,
.fa-files-o:before {
  content: "\f0c5";
}
.fa-paperclip:before {
  content: "\f0c6";
}
.fa-save:before,
.fa-floppy-o:before {
  content: "\f0c7";
}
.fa-square:before {
  content: "\f0c8";
}
.fa-navicon:before,
.fa-reorder:before,
.fa-bars:before {
  content: "\f0c9";
}
.fa-list-ul:before {
  content: "\f0ca";
}
.fa-list-ol:before {
  content: "\f0cb";
}
.fa-strikethrough:before {
  content: "\f0cc";
}
.fa-underline:before {
  content: "\f0cd";
}
.fa-table:before {
  content: "\f0ce";
}
.fa-magic:before {
  content: "\f0d0";
}
.fa-truck:before {
  content: "\f0d1";
}
.fa-pinterest:before {
  content: "\f0d2";
}
.fa-pinterest-square:before {
  content: "\f0d3";
}
.fa-google-plus-square:before {
  content: "\f0d4";
}
.fa-google-plus:before {
  content: "\f0d5";
}
.fa-money:before {
  content: "\f0d6";
}
.fa-caret-down:before {
  content: "\f0d7";
}
.fa-caret-up:before {
  content: "\f0d8";
}
.fa-caret-left:before {
  content: "\f0d9";
}
.fa-caret-right:before {
  content: "\f0da";
}
.fa-columns:before {
  content: "\f0db";
}
.fa-unsorted:before,
.fa-sort:before {
  content: "\f0dc";
}
.fa-sort-down:before,
.fa-sort-desc:before {
  content: "\f0dd";
}
.fa-sort-up:before,
.fa-sort-asc:before {
  content: "\f0de";
}
.fa-envelope:before {
  content: "\f0e0";
}
.fa-linkedin:before {
  content: "\f0e1";
}
.fa-rotate-left:before,
.fa-undo:before {
  content: "\f0e2";
}
.fa-legal:before,
.fa-gavel:before {
  content: "\f0e3";
}
.fa-dashboard:before,
.fa-tachometer:before {
  content: "\f0e4";
}
.fa-comment-o:before {
  content: "\f0e5";
}
.fa-comments-o:before {
  content: "\f0e6";
}
.fa-flash:before,
.fa-bolt:before {
  content: "\f0e7";
}
.fa-sitemap:before {
  content: "\f0e8";
}
.fa-umbrella:before {
  content: "\f0e9";
}
.fa-paste:before,
.fa-clipboard:before {
  content: "\f0ea";
}
.fa-lightbulb-o:before {
  content: "\f0eb";
}
.fa-exchange:before {
  content: "\f0ec";
}
.fa-cloud-download:before {
  content: "\f0ed";
}
.fa-cloud-upload:before {
  content: "\f0ee";
}
.fa-user-md:before {
  content: "\f0f0";
}
.fa-stethoscope:before {
  content: "\f0f1";
}
.fa-suitcase:before {
  content: "\f0f2";
}
.fa-bell-o:before {
  content: "\f0a2";
}
.fa-coffee:before {
  content: "\f0f4";
}
.fa-cutlery:before {
  content: "\f0f5";
}
.fa-file-text-o:before {
  content: "\f0f6";
}
.fa-building-o:before {
  content: "\f0f7";
}
.fa-hospital-o:before {
  content: "\f0f8";
}
.fa-ambulance:before {
  content: "\f0f9";
}
.fa-medkit:before {
  content: "\f0fa";
}
.fa-fighter-jet:before {
  content: "\f0fb";
}
.fa-beer:before {
  content: "\f0fc";
}
.fa-h-square:before {
  content: "\f0fd";
}
.fa-plus-square:before {
  content: "\f0fe";
}
.fa-angle-double-left:before {
  content: "\f100";
}
.fa-angle-double-right:before {
  content: "\f101";
}
.fa-angle-double-up:before {
  content: "\f102";
}
.fa-angle-double-down:before {
  content: "\f103";
}
.fa-angle-left:before {
  content: "\f104";
}
.fa-angle-right:before {
  content: "\f105";
}
.fa-angle-up:before {
  content: "\f106";
}
.fa-angle-down:before {
  content: "\f107";
}
.fa-desktop:before {
  content: "\f108";
}
.fa-laptop:before {
  content: "\f109";
}
.fa-tablet:before {
  content: "\f10a";
}
.fa-mobile-phone:before,
.fa-mobile:before {
  content: "\f10b";
}
.fa-circle-o:before {
  content: "\f10c";
}
.fa-quote-left:before {
  content: "\f10d";
}
.fa-quote-right:before {
  content: "\f10e";
}
.fa-spinner:before {
  content: "\f110";
}
.fa-circle:before {
  content: "\f111";
}
.fa-mail-reply:before,
.fa-reply:before {
  content: "\f112";
}
.fa-github-alt:before {
  content: "\f113";
}
.fa-folder-o:before {
  content: "\f114";
}
.fa-folder-open-o:before {
  content: "\f115";
}
.fa-smile-o:before {
  content: "\f118";
}
.fa-frown-o:before {
  content: "\f119";
}
.fa-meh-o:before {
  content: "\f11a";
}
.fa-gamepad:before {
  content: "\f11b";
}
.fa-keyboard-o:before {
  content: "\f11c";
}
.fa-flag-o:before {
  content: "\f11d";
}
.fa-flag-checkered:before {
  content: "\f11e";
}
.fa-terminal:before {
  content: "\f120";
}
.fa-code:before {
  content: "\f121";
}
.fa-mail-reply-all:before,
.fa-reply-all:before {
  content: "\f122";
}
.fa-star-half-empty:before,
.fa-star-half-full:before,
.fa-star-half-o:before {
  content: "\f123";
}
.fa-location-arrow:before {
  content: "\f124";
}
.fa-crop:before {
  content: "\f125";
}
.fa-code-fork:before {
  content: "\f126";
}
.fa-unlink:before,
.fa-chain-broken:before {
  content: "\f127";
}
.fa-question:before {
  content: "\f128";
}
.fa-info:before {
  content: "\f129";
}
.fa-exclamation:before {
  content: "\f12a";
}
.fa-superscript:before {
  content: "\f12b";
}
.fa-subscript:before {
  content: "\f12c";
}
.fa-eraser:before {
  content: "\f12d";
}
.fa-puzzle-piece:before {
  content: "\f12e";
}
.fa-microphone:before {
  content: "\f130";
}
.fa-microphone-slash:before {
  content: "\f131";
}
.fa-shield:before {
  content: "\f132";
}
.fa-calendar-o:before {
  content: "\f133";
}
.fa-fire-extinguisher:before {
  content: "\f134";
}
.fa-rocket:before {
  content: "\f135";
}
.fa-maxcdn:before {
  content: "\f136";
}
.fa-chevron-circle-left:before {
  content: "\f137";
}
.fa-chevron-circle-right:before {
  content: "\f138";
}
.fa-chevron-circle-up:before {
  content: "\f139";
}
.fa-chevron-circle-down:before {
  content: "\f13a";
}
.fa-html5:before {
  content: "\f13b";
}
.fa-css3:before {
  content: "\f13c";
}
.fa-anchor:before {
  content: "\f13d";
}
.fa-unlock-alt:before {
  content: "\f13e";
}
.fa-bullseye:before {
  content: "\f140";
}
.fa-ellipsis-h:before {
  content: "\f141";
}
.fa-ellipsis-v:before {
  content: "\f142";
}
.fa-rss-square:before {
  content: "\f143";
}
.fa-play-circle:before {
  content: "\f144";
}
.fa-ticket:before {
  content: "\f145";
}
.fa-minus-square:before {
  content: "\f146";
}
.fa-minus-square-o:before {
  content: "\f147";
}
.fa-level-up:before {
  content: "\f148";
}
.fa-level-down:before {
  content: "\f149";
}
.fa-check-square:before {
  content: "\f14a";
}
.fa-pencil-square:before {
  content: "\f14b";
}
.fa-external-link-square:before {
  content: "\f14c";
}
.fa-share-square:before {
  content: "\f14d";
}
.fa-compass:before {
  content: "\f14e";
}
.fa-toggle-down:before,
.fa-caret-square-o-down:before {
  content: "\f150";
}
.fa-toggle-up:before,
.fa-caret-square-o-up:before {
  content: "\f151";
}
.fa-toggle-right:before,
.fa-caret-square-o-right:before {
  content: "\f152";
}
.fa-euro:before,
.fa-eur:before {
  content: "\f153";
}
.fa-gbp:before {
  content: "\f154";
}
.fa-dollar:before,
.fa-usd:before {
  content: "\f155";
}
.fa-rupee:before,
.fa-inr:before {
  content: "\f156";
}
.fa-cny:before,
.fa-rmb:before,
.fa-yen:before,
.fa-jpy:before {
  content: "\f157";
}
.fa-ruble:before,
.fa-rouble:before,
.fa-rub:before {
  content: "\f158";
}
.fa-won:before,
.fa-krw:before {
  content: "\f159";
}
.fa-bitcoin:before,
.fa-btc:before {
  content: "\f15a";
}
.fa-file:before {
  content: "\f15b";
}
.fa-file-text:before {
  content: "\f15c";
}
.fa-sort-alpha-asc:before {
  content: "\f15d";
}
.fa-sort-alpha-desc:before {
  content: "\f15e";
}
.fa-sort-amount-asc:before {
  content: "\f160";
}
.fa-sort-amount-desc:before {
  content: "\f161";
}
.fa-sort-numeric-asc:before {
  content: "\f162";
}
.fa-sort-numeric-desc:before {
  content: "\f163";
}
.fa-thumbs-up:before {
  content: "\f164";
}
.fa-thumbs-down:before {
  content: "\f165";
}
.fa-youtube-square:before {
  content: "\f166";
}
.fa-youtube:before {
  content: "\f167";
}
.fa-xing:before {
  content: "\f168";
}
.fa-xing-square:before {
  content: "\f169";
}
.fa-youtube-play:before {
  content: "\f16a";
}
.fa-dropbox:before {
  content: "\f16b";
}
.fa-stack-overflow:before {
  content: "\f16c";
}
.fa-instagram:before {
  content: "\f16d";
}
.fa-flickr:before {
  content: "\f16e";
}
.fa-adn:before {
  content: "\f170";
}
.fa-bitbucket:before {
  content: "\f171";
}
.fa-bitbucket-square:before {
  content: "\f172";
}
.fa-tumblr:before {
  content: "\f173";
}
.fa-tumblr-square:before {
  content: "\f174";
}
.fa-long-arrow-down:before {
  content: "\f175";
}
.fa-long-arrow-up:before {
  content: "\f176";
}
.fa-long-arrow-left:before {
  content: "\f177";
}
.fa-long-arrow-right:before {
  content: "\f178";
}
.fa-apple:before {
  content: "\f179";
}
.fa-windows:before {
  content: "\f17a";
}
.fa-android:before {
  content: "\f17b";
}
.fa-linux:before {
  content: "\f17c";
}
.fa-dribbble:before {
  content: "\f17d";
}
.fa-skype:before {
  content: "\f17e";
}
.fa-foursquare:before {
  content: "\f180";
}
.fa-trello:before {
  content: "\f181";
}
.fa-female:before {
  content: "\f182";
}
.fa-male:before {
  content: "\f183";
}
.fa-gittip:before {
  content: "\f184";
}
.fa-sun-o:before {
  content: "\f185";
}
.fa-moon-o:before {
  content: "\f186";
}
.fa-archive:before {
  content: "\f187";
}
.fa-bug:before {
  content: "\f188";
}
.fa-vk:before {
  content: "\f189";
}
.fa-weibo:before {
  content: "\f18a";
}
.fa-renren:before {
  content: "\f18b";
}
.fa-pagelines:before {
  content: "\f18c";
}
.fa-stack-exchange:before {
  content: "\f18d";
}
.fa-arrow-circle-o-right:before {
  content: "\f18e";
}
.fa-arrow-circle-o-left:before {
  content: "\f190";
}
.fa-toggle-left:before,
.fa-caret-square-o-left:before {
  content: "\f191";
}
.fa-dot-circle-o:before {
  content: "\f192";
}
.fa-wheelchair:before {
  content: "\f193";
}
.fa-vimeo-square:before {
  content: "\f194";
}
.fa-turkish-lira:before,
.fa-try:before {
  content: "\f195";
}
.fa-plus-square-o:before {
  content: "\f196";
}
.fa-space-shuttle:before {
  content: "\f197";
}
.fa-slack:before {
  content: "\f198";
}
.fa-envelope-square:before {
  content: "\f199";
}
.fa-wordpress:before {
  content: "\f19a";
}
.fa-openid:before {
  content: "\f19b";
}
.fa-institution:before,
.fa-bank:before,
.fa-university:before {
  content: "\f19c";
}
.fa-mortar-board:before,
.fa-graduation-cap:before {
  content: "\f19d";
}
.fa-yahoo:before {
  content: "\f19e";
}
.fa-google:before {
  content: "\f1a0";
}
.fa-reddit:before {
  content: "\f1a1";
}
.fa-reddit-square:before {
  content: "\f1a2";
}
.fa-stumbleupon-circle:before {
  content: "\f1a3";
}
.fa-stumbleupon:before {
  content: "\f1a4";
}
.fa-delicious:before {
  content: "\f1a5";
}
.fa-digg:before {
  content: "\f1a6";
}
.fa-pied-piper:before {
  content: "\f1a7";
}
.fa-pied-piper-alt:before {
  content: "\f1a8";
}
.fa-drupal:before {
  content: "\f1a9";
}
.fa-joomla:before {
  content: "\f1aa";
}
.fa-language:before {
  content: "\f1ab";
}
.fa-fax:before {
  content: "\f1ac";
}
.fa-building:before {
  content: "\f1ad";
}
.fa-child:before {
  content: "\f1ae";
}
.fa-paw:before {
  content: "\f1b0";
}
.fa-spoon:before {
  content: "\f1b1";
}
.fa-cube:before {
  content: "\f1b2";
}
.fa-cubes:before {
  content: "\f1b3";
}
.fa-behance:before {
  content: "\f1b4";
}
.fa-behance-square:before {
  content: "\f1b5";
}
.fa-steam:before {
  content: "\f1b6";
}
.fa-steam-square:before {
  content: "\f1b7";
}
.fa-recycle:before {
  content: "\f1b8";
}
.fa-automobile:before,
.fa-car:before {
  content: "\f1b9";
}
.fa-cab:before,
.fa-taxi:before {
  content: "\f1ba";
}
.fa-tree:before {
  content: "\f1bb";
}
.fa-spotify:before {
  content: "\f1bc";
}
.fa-deviantart:before {
  content: "\f1bd";
}
.fa-soundcloud:before {
  content: "\f1be";
}
.fa-database:before {
  content: "\f1c0";
}
.fa-file-pdf-o:before {
  content: "\f1c1";
}
.fa-file-word-o:before {
  content: "\f1c2";
}
.fa-file-excel-o:before {
  content: "\f1c3";
}
.fa-file-powerpoint-o:before {
  content: "\f1c4";
}
.fa-file-photo-o:before,
.fa-file-picture-o:before,
.fa-file-image-o:before {
  content: "\f1c5";
}
.fa-file-zip-o:before,
.fa-file-archive-o:before {
  content: "\f1c6";
}
.fa-file-sound-o:before,
.fa-file-audio-o:before {
  content: "\f1c7";
}
.fa-file-movie-o:before,
.fa-file-video-o:before {
  content: "\f1c8";
}
.fa-file-code-o:before {
  content: "\f1c9";
}
.fa-vine:before {
  content: "\f1ca";
}
.fa-codepen:before {
  content: "\f1cb";
}
.fa-jsfiddle:before {
  content: "\f1cc";
}
.fa-life-bouy:before,
.fa-life-buoy:before,
.fa-life-saver:before,
.fa-support:before,
.fa-life-ring:before {
  content: "\f1cd";
}
.fa-circle-o-notch:before {
  content: "\f1ce";
}
.fa-ra:before,
.fa-rebel:before {
  content: "\f1d0";
}
.fa-ge:before,
.fa-empire:before {
  content: "\f1d1";
}
.fa-git-square:before {
  content: "\f1d2";
}
.fa-git:before {
  content: "\f1d3";
}
.fa-hacker-news:before {
  content: "\f1d4";
}
.fa-tencent-weibo:before {
  content: "\f1d5";
}
.fa-qq:before {
  content: "\f1d6";
}
.fa-wechat:before,
.fa-weixin:before {
  content: "\f1d7";
}
.fa-send:before,
.fa-paper-plane:before {
  content: "\f1d8";
}
.fa-send-o:before,
.fa-paper-plane-o:before {
  content: "\f1d9";
}
.fa-history:before {
  content: "\f1da";
}
.fa-circle-thin:before {
  content: "\f1db";
}
.fa-header:before {
  content: "\f1dc";
}
.fa-paragraph:before {
  content: "\f1dd";
}
.fa-sliders:before {
  content: "\f1de";
}
.fa-share-alt:before {
  content: "\f1e0";
}
.fa-share-alt-square:before {
  content: "\f1e1";
}
.fa-bomb:before {
  content: "\f1e2";
}
.fa-soccer-ball-o:before,
.fa-futbol-o:before {
  content: "\f1e3";
}
.fa-tty:before {
  content: "\f1e4";
}
.fa-binoculars:before {
  content: "\f1e5";
}
.fa-plug:before {
  content: "\f1e6";
}
.fa-slideshare:before {
  content: "\f1e7";
}
.fa-twitch:before {
  content: "\f1e8";
}
.fa-yelp:before {
  content: "\f1e9";
}
.fa-newspaper-o:before {
  content: "\f1ea";
}
.fa-wifi:before {
  content: "\f1eb";
}
.fa-calculator:before {
  content: "\f1ec";
}
.fa-paypal:before {
  content: "\f1ed";
}
.fa-google-wallet:before {
  content: "\f1ee";
}
.fa-cc-visa:before {
  content: "\f1f0";
}
.fa-cc-mastercard:before {
  content: "\f1f1";
}
.fa-cc-discover:before {
  content: "\f1f2";
}
.fa-cc-amex:before {
  content: "\f1f3";
}
.fa-cc-paypal:before {
  content: "\f1f4";
}
.fa-cc-stripe:before {
  content: "\f1f5";
}
.fa-bell-slash:before {
  content: "\f1f6";
}
.fa-bell-slash-o:before {
  content: "\f1f7";
}
.fa-trash:before {
  content: "\f1f8";
}
.fa-copyright:before {
  content: "\f1f9";
}
.fa-at:before {
  content: "\f1fa";
}
.fa-eyedropper:before {
  content: "\f1fb";
}
.fa-paint-brush:before {
  content: "\f1fc";
}
.fa-birthday-cake:before {
  content: "\f1fd";
}
.fa-area-chart:before {
  content: "\f1fe";
}
.fa-pie-chart:before {
  content: "\f200";
}
.fa-line-chart:before {
  content: "\f201";
}
.fa-lastfm:before {
  content: "\f202";
}
.fa-lastfm-square:before {
  content: "\f203";
}
.fa-toggle-off:before {
  content: "\f204";
}
.fa-toggle-on:before {
  content: "\f205";
}
.fa-bicycle:before {
  content: "\f206";
}
.fa-bus:before {
  content: "\f207";
}
.fa-ioxhost:before {
  content: "\f208";
}
.fa-angellist:before {
  content: "\f209";
}
.fa-cc:before {
  content: "\f20a";
}
.fa-shekel:before,
.fa-sheqel:before,
.fa-ils:before {
  content: "\f20b";
}
.fa-meanpath:before {
  content: "\f20c";
}
/*!
*
* IPython base
*
*/
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
code {
  color: #000;
}
pre {
  font-size: inherit;
  line-height: inherit;
}
label {
  font-weight: normal;
}
/* Make the page background atleast 100% the height of the view port */
/* Make the page itself atleast 70% the height of the view port */
.border-box-sizing {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.corner-all {
  border-radius: 2px;
}
.no-padding {
  padding: 0px;
}
/* Flexible box model classes */
/* Taken from Alex Russell http://infrequently.org/2009/08/css-3-progress/ */
/* This file is a compatability layer.  It allows the usage of flexible box 
model layouts accross multiple browsers, including older browsers.  The newest,
universal implementation of the flexible box model is used when available (see
`Modern browsers` comments below).  Browsers that are known to implement this 
new spec completely include:

    Firefox 28.0+
    Chrome 29.0+
    Internet Explorer 11+ 
    Opera 17.0+

Browsers not listed, including Safari, are supported via the styling under the
`Old browsers` comments below.
*/
.hbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
.hbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.vbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
.vbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.hbox.reverse,
.vbox.reverse,
.reverse {
  /* Old browsers */
  -webkit-box-direction: reverse;
  -moz-box-direction: reverse;
  box-direction: reverse;
  /* Modern browsers */
  flex-direction: row-reverse;
}
.hbox.box-flex0,
.vbox.box-flex0,
.box-flex0 {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
  width: auto;
}
.hbox.box-flex1,
.vbox.box-flex1,
.box-flex1 {
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex,
.vbox.box-flex,
.box-flex {
  /* Old browsers */
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex2,
.vbox.box-flex2,
.box-flex2 {
  /* Old browsers */
  -webkit-box-flex: 2;
  -moz-box-flex: 2;
  box-flex: 2;
  /* Modern browsers */
  flex: 2;
}
.box-group1 {
  /*  Deprecated */
  -webkit-box-flex-group: 1;
  -moz-box-flex-group: 1;
  box-flex-group: 1;
}
.box-group2 {
  /* Deprecated */
  -webkit-box-flex-group: 2;
  -moz-box-flex-group: 2;
  box-flex-group: 2;
}
.hbox.start,
.vbox.start,
.start {
  /* Old browsers */
  -webkit-box-pack: start;
  -moz-box-pack: start;
  box-pack: start;
  /* Modern browsers */
  justify-content: flex-start;
}
.hbox.end,
.vbox.end,
.end {
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
}
.hbox.center,
.vbox.center,
.center {
  /* Old browsers */
  -webkit-box-pack: center;
  -moz-box-pack: center;
  box-pack: center;
  /* Modern browsers */
  justify-content: center;
}
.hbox.baseline,
.vbox.baseline,
.baseline {
  /* Old browsers */
  -webkit-box-pack: baseline;
  -moz-box-pack: baseline;
  box-pack: baseline;
  /* Modern browsers */
  justify-content: baseline;
}
.hbox.stretch,
.vbox.stretch,
.stretch {
  /* Old browsers */
  -webkit-box-pack: stretch;
  -moz-box-pack: stretch;
  box-pack: stretch;
  /* Modern browsers */
  justify-content: stretch;
}
.hbox.align-start,
.vbox.align-start,
.align-start {
  /* Old browsers */
  -webkit-box-align: start;
  -moz-box-align: start;
  box-align: start;
  /* Modern browsers */
  align-items: flex-start;
}
.hbox.align-end,
.vbox.align-end,
.align-end {
  /* Old browsers */
  -webkit-box-align: end;
  -moz-box-align: end;
  box-align: end;
  /* Modern browsers */
  align-items: flex-end;
}
.hbox.align-center,
.vbox.align-center,
.align-center {
  /* Old browsers */
  -webkit-box-align: center;
  -moz-box-align: center;
  box-align: center;
  /* Modern browsers */
  align-items: center;
}
.hbox.align-baseline,
.vbox.align-baseline,
.align-baseline {
  /* Old browsers */
  -webkit-box-align: baseline;
  -moz-box-align: baseline;
  box-align: baseline;
  /* Modern browsers */
  align-items: baseline;
}
.hbox.align-stretch,
.vbox.align-stretch,
.align-stretch {
  /* Old browsers */
  -webkit-box-align: stretch;
  -moz-box-align: stretch;
  box-align: stretch;
  /* Modern browsers */
  align-items: stretch;
}
div.error {
  margin: 2em;
  text-align: center;
}
div.error > h1 {
  font-size: 500%;
  line-height: normal;
}
div.error > p {
  font-size: 200%;
  line-height: normal;
}
div.traceback-wrapper {
  text-align: left;
  max-width: 800px;
  margin: auto;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
body {
  background-color: #fff;
  /* This makes sure that the body covers the entire window and needs to
       be in a different element than the display: box in wrapper below */
  position: absolute;
  left: 0px;
  right: 0px;
  top: 0px;
  bottom: 0px;
  overflow: visible;
}
body > #header {
  /* Initially hidden to prevent FLOUC */
  display: none;
  background-color: #fff;
  /* Display over codemirror */
  position: relative;
  z-index: 100;
}
body > #header #header-container {
  padding-bottom: 5px;
  padding-top: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
body > #header .header-bar {
  width: 100%;
  height: 1px;
  background: #e7e7e7;
  margin-bottom: -1px;
}
@media print {
  body > #header {
    display: none !important;
  }
}
#header-spacer {
  width: 100%;
  visibility: hidden;
}
@media print {
  #header-spacer {
    display: none;
  }
}
#ipython_notebook {
  padding-left: 0px;
  padding-top: 1px;
  padding-bottom: 1px;
}
@media (max-width: 991px) {
  #ipython_notebook {
    margin-left: 10px;
  }
}
[dir="rtl"] #ipython_notebook {
  float: right !important;
}
#noscript {
  width: auto;
  padding-top: 16px;
  padding-bottom: 16px;
  text-align: center;
  font-size: 22px;
  color: red;
  font-weight: bold;
}
#ipython_notebook img {
  height: 28px;
}
#site {
  width: 100%;
  display: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  overflow: auto;
}
@media print {
  #site {
    height: auto !important;
  }
}
/* Smaller buttons */
.ui-button .ui-button-text {
  padding: 0.2em 0.8em;
  font-size: 77%;
}
input.ui-button {
  padding: 0.3em 0.9em;
}
span#login_widget {
  float: right;
}
span#login_widget > .button,
#logout {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button:focus,
#logout:focus,
span#login_widget > .button.focus,
#logout.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
span#login_widget > .button:hover,
#logout:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active:hover,
#logout:active:hover,
span#login_widget > .button.active:hover,
#logout.active:hover,
.open > .dropdown-togglespan#login_widget > .button:hover,
.open > .dropdown-toggle#logout:hover,
span#login_widget > .button:active:focus,
#logout:active:focus,
span#login_widget > .button.active:focus,
#logout.active:focus,
.open > .dropdown-togglespan#login_widget > .button:focus,
.open > .dropdown-toggle#logout:focus,
span#login_widget > .button:active.focus,
#logout:active.focus,
span#login_widget > .button.active.focus,
#logout.active.focus,
.open > .dropdown-togglespan#login_widget > .button.focus,
.open > .dropdown-toggle#logout.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  background-image: none;
}
span#login_widget > .button.disabled:hover,
#logout.disabled:hover,
span#login_widget > .button[disabled]:hover,
#logout[disabled]:hover,
fieldset[disabled] span#login_widget > .button:hover,
fieldset[disabled] #logout:hover,
span#login_widget > .button.disabled:focus,
#logout.disabled:focus,
span#login_widget > .button[disabled]:focus,
#logout[disabled]:focus,
fieldset[disabled] span#login_widget > .button:focus,
fieldset[disabled] #logout:focus,
span#login_widget > .button.disabled.focus,
#logout.disabled.focus,
span#login_widget > .button[disabled].focus,
#logout[disabled].focus,
fieldset[disabled] span#login_widget > .button.focus,
fieldset[disabled] #logout.focus {
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button .badge,
#logout .badge {
  color: #fff;
  background-color: #333;
}
.nav-header {
  text-transform: none;
}
#header > span {
  margin-top: 10px;
}
.modal_stretch .modal-dialog {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  min-height: 80vh;
}
.modal_stretch .modal-dialog .modal-body {
  max-height: calc(100vh - 200px);
  overflow: auto;
  flex: 1;
}
@media (min-width: 768px) {
  .modal .modal-dialog {
    width: 700px;
  }
}
@media (min-width: 768px) {
  select.form-control {
    margin-left: 12px;
    margin-right: 12px;
  }
}
/*!
*
* IPython auth
*
*/
.center-nav {
  display: inline-block;
  margin-bottom: -4px;
}
/*!
*
* IPython tree view
*
*/
/* We need an invisible input field on top of the sentense*/
/* "Drag file onto the list ..." */
.alternate_upload {
  background-color: none;
  display: inline;
}
.alternate_upload.form {
  padding: 0;
  margin: 0;
}
.alternate_upload input.fileinput {
  text-align: center;
  vertical-align: middle;
  display: inline;
  opacity: 0;
  z-index: 2;
  width: 12ex;
  margin-right: -12ex;
}
.alternate_upload .btn-upload {
  height: 22px;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
[dir="rtl"] #tabs li {
  float: right;
}
ul#tabs {
  margin-bottom: 4px;
}
[dir="rtl"] ul#tabs {
  margin-right: 0px;
}
ul#tabs a {
  padding-top: 6px;
  padding-bottom: 4px;
}
ul.breadcrumb a:focus,
ul.breadcrumb a:hover {
  text-decoration: none;
}
ul.breadcrumb i.icon-home {
  font-size: 16px;
  margin-right: 4px;
}
ul.breadcrumb span {
  color: #5e5e5e;
}
.list_toolbar {
  padding: 4px 0 4px 0;
  vertical-align: middle;
}
.list_toolbar .tree-buttons {
  padding-top: 1px;
}
[dir="rtl"] .list_toolbar .tree-buttons {
  float: left !important;
}
[dir="rtl"] .list_toolbar .pull-right {
  padding-top: 1px;
  float: left !important;
}
[dir="rtl"] .list_toolbar .pull-left {
  float: right !important;
}
.dynamic-buttons {
  padding-top: 3px;
  display: inline-block;
}
.list_toolbar [class*="span"] {
  min-height: 24px;
}
.list_header {
  font-weight: bold;
  background-color: #EEE;
}
.list_placeholder {
  font-weight: bold;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
}
.list_container {
  margin-top: 4px;
  margin-bottom: 20px;
  border: 1px solid #ddd;
  border-radius: 2px;
}
.list_container > div {
  border-bottom: 1px solid #ddd;
}
.list_container > div:hover .list-item {
  background-color: red;
}
.list_container > div:last-child {
  border: none;
}
.list_item:hover .list_item {
  background-color: #ddd;
}
.list_item a {
  text-decoration: none;
}
.list_item:hover {
  background-color: #fafafa;
}
.list_header > div,
.list_item > div {
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
.list_header > div input,
.list_item > div input {
  margin-right: 7px;
  margin-left: 14px;
  vertical-align: baseline;
  line-height: 22px;
  position: relative;
  top: -1px;
}
.list_header > div .item_link,
.list_item > div .item_link {
  margin-left: -1px;
  vertical-align: baseline;
  line-height: 22px;
}
.new-file input[type=checkbox] {
  visibility: hidden;
}
.item_name {
  line-height: 22px;
  height: 24px;
}
.item_icon {
  font-size: 14px;
  color: #5e5e5e;
  margin-right: 7px;
  margin-left: 7px;
  line-height: 22px;
  vertical-align: baseline;
}
.item_buttons {
  line-height: 1em;
  margin-left: -5px;
}
.item_buttons .btn,
.item_buttons .btn-group,
.item_buttons .input-group {
  float: left;
}
.item_buttons > .btn,
.item_buttons > .btn-group,
.item_buttons > .input-group {
  margin-left: 5px;
}
.item_buttons .btn {
  min-width: 13ex;
}
.item_buttons .running-indicator {
  padding-top: 4px;
  color: #5cb85c;
}
.item_buttons .kernel-name {
  padding-top: 4px;
  color: #5bc0de;
  margin-right: 7px;
  float: left;
}
.toolbar_info {
  height: 24px;
  line-height: 24px;
}
.list_item input:not([type=checkbox]) {
  padding-top: 3px;
  padding-bottom: 3px;
  height: 22px;
  line-height: 14px;
  margin: 0px;
}
.highlight_text {
  color: blue;
}
#project_name {
  display: inline-block;
  padding-left: 7px;
  margin-left: -2px;
}
#project_name > .breadcrumb {
  padding: 0px;
  margin-bottom: 0px;
  background-color: transparent;
  font-weight: bold;
}
#tree-selector {
  padding-right: 0px;
}
[dir="rtl"] #tree-selector a {
  float: right;
}
#button-select-all {
  min-width: 50px;
}
#select-all {
  margin-left: 7px;
  margin-right: 2px;
}
.menu_icon {
  margin-right: 2px;
}
.tab-content .row {
  margin-left: 0px;
  margin-right: 0px;
}
.folder_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f114";
}
.folder_icon:before.pull-left {
  margin-right: .3em;
}
.folder_icon:before.pull-right {
  margin-left: .3em;
}
.notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
}
.notebook_icon:before.pull-left {
  margin-right: .3em;
}
.notebook_icon:before.pull-right {
  margin-left: .3em;
}
.running_notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
  color: #5cb85c;
}
.running_notebook_icon:before.pull-left {
  margin-right: .3em;
}
.running_notebook_icon:before.pull-right {
  margin-left: .3em;
}
.file_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f016";
  position: relative;
  top: -2px;
}
.file_icon:before.pull-left {
  margin-right: .3em;
}
.file_icon:before.pull-right {
  margin-left: .3em;
}
#notebook_toolbar .pull-right {
  padding-top: 0px;
  margin-right: -1px;
}
ul#new-menu {
  left: auto;
  right: 0;
}
[dir="rtl"] #new-menu {
  text-align: right;
}
.kernel-menu-icon {
  padding-right: 12px;
  width: 24px;
  content: "\f096";
}
.kernel-menu-icon:before {
  content: "\f096";
}
.kernel-menu-icon-current:before {
  content: "\f00c";
}
#tab_content {
  padding-top: 20px;
}
#running .panel-group .panel {
  margin-top: 3px;
  margin-bottom: 1em;
}
#running .panel-group .panel .panel-heading {
  background-color: #EEE;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
#running .panel-group .panel .panel-heading a:focus,
#running .panel-group .panel .panel-heading a:hover {
  text-decoration: none;
}
#running .panel-group .panel .panel-body {
  padding: 0px;
}
#running .panel-group .panel .panel-body .list_container {
  margin-top: 0px;
  margin-bottom: 0px;
  border: 0px;
  border-radius: 0px;
}
#running .panel-group .panel .panel-body .list_container .list_item {
  border-bottom: 1px solid #ddd;
}
#running .panel-group .panel .panel-body .list_container .list_item:last-child {
  border-bottom: 0px;
}
[dir="rtl"] #running .col-sm-8 {
  float: right !important;
}
.delete-button {
  display: none;
}
.duplicate-button {
  display: none;
}
.rename-button {
  display: none;
}
.shutdown-button {
  display: none;
}
.dynamic-instructions {
  display: inline-block;
  padding-top: 4px;
}
/*!
*
* IPython text editor webapp
*
*/
.selected-keymap i.fa {
  padding: 0px 5px;
}
.selected-keymap i.fa:before {
  content: "\f00c";
}
#mode-menu {
  overflow: auto;
  max-height: 20em;
}
.edit_app #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.edit_app #menubar .navbar {
  /* Use a negative 1 bottom margin, so the border overlaps the border of the
    header */
  margin-bottom: -1px;
}
.dirty-indicator {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator.pull-left {
  margin-right: .3em;
}
.dirty-indicator.pull-right {
  margin-left: .3em;
}
.dirty-indicator-dirty {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-dirty.pull-left {
  margin-right: .3em;
}
.dirty-indicator-dirty.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-clean.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f00c";
}
.dirty-indicator-clean:before.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean:before.pull-right {
  margin-left: .3em;
}
#filename {
  font-size: 16pt;
  display: table;
  padding: 0px 5px;
}
#current-mode {
  padding-left: 5px;
  padding-right: 5px;
}
#texteditor-backdrop {
  padding-top: 20px;
  padding-bottom: 20px;
}
@media not print {
  #texteditor-backdrop {
    background-color: #EEE;
  }
}
@media print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container {
    padding: 0px;
    background-color: #fff;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
/*!
*
* IPython notebook
*
*/
/* CSS font colors for translated ANSI colors. */
.ansibold {
  font-weight: bold;
}
/* use dark versions for foreground, to improve visibility */
.ansiblack {
  color: black;
}
.ansired {
  color: darkred;
}
.ansigreen {
  color: darkgreen;
}
.ansiyellow {
  color: #c4a000;
}
.ansiblue {
  color: darkblue;
}
.ansipurple {
  color: darkviolet;
}
.ansicyan {
  color: steelblue;
}
.ansigray {
  color: gray;
}
/* and light for background, for the same reason */
.ansibgblack {
  background-color: black;
}
.ansibgred {
  background-color: red;
}
.ansibggreen {
  background-color: green;
}
.ansibgyellow {
  background-color: yellow;
}
.ansibgblue {
  background-color: blue;
}
.ansibgpurple {
  background-color: magenta;
}
.ansibgcyan {
  background-color: cyan;
}
.ansibggray {
  background-color: gray;
}
div.cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  border-radius: 2px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  border-width: 1px;
  border-style: solid;
  border-color: transparent;
  width: 100%;
  padding: 5px;
  /* This acts as a spacer between cells, that is outside the border */
  margin: 0px;
  outline: none;
  border-left-width: 1px;
  padding-left: 5px;
  background: linear-gradient(to right, transparent -40px, transparent 1px, transparent 1px, transparent 100%);
}
div.cell.jupyter-soft-selected {
  border-left-color: #90CAF9;
  border-left-color: #E3F2FD;
  border-left-width: 1px;
  padding-left: 5px;
  border-right-color: #E3F2FD;
  border-right-width: 1px;
  background: #E3F2FD;
}
@media print {
  div.cell.jupyter-soft-selected {
    border-color: transparent;
  }
}
div.cell.selected {
  border-color: #ababab;
  border-left-width: 0px;
  padding-left: 6px;
  background: linear-gradient(to right, #42A5F5 -40px, #42A5F5 5px, transparent 5px, transparent 100%);
}
@media print {
  div.cell.selected {
    border-color: transparent;
  }
}
div.cell.selected.jupyter-soft-selected {
  border-left-width: 0;
  padding-left: 6px;
  background: linear-gradient(to right, #42A5F5 -40px, #42A5F5 7px, #E3F2FD 7px, #E3F2FD 100%);
}
.edit_mode div.cell.selected {
  border-color: #66BB6A;
  border-left-width: 0px;
  padding-left: 6px;
  background: linear-gradient(to right, #66BB6A -40px, #66BB6A 5px, transparent 5px, transparent 100%);
}
@media print {
  .edit_mode div.cell.selected {
    border-color: transparent;
  }
}
.prompt {
  /* This needs to be wide enough for 3 digit prompt numbers: In[100]: */
  min-width: 14ex;
  /* This padding is tuned to match the padding on the CodeMirror editor. */
  padding: 0.4em;
  margin: 0px;
  font-family: monospace;
  text-align: right;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
  /* Don't highlight prompt number selection */
  -webkit-touch-callout: none;
  -webkit-user-select: none;
  -khtml-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  /* Use default cursor */
  cursor: default;
}
@media (max-width: 540px) {
  .prompt {
    text-align: left;
  }
}
div.inner_cell {
  min-width: 0;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_area {
  border: 1px solid #cfcfcf;
  border-radius: 2px;
  background: #f7f7f7;
  line-height: 1.21429em;
}
/* This is needed so that empty prompt areas can collapse to zero height when there
   is no content in the output_subarea and the prompt. The main purpose of this is
   to make sure that empty JavaScript output_subareas have no height. */
div.prompt:empty {
  padding-top: 0;
  padding-bottom: 0;
}
div.unrecognized_cell {
  padding: 5px 5px 5px 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.unrecognized_cell .inner_cell {
  border-radius: 2px;
  padding: 5px;
  font-weight: bold;
  color: red;
  border: 1px solid #cfcfcf;
  background: #eaeaea;
}
div.unrecognized_cell .inner_cell a {
  color: inherit;
  text-decoration: none;
}
div.unrecognized_cell .inner_cell a:hover {
  color: inherit;
  text-decoration: none;
}
@media (max-width: 540px) {
  div.unrecognized_cell > div.prompt {
    display: none;
  }
}
div.code_cell {
  /* avoid page breaking on code cells when printing */
}
@media print {
  div.code_cell {
    page-break-inside: avoid;
  }
}
/* any special styling for code cells that are currently running goes here */
div.input {
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.input {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_prompt {
  color: #303F9F;
  border-top: 1px solid transparent;
}
div.input_area > div.highlight {
  margin: 0.4em;
  border: none;
  padding: 0px;
  background-color: transparent;
}
div.input_area > div.highlight > pre {
  margin: 0px;
  border: none;
  padding: 0px;
  background-color: transparent;
}
/* The following gets added to the <head> if it is detected that the user has a
 * monospace font with inconsistent normal/bold/italic height.  See
 * notebookmain.js.  Such fonts will have keywords vertically offset with
 * respect to the rest of the text.  The user should select a better font.
 * See: https://github.com/ipython/ipython/issues/1503
 *
 * .CodeMirror span {
 *      vertical-align: bottom;
 * }
 */
.CodeMirror {
  line-height: 1.21429em;
  /* Changed from 1em to our global default */
  font-size: 14px;
  height: auto;
  /* Changed to auto to autogrow */
  background: none;
  /* Changed from white to allow our bg to show through */
}
.CodeMirror-scroll {
  /*  The CodeMirror docs are a bit fuzzy on if overflow-y should be hidden or visible.*/
  /*  We have found that if it is visible, vertical scrollbars appear with font size changes.*/
  overflow-y: hidden;
  overflow-x: auto;
}
.CodeMirror-lines {
  /* In CM2, this used to be 0.4em, but in CM3 it went to 4px. We need the em value because */
  /* we have set a different line-height and want this to scale with that. */
  padding: 0.4em;
}
.CodeMirror-linenumber {
  padding: 0 8px 0 4px;
}
.CodeMirror-gutters {
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.CodeMirror pre {
  /* In CM3 this went to 4px from 0 in CM2. We need the 0 value because of how we size */
  /* .CodeMirror-lines */
  padding: 0;
  border: 0;
  border-radius: 0;
}
/*

Original style from softwaremaniacs.org (c) Ivan Sagalaev <Maniac@SoftwareManiacs.Org>
Adapted from GitHub theme

*/
.highlight-base {
  color: #000;
}
.highlight-variable {
  color: #000;
}
.highlight-variable-2 {
  color: #1a1a1a;
}
.highlight-variable-3 {
  color: #333333;
}
.highlight-string {
  color: #BA2121;
}
.highlight-comment {
  color: #408080;
  font-style: italic;
}
.highlight-number {
  color: #080;
}
.highlight-atom {
  color: #88F;
}
.highlight-keyword {
  color: #008000;
  font-weight: bold;
}
.highlight-builtin {
  color: #008000;
}
.highlight-error {
  color: #f00;
}
.highlight-operator {
  color: #AA22FF;
  font-weight: bold;
}
.highlight-meta {
  color: #AA22FF;
}
/* previously not defined, copying from default codemirror */
.highlight-def {
  color: #00f;
}
.highlight-string-2 {
  color: #f50;
}
.highlight-qualifier {
  color: #555;
}
.highlight-bracket {
  color: #997;
}
.highlight-tag {
  color: #170;
}
.highlight-attribute {
  color: #00c;
}
.highlight-header {
  color: blue;
}
.highlight-quote {
  color: #090;
}
.highlight-link {
  color: #00c;
}
/* apply the same style to codemirror */
.cm-s-ipython span.cm-keyword {
  color: #008000;
  font-weight: bold;
}
.cm-s-ipython span.cm-atom {
  color: #88F;
}
.cm-s-ipython span.cm-number {
  color: #080;
}
.cm-s-ipython span.cm-def {
  color: #00f;
}
.cm-s-ipython span.cm-variable {
  color: #000;
}
.cm-s-ipython span.cm-operator {
  color: #AA22FF;
  font-weight: bold;
}
.cm-s-ipython span.cm-variable-2 {
  color: #1a1a1a;
}
.cm-s-ipython span.cm-variable-3 {
  color: #333333;
}
.cm-s-ipython span.cm-comment {
  color: #408080;
  font-style: italic;
}
.cm-s-ipython span.cm-string {
  color: #BA2121;
}
.cm-s-ipython span.cm-string-2 {
  color: #f50;
}
.cm-s-ipython span.cm-meta {
  color: #AA22FF;
}
.cm-s-ipython span.cm-qualifier {
  color: #555;
}
.cm-s-ipython span.cm-builtin {
  color: #008000;
}
.cm-s-ipython span.cm-bracket {
  color: #997;
}
.cm-s-ipython span.cm-tag {
  color: #170;
}
.cm-s-ipython span.cm-attribute {
  color: #00c;
}
.cm-s-ipython span.cm-header {
  color: blue;
}
.cm-s-ipython span.cm-quote {
  color: #090;
}
.cm-s-ipython span.cm-link {
  color: #00c;
}
.cm-s-ipython span.cm-error {
  color: #f00;
}
.cm-s-ipython span.cm-tab {
  background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAMCAYAAAAkuj5RAAAAAXNSR0IArs4c6QAAAGFJREFUSMft1LsRQFAQheHPowAKoACx3IgEKtaEHujDjORSgWTH/ZOdnZOcM/sgk/kFFWY0qV8foQwS4MKBCS3qR6ixBJvElOobYAtivseIE120FaowJPN75GMu8j/LfMwNjh4HUpwg4LUAAAAASUVORK5CYII=);
  background-position: right;
  background-repeat: no-repeat;
}
div.output_wrapper {
  /* this position must be relative to enable descendents to be absolute within it */
  position: relative;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  z-index: 1;
}
/* class for the output area when it should be height-limited */
div.output_scroll {
  /* ideally, this would be max-height, but FF barfs all over that */
  height: 24em;
  /* FF needs this *and the wrapper* to specify full width, or it will shrinkwrap */
  width: 100%;
  overflow: auto;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  display: block;
}
/* output div while it is collapsed */
div.output_collapsed {
  margin: 0px;
  padding: 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
div.out_prompt_overlay {
  height: 100%;
  padding: 0px 0.4em;
  position: absolute;
  border-radius: 2px;
}
div.out_prompt_overlay:hover {
  /* use inner shadow to get border that is computed the same on WebKit/FF */
  -webkit-box-shadow: inset 0 0 1px #000;
  box-shadow: inset 0 0 1px #000;
  background: rgba(240, 240, 240, 0.5);
}
div.output_prompt {
  color: #D84315;
}
/* This class is the outer container of all output sections. */
div.output_area {
  padding: 0px;
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.output_area .MathJax_Display {
  text-align: left !important;
}
div.output_area .rendered_html table {
  margin-left: 0;
  margin-right: 0;
}
div.output_area .rendered_html img {
  margin-left: 0;
  margin-right: 0;
}
div.output_area img,
div.output_area svg {
  max-width: 100%;
  height: auto;
}
div.output_area img.unconfined,
div.output_area svg.unconfined {
  max-width: none;
}
/* This is needed to protect the pre formating from global settings such
   as that of bootstrap */
.output {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.output_area {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
div.output_area pre {
  margin: 0;
  padding: 0;
  border: 0;
  vertical-align: baseline;
  color: black;
  background-color: transparent;
  border-radius: 0;
}
/* This class is for the output subarea inside the output_area and after
   the prompt div. */
div.output_subarea {
  overflow-x: auto;
  padding: 0.4em;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
  max-width: calc(100% - 14ex);
}
div.output_scroll div.output_subarea {
  overflow-x: visible;
}
/* The rest of the output_* classes are for special styling of the different
   output types */
/* all text output has this class: */
div.output_text {
  text-align: left;
  color: #000;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
}
/* stdout/stderr are 'text' as well as 'stream', but execute_result/error are *not* streams */
div.output_stderr {
  background: #fdd;
  /* very light red background for stderr */
}
div.output_latex {
  text-align: left;
}
/* Empty output_javascript divs should have no height */
div.output_javascript:empty {
  padding: 0;
}
.js-error {
  color: darkred;
}
/* raw_input styles */
div.raw_input_container {
  line-height: 1.21429em;
  padding-top: 5px;
}
pre.raw_input_prompt {
  /* nothing needed here. */
}
input.raw_input {
  font-family: monospace;
  font-size: inherit;
  color: inherit;
  width: auto;
  /* make sure input baseline aligns with prompt */
  vertical-align: baseline;
  /* padding + margin = 0.5em between prompt and cursor */
  padding: 0em 0.25em;
  margin: 0em 0.25em;
}
input.raw_input:focus {
  box-shadow: none;
}
p.p-space {
  margin-bottom: 10px;
}
div.output_unrecognized {
  padding: 5px;
  font-weight: bold;
  color: red;
}
div.output_unrecognized a {
  color: inherit;
  text-decoration: none;
}
div.output_unrecognized a:hover {
  color: inherit;
  text-decoration: none;
}
.rendered_html {
  color: #000;
  /* any extras will just be numbers: */
}
.rendered_html em {
  font-style: italic;
}
.rendered_html strong {
  font-weight: bold;
}
.rendered_html u {
  text-decoration: underline;
}
.rendered_html :link {
  text-decoration: underline;
}
.rendered_html :visited {
  text-decoration: underline;
}
.rendered_html h1 {
  font-size: 185.7%;
  margin: 1.08em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h2 {
  font-size: 157.1%;
  margin: 1.27em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h3 {
  font-size: 128.6%;
  margin: 1.55em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h4 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h5 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h6 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h1:first-child {
  margin-top: 0.538em;
}
.rendered_html h2:first-child {
  margin-top: 0.636em;
}
.rendered_html h3:first-child {
  margin-top: 0.777em;
}
.rendered_html h4:first-child {
  margin-top: 1em;
}
.rendered_html h5:first-child {
  margin-top: 1em;
}
.rendered_html h6:first-child {
  margin-top: 1em;
}
.rendered_html ul {
  list-style: disc;
  margin: 0em 2em;
  padding-left: 0px;
}
.rendered_html ul ul {
  list-style: square;
  margin: 0em 2em;
}
.rendered_html ul ul ul {
  list-style: circle;
  margin: 0em 2em;
}
.rendered_html ol {
  list-style: decimal;
  margin: 0em 2em;
  padding-left: 0px;
}
.rendered_html ol ol {
  list-style: upper-alpha;
  margin: 0em 2em;
}
.rendered_html ol ol ol {
  list-style: lower-alpha;
  margin: 0em 2em;
}
.rendered_html ol ol ol ol {
  list-style: lower-roman;
  margin: 0em 2em;
}
.rendered_html ol ol ol ol ol {
  list-style: decimal;
  margin: 0em 2em;
}
.rendered_html * + ul {
  margin-top: 1em;
}
.rendered_html * + ol {
  margin-top: 1em;
}
.rendered_html hr {
  color: black;
  background-color: black;
}
.rendered_html pre {
  margin: 1em 2em;
}
.rendered_html pre,
.rendered_html code {
  border: 0;
  background-color: #fff;
  color: #000;
  font-size: 100%;
  padding: 0px;
}
.rendered_html blockquote {
  margin: 1em 2em;
}
.rendered_html table {
  margin-left: auto;
  margin-right: auto;
  border: 1px solid black;
  border-collapse: collapse;
}
.rendered_html tr,
.rendered_html th,
.rendered_html td {
  border: 1px solid black;
  border-collapse: collapse;
  margin: 1em 2em;
}
.rendered_html td,
.rendered_html th {
  text-align: left;
  vertical-align: middle;
  padding: 4px;
}
.rendered_html th {
  font-weight: bold;
}
.rendered_html * + table {
  margin-top: 1em;
}
.rendered_html p {
  text-align: left;
}
.rendered_html * + p {
  margin-top: 1em;
}
.rendered_html img {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.rendered_html * + img {
  margin-top: 1em;
}
.rendered_html img,
.rendered_html svg {
  max-width: 100%;
  height: auto;
}
.rendered_html img.unconfined,
.rendered_html svg.unconfined {
  max-width: none;
}
div.text_cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.text_cell > div.prompt {
    display: none;
  }
}
div.text_cell_render {
  /*font-family: "Helvetica Neue", Arial, Helvetica, Geneva, sans-serif;*/
  outline: none;
  resize: none;
  width: inherit;
  border-style: none;
  padding: 0.5em 0.5em 0.5em 0.4em;
  color: #000;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
a.anchor-link:link {
  text-decoration: none;
  padding: 0px 20px;
  visibility: hidden;
}
h1:hover .anchor-link,
h2:hover .anchor-link,
h3:hover .anchor-link,
h4:hover .anchor-link,
h5:hover .anchor-link,
h6:hover .anchor-link {
  visibility: visible;
}
.text_cell.rendered .input_area {
  display: none;
}
.text_cell.rendered .rendered_html {
  overflow-x: auto;
  overflow-y: hidden;
}
.text_cell.unrendered .text_cell_render {
  display: none;
}
.cm-header-1,
.cm-header-2,
.cm-header-3,
.cm-header-4,
.cm-header-5,
.cm-header-6 {
  font-weight: bold;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
}
.cm-header-1 {
  font-size: 185.7%;
}
.cm-header-2 {
  font-size: 157.1%;
}
.cm-header-3 {
  font-size: 128.6%;
}
.cm-header-4 {
  font-size: 110%;
}
.cm-header-5 {
  font-size: 100%;
  font-style: italic;
}
.cm-header-6 {
  font-size: 100%;
  font-style: italic;
}
/*!
*
* IPython notebook webapp
*
*/
@media (max-width: 767px) {
  .notebook_app {
    padding-left: 0px;
    padding-right: 0px;
  }
}
#ipython-main-app {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook_panel {
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook {
  font-size: 14px;
  line-height: 20px;
  overflow-y: hidden;
  overflow-x: auto;
  width: 100%;
  /* This spaces the page away from the edge of the notebook area */
  padding-top: 20px;
  margin: 0px;
  outline: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  min-height: 100%;
}
@media not print {
  #notebook-container {
    padding: 15px;
    background-color: #fff;
    min-height: 0;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
@media print {
  #notebook-container {
    width: 100%;
  }
}
div.ui-widget-content {
  border: 1px solid #ababab;
  outline: none;
}
pre.dialog {
  background-color: #f7f7f7;
  border: 1px solid #ddd;
  border-radius: 2px;
  padding: 0.4em;
  padding-left: 2em;
}
p.dialog {
  padding: 0.2em;
}
/* Word-wrap output correctly.  This is the CSS3 spelling, though Firefox seems
   to not honor it correctly.  Webkit browsers (Chrome, rekonq, Safari) do.
 */
pre,
code,
kbd,
samp {
  white-space: pre-wrap;
}
#fonttest {
  font-family: monospace;
}
p {
  margin-bottom: 0;
}
.end_space {
  min-height: 100px;
  transition: height .2s ease;
}
.notebook_app > #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
@media not print {
  .notebook_app {
    background-color: #EEE;
  }
}
kbd {
  border-style: solid;
  border-width: 1px;
  box-shadow: none;
  margin: 2px;
  padding-left: 2px;
  padding-right: 2px;
  padding-top: 1px;
  padding-bottom: 1px;
}
/* CSS for the cell toolbar */
.celltoolbar {
  border: thin solid #CFCFCF;
  border-bottom: none;
  background: #EEE;
  border-radius: 2px 2px 0px 0px;
  width: 100%;
  height: 29px;
  padding-right: 4px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
  display: -webkit-flex;
}
@media print {
  .celltoolbar {
    display: none;
  }
}
.ctb_hideshow {
  display: none;
  vertical-align: bottom;
}
/* ctb_show is added to the ctb_hideshow div to show the cell toolbar.
   Cell toolbars are only shown when the ctb_global_show class is also set.
*/
.ctb_global_show .ctb_show.ctb_hideshow {
  display: block;
}
.ctb_global_show .ctb_show + .input_area,
.ctb_global_show .ctb_show + div.text_cell_input,
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border-top-right-radius: 0px;
  border-top-left-radius: 0px;
}
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border: 1px solid #cfcfcf;
}
.celltoolbar {
  font-size: 87%;
  padding-top: 3px;
}
.celltoolbar select {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
  width: inherit;
  font-size: inherit;
  height: 22px;
  padding: 0px;
  display: inline-block;
}
.celltoolbar select:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.celltoolbar select::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.celltoolbar select:-ms-input-placeholder {
  color: #999;
}
.celltoolbar select::-webkit-input-placeholder {
  color: #999;
}
.celltoolbar select::-ms-expand {
  border: 0;
  background-color: transparent;
}
.celltoolbar select[disabled],
.celltoolbar select[readonly],
fieldset[disabled] .celltoolbar select {
  background-color: #eeeeee;
  opacity: 1;
}
.celltoolbar select[disabled],
fieldset[disabled] .celltoolbar select {
  cursor: not-allowed;
}
textarea.celltoolbar select {
  height: auto;
}
select.celltoolbar select {
  height: 30px;
  line-height: 30px;
}
textarea.celltoolbar select,
select[multiple].celltoolbar select {
  height: auto;
}
.celltoolbar label {
  margin-left: 5px;
  margin-right: 5px;
}
.completions {
  position: absolute;
  z-index: 110;
  overflow: hidden;
  border: 1px solid #ababab;
  border-radius: 2px;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  line-height: 1;
}
.completions select {
  background: white;
  outline: none;
  border: none;
  padding: 0px;
  margin: 0px;
  overflow: auto;
  font-family: monospace;
  font-size: 110%;
  color: #000;
  width: auto;
}
.completions select option.context {
  color: #286090;
}
#kernel_logo_widget {
  float: right !important;
  float: right;
}
#kernel_logo_widget .current_kernel_logo {
  display: none;
  margin-top: -1px;
  margin-bottom: -1px;
  width: 32px;
  height: 32px;
}
#menubar {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  margin-top: 1px;
}
#menubar .navbar {
  border-top: 1px;
  border-radius: 0px 0px 2px 2px;
  margin-bottom: 0px;
}
#menubar .navbar-toggle {
  float: left;
  padding-top: 7px;
  padding-bottom: 7px;
  border: none;
}
#menubar .navbar-collapse {
  clear: left;
}
.nav-wrapper {
  border-bottom: 1px solid #e7e7e7;
}
i.menu-icon {
  padding-top: 4px;
}
ul#help_menu li a {
  overflow: hidden;
  padding-right: 2.2em;
}
ul#help_menu li a i {
  margin-right: -1.2em;
}
.dropdown-submenu {
  position: relative;
}
.dropdown-submenu > .dropdown-menu {
  top: 0;
  left: 100%;
  margin-top: -6px;
  margin-left: -1px;
}
.dropdown-submenu:hover > .dropdown-menu {
  display: block;
}
.dropdown-submenu > a:after {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: block;
  content: "\f0da";
  float: right;
  color: #333333;
  margin-top: 2px;
  margin-right: -10px;
}
.dropdown-submenu > a:after.pull-left {
  margin-right: .3em;
}
.dropdown-submenu > a:after.pull-right {
  margin-left: .3em;
}
.dropdown-submenu:hover > a:after {
  color: #262626;
}
.dropdown-submenu.pull-left {
  float: none;
}
.dropdown-submenu.pull-left > .dropdown-menu {
  left: -100%;
  margin-left: 10px;
}
#notification_area {
  float: right !important;
  float: right;
  z-index: 10;
}
.indicator_area {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
#kernel_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  border-left: 1px solid;
}
#kernel_indicator .kernel_indicator_name {
  padding-left: 5px;
  padding-right: 5px;
}
#modal_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
#readonly-indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  margin-top: 2px;
  margin-bottom: 0px;
  margin-left: 0px;
  margin-right: 0px;
  display: none;
}
.modal_indicator:before {
  width: 1.28571429em;
  text-align: center;
}
.edit_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f040";
}
.edit_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.edit_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.command_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: ' ';
}
.command_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.command_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.kernel_idle_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f10c";
}
.kernel_idle_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_idle_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_busy_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f111";
}
.kernel_busy_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_busy_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_dead_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f1e2";
}
.kernel_dead_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_dead_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_disconnected_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f127";
}
.kernel_disconnected_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_disconnected_icon:before.pull-right {
  margin-left: .3em;
}
.notification_widget {
  color: #777;
  z-index: 10;
  background: rgba(240, 240, 240, 0.5);
  margin-right: 4px;
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget:focus,
.notification_widget.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.notification_widget:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active:hover,
.notification_widget.active:hover,
.open > .dropdown-toggle.notification_widget:hover,
.notification_widget:active:focus,
.notification_widget.active:focus,
.open > .dropdown-toggle.notification_widget:focus,
.notification_widget:active.focus,
.notification_widget.active.focus,
.open > .dropdown-toggle.notification_widget.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  background-image: none;
}
.notification_widget.disabled:hover,
.notification_widget[disabled]:hover,
fieldset[disabled] .notification_widget:hover,
.notification_widget.disabled:focus,
.notification_widget[disabled]:focus,
fieldset[disabled] .notification_widget:focus,
.notification_widget.disabled.focus,
.notification_widget[disabled].focus,
fieldset[disabled] .notification_widget.focus {
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget .badge {
  color: #fff;
  background-color: #333;
}
.notification_widget.warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning:focus,
.notification_widget.warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.notification_widget.warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active:hover,
.notification_widget.warning.active:hover,
.open > .dropdown-toggle.notification_widget.warning:hover,
.notification_widget.warning:active:focus,
.notification_widget.warning.active:focus,
.open > .dropdown-toggle.notification_widget.warning:focus,
.notification_widget.warning:active.focus,
.notification_widget.warning.active.focus,
.open > .dropdown-toggle.notification_widget.warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  background-image: none;
}
.notification_widget.warning.disabled:hover,
.notification_widget.warning[disabled]:hover,
fieldset[disabled] .notification_widget.warning:hover,
.notification_widget.warning.disabled:focus,
.notification_widget.warning[disabled]:focus,
fieldset[disabled] .notification_widget.warning:focus,
.notification_widget.warning.disabled.focus,
.notification_widget.warning[disabled].focus,
fieldset[disabled] .notification_widget.warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.notification_widget.success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success:focus,
.notification_widget.success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.notification_widget.success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active:hover,
.notification_widget.success.active:hover,
.open > .dropdown-toggle.notification_widget.success:hover,
.notification_widget.success:active:focus,
.notification_widget.success.active:focus,
.open > .dropdown-toggle.notification_widget.success:focus,
.notification_widget.success:active.focus,
.notification_widget.success.active.focus,
.open > .dropdown-toggle.notification_widget.success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  background-image: none;
}
.notification_widget.success.disabled:hover,
.notification_widget.success[disabled]:hover,
fieldset[disabled] .notification_widget.success:hover,
.notification_widget.success.disabled:focus,
.notification_widget.success[disabled]:focus,
fieldset[disabled] .notification_widget.success:focus,
.notification_widget.success.disabled.focus,
.notification_widget.success[disabled].focus,
fieldset[disabled] .notification_widget.success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.notification_widget.info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info:focus,
.notification_widget.info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.notification_widget.info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active:hover,
.notification_widget.info.active:hover,
.open > .dropdown-toggle.notification_widget.info:hover,
.notification_widget.info:active:focus,
.notification_widget.info.active:focus,
.open > .dropdown-toggle.notification_widget.info:focus,
.notification_widget.info:active.focus,
.notification_widget.info.active.focus,
.open > .dropdown-toggle.notification_widget.info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  background-image: none;
}
.notification_widget.info.disabled:hover,
.notification_widget.info[disabled]:hover,
fieldset[disabled] .notification_widget.info:hover,
.notification_widget.info.disabled:focus,
.notification_widget.info[disabled]:focus,
fieldset[disabled] .notification_widget.info:focus,
.notification_widget.info.disabled.focus,
.notification_widget.info[disabled].focus,
fieldset[disabled] .notification_widget.info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.notification_widget.danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger:focus,
.notification_widget.danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.notification_widget.danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active:hover,
.notification_widget.danger.active:hover,
.open > .dropdown-toggle.notification_widget.danger:hover,
.notification_widget.danger:active:focus,
.notification_widget.danger.active:focus,
.open > .dropdown-toggle.notification_widget.danger:focus,
.notification_widget.danger:active.focus,
.notification_widget.danger.active.focus,
.open > .dropdown-toggle.notification_widget.danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  background-image: none;
}
.notification_widget.danger.disabled:hover,
.notification_widget.danger[disabled]:hover,
fieldset[disabled] .notification_widget.danger:hover,
.notification_widget.danger.disabled:focus,
.notification_widget.danger[disabled]:focus,
fieldset[disabled] .notification_widget.danger:focus,
.notification_widget.danger.disabled.focus,
.notification_widget.danger[disabled].focus,
fieldset[disabled] .notification_widget.danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger .badge {
  color: #d9534f;
  background-color: #fff;
}
div#pager {
  background-color: #fff;
  font-size: 14px;
  line-height: 20px;
  overflow: hidden;
  display: none;
  position: fixed;
  bottom: 0px;
  width: 100%;
  max-height: 50%;
  padding-top: 8px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  /* Display over codemirror */
  z-index: 100;
  /* Hack which prevents jquery ui resizable from changing top. */
  top: auto !important;
}
div#pager pre {
  line-height: 1.21429em;
  color: #000;
  background-color: #f7f7f7;
  padding: 0.4em;
}
div#pager #pager-button-area {
  position: absolute;
  top: 8px;
  right: 20px;
}
div#pager #pager-contents {
  position: relative;
  overflow: auto;
  width: 100%;
  height: 100%;
}
div#pager #pager-contents #pager-container {
  position: relative;
  padding: 15px 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
div#pager .ui-resizable-handle {
  top: 0px;
  height: 8px;
  background: #f7f7f7;
  border-top: 1px solid #cfcfcf;
  border-bottom: 1px solid #cfcfcf;
  /* This injects handle bars (a short, wide = symbol) for 
        the resize handle. */
}
div#pager .ui-resizable-handle::after {
  content: '';
  top: 2px;
  left: 50%;
  height: 3px;
  width: 30px;
  margin-left: -15px;
  position: absolute;
  border-top: 1px solid #cfcfcf;
}
.quickhelp {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  line-height: 1.8em;
}
.shortcut_key {
  display: inline-block;
  width: 21ex;
  text-align: right;
  font-family: monospace;
}
.shortcut_descr {
  display: inline-block;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
span.save_widget {
  margin-top: 6px;
}
span.save_widget span.filename {
  height: 1em;
  line-height: 1em;
  padding: 3px;
  margin-left: 16px;
  border: none;
  font-size: 146.5%;
  border-radius: 2px;
}
span.save_widget span.filename:hover {
  background-color: #e6e6e6;
}
span.checkpoint_status,
span.autosave_status {
  font-size: small;
}
@media (max-width: 767px) {
  span.save_widget {
    font-size: small;
  }
  span.checkpoint_status,
  span.autosave_status {
    display: none;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  span.checkpoint_status {
    display: none;
  }
  span.autosave_status {
    font-size: x-small;
  }
}
.toolbar {
  padding: 0px;
  margin-left: -5px;
  margin-top: 2px;
  margin-bottom: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.toolbar select,
.toolbar label {
  width: auto;
  vertical-align: middle;
  margin-right: 2px;
  margin-bottom: 0px;
  display: inline;
  font-size: 92%;
  margin-left: 0.3em;
  margin-right: 0.3em;
  padding: 0px;
  padding-top: 3px;
}
.toolbar .btn {
  padding: 2px 8px;
}
.toolbar .btn-group {
  margin-top: 0px;
  margin-left: 5px;
}
#maintoolbar {
  margin-bottom: -3px;
  margin-top: -8px;
  border: 0px;
  min-height: 27px;
  margin-left: 0px;
  padding-top: 11px;
  padding-bottom: 3px;
}
#maintoolbar .navbar-text {
  float: none;
  vertical-align: middle;
  text-align: right;
  margin-left: 5px;
  margin-right: 0px;
  margin-top: 0px;
}
.select-xs {
  height: 24px;
}
.pulse,
.dropdown-menu > li > a.pulse,
li.pulse > a.dropdown-toggle,
li.pulse.open > a.dropdown-toggle {
  background-color: #F37626;
  color: white;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
/** WARNING IF YOU ARE EDITTING THIS FILE, if this is a .css file, It has a lot
 * of chance of beeing generated from the ../less/[samename].less file, you can
 * try to get back the less file by reverting somme commit in history
 **/
/*
 * We'll try to get something pretty, so we
 * have some strange css to have the scroll bar on
 * the left with fix button on the top right of the tooltip
 */
@-moz-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-webkit-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-moz-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
@-webkit-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
/*properties of tooltip after "expand"*/
.bigtooltip {
  overflow: auto;
  height: 200px;
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
}
/*properties of tooltip before "expand"*/
.smalltooltip {
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
  text-overflow: ellipsis;
  overflow: hidden;
  height: 80px;
}
.tooltipbuttons {
  position: absolute;
  padding-right: 15px;
  top: 0px;
  right: 0px;
}
.tooltiptext {
  /*avoid the button to overlap on some docstring*/
  padding-right: 30px;
}
.ipython_tooltip {
  max-width: 700px;
  /*fade-in animation when inserted*/
  -webkit-animation: fadeOut 400ms;
  -moz-animation: fadeOut 400ms;
  animation: fadeOut 400ms;
  -webkit-animation: fadeIn 400ms;
  -moz-animation: fadeIn 400ms;
  animation: fadeIn 400ms;
  vertical-align: middle;
  background-color: #f7f7f7;
  overflow: visible;
  border: #ababab 1px solid;
  outline: none;
  padding: 3px;
  margin: 0px;
  padding-left: 7px;
  font-family: monospace;
  min-height: 50px;
  -moz-box-shadow: 0px 6px 10px -1px #adadad;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  border-radius: 2px;
  position: absolute;
  z-index: 1000;
}
.ipython_tooltip a {
  float: right;
}
.ipython_tooltip .tooltiptext pre {
  border: 0;
  border-radius: 0;
  font-size: 100%;
  background-color: #f7f7f7;
}
.pretooltiparrow {
  left: 0px;
  margin: 0px;
  top: -16px;
  width: 40px;
  height: 16px;
  overflow: hidden;
  position: absolute;
}
.pretooltiparrow:before {
  background-color: #f7f7f7;
  border: 1px #ababab solid;
  z-index: 11;
  content: "";
  position: absolute;
  left: 15px;
  top: 10px;
  width: 25px;
  height: 25px;
  -webkit-transform: rotate(45deg);
  -moz-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  -o-transform: rotate(45deg);
}
ul.typeahead-list i {
  margin-left: -10px;
  width: 18px;
}
ul.typeahead-list {
  max-height: 80vh;
  overflow: auto;
}
ul.typeahead-list > li > a {
  /** Firefox bug **/
  /* see https://github.com/jupyter/notebook/issues/559 */
  white-space: normal;
}
.cmd-palette .modal-body {
  padding: 7px;
}
.cmd-palette form {
  background: white;
}
.cmd-palette input {
  outline: none;
}
.no-shortcut {
  display: none;
}
.command-shortcut:before {
  content: "(command)";
  padding-right: 3px;
  color: #777777;
}
.edit-shortcut:before {
  content: "(edit)";
  padding-right: 3px;
  color: #777777;
}
#find-and-replace #replace-preview .match,
#find-and-replace #replace-preview .insert {
  background-color: #BBDEFB;
  border-color: #90CAF9;
  border-style: solid;
  border-width: 1px;
  border-radius: 0px;
}
#find-and-replace #replace-preview .replace .match {
  background-color: #FFCDD2;
  border-color: #EF9A9A;
  border-radius: 0px;
}
#find-and-replace #replace-preview .replace .insert {
  background-color: #C8E6C9;
  border-color: #A5D6A7;
  border-radius: 0px;
}
#find-and-replace #replace-preview {
  max-height: 60vh;
  overflow: auto;
}
#find-and-replace #replace-preview pre {
  padding: 5px 10px;
}
.terminal-app {
  background: #EEE;
}
.terminal-app #header {
  background: #fff;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.terminal-app .terminal {
  width: 100%;
  float: left;
  font-family: monospace;
  color: white;
  background: black;
  padding: 0.4em;
  border-radius: 2px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
}
.terminal-app .terminal,
.terminal-app .terminal dummy-screen {
  line-height: 1em;
  font-size: 14px;
}
.terminal-app .terminal .xterm-rows {
  padding: 10px;
}
.terminal-app .terminal-cursor {
  color: black;
  background: white;
}
.terminal-app #terminado-container {
  margin-top: 20px;
}
/*# sourceMappingURL=style.min.css.map */
    </style>
<style type="text/css">
    .highlight .hll { background-color: #ffffcc }
.highlight  { background: #f8f8f8; }
.highlight .c { color: #408080; font-style: italic } /* Comment */
.highlight .err { border: 1px solid #FF0000 } /* Error */
.highlight .k { color: #008000; font-weight: bold } /* Keyword */
.highlight .o { color: #666666 } /* Operator */
.highlight .ch { color: #408080; font-style: italic } /* Comment.Hashbang */
.highlight .cm { color: #408080; font-style: italic } /* Comment.Multiline */
.highlight .cp { color: #BC7A00 } /* Comment.Preproc */
.highlight .cpf { color: #408080; font-style: italic } /* Comment.PreprocFile */
.highlight .c1 { color: #408080; font-style: italic } /* Comment.Single */
.highlight .cs { color: #408080; font-style: italic } /* Comment.Special */
.highlight .gd { color: #A00000 } /* Generic.Deleted */
.highlight .ge { font-style: italic } /* Generic.Emph */
.highlight .gr { color: #FF0000 } /* Generic.Error */
.highlight .gh { color: #000080; font-weight: bold } /* Generic.Heading */
.highlight .gi { color: #00A000 } /* Generic.Inserted */
.highlight .go { color: #888888 } /* Generic.Output */
.highlight .gp { color: #000080; font-weight: bold } /* Generic.Prompt */
.highlight .gs { font-weight: bold } /* Generic.Strong */
.highlight .gu { color: #800080; font-weight: bold } /* Generic.Subheading */
.highlight .gt { color: #0044DD } /* Generic.Traceback */
.highlight .kc { color: #008000; font-weight: bold } /* Keyword.Constant */
.highlight .kd { color: #008000; font-weight: bold } /* Keyword.Declaration */
.highlight .kn { color: #008000; font-weight: bold } /* Keyword.Namespace */
.highlight .kp { color: #008000 } /* Keyword.Pseudo */
.highlight .kr { color: #008000; font-weight: bold } /* Keyword.Reserved */
.highlight .kt { color: #B00040 } /* Keyword.Type */
.highlight .m { color: #666666 } /* Literal.Number */
.highlight .s { color: #BA2121 } /* Literal.String */
.highlight .na { color: #7D9029 } /* Name.Attribute */
.highlight .nb { color: #008000 } /* Name.Builtin */
.highlight .nc { color: #0000FF; font-weight: bold } /* Name.Class */
.highlight .no { color: #880000 } /* Name.Constant */
.highlight .nd { color: #AA22FF } /* Name.Decorator */
.highlight .ni { color: #999999; font-weight: bold } /* Name.Entity */
.highlight .ne { color: #D2413A; font-weight: bold } /* Name.Exception */
.highlight .nf { color: #0000FF } /* Name.Function */
.highlight .nl { color: #A0A000 } /* Name.Label */
.highlight .nn { color: #0000FF; font-weight: bold } /* Name.Namespace */
.highlight .nt { color: #008000; font-weight: bold } /* Name.Tag */
.highlight .nv { color: #19177C } /* Name.Variable */
.highlight .ow { color: #AA22FF; font-weight: bold } /* Operator.Word */
.highlight .w { color: #bbbbbb } /* Text.Whitespace */
.highlight .mb { color: #666666 } /* Literal.Number.Bin */
.highlight .mf { color: #666666 } /* Literal.Number.Float */
.highlight .mh { color: #666666 } /* Literal.Number.Hex */
.highlight .mi { color: #666666 } /* Literal.Number.Integer */
.highlight .mo { color: #666666 } /* Literal.Number.Oct */
.highlight .sa { color: #BA2121 } /* Literal.String.Affix */
.highlight .sb { color: #BA2121 } /* Literal.String.Backtick */
.highlight .sc { color: #BA2121 } /* Literal.String.Char */
.highlight .dl { color: #BA2121 } /* Literal.String.Delimiter */
.highlight .sd { color: #BA2121; font-style: italic } /* Literal.String.Doc */
.highlight .s2 { color: #BA2121 } /* Literal.String.Double */
.highlight .se { color: #BB6622; font-weight: bold } /* Literal.String.Escape */
.highlight .sh { color: #BA2121 } /* Literal.String.Heredoc */
.highlight .si { color: #BB6688; font-weight: bold } /* Literal.String.Interpol */
.highlight .sx { color: #008000 } /* Literal.String.Other */
.highlight .sr { color: #BB6688 } /* Literal.String.Regex */
.highlight .s1 { color: #BA2121 } /* Literal.String.Single */
.highlight .ss { color: #19177C } /* Literal.String.Symbol */
.highlight .bp { color: #008000 } /* Name.Builtin.Pseudo */
.highlight .fm { color: #0000FF } /* Name.Function.Magic */
.highlight .vc { color: #19177C } /* Name.Variable.Class */
.highlight .vg { color: #19177C } /* Name.Variable.Global */
.highlight .vi { color: #19177C } /* Name.Variable.Instance */
.highlight .vm { color: #19177C } /* Name.Variable.Magic */
.highlight .il { color: #666666 } /* Literal.Number.Integer.Long */
    </style>
<style type="text/css">
    
/* Temporary definitions which will become obsolete with Notebook release 5.0 */
.ansi-black-fg { color: #3E424D; }
.ansi-black-bg { background-color: #3E424D; }
.ansi-black-intense-fg { color: #282C36; }
.ansi-black-intense-bg { background-color: #282C36; }
.ansi-red-fg { color: #E75C58; }
.ansi-red-bg { background-color: #E75C58; }
.ansi-red-intense-fg { color: #B22B31; }
.ansi-red-intense-bg { background-color: #B22B31; }
.ansi-green-fg { color: #00A250; }
.ansi-green-bg { background-color: #00A250; }
.ansi-green-intense-fg { color: #007427; }
.ansi-green-intense-bg { background-color: #007427; }
.ansi-yellow-fg { color: #DDB62B; }
.ansi-yellow-bg { background-color: #DDB62B; }
.ansi-yellow-intense-fg { color: #B27D12; }
.ansi-yellow-intense-bg { background-color: #B27D12; }
.ansi-blue-fg { color: #208FFB; }
.ansi-blue-bg { background-color: #208FFB; }
.ansi-blue-intense-fg { color: #0065CA; }
.ansi-blue-intense-bg { background-color: #0065CA; }
.ansi-magenta-fg { color: #D160C4; }
.ansi-magenta-bg { background-color: #D160C4; }
.ansi-magenta-intense-fg { color: #A03196; }
.ansi-magenta-intense-bg { background-color: #A03196; }
.ansi-cyan-fg { color: #60C6C8; }
.ansi-cyan-bg { background-color: #60C6C8; }
.ansi-cyan-intense-fg { color: #258F8F; }
.ansi-cyan-intense-bg { background-color: #258F8F; }
.ansi-white-fg { color: #C5C1B4; }
.ansi-white-bg { background-color: #C5C1B4; }
.ansi-white-intense-fg { color: #A1A6B2; }
.ansi-white-intense-bg { background-color: #A1A6B2; }

.ansi-bold { font-weight: bold; }

    </style>


<style type="text/css">
/* Overrides of notebook CSS for static HTML export */
body {
  overflow: visible;
  padding: 8px;
}

div#notebook {
  overflow: visible;
  border-top: none;
}

@media print {
  div.cell {
    display: block;
    page-break-inside: avoid;
  } 
  div.output_wrapper { 
    display: block;
    page-break-inside: avoid; 
  }
  div.output { 
    display: block;
    page-break-inside: avoid; 
  }
}
</style>

<!-- Custom stylesheet, it must be in the same directory as the html file -->
<link rel="stylesheet" href="custom.css">

<!-- Loading mathjax macro -->
<!-- Load mathjax -->
    <script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS_HTML"></script>
    <!-- MathJax configuration -->
    <script type="text/x-mathjax-config">
    MathJax.Hub.Config({
        tex2jax: {
            inlineMath: [ ['$','$'], ["\\(","\\)"] ],
            displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
            processEscapes: true,
            processEnvironments: true
        },
        // Center justify equations in code and markdown cells. Elsewhere
        // we use CSS to left justify single line equations in code cells.
        displayAlign: 'center',
        "HTML-CSS": {
            styles: {'.MathJax_Display': {"margin": 0}},
            linebreaks: { automatic: true }
        }
    });
    </script>
    <!-- End of mathjax configuration --></head>
<body>
  <div tabindex="-1" id="notebook" class="border-box-sizing">
    <div class="container" id="notebook-container">

<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1><center>Tomography with TomoPy &amp; Astra Toolbox</h1>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[1]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">tomopy</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">import</span> <span class="nn">astra</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="kn">from</span> <span class="nn">skimage.transform</span> <span class="k">import</span> <span class="n">radon</span><span class="p">,</span> <span class="n">iradon</span>

<span class="o">%</span><span class="k">matplotlib</span> inline
<span class="o">%</span><span class="k">config</span> InlineBackend.figure_format = &#39;svg&#39;
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="-Shepp&#8211;Logan-Phantom-"><center> Shepp&#8211;Logan Phantom </center><a class="anchor-link" href="#-Shepp&#8211;Logan-Phantom-">&#182;</a></h3><p>The Shepp–Logan phantom is a standard test image created by Larry Shepp and Benjamin F. Logan for their 1974 paper The Fourier Reconstruction of a Head Section. It serves as the model of a human head in the development and testing of image reconstruction algorithms</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[2]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">phantom2d</span> <span class="o">=</span> <span class="n">tomopy</span><span class="o">.</span><span class="n">misc</span><span class="o">.</span><span class="n">phantom</span><span class="o">.</span><span class="n">shepp2d</span><span class="p">()</span><span class="o">.</span><span class="n">squeeze</span><span class="p">()</span>
<span class="n">phantom3d</span> <span class="o">=</span> <span class="n">tomopy</span><span class="o">.</span><span class="n">misc</span><span class="o">.</span><span class="n">phantom</span><span class="o">.</span><span class="n">shepp3d</span><span class="p">()</span>

<span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">121</span><span class="p">);</span> <span class="n">plt</span><span class="o">.</span><span class="n">imshow</span><span class="p">(</span><span class="n">phantom2d</span><span class="p">,</span> <span class="n">cmap</span><span class="o">=</span><span class="s1">&#39;gray&#39;</span><span class="p">);</span>
<span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">122</span><span class="p">);</span> <span class="n">plt</span><span class="o">.</span><span class="n">imshow</span><span class="p">(</span><span class="n">phantom3d</span><span class="p">[</span><span class="mi">64</span><span class="p">,:,:],</span> <span class="n">cmap</span><span class="o">=</span><span class="s1">&#39;gray&#39;</span><span class="p">);</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt"></div>


<div class="output_svg output_subarea ">
<?xml version="1.0" encoding="utf-8" standalone="no"?>

<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN"

  "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">

<!-- Created with matplotlib (https://matplotlib.org/) -->

<svg height="186.910547pt" version="1.1" viewBox="0 0 378.7875 186.910547" width="378.7875pt" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">

 <defs>

  <style type="text/css">

*{stroke-linecap:butt;stroke-linejoin:round;}

  </style>

 </defs>

 <g id="figure_1">

  <g id="patch_1">

   <path d="M 0 186.910547 

L 378.7875 186.910547 

L 378.7875 0 

L 0 0 

z

" style="fill:none;"/>

  </g>

  <g id="axes_1">

   <g id="patch_2">

    <path d="M 33.2875 163.032422 

L 185.469318 163.032422 

L 185.469318 10.850604 

L 33.2875 10.850604 

z

" style="fill:#ffffff;"/>

   </g>

   <g clip-path="url(#p777f05ed8a)">

    <image height="153" id="imagec7294525f4" transform="scale(1 -1)translate(0 -153)" width="153" x="33.2875" xlink:href="data:image/png;base64,

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" y="-10.032422"/>

   </g>

   <g id="matplotlib.axis_1">

    <g id="xtick_1">

     <g id="line2d_1">

      <defs>

       <path d="M 0 0 

L 0 3.5 

" id="medafac6004" style="stroke:#000000;stroke-width:0.8;"/>

      </defs>

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.436115" xlink:href="#medafac6004" y="163.032422"/>

      </g>

     </g>

     <g id="text_1">

      <!-- 0 -->

      <defs>

       <path d="M 31.78125 66.40625 

Q 24.171875 66.40625 20.328125 58.90625 

Q 16.5 51.421875 16.5 36.375 

Q 16.5 21.390625 20.328125 13.890625 

Q 24.171875 6.390625 31.78125 6.390625 

Q 39.453125 6.390625 43.28125 13.890625 

Q 47.125 21.390625 47.125 36.375 

Q 47.125 51.421875 43.28125 58.90625 

Q 39.453125 66.40625 31.78125 66.40625 

z

M 31.78125 74.21875 

Q 44.046875 74.21875 50.515625 64.515625 

Q 56.984375 54.828125 56.984375 36.375 

Q 56.984375 17.96875 50.515625 8.265625 

Q 44.046875 -1.421875 31.78125 -1.421875 

Q 19.53125 -1.421875 13.0625 8.265625 

Q 6.59375 17.96875 6.59375 36.375 

Q 6.59375 54.828125 13.0625 64.515625 

Q 19.53125 74.21875 31.78125 74.21875 

z

" id="DejaVuSans-48"/>

      </defs>

      <g transform="translate(30.254865 177.630859)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_2">

     <g id="line2d_2">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="92.882138" xlink:href="#medafac6004" y="163.032422"/>

      </g>

     </g>

     <g id="text_2">

      <!-- 200 -->

      <defs>

       <path d="M 19.1875 8.296875 

L 53.609375 8.296875 

L 53.609375 0 

L 7.328125 0 

L 7.328125 8.296875 

Q 12.9375 14.109375 22.625 23.890625 

Q 32.328125 33.6875 34.8125 36.53125 

Q 39.546875 41.84375 41.421875 45.53125 

Q 43.3125 49.21875 43.3125 52.78125 

Q 43.3125 58.59375 39.234375 62.25 

Q 35.15625 65.921875 28.609375 65.921875 

Q 23.96875 65.921875 18.8125 64.3125 

Q 13.671875 62.703125 7.8125 59.421875 

L 7.8125 69.390625 

Q 13.765625 71.78125 18.9375 73 

Q 24.125 74.21875 28.421875 74.21875 

Q 39.75 74.21875 46.484375 68.546875 

Q 53.21875 62.890625 53.21875 53.421875 

Q 53.21875 48.921875 51.53125 44.890625 

Q 49.859375 40.875 45.40625 35.40625 

Q 44.1875 33.984375 37.640625 27.21875 

Q 31.109375 20.453125 19.1875 8.296875 

z

" id="DejaVuSans-50"/>

      </defs>

      <g transform="translate(83.338388 177.630859)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-50"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_3">

     <g id="line2d_3">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="152.328161" xlink:href="#medafac6004" y="163.032422"/>

      </g>

     </g>

     <g id="text_3">

      <!-- 400 -->

      <defs>

       <path d="M 37.796875 64.3125 

L 12.890625 25.390625 

L 37.796875 25.390625 

z

M 35.203125 72.90625 

L 47.609375 72.90625 

L 47.609375 25.390625 

L 58.015625 25.390625 

L 58.015625 17.1875 

L 47.609375 17.1875 

L 47.609375 0 

L 37.796875 0 

L 37.796875 17.1875 

L 4.890625 17.1875 

L 4.890625 26.703125 

z

" id="DejaVuSans-52"/>

      </defs>

      <g transform="translate(142.784411 177.630859)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-52"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

   </g>

   <g id="matplotlib.axis_2">

    <g id="ytick_1">

     <g id="line2d_4">

      <defs>

       <path d="M 0 0 

L -3.5 0 

" id="meb6c022222" style="stroke:#000000;stroke-width:0.8;"/>

      </defs>

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#meb6c022222" y="10.999219"/>

      </g>

     </g>

     <g id="text_4">

      <!-- 0 -->

      <g transform="translate(19.925 14.798437)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_2">

     <g id="line2d_5">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#meb6c022222" y="40.72223"/>

      </g>

     </g>

     <g id="text_5">

      <!-- 100 -->

      <defs>

       <path d="M 12.40625 8.296875 

L 28.515625 8.296875 

L 28.515625 63.921875 

L 10.984375 60.40625 

L 10.984375 69.390625 

L 28.421875 72.90625 

L 38.28125 72.90625 

L 38.28125 8.296875 

L 54.390625 8.296875 

L 54.390625 0 

L 12.40625 0 

z

" id="DejaVuSans-49"/>

      </defs>

      <g transform="translate(7.2 44.521449)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_3">

     <g id="line2d_6">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#meb6c022222" y="70.445241"/>

      </g>

     </g>

     <g id="text_6">

      <!-- 200 -->

      <g transform="translate(7.2 74.24446)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-50"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_4">

     <g id="line2d_7">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#meb6c022222" y="100.168253"/>

      </g>

     </g>

     <g id="text_7">

      <!-- 300 -->

      <defs>

       <path d="M 40.578125 39.3125 

Q 47.65625 37.796875 51.625 33 

Q 55.609375 28.21875 55.609375 21.1875 

Q 55.609375 10.40625 48.1875 4.484375 

Q 40.765625 -1.421875 27.09375 -1.421875 

Q 22.515625 -1.421875 17.65625 -0.515625 

Q 12.796875 0.390625 7.625 2.203125 

L 7.625 11.71875 

Q 11.71875 9.328125 16.59375 8.109375 

Q 21.484375 6.890625 26.8125 6.890625 

Q 36.078125 6.890625 40.9375 10.546875 

Q 45.796875 14.203125 45.796875 21.1875 

Q 45.796875 27.640625 41.28125 31.265625 

Q 36.765625 34.90625 28.71875 34.90625 

L 20.21875 34.90625 

L 20.21875 43.015625 

L 29.109375 43.015625 

Q 36.375 43.015625 40.234375 45.921875 

Q 44.09375 48.828125 44.09375 54.296875 

Q 44.09375 59.90625 40.109375 62.90625 

Q 36.140625 65.921875 28.71875 65.921875 

Q 24.65625 65.921875 20.015625 65.03125 

Q 15.375 64.15625 9.8125 62.3125 

L 9.8125 71.09375 

Q 15.4375 72.65625 20.34375 73.4375 

Q 25.25 74.21875 29.59375 74.21875 

Q 40.828125 74.21875 47.359375 69.109375 

Q 53.90625 64.015625 53.90625 55.328125 

Q 53.90625 49.265625 50.4375 45.09375 

Q 46.96875 40.921875 40.578125 39.3125 

z

" id="DejaVuSans-51"/>

      </defs>

      <g transform="translate(7.2 103.967472)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-51"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_5">

     <g id="line2d_8">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#meb6c022222" y="129.891264"/>

      </g>

     </g>

     <g id="text_8">

      <!-- 400 -->

      <g transform="translate(7.2 133.690483)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-52"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_6">

     <g id="line2d_9">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#meb6c022222" y="159.614276"/>

      </g>

     </g>

     <g id="text_9">

      <!-- 500 -->

      <defs>

       <path d="M 10.796875 72.90625 

L 49.515625 72.90625 

L 49.515625 64.59375 

L 19.828125 64.59375 

L 19.828125 46.734375 

Q 21.96875 47.46875 24.109375 47.828125 

Q 26.265625 48.1875 28.421875 48.1875 

Q 40.625 48.1875 47.75 41.5 

Q 54.890625 34.8125 54.890625 23.390625 

Q 54.890625 11.625 47.5625 5.09375 

Q 40.234375 -1.421875 26.90625 -1.421875 

Q 22.3125 -1.421875 17.546875 -0.640625 

Q 12.796875 0.140625 7.71875 1.703125 

L 7.71875 11.625 

Q 12.109375 9.234375 16.796875 8.0625 

Q 21.484375 6.890625 26.703125 6.890625 

Q 35.15625 6.890625 40.078125 11.328125 

Q 45.015625 15.765625 45.015625 23.390625 

Q 45.015625 31 40.078125 35.4375 

Q 35.15625 39.890625 26.703125 39.890625 

Q 22.75 39.890625 18.8125 39.015625 

Q 14.890625 38.140625 10.796875 36.28125 

z

" id="DejaVuSans-53"/>

      </defs>

      <g transform="translate(7.2 163.413494)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-53"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

   </g>

   <g id="patch_3">

    <path d="M 33.2875 163.032422 

L 33.2875 10.850604 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_4">

    <path d="M 185.469318 163.032422 

L 185.469318 10.850604 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_5">

    <path d="M 33.2875 163.032422 

L 185.469318 163.032422 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_6">

    <path d="M 33.2875 10.850604 

L 185.469318 10.850604 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

  </g>

  <g id="axes_2">

   <g id="patch_7">

    <path d="M 215.905682 163.032422 

L 368.0875 163.032422 

L 368.0875 10.850604 

L 215.905682 10.850604 

z

" style="fill:#ffffff;"/>

   </g>

   <g clip-path="url(#p900d5404d4)">

    <image height="153" id="image4b342b2f9f" transform="scale(1 -1)translate(0 -153)" width="153" x="215.905682" xlink:href="data:image/png;base64,

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" y="-10.032422"/>

   </g>

   <g id="matplotlib.axis_3">

    <g id="xtick_4">

     <g id="line2d_10">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="216.500142" xlink:href="#medafac6004" y="163.032422"/>

      </g>

     </g>

     <g id="text_10">

      <!-- 0 -->

      <g transform="translate(213.318892 177.630859)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_5">

     <g id="line2d_11">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="275.946165" xlink:href="#medafac6004" y="163.032422"/>

      </g>

     </g>

     <g id="text_11">

      <!-- 50 -->

      <g transform="translate(269.583665 177.630859)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-53"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_6">

     <g id="line2d_12">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="335.392187" xlink:href="#medafac6004" y="163.032422"/>

      </g>

     </g>

     <g id="text_12">

      <!-- 100 -->

      <g transform="translate(325.848437 177.630859)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

   </g>

   <g id="matplotlib.axis_4">

    <g id="ytick_7">

     <g id="line2d_13">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="215.905682" xlink:href="#meb6c022222" y="11.445064"/>

      </g>

     </g>

     <g id="text_13">

      <!-- 0 -->

      <g transform="translate(202.543182 15.244283)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_8">

     <g id="line2d_14">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="215.905682" xlink:href="#meb6c022222" y="35.223473"/>

      </g>

     </g>

     <g id="text_14">

      <!-- 20 -->

      <g transform="translate(196.180682 39.022692)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-50"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_9">

     <g id="line2d_15">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="215.905682" xlink:href="#meb6c022222" y="59.001882"/>

      </g>

     </g>

     <g id="text_15">

      <!-- 40 -->

      <g transform="translate(196.180682 62.801101)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-52"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_10">

     <g id="line2d_16">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="215.905682" xlink:href="#meb6c022222" y="82.780291"/>

      </g>

     </g>

     <g id="text_16">

      <!-- 60 -->

      <defs>

       <path d="M 33.015625 40.375 

Q 26.375 40.375 22.484375 35.828125 

Q 18.609375 31.296875 18.609375 23.390625 

Q 18.609375 15.53125 22.484375 10.953125 

Q 26.375 6.390625 33.015625 6.390625 

Q 39.65625 6.390625 43.53125 10.953125 

Q 47.40625 15.53125 47.40625 23.390625 

Q 47.40625 31.296875 43.53125 35.828125 

Q 39.65625 40.375 33.015625 40.375 

z

M 52.59375 71.296875 

L 52.59375 62.3125 

Q 48.875 64.0625 45.09375 64.984375 

Q 41.3125 65.921875 37.59375 65.921875 

Q 27.828125 65.921875 22.671875 59.328125 

Q 17.53125 52.734375 16.796875 39.40625 

Q 19.671875 43.65625 24.015625 45.921875 

Q 28.375 48.1875 33.59375 48.1875 

Q 44.578125 48.1875 50.953125 41.515625 

Q 57.328125 34.859375 57.328125 23.390625 

Q 57.328125 12.15625 50.6875 5.359375 

Q 44.046875 -1.421875 33.015625 -1.421875 

Q 20.359375 -1.421875 13.671875 8.265625 

Q 6.984375 17.96875 6.984375 36.375 

Q 6.984375 53.65625 15.1875 63.9375 

Q 23.390625 74.21875 37.203125 74.21875 

Q 40.921875 74.21875 44.703125 73.484375 

Q 48.484375 72.75 52.59375 71.296875 

z

" id="DejaVuSans-54"/>

      </defs>

      <g transform="translate(196.180682 86.57951)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-54"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_11">

     <g id="line2d_17">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="215.905682" xlink:href="#meb6c022222" y="106.5587"/>

      </g>

     </g>

     <g id="text_17">

      <!-- 80 -->

      <defs>

       <path d="M 31.78125 34.625 

Q 24.75 34.625 20.71875 30.859375 

Q 16.703125 27.09375 16.703125 20.515625 

Q 16.703125 13.921875 20.71875 10.15625 

Q 24.75 6.390625 31.78125 6.390625 

Q 38.8125 6.390625 42.859375 10.171875 

Q 46.921875 13.96875 46.921875 20.515625 

Q 46.921875 27.09375 42.890625 30.859375 

Q 38.875 34.625 31.78125 34.625 

z

M 21.921875 38.8125 

Q 15.578125 40.375 12.03125 44.71875 

Q 8.5 49.078125 8.5 55.328125 

Q 8.5 64.0625 14.71875 69.140625 

Q 20.953125 74.21875 31.78125 74.21875 

Q 42.671875 74.21875 48.875 69.140625 

Q 55.078125 64.0625 55.078125 55.328125 

Q 55.078125 49.078125 51.53125 44.71875 

Q 48 40.375 41.703125 38.8125 

Q 48.828125 37.15625 52.796875 32.3125 

Q 56.78125 27.484375 56.78125 20.515625 

Q 56.78125 9.90625 50.3125 4.234375 

Q 43.84375 -1.421875 31.78125 -1.421875 

Q 19.734375 -1.421875 13.25 4.234375 

Q 6.78125 9.90625 6.78125 20.515625 

Q 6.78125 27.484375 10.78125 32.3125 

Q 14.796875 37.15625 21.921875 38.8125 

z

M 18.3125 54.390625 

Q 18.3125 48.734375 21.84375 45.5625 

Q 25.390625 42.390625 31.78125 42.390625 

Q 38.140625 42.390625 41.71875 45.5625 

Q 45.3125 48.734375 45.3125 54.390625 

Q 45.3125 60.0625 41.71875 63.234375 

Q 38.140625 66.40625 31.78125 66.40625 

Q 25.390625 66.40625 21.84375 63.234375 

Q 18.3125 60.0625 18.3125 54.390625 

z

" id="DejaVuSans-56"/>

      </defs>

      <g transform="translate(196.180682 110.357919)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-56"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_12">

     <g id="line2d_18">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="215.905682" xlink:href="#meb6c022222" y="130.337109"/>

      </g>

     </g>

     <g id="text_18">

      <!-- 100 -->

      <g transform="translate(189.818182 134.136328)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_13">

     <g id="line2d_19">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="215.905682" xlink:href="#meb6c022222" y="154.115518"/>

      </g>

     </g>

     <g id="text_19">

      <!-- 120 -->

      <g transform="translate(189.818182 157.914737)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-50"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

   </g>

   <g id="patch_8">

    <path d="M 215.905682 163.032422 

L 215.905682 10.850604 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_9">

    <path d="M 368.0875 163.032422 

L 368.0875 10.850604 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_10">

    <path d="M 215.905682 163.032422 

L 368.0875 163.032422 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_11">

    <path d="M 215.905682 10.850604 

L 368.0875 10.850604 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

  </g>

 </g>

 <defs>

  <clipPath id="p777f05ed8a">

   <rect height="152.181818" width="152.181818" x="33.2875" y="10.850604"/>

  </clipPath>

  <clipPath id="p900d5404d4">

   <rect height="152.181818" width="152.181818" x="215.905682" y="10.850604"/>

  </clipPath>

 </defs>

</svg>


</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="-Radon-Transform-"><center> Radon Transform </center><a class="anchor-link" href="#-Radon-Transform-">&#182;</a></h3><p><img src='Radon_transform.png' width=30% align='left'>
$$R(L) = \int_L f(\mathbf{x})\,|d\mathbf{x}|.$$
Concretely, the parametrization of any straight line $L$ with respect to arc length $z$ can always be written
$$(x(z),y(z)) = \Big( (s\cos\alpha - z\sin\alpha), (s\sin\alpha+z\cos\alpha)  \Big) \,$$
where $s$ is the distance of $L$ from the origin and $\alpha$ is the angle the normal vector to $L$ makes with the $x$ axis.  It follows that the quantities $(\alpha, s)$  can be considered as coordinates on the space of all lines in $R$<sup>2</sup>, and the Radon transform can be expressed in these coordinates by
$$\begin{align}R(\alpha,s) &= \int_{-\infty}^{\infty} f(x(z),y(z))\, dz\\ &= \int_{-\infty}^{\infty} f\big(  (s\cos\alpha - z\sin\alpha), (s\sin\alpha+z\cos\alpha) \big)\, dz\end{align}$$</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[3]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># 2D</span>
<span class="n">theta2d</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">linspace</span><span class="p">(</span><span class="mf">0.</span><span class="p">,</span> <span class="mf">180.</span><span class="p">,</span> <span class="nb">max</span><span class="p">(</span><span class="n">phantom2d</span><span class="o">.</span><span class="n">shape</span><span class="p">),</span> <span class="n">endpoint</span><span class="o">=</span><span class="kc">False</span><span class="p">)</span>
<span class="n">sinogram2d</span> <span class="o">=</span> <span class="n">radon</span><span class="p">(</span><span class="n">phantom2d</span><span class="p">,</span> <span class="n">theta</span><span class="o">=</span><span class="n">theta2d</span><span class="p">,</span> <span class="n">circle</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>

<span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">8</span><span class="p">,</span> <span class="mf">4.5</span><span class="p">));</span>
<span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">121</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s2">&quot;Original&quot;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">imshow</span><span class="p">(</span><span class="n">phantom2d</span><span class="p">,</span> <span class="n">cmap</span><span class="o">=</span><span class="s1">&#39;gray&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">122</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">imshow</span><span class="p">(</span><span class="n">sinogram2d</span><span class="p">,</span> <span class="n">cmap</span><span class="o">=</span><span class="s1">&#39;gray&#39;</span><span class="p">,</span>
           <span class="n">extent</span><span class="o">=</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="mi">180</span><span class="p">,</span> <span class="mi">0</span><span class="p">,</span> <span class="n">sinogram2d</span><span class="o">.</span><span class="n">shape</span><span class="p">[</span><span class="mi">0</span><span class="p">]),</span> <span class="n">aspect</span><span class="o">=</span><span class="s1">&#39;auto&#39;</span><span class="p">);</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;Radon transform</span><span class="se">\n</span><span class="s1">(Sinogram)&#39;</span><span class="p">);</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s2">&quot;Projection angle (deg)&quot;</span><span class="p">);</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s2">&quot;Projection position (pixels)&quot;</span><span class="p">);</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt"></div>


<div class="output_svg output_subarea ">
<?xml version="1.0" encoding="utf-8" standalone="no"?>

<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN"

  "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">

<!-- Created with matplotlib (https://matplotlib.org/) -->

<svg height="317.93175pt" version="1.1" viewBox="0 0 490.3875 317.93175" width="490.3875pt" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">

 <defs>

  <style type="text/css">

*{stroke-linecap:butt;stroke-linejoin:round;}

  </style>

 </defs>

 <g id="figure_1">

  <g id="patch_1">

   <path d="M 0 317.93175 

L 490.3875 317.93175 

L 490.3875 0 

L 0 0 

z

" style="fill:none;"/>

  </g>

  <g id="axes_1">

   <g id="patch_2">

    <path d="M 33.2875 259.520045 

L 236.196591 259.520045 

L 236.196591 56.610955 

L 33.2875 56.610955 

z

" style="fill:#ffffff;"/>

   </g>

   <g clip-path="url(#pcb845ba5ce)">

    <image height="203" id="image2e94fcf298" transform="scale(1 -1)translate(0 -203)" width="203" x="33.2875" xlink:href="data:image/png;base64,

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" y="-56.520045"/>

   </g>

   <g id="matplotlib.axis_1">

    <g id="xtick_1">

     <g id="line2d_1">

      <defs>

       <path d="M 0 0 

L 0 3.5 

" id="m8736a96668" style="stroke:#000000;stroke-width:0.8;"/>

      </defs>

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.485653" xlink:href="#m8736a96668" y="259.520045"/>

      </g>

     </g>

     <g id="text_1">

      <!-- 0 -->

      <defs>

       <path d="M 31.78125 66.40625 

Q 24.171875 66.40625 20.328125 58.90625 

Q 16.5 51.421875 16.5 36.375 

Q 16.5 21.390625 20.328125 13.890625 

Q 24.171875 6.390625 31.78125 6.390625 

Q 39.453125 6.390625 43.28125 13.890625 

Q 47.125 21.390625 47.125 36.375 

Q 47.125 51.421875 43.28125 58.90625 

Q 39.453125 66.40625 31.78125 66.40625 

z

M 31.78125 74.21875 

Q 44.046875 74.21875 50.515625 64.515625 

Q 56.984375 54.828125 56.984375 36.375 

Q 56.984375 17.96875 50.515625 8.265625 

Q 44.046875 -1.421875 31.78125 -1.421875 

Q 19.53125 -1.421875 13.0625 8.265625 

Q 6.59375 17.96875 6.59375 36.375 

Q 6.59375 54.828125 13.0625 64.515625 

Q 19.53125 74.21875 31.78125 74.21875 

z

" id="DejaVuSans-48"/>

      </defs>

      <g transform="translate(30.304403 274.118483)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_2">

     <g id="line2d_2">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="73.116335" xlink:href="#m8736a96668" y="259.520045"/>

      </g>

     </g>

     <g id="text_2">

      <!-- 100 -->

      <defs>

       <path d="M 12.40625 8.296875 

L 28.515625 8.296875 

L 28.515625 63.921875 

L 10.984375 60.40625 

L 10.984375 69.390625 

L 28.421875 72.90625 

L 38.28125 72.90625 

L 38.28125 8.296875 

L 54.390625 8.296875 

L 54.390625 0 

L 12.40625 0 

z

" id="DejaVuSans-49"/>

      </defs>

      <g transform="translate(63.572585 274.118483)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_3">

     <g id="line2d_3">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="112.747017" xlink:href="#m8736a96668" y="259.520045"/>

      </g>

     </g>

     <g id="text_3">

      <!-- 200 -->

      <defs>

       <path d="M 19.1875 8.296875 

L 53.609375 8.296875 

L 53.609375 0 

L 7.328125 0 

L 7.328125 8.296875 

Q 12.9375 14.109375 22.625 23.890625 

Q 32.328125 33.6875 34.8125 36.53125 

Q 39.546875 41.84375 41.421875 45.53125 

Q 43.3125 49.21875 43.3125 52.78125 

Q 43.3125 58.59375 39.234375 62.25 

Q 35.15625 65.921875 28.609375 65.921875 

Q 23.96875 65.921875 18.8125 64.3125 

Q 13.671875 62.703125 7.8125 59.421875 

L 7.8125 69.390625 

Q 13.765625 71.78125 18.9375 73 

Q 24.125 74.21875 28.421875 74.21875 

Q 39.75 74.21875 46.484375 68.546875 

Q 53.21875 62.890625 53.21875 53.421875 

Q 53.21875 48.921875 51.53125 44.890625 

Q 49.859375 40.875 45.40625 35.40625 

Q 44.1875 33.984375 37.640625 27.21875 

Q 31.109375 20.453125 19.1875 8.296875 

z

" id="DejaVuSans-50"/>

      </defs>

      <g transform="translate(103.203267 274.118483)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-50"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_4">

     <g id="line2d_4">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="152.377699" xlink:href="#m8736a96668" y="259.520045"/>

      </g>

     </g>

     <g id="text_4">

      <!-- 300 -->

      <defs>

       <path d="M 40.578125 39.3125 

Q 47.65625 37.796875 51.625 33 

Q 55.609375 28.21875 55.609375 21.1875 

Q 55.609375 10.40625 48.1875 4.484375 

Q 40.765625 -1.421875 27.09375 -1.421875 

Q 22.515625 -1.421875 17.65625 -0.515625 

Q 12.796875 0.390625 7.625 2.203125 

L 7.625 11.71875 

Q 11.71875 9.328125 16.59375 8.109375 

Q 21.484375 6.890625 26.8125 6.890625 

Q 36.078125 6.890625 40.9375 10.546875 

Q 45.796875 14.203125 45.796875 21.1875 

Q 45.796875 27.640625 41.28125 31.265625 

Q 36.765625 34.90625 28.71875 34.90625 

L 20.21875 34.90625 

L 20.21875 43.015625 

L 29.109375 43.015625 

Q 36.375 43.015625 40.234375 45.921875 

Q 44.09375 48.828125 44.09375 54.296875 

Q 44.09375 59.90625 40.109375 62.90625 

Q 36.140625 65.921875 28.71875 65.921875 

Q 24.65625 65.921875 20.015625 65.03125 

Q 15.375 64.15625 9.8125 62.3125 

L 9.8125 71.09375 

Q 15.4375 72.65625 20.34375 73.4375 

Q 25.25 74.21875 29.59375 74.21875 

Q 40.828125 74.21875 47.359375 69.109375 

Q 53.90625 64.015625 53.90625 55.328125 

Q 53.90625 49.265625 50.4375 45.09375 

Q 46.96875 40.921875 40.578125 39.3125 

z

" id="DejaVuSans-51"/>

      </defs>

      <g transform="translate(142.833949 274.118483)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-51"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_5">

     <g id="line2d_5">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="192.008381" xlink:href="#m8736a96668" y="259.520045"/>

      </g>

     </g>

     <g id="text_5">

      <!-- 400 -->

      <defs>

       <path d="M 37.796875 64.3125 

L 12.890625 25.390625 

L 37.796875 25.390625 

z

M 35.203125 72.90625 

L 47.609375 72.90625 

L 47.609375 25.390625 

L 58.015625 25.390625 

L 58.015625 17.1875 

L 47.609375 17.1875 

L 47.609375 0 

L 37.796875 0 

L 37.796875 17.1875 

L 4.890625 17.1875 

L 4.890625 26.703125 

z

" id="DejaVuSans-52"/>

      </defs>

      <g transform="translate(182.464631 274.118483)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-52"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_6">

     <g id="line2d_6">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="231.639062" xlink:href="#m8736a96668" y="259.520045"/>

      </g>

     </g>

     <g id="text_6">

      <!-- 500 -->

      <defs>

       <path d="M 10.796875 72.90625 

L 49.515625 72.90625 

L 49.515625 64.59375 

L 19.828125 64.59375 

L 19.828125 46.734375 

Q 21.96875 47.46875 24.109375 47.828125 

Q 26.265625 48.1875 28.421875 48.1875 

Q 40.625 48.1875 47.75 41.5 

Q 54.890625 34.8125 54.890625 23.390625 

Q 54.890625 11.625 47.5625 5.09375 

Q 40.234375 -1.421875 26.90625 -1.421875 

Q 22.3125 -1.421875 17.546875 -0.640625 

Q 12.796875 0.140625 7.71875 1.703125 

L 7.71875 11.625 

Q 12.109375 9.234375 16.796875 8.0625 

Q 21.484375 6.890625 26.703125 6.890625 

Q 35.15625 6.890625 40.078125 11.328125 

Q 45.015625 15.765625 45.015625 23.390625 

Q 45.015625 31 40.078125 35.4375 

Q 35.15625 39.890625 26.703125 39.890625 

Q 22.75 39.890625 18.8125 39.015625 

Q 14.890625 38.140625 10.796875 36.28125 

z

" id="DejaVuSans-53"/>

      </defs>

      <g transform="translate(222.095312 274.118483)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-53"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

   </g>

   <g id="matplotlib.axis_2">

    <g id="ytick_1">

     <g id="line2d_7">

      <defs>

       <path d="M 0 0 

L -3.5 0 

" id="mf2ae93be4b" style="stroke:#000000;stroke-width:0.8;"/>

      </defs>

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#mf2ae93be4b" y="56.809108"/>

      </g>

     </g>

     <g id="text_7">

      <!-- 0 -->

      <g transform="translate(19.925 60.608327)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_2">

     <g id="line2d_8">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#mf2ae93be4b" y="96.43979"/>

      </g>

     </g>

     <g id="text_8">

      <!-- 100 -->

      <g transform="translate(7.2 100.239009)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_3">

     <g id="line2d_9">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#mf2ae93be4b" y="136.070472"/>

      </g>

     </g>

     <g id="text_9">

      <!-- 200 -->

      <g transform="translate(7.2 139.86969)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-50"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_4">

     <g id="line2d_10">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#mf2ae93be4b" y="175.701153"/>

      </g>

     </g>

     <g id="text_10">

      <!-- 300 -->

      <g transform="translate(7.2 179.500372)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-51"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_5">

     <g id="line2d_11">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#mf2ae93be4b" y="215.331835"/>

      </g>

     </g>

     <g id="text_11">

      <!-- 400 -->

      <g transform="translate(7.2 219.131054)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-52"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_6">

     <g id="line2d_12">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#mf2ae93be4b" y="254.962517"/>

      </g>

     </g>

     <g id="text_12">

      <!-- 500 -->

      <g transform="translate(7.2 258.761736)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-53"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

   </g>

   <g id="patch_3">

    <path d="M 33.2875 259.520045 

L 33.2875 56.610955 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_4">

    <path d="M 236.196591 259.520045 

L 236.196591 56.610955 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_5">

    <path d="M 33.2875 259.520045 

L 236.196591 259.520045 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_6">

    <path d="M 33.2875 56.610955 

L 236.196591 56.610955 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="text_13">

    <!-- Original -->

    <defs>

     <path d="M 39.40625 66.21875 

Q 28.65625 66.21875 22.328125 58.203125 

Q 16.015625 50.203125 16.015625 36.375 

Q 16.015625 22.609375 22.328125 14.59375 

Q 28.65625 6.59375 39.40625 6.59375 

Q 50.140625 6.59375 56.421875 14.59375 

Q 62.703125 22.609375 62.703125 36.375 

Q 62.703125 50.203125 56.421875 58.203125 

Q 50.140625 66.21875 39.40625 66.21875 

z

M 39.40625 74.21875 

Q 54.734375 74.21875 63.90625 63.9375 

Q 73.09375 53.65625 73.09375 36.375 

Q 73.09375 19.140625 63.90625 8.859375 

Q 54.734375 -1.421875 39.40625 -1.421875 

Q 24.03125 -1.421875 14.8125 8.828125 

Q 5.609375 19.09375 5.609375 36.375 

Q 5.609375 53.65625 14.8125 63.9375 

Q 24.03125 74.21875 39.40625 74.21875 

z

" id="DejaVuSans-79"/>

     <path d="M 41.109375 46.296875 

Q 39.59375 47.171875 37.8125 47.578125 

Q 36.03125 48 33.890625 48 

Q 26.265625 48 22.1875 43.046875 

Q 18.109375 38.09375 18.109375 28.8125 

L 18.109375 0 

L 9.078125 0 

L 9.078125 54.6875 

L 18.109375 54.6875 

L 18.109375 46.1875 

Q 20.953125 51.171875 25.484375 53.578125 

Q 30.03125 56 36.53125 56 

Q 37.453125 56 38.578125 55.875 

Q 39.703125 55.765625 41.0625 55.515625 

z

" id="DejaVuSans-114"/>

     <path d="M 9.421875 54.6875 

L 18.40625 54.6875 

L 18.40625 0 

L 9.421875 0 

z

M 9.421875 75.984375 

L 18.40625 75.984375 

L 18.40625 64.59375 

L 9.421875 64.59375 

z

" id="DejaVuSans-105"/>

     <path d="M 45.40625 27.984375 

Q 45.40625 37.75 41.375 43.109375 

Q 37.359375 48.484375 30.078125 48.484375 

Q 22.859375 48.484375 18.828125 43.109375 

Q 14.796875 37.75 14.796875 27.984375 

Q 14.796875 18.265625 18.828125 12.890625 

Q 22.859375 7.515625 30.078125 7.515625 

Q 37.359375 7.515625 41.375 12.890625 

Q 45.40625 18.265625 45.40625 27.984375 

z

M 54.390625 6.78125 

Q 54.390625 -7.171875 48.1875 -13.984375 

Q 42 -20.796875 29.203125 -20.796875 

Q 24.46875 -20.796875 20.265625 -20.09375 

Q 16.0625 -19.390625 12.109375 -17.921875 

L 12.109375 -9.1875 

Q 16.0625 -11.328125 19.921875 -12.34375 

Q 23.78125 -13.375 27.78125 -13.375 

Q 36.625 -13.375 41.015625 -8.765625 

Q 45.40625 -4.15625 45.40625 5.171875 

L 45.40625 9.625 

Q 42.625 4.78125 38.28125 2.390625 

Q 33.9375 0 27.875 0 

Q 17.828125 0 11.671875 7.65625 

Q 5.515625 15.328125 5.515625 27.984375 

Q 5.515625 40.671875 11.671875 48.328125 

Q 17.828125 56 27.875 56 

Q 33.9375 56 38.28125 53.609375 

Q 42.625 51.21875 45.40625 46.390625 

L 45.40625 54.6875 

L 54.390625 54.6875 

z

" id="DejaVuSans-103"/>

     <path d="M 54.890625 33.015625 

L 54.890625 0 

L 45.90625 0 

L 45.90625 32.71875 

Q 45.90625 40.484375 42.875 44.328125 

Q 39.84375 48.1875 33.796875 48.1875 

Q 26.515625 48.1875 22.3125 43.546875 

Q 18.109375 38.921875 18.109375 30.90625 

L 18.109375 0 

L 9.078125 0 

L 9.078125 54.6875 

L 18.109375 54.6875 

L 18.109375 46.1875 

Q 21.34375 51.125 25.703125 53.5625 

Q 30.078125 56 35.796875 56 

Q 45.21875 56 50.046875 50.171875 

Q 54.890625 44.34375 54.890625 33.015625 

z

" id="DejaVuSans-110"/>

     <path d="M 34.28125 27.484375 

Q 23.390625 27.484375 19.1875 25 

Q 14.984375 22.515625 14.984375 16.5 

Q 14.984375 11.71875 18.140625 8.90625 

Q 21.296875 6.109375 26.703125 6.109375 

Q 34.1875 6.109375 38.703125 11.40625 

Q 43.21875 16.703125 43.21875 25.484375 

L 43.21875 27.484375 

z

M 52.203125 31.203125 

L 52.203125 0 

L 43.21875 0 

L 43.21875 8.296875 

Q 40.140625 3.328125 35.546875 0.953125 

Q 30.953125 -1.421875 24.3125 -1.421875 

Q 15.921875 -1.421875 10.953125 3.296875 

Q 6 8.015625 6 15.921875 

Q 6 25.140625 12.171875 29.828125 

Q 18.359375 34.515625 30.609375 34.515625 

L 43.21875 34.515625 

L 43.21875 35.40625 

Q 43.21875 41.609375 39.140625 45 

Q 35.0625 48.390625 27.6875 48.390625 

Q 23 48.390625 18.546875 47.265625 

Q 14.109375 46.140625 10.015625 43.890625 

L 10.015625 52.203125 

Q 14.9375 54.109375 19.578125 55.046875 

Q 24.21875 56 28.609375 56 

Q 40.484375 56 46.34375 49.84375 

Q 52.203125 43.703125 52.203125 31.203125 

z

" id="DejaVuSans-97"/>

     <path d="M 9.421875 75.984375 

L 18.40625 75.984375 

L 18.40625 0 

L 9.421875 0 

z

" id="DejaVuSans-108"/>

    </defs>

    <g transform="translate(111.263295 50.610955)scale(0.12 -0.12)">

     <use xlink:href="#DejaVuSans-79"/>

     <use x="78.710938" xlink:href="#DejaVuSans-114"/>

     <use x="119.824219" xlink:href="#DejaVuSans-105"/>

     <use x="147.607422" xlink:href="#DejaVuSans-103"/>

     <use x="211.083984" xlink:href="#DejaVuSans-105"/>

     <use x="238.867188" xlink:href="#DejaVuSans-110"/>

     <use x="302.246094" xlink:href="#DejaVuSans-97"/>

     <use x="363.525391" xlink:href="#DejaVuSans-108"/>

    </g>

   </g>

  </g>

  <g id="axes_2">

   <g id="patch_7">

    <path d="M 276.778409 280.3755 

L 479.6875 280.3755 

L 479.6875 35.7555 

L 276.778409 35.7555 

z

" style="fill:#ffffff;"/>

   </g>

   <g clip-path="url(#p10a7be7180)">

    <image height="245" id="image0c331a5b0c" transform="scale(1 -1)translate(0 -245)" width="203" x="276.778409" xlink:href="data:image/png;base64,

iVBORw0KGgoAAAANSUhEUgAAAMsAAAD1CAYAAAD+iwHuAAAABHNCSVQICAgIfAhkiAAAIABJREFUeJzsnemSHMd1tk8vM92zDzDYQVIyJMoMhyxLPxRhh69C16eb8F1YS4T0WbJlWqYsUiABEJgNs/Q63f39GL45T71zsgHbIkXJkxEd3V2VlctZ33Myq6oVEYu4KTflpryxtP/UA7gpN+XPpdwoy025KW9ZbpTlptyUtyw3ynJTbspblhtluSk35S3LjbLclJvyluVGWW7KTXnLcqMsN+WmvGXp/qkHcFMuS6vVKr8Xi0W0Wq1ybLFYNL5vyp+m3CjLl1xarVZ0u91YX1+PtbW12N7ejn6/H2tra7GyshL9fj86nU7M5/NotVrR6XTKtYvFIubzebTblwBgPB7HdDqNyWQSk8kkzs7OYjgcxsnJSTl3o1BfXrlRlj9CabVasbu7Gzs7O3H//v1YX1+P7e3t6PV60ev1otvtRq/Xi9XV1eh0OrFYLGJ1dTXa7XZRkFarVf7To0hhFotFXFxcRKvViul0GrPZLCIiZrNZjMfjuLi4KN/n5+cxHA7j+Pg4Tk9P4/nz53F+fl6uuSn/s3KjLP+D0mq1ot/vx7vvvhsPHz6M9fX12Nrain6/HxsbG0U5ut1u8RwRESsrK7G6ulp+LxaL8i3vIQjmRcqi37PZLBaLRUwmk6JM9DxSntFoVJTn5OQkPv3003j16lWcnp5+RdT6yymtuNlI+Val3W7H/fv34/79+/Hw4cPY2NiIra2tWF9fL7DKlaTbvbRFKysr0W63o91uR6fTaXzLo6i4ohBWuZeJiJhOpxERcXFxUY5RafQ9Ho/j/Pw8BoNBjEajeP36dRwdHcXvf//7ODo6Ku3clHq5UZYlZWVlJe7cuRNPnjyJ3d3duH37dqytrcXGxkb0+/2iKFQSfbdarVhZWSkQq9vtRqfTaShJRFyDXu12u8QpDOzn83kZl37P5/OYTqcxn88LxJpOp0XwqSwXFxcxmUzi/Pw8ptNpnJ+fx3g8jtPT0zg7O4sXL17Ey5cv4w9/+ENRupvSLDfKYqXVasU777wTjx49iocPH8b29nbs7u4WiNXr9WJtba3EICsrKwVeUUn4W3GJPI28CZVGCuNZMf+md+FvBfcXFxfl/2w2KwolWKbf5+fncXFxUTzN+fl5nJ6exsHBQRwfH8d//ud/xqtXr24UB+VGWb4om5ub8d3vfjfu3r0bd+7cic3NzdjZ2Yler1c8iAJ2D9q73W4R/n6/XwL4iCiehB8dj4hGYF8rUgwpjRREHkZKMp/Py2c2m8VsNovJZBIRUX6Px+PyezqdxmAwiOl0GsPhMEajUcmwHR0dxdnZWTx9+jQ+/vjjePny5ZdG+z+X8n9aWXq9Xrz77rvx13/91wVmbWxsxM7OToFZq6ur0e/3y3e32y1ZLXmWiIh+vx/tdrv8l2dRfJLBLgn9bDZrxAyCYlIQKZyUUtdLYag0UpKISximJABjHEEyfY/H4/IZjUYlLT0YDOL4+DjOz8/jxYsX8fz58/jNb35TFPD/Wvk/qSz379+Pb33rW/Hee+/F9vZ23Lp1K9bW1q4pydraWnQ6nZLhcsjFj0OudrsdFxcXMRwOixDKkmtNJeLSS8grSEmkCEwhSxFbrVbMZrPS3+rqavFwGxsbJU5S/xFRhHs8HhcvRGVxpZlMJmXcUpqTk5MYDAbx6tWrODg4iF/96ldxcHDQiKX+0sv/GWVpt9vxwQcflHiESrK9vR1ra2uxvr4evV4v+v1+WTCU95AnkWeJiOJhWq1WDAaDGI/HcXJyUiAO4wR5BKV8Ly4uot1ul/8R9bSxlIcLlvI0ajMiijLr0+/3o9/vx87OTpmDUs2z2awoiWDZbDaLwWAQs9kshsNhUfbRaBSnp6cl/TwYDOLly5dxfHwcH374YTx9+jSGw+FXwMU/bfmLV5Z+vx/f+9734uHDh0VJlNXa2toq2a2VlZVYW1uL1dXV8un1etHpdErAru+Li4sYjUZxcHBQLPDFxUWBQFKUiCtIpaxVp9NpLA7OZrNSR0VKkymP6ipZoN/dbrconaAf13Q6nU70+/3Y3Nwsae+VlZWSCJCyuJLL2wyHw5hMJnF6elpSz+fn5/Hq1as4OjqKjz76KH7961/HeDz+Uvn5pyx/scqys7MT3/72t+ODDz6IR48excbGRuzu7sba2lpsbm4WwRHc6na7BXatr683YpNWqxWj0ShevXoV5+fnMZlMYjQaxXw+L3GBBE2eQsKu//IiEdGAXBFX2S7GIUoE6FhENNZjdE5xka7R5+LiosAxzSPiyhsq/trd3S3JDMY32TqN4JkSAaPRKE5OTuL09DQODw/j5cuX8eLFi/jZz372F7no+RelLHfv3o1/+Id/iL29vXjw4EFJ+yoWUep3Y2PjWuDe6XSi1+tFq9WK4+PjYjkZ/Aq6RERRAnkMZqp8TYQCr2MRcS0uoZJJwXSMQT8VSfVVl99SdI2h3W5Hr9cr/clrttvtYigE3e7evRvb29sREcXD6FvGYjQaFfh5dnYWx8fHMRgMSvr5s88+i//6r/+Kf/3Xf/2SOf/VlD97Zel0OvHuu+/GD3/4w9jb24t79+7F1tZW3Lp1q2xD2dzcLClgrZNIMFZXV0vM8dlnn8VgMGgEvYIo2pPVarUK5KKAMwsVsVxJCK2034uexmGZiuIe90Q6p28pi8ag2Ib/pUy6hh5IKfCVlZXY2tqKnZ2duHPnTrRaraI0TFgIpgminZycxNnZWRwcHMTJyUl89tln8fTp0/j5z3/+Z70/7c9WWdbW1uLJkyfx/e9/P+7cuRN37twp8Qg3Mm5sbDSyW4pF2u12HB4exuHhYQnKGZh7ylUwR55EAq+Fv4hoZKoUwLvQ03v48YjrK/hUDF7v/1moBBqjEgI6rutWVlZiNpsVLyTjod0GSmpo18K9e/diZ2enzFWxzGAwKPEb45rBYBD7+/txenoan376aXz66afxs5/9LAaDwR9BCr7a8menLLu7u/Htb387/u7v/i729vbi7t27sbGx0fAkCtpXV1fL1ngxfTQaxaeffhqDwSAGg0EjfaoUrryErKAEVvEJBZUeREIZ0YRang7Wt45T2KmIEbmX4Rg8vZxl07TTWe0pySCPtrKyUpIPquP72ZRh02Ls1tZW7O3txZ07d0rCQ4rjcc3r168LTDs5OYnnz58XT3NwcPC/lIivrvzZKMvjx4/jO9/5TnznO9+J27dvx/3791MlUdC+vr5eMlzKXB0cHBSmSjkUh3B/lf5HXMUgEnrde+KLgfQW2T0lvr+LpbbLuLapknGLrvfY5U0paCmG2pTX0fy0pqN2fE2p1+vFyspKya49fvw4+v1+2Q0gaKatNFqrOT8/j+Pj4zg+Po5nz57F559/Hr/4xS/i6dOnX/s1m6+9skhBvvGNb8Tdu3fj7t27BUcLbtGTcGHu5OQknj17FicnJyWrQ+UQpOJKOrNZhFjKLkVEA3f7Zke/u5EBu45nMCxTDG/Lz/EaKgyTAqzLWIaZM9GAi6pKSXPHQLY5lGs6W1tbsbW1FY8fP46IiOFweG3TpjzNcDiMg4ODsqXm4OAg/uVf/iU++uijGI1G/wuJ+fLK11JZOp1OfP/73y+r7Ldu3Yr79+8XJdFCYq/XawTvKysrZZX59evXZVu6duIyMKdi+M1VVBQKmgf1EVfxAPdv6b9nr/xa/x8RDaEWVGJZFrvoPCFalk3Ted4uIAPg6WhXGP3Wth4pmNamVlZWCvTVupbiQWbOlBAYDAZxdHQUr1+/jhcvXsTR0VH827/9W/z7v//71w6ifa2UZW1tLf7xH/8x3n333XjnnXdie3s77t27d22NRN9Skm63G8+ePYujo6M4PT0t2Rouskn4Cako/MxK1RbWPNZQdsz3evm2FSqR2sk8T+0GsGzri7cTcQWhPGvmsK3b7V7bXqNrI66ybn67M+cqRVN7inO4eKtNp4LNKysrDaWRp9FtAkdHR3FyclJSzx999FF8+OGH8bvf/S6Ftl91+Vooy8OHD+Pv//7v48GDB/Ho0aPY2dmJvb292N7eLnCLC4nakjIajeLp06dxdnYWZ2dnZR3A4xApCjcekvjchp5tSWf8Qk+jY1SiTFE83atvxjE1+EZFJLRSXYdfFHAfgwJ5zksr/+5R1L52ATiUo0Kp34ir2Ea3JGj/Wr/fL+teDx48uHZ7gODZaDSK/f39OD8/L9nKjz/+OH75y1/Gxx9//CfdIfAnU5ZOpxPf/e5348mTJ/HkyZN4+PBh7OzslBXl27dvR6/Xa6SAlfLd39+P58+fF5iljJY8hDYnujfxDwVdnoKFQkkh9rUC7vFy5aDyRFzPdmVKxRV81fHiiuLjYfqZe8r82tlsVhSG2TR6M6WXpSSsy2u405rwjR6HivPNb34zer1eA54pi6bs2fn5eezv78eLFy/i4OAgPvzww/jtb38bL168eBsx+6OWr1RZWq1W3Lp1K374wx/GO++8E48fP47d3d24c+dOyWrt7OyUDIt2APd6vTg+Po79/f04PDwsMIspX94pKAWRMFA5VHylnQog5iuoV+xAgaZnkVBQKdWOB/3MpnnM4V5Fv7PUMsfDwusyhaspMs87HFTwr2u8D17jxxgXyeMojS8j+ODBg7h9+3ZERFGa8Xhc1mlOTk7K/TWff/55nJycxMcffxyffPJJ/L//9/++slsGvlRlabfbcfv27fjhD38YDx48iHfffTdu3boVe3t7sbW1Fbu7uwVi6X52LSCenZ2V7eDaWqFAPVsLyTyIBNl39ipY138JhLA8M2K+Eu+eQH17Hfbt8QeVhgq4DIplAb2fZ/Yr83AqrmBUdikQ78EhLZkcoIIJjtGTcd2GME9eh7GOEgPr6+vx8OHD2NvbK3vvTk9PG7sDlBQ4OzuL/f39srXmD3/4Q/ziF7/40val/dGVpdW6vC33yZMn8cEHH8Tu7m7cu3evbIlnsL61tRWrq6sl5TibzeLTTz8ti1faIh4RaTaLysG4Qt8SgNqinlbqCSvoRViXQp8Jdk2p9Jtj8Paz+uyHAu9xjOq795Hw1iAdY4/Mu7BvKgLjFdKT3oQJBSoJFU0fKZqyakwM7O7uloVnbUNSfKNM2vHxcQyHw7JLYH9/P/b39+O3v/1tfPzxx/H8+fM/2vrNH0VZ5Er/9m//Nu7evRuPHz+Ora2tcufhrVu3yn0VVBJlsg4ODuLZs2cxHA5Lbl4fMZzbTjyrxcBddTJh5rdDGFcqCaN7ALaR/fdVfAqjxytv400oeJmXcQVj2y7kjG1c4N1rsR7b19YYFfWh8/RS7lkyqMZnpil20h413b69vr4ee3t7sbe3F5ubm2VPGu+zOTs7Kwue+n79+nV8/vnnsb+/Hx9++GE8f/48jo6OrsV4b1v+28rSarVia2sr7t69G++//37cvXu37PDVZASptGCoDNbm5masr69Hp9OJ09PToiBatJL34P3kvhbimSzPbvH+EIdjVJQa3mfswONZIM32VNhPTUF0bZYqZmDuyuxewLfCMP1LWFVTKnqcbFtNtn0mg1o0EIRcnjRwxWM6mv/lvbTlRus3MrCbm5vx6NGjWF9fLzvCFef4Uzq1e/zo6CjOz8/j5cuX8fr16/jkk0/i1atX8eLFixgMBm+lQFVlUfZiZ2cndnZ24uHDh/HgwYNGxkoxx/b2dpkE10LW1tbK1vh2ux0HBwdxeHgYx8fHjWdbKdWrGEQQyXfxUjFo6ViHDHUCqG0KJBVHzBXzGde4ADOBQPjCtQpd75siKXgUHs6DgrzseA06cTzMimVGwsfIvWTeRwb/2K4riNpmW2zPU9D6TW8khVksFo3nsq2ursatW7fKUoOeWqNnCHDLjTwQYx8Zat1acHh4GGdnZ+X79PS0LKheXFxE60c/+tFCE2q1rvb8cPuIUrgbGxuNm6eoENy0qHvWp9NpHB0dxatXrwre1DqIoBWDde3UlWAzXsgUgKvOfsehxwSEYQ5J3FMRRmUxxdsE/Zml8jiIxzIB9usyK++CyLruDTMF5LUcE8eYQSyHg5nXYDscj8cw9EocK1PgimkirtZyIqKhPLoPR4+uYtZUHkgKoHS1ntYpaOcbamXQ5/N5tH784x8v6Fbl7rQHSMGX7gPh7be8iUoLXny2LlO7+k1oRIjlUEqCwDQrGUlYQqYQSlDZ1K6vJVCAKXzuwSi0b1I4/ndFYn/ZAiOPkwa+au/Cx774m9dJCLM6rljeNoXYIaOKYFRNYalUasuLPIva03yVOeO1SkkrMRAR5Q5QKY+SShsbG9FqtRo3r/EuUD5j7fz8vMyPsXLrpz/96YKucDablXvPI6KkcqU0ypfPZrOy4vr69esygGzNQwuGVAb3ANxjpcEtFosGlHGLLqUhoT2AZ5yTWfNlHsfjDe/LIUmWPMg8TiZshG8eY7EOPYCKexgqhsaWwSrVcQV0Gvk1Pial3P3OTF3HOdEYeMzmHkZGnHCX22yo7FwE9VsN5Ilk6IWUtI5HlDOfz2M0GpWHexDZtI6Ojha03sLabEDuim6Jax4eb3h8oYmrDnfv1jJLKp7hogfRRBjYuoBnd+Y5NPP+Xbi8Tx2jUPK6mrJkMYXDJKau3Stk1p4K5NAou4YeS3PiFhldw3iH19KgSJC1r07HvG6WZMjm4vfdcO4eb3HOqu/zplIJJWmXwerqapFPPRhRiiWPJb5K3lv/9E//tOCJiCgrrbL2k8kkOp1OY52DGkeYQyF0yEHB9uA5C4YzD+DQya00PRQVRcT29RK26bCHKd+suBK4d/Dxe6DvVl3Fs0tsN4NtNbjjhkPFoaULmdfx/35OsiGZkSB63beBgO4hmaamB6JCZ4pHD6PzknPJIW96owxIPnVex7onJyfXtLvb7ZYNa9rmIIKoM3VIGKUJ6Vsd6fFBskIiCgdCoae1pNCpXVpgumhaQt7WKyZmGNwFpyYwnlrNFMsFgjGXCwr787YFazQ3/Wc7FDYXzAwKucDROHA+FC6NTXyh13DlpmBS2dmuw8gsA0c6uqf2eDKL7XxcvJVa8CoiyuOeJJssGv94PG5A+C5vlaUGCotq7YPuWIPgkxRFJE2GsE5b2UU83j+RWXwnkltjZ6K7dT3UjoriAulCQYvFvim07gmWKQrbdIWn4LoHYbv0xKRfBkdrHiFr1xWF9FQfPkYfh/chGvnOAfbv42S8Q2ShfjVHV1K1T9lzGM6+eUyKITlhDE6aKhlFeegqiFFjGQRaLC4f3iA8x5V1MpH/XQncWzjEcSKRCZygM5PHKWC0yF7HlcbhknuszBNkls3H5efcE7i3ccvpMILKzTm5AHqcQS/E9jKaugK5Zc+8s67ndn/Ng1ksN8aEzaQLPQ3bcp5LvnS9rpPMSBb0nwZdC5581hsRiPqQ0szn88u3FXuMwf8M3PXbPYk8TAabnOGyIm7FeQ2JpwnTQlMYXMh0jIwT4WveJRMEehK2y7YyofJ2szl5f66QfDUF25CA+bh9PiyuBBRYVxpemymUH2chb1g3g2S04L4eE9EM9Ol1SKMCjb4I2HVdRBQkJE/CZ71pvWY8Hl+jLd/JuVhcvb5DfbdJALfg7Mix4MXFRXlsDq/P0ocauITc3SPbJWPpYslg307v1o+W2KEhCwVI3w5XHDrQgmaQy71PBovEDH1zDoSPTiMKkXsO0tqP+zVZoO3t8FxGL/GTayKEYlRkzcuNCj0M+afixxg/0GASgZB2jKOVtJICEIWQ9248GvMnI4k3OcFsYLT8tFYcDM/zwzYpwDym35n1FLxa5mXUDm9s8naywjZ4DRlPT+Mwhgqn/2J0xoQMyvG2X13LrJB7I/53JVj22/mpebAtKhbHxLbcy7oHdIPgHldzrimuQ1U3vBw37z+SMnPNxBVeCkUPRY/CjbQN6eEAxVxBAse+1PCLi4vSmerL/dJC6r8rjvojUVwZ2CfbJjSktdZEOU4pj5jEkhkE95A+jgySuDDxWh+beyIKG4XMBSbzFlk9/ucxztENU1ay45QFGjwfn3gg1JGlgjUONzD0Qm5kqRikIR864giG6IRzZxsaM5M3RUHdpVFD1UEN56v+snw2MTqJ4RN3T0OldcVjfTLHF7WcGXozMBmmulnQn2HwzDJyHJ6w8GyV09GLw9eMdhyjx2uEO+Qr55zBMI6JCpjFJzRCWYra4zKOieOn4DqteZ17UrXFeFb/+XBATx07//St9RTKJWVNny4nQSvj8MCZ7JbDrYy8jBSGawUurE5otccUtns6h29ueX1ln/PhXL0tMsotOwWD1kr9egzmBsiZrvlk8QsFQ0z38WReo+aZ3Pqznit2xpeI6zETZYNt6J59lx21L/5TGMnjLH5RH+KtxuBIg4ujfDQtPYXa5jmvo/443y4tIvfUcDAsFEBOgoJI5ktrsxRhLXefCbTapcXhS4JUX+eJ+2V13BtSwTPr7d8cR3aMBM/ol3kSh6FZndXV1Uaw6t6FYyDjfXzZXNiO43+NjwYrg470qFzX8n4yr6zzVC6vQ2PjMTDXAN3YUBkzmEuPwnMZ0oiIS2VxRcnwsbtDtyyaiF6Qw4wRtZ59cBHLIQytjAd8EiwG+iS+K4bq+uIkhdyte1Zc0NwyS1hYyAD26VDH14RcuOmBVKQcVDj175baPZF7qZoSudUlPzRfChx56p6BMkF++loJhVfjceEXjynwGuvFxcW146SR98OkgBsF8qIrt1jTZlcUNsQJyv3qezqdlhiBAstUtE/ErRGZk2FaTU6Kp+NuGXSdMzHD425tM8WhAKt9F37+Vj2Oj/VUl4bDvasrNZmreg7VSD8VGhefb1YIVwi9JYhMrlBuXDi5a4P9usFlWz4HGkt/jYboJ4PNPjyGk2x44E/j4x66wDA27N/LgjnXfAqqFIeCMZ/PY3V1tayuUpk4ISpQpiScHP+7S3XrTKwroRFRqABSaDKY9KgJmWNitV2LRTJl5bzdULGPGlzxJAfhXUZLGhmP8TRPX02nPPgCItfZSC96e/2nsaUcOY04X67lUW5cVtzY+NhdSdWfyz3b7zrRVRxuubbXmBzRTDfLLYroEqZer9fAqW4hRPxl1sAxpqcSa5vzmIcn4zzmUP3Mc3DMJCoZ6Z7VvSXpLHqpX4dk7J97pWpCkgmEexQmDkhbr5spedZfJiu03JzTm6Cr+KJ0s373er2GMSP/srjJPZoUlCnmzBm4p1wsFk3PUiOuN+rWn4LKiUtYFS+QUXKlypa5u3VcS5ev81rfccVRXVp5WSTHoVyBpmXMLDHn5XPNcLGY44kDVzTvy2FiRpuaZ3Khy7w2BdhpQeWuKbXTxMfrMaAbDNLbPagK6UFo5YYu4mpnvMfePl7KBWO6LOuq9ih/xbN4R1k6zbebUEC5zYGT9aCdAkaBc+hFwjHLRWjhMINwS+eImdkHmSJPqPswMhfs4/M6tPa+8JbFSG6UOK7Mwmew0g2dftMTuwI6HTJoxjS/88Db57wJ2TgWwiHOpZYIcMOj5y3TE7qhkLCTvp4R5HEqE7dEcfycV0RceRYnqggmDE/s7JiRWunWjJbE3ZostPqguybBKVieqeB/Mp/MKJgT99WoPc1F1/CGIDcUJF4mbBRyZzohChlBRmaK4wando3DtSzOcAjFNtUP1yY4Z8FZ8qbmAfU7UyrOsebB2S53hFDGKEMOqUhzGXKni8sqjXOmWPP5PLocnFssKgInSu1mZ75Ow7bcpbkAq02unTgj9J0tNKlkQu6Wg8JAIgsWEj5S6XxOGTxVoYdxWOlWvwY9M6F0gazRlXBZdX0MHoc4HGGMyfPcD8i+fLy+49j7k8z4bnbyWBBaSpwhF3ryTPYcXlKRNYbMm/N/p9OJbs0VqrJDM8fgZBTPO5Fq0I5uv9Vq5rlpxehxahk6WQxOmEqgcSjw5tjd6roA+loD++bcOAZXJgprZslcCT3WYX1vz5XZrawrosdvjNnIEzcAhLSLxdVaGRWDtGG/PO9KSwNJA63d7VSmiCZKoNFwD8tz4p3m5R5KykR66prF4osAn5pGC+EK4QrldWseSuccork1kofRbwqmB9Q+Bp8kCRVx9YYqFTI4E1wqm+P8TBC56OmwkG1nuDibE40Ar3clz74JPTKD4orvBtO/I/L9XlQqWmNXTKevz0v8IGTTHPydMq7YOpbJnvOJ9CWdHUbrnEPeoizsnIrjzKNwusBQYDNPJCUgUdmf1mBkvRjQzefzokwuSGrL44FWq3XtRaIs3EZCgjnRKRzuScVcryNmO+Oy8Xup3aGZeSqdd0WuLSKSL9m8WEgT7slzejK96+tSmcKwuGKpLmMUp3FtjcbH7kjAUQkVj9c4KlDpZmsLjls9C0FlcHfF3+6R1C4Jei2IMvfqBKDbp3DQii4Wi4aSZDhW8xAW1lwdUlCwSVjOS+26Z86wcuYZKDR+vuZJyANXrMyQcKz6TXjqfPK1HHqhzMszDmRcw3G7jPEcM5i6N57vXSH60ZjIJyq/z9npWKOTaJJl0RaLRTPAz4jpAVQGy9z6ckAOSUhw12AqzGQyKZafAq+MjFtdFaavqYjLrLSslOpSYbJYztt271RLPnjfvjfubRnq811W349lnoV1vc1Wq9WIGRaLRXnuMEuG9SPyNLhu6c08heq7somONORZbELjTvkiL51G5HcNlrVaX6yzcECZS3TCsjgsyATElYkWgH3q98XFRVmpJf729h3bE0Zy7BxrTckIJwXfqNA+bnq4zJVn1tMhg4+3Bin8fw02vakex1uDdj4WQjj9Z10aQNJysWg+rES0cGjKR1Yp68UNt2xP/fPFtzon5VE9Pp2FxpLXybBSySgHrlxdP1mzyoxJMgFSG1knFCi3KFQUBnVZlsXLfD4vN/u40FAZsmCWAkHBUd7eBYPzEXHdYqmOGwyeUyGUVKFFY5uOrd1TaL6ejaQV5vzdIGYK7sGzCxuL+vbfpEe7ffVUIFdUwa52++qBjt4m+yKEXoDvAAAgAElEQVR/PUlDGXPjSuWZzWaNZ+MRQWkshM3Fs2RumYTmpN1DLLOCbo3czUlgaLl8UZCWhszThKi8zkCOwwXdXSyJzLjKPYQzgIpOQXCFIV01PlcY95Qqy2KljO6uKJmxI+8Yk9Y8DY+32+3Gs4HfNDb27c8Jo5IypqWhdEjsEM0RgPOGxoZ1JJfj8bgBpyOu9jcqDmu329F1q8PKHrA6tqZHcYZRqDJMrmuIPx2SiSkM+qkkFAx6DBdezoEC6UJExtJQuIWhwomgmRXLgmHH5SpUHFdWFs7dBZECli2ousAT2vhv1tO1glbLXniaeVSnvebgb1WQV2fM51uiXMm5kOoyxP+E8mpDC+Bu6CKiQD15vQjAMCcSGcW8dubSGHTzenftziQnLgVD9bjCr7F4W1QYei4qAMflXkffnjggVCSjXUHdmLDtDMr5OguxOb2xBCKDessMFJWb9chX57HTzVEGA2xXiBrsVP3MO4m3i8WiCKSni0WHDLpRmcg798qii651eZNCOT/orfTK9y47oJbS6jEAYibLhdutNhmYWfiIqMIQMXs+n5fsC3cTeFzi7TqR2F5mrTP4Q2aRBoSkap/9ZVDNx0FhFB2oNOwnE/rMUzsU87Fk6WD991SwB8zOK6/LQlo7fThuyZlePOR799S2eEYPo/G4B+F8SXfW1zEqGmnCpANpn26kdEZqcJ5KdvfqnqRWHAIwLel42d+/nsEoWisVt7guoFl9V0AS3GM7n4dbpsxLe+DrNCTU8aDb5+NtOMTSNRlMZX8s6pt9UEFcIf0/5+ZGj3Vp0WUYFJvSOEmJSZvMENGQMcZxeSS9srUih/80WhHJzV8+wYjm/d9ulTV4x+DeHongllIZGj5RkOslqi9LxMU0d/EkjPdDYeUcMwjie50impjZlSSDYE4np4GPxRnq0NAVzPvKvDgFxmMv8lSZKl+QVbs+nppH03U+ZtKQ8J785MNNnDbknSuKZI/z4/UeKkheyU+2Rc9CWncp/G593Xpz8CQgFSbzSr6RkX1xgJ1Op3EzF4sHclRgEsuJvGwOLA4TPTB2JXxToiArGSyLuJ508BjPSw1muHJlyuOCMp/PCyZnXMIx1+iWHc/QQUZj8Yz8VF+SAz0+mGPOZJNjpXJkUJ//OTbS3NsqSZPMdWf4OCMQA36fCF+m6oyltXBrQJjEPjVBYVrCBF3j59ge28qgAZnpHiizPjXvsMywuAB5UsITJZ4M8XH6XH2czNKRHvLgolmtuAD5GETPzONl3sY9te9F5Jw17tXV1aLMTm8eq8lTzXvUaOdQmfzucoDZ6qw3qkZ4DQlbGk7iG7lYEYP4WC6YRK0xyT2YK0kGk5zITnARN1sEZVu+RkMo45YoMxBUHmese8I3CUQG3zhON4LtdrssxIkfTgda1qzdGmRkqXltGiI3VLWEBPniaIY08xiJgu9tqz0qVBbjuEFsbHdxQrg7UycaALWQQiSBkXIQajkzREROnH1kbt3xszOB3658NSUiA3VNBnMkiD5GP++EZjsZvTMvlwmq76vLrLl7adFBcQn7zjakZgkan6PD92y+Pg8KY7bQmqEUQTQVKQ3HkfHSt65kNHWHkMUpVNBuRmR24FmobAWW77+glfePt8tsBN2jWwqHh8yiUDC9nuqqDc/ZO1NJTBdIekymLEl0/qZQa76cJ/t1eJLxxAWu5g3IL8IteW2fqws44bPTxOklZXO+ZePWNa4QHL+n5rlUwUdrRVwtGmaJHvLL17k8dnYl9Tmqzel02lxnYaGrl0BOJpNCdE2cwqeBMHWnTvmCGSkKGUbFEOG4VZ/K5gpM5rkyZNDC6+ucw7eMAXzlH8fm7l2MomJltKZVk9XU/CkMzsTM29IT8906FHryzOfnHtv745iz8Xg8QKFk8C46efFNnkonu8FZLK5urcjeH6Q6GeJwb5tlxny+WgPqupXSoKkci8Wi4UkyS+8DkFC5AohgLjzuUimALsC0XtkEyfwMg7JPtqvfVDbfN+Xzpeekp5Sye+IkY6roS+j3pvjNlV10oddXO5xnBqdq3taLQ8aaVddvGQAKO70856W500PRM3AuXLx0g0JFZ31XBspGZhhcDi8uLq5ewMp350XkAZWvmGYxigbJIm/iXoIM43WMlTLLTyKRIU4Mr0MiUZhqRdf6HZrZWgSFW325B3R8zd8ehDqs8aSD6Mf5KmtET086k5YyXK4ojCvcsDjE4dg9zlP/3Cql/w6NMkiU8ZHrVISu3CnuY/bbnp1uTMiQdlS4EoKcnp42iEhL457DCSSCLNtGL8jlApAR3nElj7v2ZxkMwQ8PzlnHic3iQsNvPhPAkxukh9aL/CmcrjAUPmcUlZPW2CErvRKNXDYfFULkjPY0mA7z3ABR2NxYRTRjEN9JnHmjzCCqHr27K6XaER1IK3oOegt+Z9BTtKJMdUejUWF2ZmVdIzVgPudLnkl1VI/3Beg4GSWCZ5vlyCwJuQfCutbfec9tE/xkAsGyzMtk52vQzL0ZBYM0Yrs85lv3MwVpt5tpYPWr/+69Oa6Iq/1nnEc2VrZPpa0ZDfbL1XkqCsfliuFKtww2yRi50NN4ZPR1COq88WNlp8Gyp9pz8qyTLQSqUQ2Me7pcMBxDZh6LVtXH5oLJNQUPElncsrtQLCvOWDLHYy3OiTFcbSMoBUjMzpIXPDYajQovVIeCzHG4Isgbka887/PIvLAfc9pEXL8z03e2+7Ga/DlEdQ+n8ehaQWefp0M/eiE/T3lS6Xq2hW7HLSeZ7JkqMZF3Lmbb6clAKlnN2mfY1l21M57X+u8MUrol9/69bT/mQurzFT3l8aQ4oh/bcYvN+chTMVWvuVCAyDNvtwZ5anPMIErmrWvX8ZjDt8zLsA/KiCuRy6fLAh9EwqJxEd04r91QiN5dBoFudZ2QWQwhBna73WuPHcp+06I64X1twl0pLQyFQK4+gxMeMJLYxPk1SOFtuhBnCuRjp9V3xaE1ZFzlRmU+nzfuTszG6FbSlZdj0W8KHQXdFYjn3OO78XBaSIiZLcxkzGmdQXbOI9ux7rwQrR2qZ8jGYRmD//l8fnmnpE+AlWobIDm5lZWV1FI6QTlhDipjNifrUMfbo6K4ULr1kbA542rYO6JpoXmetPA0Kq91vM4sGxlIJnGeujMxyzi64XBoqLbds7oC+Lz4n3KRZaycDnxOtmBltk9NbdKb0qjSQHIeNOrumZ3G8/nVcxp0Z6RvpHSZptFqjFXCQwulxrJ8vWcclAp0Quq/KwyJQbzpbpdJgdqHjOR1IpqvtLsxyCxdVjKYQJp4LJS5c1ozXas6oqsW2ejxptNpEThmCakg5AmvdeiSZcr8m2PjHFUniwE4pyz7p77d4Ii2lAPGMC5PzmvJH39TodRexCXU1tP4HUV5Xww5qISNe/CJpbMJsyMpCBcaNSgKtIhK90niupdQHx4HuPA5BKCSc8KeFCCz+GZbvyb7XxMq91ykH70Ir3errLrdbjdGo1HDM/I6GjYPQB1WcJw1ftZo6W24cGnOvpbiKID9CjoRQVAZ1F6mGLWYd7Fobu93T0pPQYPObT0cp3tq9T2fz6OtAZLg+nBS0rR2u12eR+yKoY6ywbrb9OJWOYNxFErHuZ6WdPeuwqSDriPsIC3ItGy8+vYYwINnLoh6G2KKmDeZTGI4HMZ8frmD4uLiongXejJaeTdAVGL+57ePh3PwdjSnDIZmhsEFnZaallz8ood3w5x9uG6XQW2dU3veX7t9+XD47F0vNAikTcOzZJhdlkBMWV1dbUAoDoIaTeuVeQ4PtEhYVxiHVO5xKJwOGdxLcC4OH2j9SKxMwLNj3H6RKSG9CM/z+HA4LP/11EYWpp59HKrLN/XWxs/6PJYZkBpcyXZWe2o464cyRWVyo+hy43XZtuozaeJ3pao90Ubj6/V6156QyfM0/ld7n42gjDmkhZk3oUCToWwnYxaZo0FlGk145TBLhcxRoRKpeHrYFcahQW3MrJ+d87azdgkZptNpiUk0To9xdFxGinCZHsSNh+jHNQ+nfTZXwrzMytJbkB5Z/Ok0yXZ80JCq0ODqO5MXzZGPf8oUkO3SMOiBKIwXNReuIzaUhQOVVq6url5jkOpmLpJtkVFUHE2IFsutuXuGzEo7c9kWmSpC+sP6SHQSPrNwZHgWpGZwrQY9WXc4HEZEXINqk8mkMUf/LSHm87Iiru+vU8lW631sTgcey24mo/IRZjl92b6ne4kuKBOuKKS1CuXJeVXLnOm3x8vZpldXvC47p4cgrouIxoOWa3gxy4S4paHVcwKonnsEV0RavUwAKCyLxaKhKO4J+KkFpy4ELhAUsswr0SMwJa9YhMKebX7kdaSJYhwaLs69VjLv7vPyp624UfNvKW9t94TGXEu8ZJBpGZSnHHDOta1THAPlrWxl+QI5Cc5pPOwvhWGEXRFXikImkdBujTloKknmLRyuOMxxxtCquRCzbcIHtxqZkEiAOQcKeqbk7JvXiHlkoubUbl/u6fLVd58bme9PG3HDIwsv4+SZHhbPPmn8pLfT13nkQhdxZckziMW5z+fNx8o6KnHP5t/eN3ngr9BQ3QwyO53o3TR/1p/P51fKIq3SAqMI78ShFePEHGsuc590vSQQr6e1dfeoa+gNSDj1J8Y59nbPQO+nNvlS2GVrBA5/SFzSTsqhBUbBQ42DFlYK0u12y31BTCD4nKlQ4gUXScmrrDjdyJPMIDk80fiYccp4617F6a/+szG7vHFMvKHMDblDPR7nmxI8llO/iiXb7fbVAyu0oCOPwoBd/x1Hsk7mXsU8t8rqk0KSQR7PxNDi6pwrEi08V5BdUDJYlcGKDHItY2RmBCRMWijUd6ZsrdZlJqzT6TQeWM3d3VIOeR72QYPGx0VlgsvviGjEPxTKDAIxXhGM4Xz8hjkVh1bkfQ0echyUPUcwrjQct3sojkM09jEQmn0xx25REnVIgqvBWgyiiTEJQG3ngKkMVCIXYJaaF1Ch4rkQk/FsT3MhJl8m6N6OK3jNu6id6XRalIWLjfRY3rdiLB2Xl2Ospro0Bg47ZAgpKBl9HUa5wXPe0KDQk6kvp7t4R6+o/rPj7kHYhiuwx2jMyLItQt7M6FIhMxjY1VZ6WihCMCoBGaBvCm+mEJyw7+51wdegHFvS6nrMkmFrx9lkDBXDMzOumPRkJDKLp6PdOurWbGa7dB9Kp9MpAXrNg7ng0yMRcmgc5IlDEV7nlpqeO6Ip7PS8GXKQl/E23CASVnNs4kWNV/r2uFPFPYwrBGlAY0Vv7VCdyKfE7lpodKjlEItYkh8RxQWJLl1t8Leuo0V37OoQSYRx95pZMHkNEp4EoKIxl+79Eftzfxbb9eJ7ugiZfDMkvUjWlurRaBBiagwufOQhEwCrq6uNRAQhnPenvmj0qBAMip1uNFZuuCjcOi+eONTX7xpE97H5Mfcc/m5Ujp+yzvbEsy73drkSsAMKiA+Q1oi4kQxzQclKzRPwt1sp/XZmcAwiOAU/Iwr79fbJrAxKqN58Pi9bwvVbRffIRzRvmtNYPfHB4oriDxakYjBW1DkZD61Wk6c+V9GLc9MxF0BfjWdxAWY7bjDdk/K4857j8uSO9+PHsrqu2JSNhmdhrELvQA13TaWg0C36q5g5sJrVrE2Q1pTEzayVX5NBIyqJu2uv64oj68I++U4Rldls1oBd6suVmRaa89YWcs2lVgQb+DIeGidPpLgyiA6C4Cq01p4CJq2zhMMyQc4UScddmRzmslCRsnF5OzQWVADJqRsGh2EOKbsM/oh3+c3J+be7ay4KcfC0iD4ZCqFnYqgo7McJ4b9ZX8fZdrY3yRlDOpApGWzSpkdBNSqZt+n/2Xcm2Nl8CeVo/Rh0R0Qjpcw5rK6uNh6qwfgtE54abKI3zGSFPFMdwnPVzYypIx3On8czD+JowA28X0dZ8N3TULJuOiARSIR3wrmgZyunLoz0Fi7UFMqacrAdhxBUNhYfU+ZZagopYfdYh3OYz692BzOQzxTGvZ7PhUymJaSlzjwO2yW/KCz6yCAqscAEBuEb+af2mOkSTRz2sX/K0nzefEepw6dMFjx2yhTFr3NkQ1oz0+eenbSjPFPpunrHecTVSycp2NRMCgqDoawDCl7t/gIKiCtrBpHobWpCzuJMdeVwBlDx2BZjLfY/nU5LDMAtEqrviskHDzoT6cX0xl6OxQN80qr2yFXykB7eMbmnljNYTAVk5ok0IR+oJO4da8XRhfOctOMx57fzibG36kXUn6LDLUmUxe7KykojQ0LB5yQyQjJ+IcTIgq4Ml3qgrHP0Il7c2rKNTHEosCIEvSJjkSxeYbv6rza0bUXn/S5H1ieTs7lLyTTn7HVxbmTIUI9ZaNhYlBVTXQmMQ2/JhMMs0sy9s/OZSuPn1LZfr7r85vW1UouPCKWcjpw/aeehiH53+Sptt9pq3AdMYkuwPStCAmRQg9dnxS0Vf0uZl+2BcqhFptD7ZRYvg4OsOxqNSmaLzxTW3OhV1Ce3ttSUkIxxOmWwgW1LOZR48LbUTkQ0EgmCV0wvi0bcDkIonsEuRxnqj8JHhMLx81qNiRDR2xQvMmOaGWiHcpIf75ftk1+q2+31eg1c7S6VWFgMJLNFYA6Eg81+c2LumTLrkR3PBM29Ett0K69xeADux8jQ6XRaoJeUiSvtVDDCPtLMFYUM4px0De9rybwKaeqCK4MScbUZVrFKRDOjJzjHYF9xBrfha5w6V4shKQukYwbZJPgOudygUai9HYec7uEcHXm/LkN+/0+73b5SloypvvhEeOaBKC22D5IDdIa7FSbz3RuwUIhd0PitwjYkaLTMWT/cJTCbzWIwGJTxMusl70Ji+zgyT0VGs8hjLttwmikbvY/iKCmQ7o+REol/xOXkowfmim3VHmOlzPK7B80UIqOBey6OMYvBvA2GDw776d1oRH2jpUM3tdHd29uLyWRSrKYa8EUyCYkPyuMTFxYvFEiHeCzuEfwciek3dTGbkhkCBrgS+AyKqe5gMCj3wlNBXMnUHueYzZXHa/NnfQrJMkGLuJ4c0dyYZNGuAgkms568LZlGaza7fEeK7irkvjYKr0Mzj8uo2IRYTjO/1r2AF4d33i/rOA05Xha+33Q2m0Xr6dOnhWtqbDqdxmg0alhPPjRBA9KknLEUdLcw/OY5F3iHRK7EDoNIaF6fQTH2L7hBWKbzp6enBX7pnNrWuDJvLFpmCuJCQSPjBieDGWynJjgMWplVE2Rm22xHXkLH2u12ySDxRsBOpxO9Xq8hwFyYdA/mm3OpSFkM4t6D12XQiXGHxyCsw/MOEWnk9d8NQNfdmwa3vr4eEZdCrC3jvpZA1+l5dcIBxhEcmDO+BrUIxxiLeF19Z+f48ZeOyhioyMtyXxfnzPb13xm0zFOxvntCWlpmnRxnq71MYVxRCLWypIgbERoOCprfOSl45pZbbWQpbf2mINaSNGqHkLBmMGrxi86RbplXd3iWKWWXWQEyj8G7Vt6VKpUA0bpTMwlFaKUYeGeKw7jGJ0XhcYjD82QMvQyVjB95EtFhOBzGxcVF6L01HqhTECjcxO+eiqVQ0gDwehckNyYuLORX7T/H7NcTmrmwejaK14omfGTuyspKoy8uPvq1/M9vv1Uis+w15fB512jjkLFW6Mkoo91Wq1Umy8YZKElhpDR6CBwtGAWBA2NnPlEqFIP9bIK8XpberRYVymGclJwKIMJpXufn57FYLIIveKLwUME4FgoZLZg/QrZGH6cdt6jQK1PACBdIA/HLx+ZGhrRi4E5BZb+aH69V/YuLi1hdXS3PuqanUYLAvabG5EG8e4DMY1OIKdzu8X0xnArg/FDJFtD1v6sKEkAKOAWFE9/c3IzZbFassFuJTJAy76JCK+txjQuCp3p1HWMXQqUMQrnAUvl9JV6Fb9WSwmTjdUa4VXWP6W7fhYIe27NE/J0VCoiv0YjvFExf4FSM4ltnyD9BVvFCsIzzcYNHb+JCW/MGKqzvY6FSuiGm4Ds8o2JmvJLz6JLQmWXJshqqu7Gx0fA0HgvoWlfCjABiCo85BMgUzes5PNTxjNgREYPBoDBcdZnYcDjBYx4Q+loV61MYyOw3/WfJIBn/LxaLa+nmzNK7NyJvqbjMmPG8G4p2u13uBp1MJtHr9cqCZgZpqJRMDLigZ9DKx6jiXlfX+XF3BqzHc6S9/neVKnSs54EoB0QmdDqd6Pf7MZvNGhm0iCYs4Z161GifNIWMxRWBAsLf9Axs063FxcVFDIfDa4qh/w41NB8yjG1TAOgF1K5vzNOYRVeOjb9rwpNBT4cQvoerFiN4IkH1XJDVNwWYxzudTjE60+k01tbWGvzL4hJmNz3pQVnJ4hY3upRT5zvHnMlcbW6U0+7p6WmBVhHXIZlbdxY1Loaur6/HZDIpD1qQgNHq+mB9MmRophiuiArQJaQcl4rDnuFwGJPJpCgG26S3kHVV/2wrw+4cA2Mq1SMjpfy+W9uLe3opAZnJudWOk74+PtYjn/lEGY7dDQRpI0jcbrdjOByW9/b4PS8Oo2hYMg9IA6vC8bhBctl0GOae2RMa7lEjIrrj8bhY49XV1VhbW2tomAbH3D2FiRY84urNX9oSIhdNweZkqQBkmgs4r8kWBp3hHK/mIUVWWphQjZsg6X18XPx2BXb4RPdPL5IphtPF+yWkIPbXO9oz70OPkRUXmIjrD65wz8R1G58rx0taMZZh7CvF13jVvsMmwu9lAbobSzfIVEAmE6iIpL3fZtylNRUjer1eY8+QB7vqzGGQBthqtaLf78d0Oi13DqoNZnJc+FjIbLf8hE7OeI2Nrnw+nze8iXYqMDumkgXCDo2y8w513EqT8aKV34LNuZDOjt0zqMUPH2LHvl242BfH4l6AEMiDfQoX26KQMcXMZzPoBjSNl4pC4+JKS5lTEsLp5YE6jYLToJYgEbQUTRpv/pIgTiaT6Pf713adZjECB+/f7Xa74FYqDCdFK8k2qSgiuK6nYtJFO8Fms1mMx+MSm/AhEoRNhHpuoTkeEtrhWOZFIq52JmhdwuML98xe3Jo6BCJsdiih8bmwZUUCQdqruJBRKYgyKOyCsFqro4Hq9/vRarWqj551xXBYWfMuPq4sFlGbmiu3bbE9Xi/P3XgBq4RVmr6yslJgVaYcNcHyzFWv1ysCqr5c+MgYwiGuoJNYbIMT1OQFuUajUfEotHIOKYnl2R4FUzSildU1wuq0RNr14Fi75qFqxXF8FqdwjAyaOWbvsyaAbDeD5KzjSlzrr9VqFcg4Go0aq//j8bg8D0BtOlzSOa/jRiDrl8czD+O3NNAA6kF7BYa5lW+1Lhcq+SQQZb0y5aCAZ95H57RwNRqNGufd5c/n87Iw6JaXlpX4WdcOBoNQHMaVeH/YMxVB1/qYKAxUdHo2QlUpB2+okrXlQmPE1cLj2xaOTx6F9PFHT2UCU2vXs3N+4x+/aXUzb0ojQnpJ6Ph6DRmStbW1Bl9koDnH7C5H97q14sqkj2ffnM/Fo+jh+BQYJ5Cso5RGFkBu1APizHoSo8uL0YqQAIRbNQuh4jerjUajGI1GZUuOmKH+6VWoNN6/M5wEpsCy+PzYnsNcx/j/HYXhdYI3b9rrRYHgfHTMvZGOOxRxr+JjURseONMrZh5bxlM7mj3OoYf2ne5u0JYpDmGee1T+Z7wmJVGdLlfgKYDCk9wxKos/Ho+j2+3G2traNUWhEJLwhGUSKg2GK8CctAbKMbpADIfDkuGSN+Ezu8gY9you/A5pMs9WizGUpVsGbSjUGTRzxnrJ4K/HB37XowuP90MYRYF2qyveqG0G4A5TqYC8Vue50q5YRnKhNT/GnfI27sE8RlL7LkM0/q70/OZY5VWo/F0Gh47jebEIoNVupYe73W70er1yXWaB3aKLKQx+uV3F8TeFTK5bK+/j8Tjm83lRFl3PvWuuJA7HSFBdo8U1WltXVgoh94GRCY6FKZxq03F5Zh29XcIvv62ZCu8QlwLG9lTYvmfFdJ5JHxYqkBfR1XcYuHeUUZOnUbuSOSqNxqDxLBZXT5zUWF0pRBPShoZBBkd1dK7T6VzCsFpcoPUR5sIjoqEs7XY7zs/Py+SILRmzUFG4xiHh0J14FFoGXqp/dnZWslx8Tpc+3kdNeUUchxqEDhHNB0fQ82Sr0apDoaIC8TzpzFgxKxkEIqRhep+pVveUyzyN9y0hzJ6Gz7G6gRSdaRDYPucruSCtu91uuRlxNrt8hR3hmW6F5pOIPCgnL9i+G0bNkx5W/6U0EVE2EXc1YD7ogBNTylXuUQOQ5VUHo9GodKLG+SJQEVFCT3eq0ulcvquc7yTRWo3frVjb+KjvzIN4bKL+dTyDe7SEGquvBzgEiIiGtSNUYfsUqGUwjAz38atd985cJ8tSrYTdmTCpHq0+4TTHSoXg/Gg4GUBLSDNDIpimWFlGsN/vN6CeL8YqZGD7HnfVDJJowY/G1+l0YnNz82qdRY1mwkIP4RaJaVZ+yDBOxFeUCYsYlE+n07KIqE2aymppZwBTylx7UfxDq615UCCy+McDUQmjCK3rMqvp8YrazQJ6v5ZC5G24cGaekG071CIcq9Vh8OxjZts+NxaOw8dIuJm14XMUbx0Cd7vdklySDCie0Vx1jV/viumximSUvxWXlwA/4vqDGTw4Wiwut4r4y3GylXQnkuo5QZxY9AzyXPJCikf8HJWFjHImZf8dOnAOVGyec6JLAGgwdDyi+QgjCSmvcatH689+fRykNY0bcX9ENCwv280CdrXnkMTLm6xzpsDu1Ugj0pvxhEM1KYc2/nJblpIE2cubqDCeQVU/eslwUYov1oD4hon5fH7pWVxofCFNdfSKN1cI3iRF4mXKxML2qbC1eEfQy5XLA3iOmeOkwjr0oeXLslpuqXVc12ZQTG2R+cTRVB4XMJU3eRWPNwXHHMdHxDXYpfZpQChgHsh7DOA0YnHpgDwAACAASURBVBDP+bE9QbPMEGQGVZ6PhkpyIMuvecmI8lo3ZF4ybyLvxTYWC1uUpGVnoVKImIQ3nnkSpszwuLteCrLHFxR4whV+sowXx8HJsn+HY8yq8Dg9AwN7QhrVo3K6B9Jxt9yuMByfeyuHf1kRXGGswYxTpvgU6MxTUdn0P6uXeaMavTk3z3iy/QzSKbkkudOCuR7r5Q8a9GwZx0tl6fV61xIHHF834mr/EglAL0GrLW9BF+nZKHkgEseJx3PuGVxpWEdMdgWgZaLV8hV6FzRBABKUzHQBVz8eTLpFU18ZDGL84MLvcYYLmIrDGgoZIQcTAOyT6yXMeLnnyQqhI+nviQ+ft9OEJVNI0YM7Ikh/Ks9sdnk/lZRG9XW9FEO0lxdpt9slk0vP6zHOZDK5XJRUyRbxNEEKMIVL1zGNS+/kAsy2dJ5wgULrSqRr6C08ySAISeH1eVBgnJFkpv/3+INwit7CFbnmMTgW0inb1+XK5ooiurjQcW7eHgVb4/b/6s+zaypsR/85z4gmnHMYR+hF/vlWJo+v1L48prJjuqmP70rt9XqxtbVV9joqW9tut8uGYY3TXyTbgH0UWBdgCiMtPGMRZbB4zttwKJZ5LyqQu07VIy52y+zWTUXKm+0uzVy8B9xqz/ciySI7rPC5Upgy6+0KQ0Hy/WQcV82zcN6CGD6WiObmQQollZa0IVSiwommKrT2+q3d65wvi3tzjp9ySA9IWKnrXZ5arcutVcqqaqtWr9eLjY2NspjOZQ+OTYkljbGkjgmpGBvQy2jg0rTRaHQNa6phKY57FCcQFwjVhp/zdslAbgEnMyjQ9ChUPreCbm1lzfhdgyqO79U+BYf/PZ7iWFif9HL4UwtaeQ29jZTfYadvvPTC+ErFt+eLX5yHCr0xz9Gr8LjzhTGjwynV9/hOnkPX8hkRUmAtrqtN7gWj4VfpSvjViAu6FIUQTVtMCGUoYNybxRiDRHE3lxGzpmBigCamb40ni7dExKwQDjjUojfjfHV/Ss2y+zz4TQNFhaHQ8j+FquZVaoW8oVdRm9nuXcYEhMSuMKK7jFbmRWtGJZsnjZD69B3cEdffm8k4h4ZPfWg8KysrZZfAyclJgV+EbOSzy0iXWass0JbizOfzoiRep+aRNDHCLseDJIw+mQfwwZOx/E8rSI8gYsp1uxV0uEIIRuhG/E5m08rRQpJhLnBuhRl3uZAtg19s3wuF1uFcBgH9O+JKuXiMWVRf/MuUhrznWEgjGjZ6K092eAJFxzlPGqT5fF4WLtvtdklADQaD6Pf7pU1/3gINcURcPmSPlp/KIYGdza72YnGQrOM41ZWJ3xRwnmOMkimH/3biUpg1SRdOv3PRA3RXZLWT9ePnfGwsNWFkLODX0NoSw2ceJbP43jcF1610Vs/jMtbJYFgW27nBYBuZ9Xcau1ejIeUtxW54WV/jFTpiv9ohwpQylZ7esavVT1Ui/BJE0n30tPD0ILpe2/rd+zBJ4JNyJfHrOTEKBa0yFdW9gurKAPD98WpP9WktHY5RGNwruTXMBNqtHb85/oirh8URDrlieeE4szqZwBGe+fU87+do3QlTqUDkBdvKkg4cH4XdC9ul4fBkAOFZu90u+w07nU5Z7acSzOdXe80YB/sibleDYB6b6yaMVdxL0AJQuUgkts8Jq66ITUtLIarFAf5bxPD7cyTcIgD3Hake4w8Kuscj9EYu4K7YruQkus47JPHi9VkvE2CONYNxEdcfJkFrSq/AOTHWISwSXxWvsB33zPr2653OrsAZbWpQlDBMwk4oxnb9oR7z+bwkrBTDSIFEp/LACioBb6DSOWeaCz+tL4lMglAh3bILIrE+lY6WPqKZWnTsL8a6BZnNZuW+bz5tkXPJGNdqtRpEyzxXxsDMWpMW2XqKCxTr0Qi4crBklpt9Ey67wrshIAT0MXPhUzQgHZbFbDXPwXE7PTPloHLyvBRlsbh6oS1llOsz6ltzubi4KIuUfKtzlxsU5Y4Ut3AChF2aLAdB76H/FEQy1uGYf7xfv16FKUUKUnatLIbGqdShrzpn0MPhVSaA2bcrsmN7KkBmQQkPWf+/c/++B8g+Jqcvx0/I6TFWq9UqqVeHQOQjoZXmvsybUlEZF2pc9IiMT/VbH3pE0UFtEoprnDTErdbl8687nU7jxU5dCjrTxI7J2TCtPOMREcOZwOtJTD/GdHAGv0hgVwh9u5dwKCEMy+dVUXE8TskCT48fMqVifadDFqeor8xj8tuDZF7LY4ROKm71+d+9jdpwKKqi3b/iNSFQDSbRMLjxqCm0z1XtO1SU0rriOizX2ElvlxGeUyKh0+lcBvjcrUkL4u6ZikEPweOcJF8QREhHSMbBa5CyWJk7Z3GF4KRrDIu42tag7+l0Wu7U5JMSszkxLnJPo+LQgeMjw/0/EwiMLVwBIuLaOo97xZrnqcEk0Z64noLIsRHWupBncRzHyOPq0+E2acgYhMooXug4ISETJFIYX8NqtVrlTl/yWArFzZgywF33IiIChVrHVDIrT0GlpfX2yQzGRSqeIKDGZ9kgj6sygis4F7xk1kNxDAN8xlHsT9cTz7Mfh5AOIzx49mt1jqlvFVp+KlJWT6WG9z2WcKPI+ZPG7nVJZ0cMvreLhde5QvnY9E1aS0kEqWgkCA81drapb9WhfDJs4O/CDxFBDVGLPSCntXEYpYGRsPRIXDvJsD2v9fjI4YuuITR0ovO8lEN98v4bCosIL4awPTIrw9zs35mrORFf8zoKFBXKFdWFt6YY3rZ7Ma/v/VChs7FEXH8UFY0NaeprXm4I3FuQxhFNnijuFH90qzs9PT2saOZy5nItg0wZIV9KDO6arwYlUGposbjaFkPBZqGVd+jg3xmjXPlcGbyfrJ1MQMjIbMyEGBHRuEOOLp7pZhce9y5+jMpDQaL7p2J7XORtUtjcE6gehc7pzLa8fSo+lZzxDxc2FSuwX1ds74MWn56E17NNKhqfxe1rY5qf+JUpCukr9ERU4UmowkMnIL2IiMIJegOcLFeFCbfYVuaRah4jw7r87dc4PHABUF1awIhoeB5CIQV2ZBjnQ8xMZrNwHp4soJBn8Qq/vXgwmkHHZXRwCOV1M+USzSS4EniOJVNAtumxCCEc+1UfpLm229NrkDaSg9ojcz3O5lgpOzUetd1KUlgzN5tZCicqtVbXijjKY7s19IG7Z8owtvftloU434WCniSDNRqTFEZWyhUis+A1eJQpM2GJwwZCWtZznM52anShAGRe1nnhPPA5i76eDMiUxe9OdHqpLa6cu5L0+/1ri50ZnPdFUvcYPEbYplKTieJZMiZ6rMDjVJiM6OpEbo8DZ4DIsswiupchVMg8ndqg8LGeZ0B8PGxD7tzjGTGSzKewuPK4NyI9+a1sG4XfPQ6Fi/OQMXLvWVMYF+6M1x6/uEzUFIVC7+edRtzj1W63G5se9fAI8oN0VVuaN6EyjXtN5kQzh6up3PBi11oOptW6Cow9jqD2kgmZUmXJg0zoXPAdgmVWxeu6d1JxyEVhpovnGCKioTQKNDkGKoQH9ISkmifvnyBddLMUH+4gocuyTByHK7Xaryk1C+fBsXKuHqBTKXktkYMraubBdRej6kvodUxzdsMpY+xejnRiJjczHlQuR1Sca1d/uNVEA9E3hS/LTtFluTdxxr7Jojsj3aPomHsXVxqHNZmC1RIF2hfELROEf/7IHbVJaMJ7IzIhdxilY+KFbpHVt0MQGhlvh0JTK64s/t/b0G8d53pG1rcvhronozchxHUFpcGSAfI5KxvGB0GKRpTNDCll868t5JbbimvEoyXwYN8FO4MSGQYUo7lo6QNzSOFuPLOs/O1EcYhARfFgOVtFz3A7t8+ozywGZP9u/WiBRTN5Fn17ytnpzi07nJtbdbfotSJlz+asb26/Ie1Yz+M7jpfjoydpt9sFdpH+3H+mayX82QM3nO6q5+sqHIejAadZ2XWsb0IjehHGKqznRCDEkUDQMvpg3bpz4DzPjXAkjHuMWqDp+5yy4msHHFOtOOxQIU25BYPMUB2NTdaWVtv3OTkeJ/xxYXHauIflHNi+6lFhnMYcR6YkLISAjLk0d3kipqDVjtONdKWyOXz3ONw9eRa3UrkdtbRarcvbijkIdujnOAkxNRMQ1ZFw0oK6Nc32Y+l6F8LMYjjcIGM5UaZmawT0RUq28TaFe5O4/4jMcEVXfT7UQbe/MrjOjEgGF1SfsMnrsVBonX5ZgE+lI9R0D+SQV9a/vBgIsZ8+biBrvHalJ40z7+vy4FCZ/MtKqa+OGeCQONRQ3y9FzXeB1fUMwCKuu1PPRNCTSJgI5dzKuoK65aFHcljB4xR0MoMWmvRx7+NCpfaUJqe1pbCpbUKf+XzeeKg6mU2P7YqcxSkUMI6TljSbM+vWPLX36QKaJQEYl+iV35Qj9zzuyQiTCemZLeTYNU7RV/KWBfqUO/K7LBhrQOxInWUKlEEYTYIxiGu4exb+dw9Ghrpb5jEXlkx4a5CL7YnYFB6fRwbv/JyOMeZxb0NPyuuYBuZ4amN2GmcYveZF+Duz1JlyZG0RRvp4+O2C2+l0otfrXRNYGgJfL2GfCuRpYBi3ZfxT3zJCbryysZOWnU6nCcNcMcgAMVJBEs85nKEbpXBQyGVVs4nxWk6UDKX1+e9CJSo9b+pSW1lxJckwbcT1+yJIv16vV7a206upyPLRs7gQU6hqY9L/LHYgvTLFz4STUIprQG7IWLh7W2OR/GgVnn349VQUt/bs2+MtzcFjHF2rMeg8n83m43Ck0mVj/nuZleIuXg3C4w9aFCmIsjz+sGdnanaMno5CRqvi37L07jU8IPQ5Z3TIxkPiUsFJN86TaysOdTUXjTnznJlQ81pmz9wzq2juHL8rCedJGjNOycYho+iwq91uN15KlMVjPM5xZYmMiCj303gqn8rJOCXzlr1er9G/902D3nWLWhNUMZWBMn8TIvmNUbQIgmuynL6olC26ZRaz3W7eMegKkgWm3g7hjAuuW1UaDhckHyP/O5wl88UIxmWLxdWdnKIPaeMK6v9pcd1ocVyu2JpPJvwZfPP6rKd5M3mhdRP3JJ5FrMVdjHU4Dr+nRnPzFx352FT8IYycE/lWYhYRMSOCKpLp7IT3slMAKcQM3sRQDUL3xDsBPVWsPjkJwRoynwKSEd1hjLt3jpelBl0yC5/BRY6J/ZO5mhtTtqKJlMdf2eCBvvPOdxNwTBkMEw2YttZ5t/oqqkf4I2XR1hVeR+Og+r6exPFwb5knYbhjQR/1LegrOvDj8ukGRWOiEWvkzjLIIQKQwIIInoHQQAW36NZc0WqZKU5afVGQSHQKg0MLnvP5UCjU7jJ4kx1zwjpkpYd2aJrRWcdkEcUoPrSaBsDbySAVIRTpWIOXWUzpltz/05NTULlmskwRhSw0T43DIRnbYrwrryEF6Ha7RUEJ10Qjlxf2xzGSHkVuVYEM9nx3q3W1ukyBrVnViCuFIHPb7evvVhRjBDlUmM6NuP4iHBHK3xLssUjmYZyB7sJduVkngzUsDln8zsosPnKYK/opoNZ/0cDbcC/g8xQU0njdkzoNHD04vehJ3JorNvFYge3SO3gCgDzUNxMKpJWewMLxZPCbcXUWImiOpKd76Ha7fRWz+FqET5CLRuxA0IDMF1P9CZYuTLS4shjZvQgck0/QvQ4hnSv9mwoNRqZkriiEDn4965OOFHIKIqGSjFNEM+OkhUsKgPf7Js+YWXu2EZGvr2RQh+1pzSTi+gJmzTBFXD1nmLDTP51Op3jcLJh3euo/F8XFD8qQxz26Vh/OdTabXSqLPzDC8XAWVKpTpjgd/sjC1GAOc+Rql7+5FsNJsb2aMhD7L/MEHistg0k1rO713Dp5e6SFr7vUPLfapNXVmJcVelzO0cfhRoJegNe7t5CwU7Bc2ZxGmrPkQ7ErFVBQio+PFQ2y+JFIw8fuW7DUFpXEFYbKJ6XrEgZRCB3+0FpLiehKS8YgiS88HnHcrb6lwYqHuHHTH72jPujZ/E5MjtWtsYpbXSqnW38SkYkAZ5wrKN259++wICsURNJJVvdNnsXn4PNWu77mRKvsysDA2s/TkLmSic5qQ+Njckb9iu+ONEhvJo381guXQRpyJo8I0Tx+ofHrkgFOcAoOB+UDIhHo4nh9xNXbc3U9BxJxlX2Yz+dlN8BkMmmkUvnee3o+CjAhDAnjGSEVwjWnAf9TUZxp3lZWXDEz5nhd8sITBj4G97ZeJ/NwOi76ZguNEnp5Ego+jSuhU6Y8NZpJUKWwUpKI6y+UJdSjsaJM8O1hRDYyqG7YGEbUbodotVqXe8MouO6WyAAXFhE5sxi0HIQlGiAHQu/jnoPKo9d867gmT8jm7WXvfnE3S4/C/slMEm1Z8QC/ZvlcUZgW1rjflBaueRMqfxY7+BjVNm+08iDbPYlfKy/nMW/NeAgyCdU4utH4/UW+WbxCzyG6EUm4EcjCiojmLSgusxFfvHIic89SoJoVJQTQotOyLIMKJ+zWUtcqkJUAq2/d5xBx6XH0dH8pka6XAun62WzWiMuc8I7VMw9LojrT3yaBQOVgbKTfVBzCWRqATGkz5XVBV+H1bvwy+KRxecxHo8drHdqoT8+AEu5pgZqKwzZEN962wHGz32zNhryj8jqyIO3oKMi3bs2FZ+5YaTqlNckIhxIZbHCP4gGUhEQvm6FLJZOlBOvr6+V6Pcx8Op0WReND/NQW04iZq3Vh4LEavKodp4UnPakYjPdY1K8rEa02rZ97Eh+XwzXR0de8iA5qXow08oSA2s+SMG5wsztCiWw4Phdw5w/3rWXGX/85FiIkjlttq74MeZeKIKZpDw8JyKdruMdwZqq4QhCK8ByFiuk+uWAqE3En8ejq6mqsrKyUFVu9fKn2yj715cKZWW/BC8KMzDj4tVnCgMW9WCaAhBmuBPQKpKGn8l3hXZB4rwmhIOstUxQ3hA7BsrnQEHj8xoSQ3zNFWaUx1eshMv64B5LMcW4cN+fJa7pc8FHDXIHlimfNM2RexK0lmS2BZ2HWo9W6fA4t7z+QgjDYIxMcy/Z6vbKVRt5GyiMLpLnp+hrDJfjO/FrJPI1bXlqsLB4krTKrrDpO41qcQyXxGJNQV+VNisLiN9QROtYSQBqveErBp/HIaE6kIuNAGXFFIf3ofTgWypErjOjRFayS8PAR+8TU9Ai09hwcAyUe50Ia61HZKJSakJ5Hy+tpmThBD9ooGHqWsfL69Dq6lt8cE4WvBt0o3DqeCawLOKEZBS1TSI7BEwcRzcXZbG2EH8KsDL9nHsm9n+rSy9ESexscM8eo66Qo9DAucz5OzZHLCupLYyEdNTdfU/GxULnYZ3djYyPNDLjLctdIZXKGZlAtm7jDN/UjRfE1ksxqZYrjDPUAvN/vl7Ez1qHiUWgz654JisMbx9qZyycTSd9McTgvV+LCUEAwh23cGkL442Pz+RDu+Zictp6ep4fQWDhHCqdiFwXzznOHScuUhwvGbMcNBOWJ8prRo8uDLFSODOvRCpPhFCz3OPqdYUgWPuHcMS/fo8L2MliYeZpr1uILF84t8Z6OdqHPBI3f9JKZwFBgM0/iDNV/54srg0MhZrXYtqOFmgywH4dUhCfs17cAcQ6iqdr0xE+32y3ZMb6ijvxn2+55SXvKg0Muz375dRwT27r2KCSHGfxPj0IByCw7vQ69S2YxVEepRAmirA0n5GsTTDq48jpz3RM6MyXgdMtSIHkh0sXruUA5Qx12uVfQb0JhMVS/eZ+GzlE5WC+bJ3lSs6j6X/N+/M2S0ZbGgO3qnPgdEY3YhYpH3tKDMOnixWmdeWnKjSdJMh51uZvY3S8Jw8nqmH/XGEKNVYaLKWFa8IjrMY73WbMSb/O/5mapVBw/BVAJA/bNxdFaH5ybW0P3SmqXQTc/zkSuLWSelH2wH/fC7un8GsIuFyjVYdpXxSGbZEB1iSCoKLqGcJzxLA0X41qOgQrgUDBzBPS2pF1jnUWC6x7GBZKE5du5XNtZl5NxnO/1OBEShfd9U6nJ4ExYOQ8X4AwS1ISDRXMRAxhgO5RhvFTz3pyHe+0s5eyC6gt+mafg/j72nVl8h3IaO7NK3BVBYfL5u0H1rKZQhuSJ8kZ0wQXJjH4ZPdSOjlF+PF5y2pN/RDvlnZI1KJMxupbV8uQAXa0K++CWDkI1DZLviFG/LtyZC3YFqVndGlanopAZPEYoyeIwjBb0bQstpJfMU6rPDAa6RXbY4UJCAyiBZV0XftLLFVGFvGJf9BorKysxmUxKDOnbfeTBmQ1l1oxK6/DNDQw9Z4acVJjqns1m0XV35YG7mEft9HpZjMKgONN291BsQxZIFiWi+dJM9sW2ON6a4vs1rFeDaFRQ9zr8n+1U8D7V/rLiSuieMWuLfWb9E2L488pEf+/HPYjTRIJIQ6t26LWXxXP0eh5Y+4MGNbdszjSgtQDdz6m4wXYDouNdCjO9jGuiiO1CWINrEdefWKlzGdFpEXzHKUsmCJyUwzt3q6qfQSzH4yReZkwIP7M1IM6ZTMi8mc8nq8u5uVX3oNuhm8/TvYNDQZ8j++I14pkbWfdeVDwPtLXepbs5GcOoHU8KcbU/21lC5aAsUKHYthd6VV1fnnVMLEfCRFwF3G5hfGBOWLfKbomceb4vjMrrgaIz0IVF5zgu1iUxdY44OYNeThMxn/Azc+ccP89RMDm/TEFoENzK85jXc77oP4XRjUEGM135aVQcqtFYOi3cA7viEU5GXBrM8Xh8LbmSxaiZx2e/rkCkBdvOYH6ng4fsZbjSBYaE4QBruM8VQtfXLK0UZVlCwPeJqW1XIrfOmeWkVSE+5XyytqlYLqDujVQ3Y2Cm9O51HArwWs0xu36Z8hD2ZtkqWmvV97YIkSKa8acKobvTn3Kk/mSwGYxPJpMSz1C51Q/Xu9zQe3xD40HvnHk9GnrNpZtZXTJHE8u0zpmewQd27BBFCiGPQqviSlmLB1yIXHBccUlY/ibzHc5kQk0v7ErD/txak46s58apNjfRO6tTixM0Dn7rWodkTKEuizlcyF1OMsPjNNA1NCaCZdzvpQVKHc9kyQWdvHZPKEUi7fyBLD6PiLhUlswqk8E8LiI5kzzw1gCFR5lDV/siNtPQFDyHa1nA6crEvjhpFyZXmoyRFCpdTyybCW6mXDxHQfN4wftlqcEh/nZPWlOUjIaMD1wp3BPTW7rA0mLzPxWGdMzmrnOUK2XO/O0ETAM7/2i8ua6XoQ7npdqWYkV88SgkD9wd65JgZK4rDBlGwrbbzYUopZJbrVbjuJTFH6PE4lba3X673S5eKhMqZyIf1u0QjVbGYZt7OL/WaZYVQo5MOf0/5+tK6hCE12SeUjTk+ouPX/3ov79vvqac9ErOI9KWnklj4xwcxnr/UnB/Q1q2yM55y3s5b2lcMifSdaFzKEYrwYnotxOCjfv2BY+BOBkO3pXUBSxLEsgCcEXdAzdd76ve2fjowumNsmyZC6If83F7fX5nxQWYx7PfKrK4KhSGxWLRSNnSimYoQ0LrsQYRgWfdOO4MPtcMEtuWh2GmrNW62p2uMSu28aSC91+D1TxWWyLoekPszK0jPYUXWQr9dljFdikYmVunW848jD9YL7MUPMZ7UeTNPN1JxRGR9S2lJ0TJMj1uSDIolMUT7g1YnGE87lDDg3JXPsIV8s0RAs8z4KcQiSZKymgTJANp8pqGy+MD70uFEGs8Hl8KLB4bTHqqvhs5yiIDfmbe6AXp7TzY73JwJJwzmwylUjDfTQvFO9fIYOJhxTOs5wqn61jEcGZQeM6Fy7fmUGHcozLB4CvfZAr7c/iqMZOWPE6FZt0Mv9PietFcqRhkfERTADNekNa+LkY606No/tyGlN0aTGGbz5vPcHbvpXnSQzHhwGDfs270/FLGbOHV1+w8A0Y50JwYY5d1FgqYY1IJCC0T8a2UjELpwqk6skBq1z0KieA7jjPiaGyyaHLbJLb6p+LTjWfFLZYTOPMCjosdYvA3magx1TyMM1UwhG25R8uu53hcYRmLsR/Oww0r6RsRZX+X80r8GY/HjZjCi0NsjYEQkeiG6XvnDRMEPO51I652h2T3+5OfJRvmgSs1nbDGrYt7I7lCbpLjBCeTSWmPk1d/LigeH1B5NAZ/VrII4flzKhEV2921Co2BCEZrw3qZoFKAvS6NUeZR2IaMDMekcx7Y+7ikJG6JddyvoSfz2NUVyedAb0be+f0tjP1oWEkXFs6ZWTAmKNifkAOfeEmjzUQT124826o2Vb9kwzSoDG6RMG7t3XULmlEYVfTwCH9qpSuJiOiWWnXdnQrOcYIibGYB/VjmCdyIcJzOUBekzCq7Jc+ETYVjkhekgcmu8f817yd+UznJzyx2lPBRkDzZQQMimvG/FN7RgC9GOuTkOCm4oh/jUsZUerwSvQ8NC29jzowmi+ZcYhYKgLTfrb1DKhcmrrzS/SpVLNfpbj2zvBHNQJ6unn0xW+KLg2ory3bR1bvldKHz9rxehntVPG5jYfCs4krkFrVGL4daDvtY/Bz74+0aHKfmyXjBeeW3FFABiEZ0LY00V+JJi2zOOsc4hB6q1WqV5QNHHJRLGk2/hUHKTefR9Qp0z25BKVi87VPeYjweF41W0RMk3fpmXiUTKg1Uk6eAEpPSpXI++l1bAHOIRoXivN2CemraoYjHEC6g+k+vIZr71vgaTWi0OB8/xuuyMXEO7smcdqK7Kw2tsupTAXzjI42fjKgrPAuDfEJ4DwtIw4go2/4zB0B59tQ529d3ua1YxZlPoaQ3cUHRo4ukKFQ6ehN/MqT3T7jhMI9jIsNpuZxxFJCaUjoM9Hk6PcSUbC2HEIoCymsJ1XhO1/lCqRsuCq2u9/ETthBeSfDYHgWa9Km1yblzjrqWHl39cS5cH3FjSMTAtl0OnUaUPSVvpPhuALN7ZXSdwzImiBpvK6YrcwGmRfEMS7/CIQAAE85JREFUiJ6Ry81u6ty9VW1hzy2zruFxMsuF3N0rGcc2dZ1cOHEs65D5LIQk9LDsk5bTFYdC4EpKYSa8IA9IB97sVCvE4PrNe9xZ3IPS4GQGJEMgblg8u0UaMllCr+IIQoXCy/Fy4Zu0i7gK4im3jKkJ0agYHm9HRPM1eZy4B8UUBDJxZWWlpARbrVZjcJk3iahv3dYxCQCJ5mlpJ6Ta8IwGhYuFHtAtKufr2SYKmH7z4dVex72bC5yOkzkMpr3Qoy5TEp+He0ZZ9ww+kV6kgaeXXbDf1Jbo4ciAfbAfVxpew7lkyQbFskomyZD7pk3RnohA1zOWLDDMGUP8lhFejY7H44horpXwkUJOYDLcPYmO09q4paN757oKCSghklumpa8JV6a8WayRwUX+9j5ofNiO5pAV0iazbqIlLbba9TFTyN0YUQgzi+1zyMbAMbvHmc2uXhPCthwdsA3KlmjEpIF7ZhXKL5cT5EGkJJJZPWBeYyXd5JmkZJTFrm6qWeYCmRWgxlJLGWM4hFJbtTjCMaVfmzGTj/p06zSfz8v2CBHdBcFjHmdAVlfM8LaopJ4+zrwnr+X1Ou7p2yzT5kwm8/Xbd167schgVBan6LdDVkKnrA8aSr5SQpbb3xrHebk30zxqSubjYvwiRZnP5yVkkAxpzxk37/Z6vZJdlbK22+3o6kHaEihabb0ThTlxV5iIq3UOBdgep+had89u5bJjxKJkLktmQUV4Wjv+phBQGLxtd/k1RdFvCk5mkTVOunhCR+234tYRPlvLPU0WcLvXIW19zByjwyG2n9FKPPc0PmEtFcVjSs9gqX9v2+nPlXYqsEM7eiI99JwGXh5G7agvvXNID8jXo2G7W1tbZRDT6TRGo1HplHhPLoyEEswh7KJ2Z26X6y4OnRjsMZNC/ExFovCJoJ4/J3MdKmTWeplAZjAtgxS12Ice0OMbjjlLHXPNIuuHMQTHy74cevFa0lDClS3Iqn4mnBR0N04cG8ef8ZNeQf/ZNlGFKxLjDx+7Pt1ut7xtodVqxfr6elEKvdtSL5SVsW+329E6ODhYTKfTGI/HMZlMYjgcxmg0itPT0xiPxzGdTmM4HJbX1V1cXMRkMinP89IAZFXoXRwmufumktQETZMVMTh5t+oZQ10wGANRqERgEt6tNgUgE1oXBk+SUDCWebHa/6wsa5Peyb2G6tHDZaly8spvbXC60VC5UaDnVrvkpdrP5kyvK2HnmCOiwCu2LQWj59DrwAW1NjY2YnNzM3q9Xuzs7MTa2lpRFtJusVhE66c//elCjcui9Xq9MmBp3XA4jIODg3j9+nVRJCkNX13nwT3jl4hm/KFjnj3KUpqZcNA6c0Eys6QsrhRkqEMaXp9BFLfoPu4sTnElZ133asviHB3zeCJTzux/pty1eXEZgKvdnnnkmDLoSAXkfLO4LCIasI0Ll7pWx3Scbznmq/36/X70er3Y2tqK7e3t2NvbK29XkCOYzy9fTzIYDMpYGtt8fvzjHy/oruWK+MDsdrsd/X4/+v1+rK6uxtraWkREnJ+fx/HxcRweHhblEZSTkjCeySywf3vMUsvSUADYnnsYx60OCbJtFlkfNaFzD5oJTRZDUHi8PZ7zPv18NjZa9CwOedP8ascleL6IR8VwOEb+eHYvg0v0DKSBPAOvp9eIiAaM6vV60el0YmdnJ7a3t+PRo0fRbrdjOBzGeDyOwWAQk8kkzs/PYzgcFiURYpLRn81mJevb+tGPfrTgQOWe1tfXo9frxfr6evT7/dja2mr87vV6sba2VupERBwcHMTx8XGcnp7GYDBovERosViUHcfE561WqwHnnEmON7MA2z2BmEaiunfwMbhg16y//nvgK8azHQawmRLXBLMm4B6TZO2oLQom4aMrEL2Ce/DM2mfwrAab/FgGmwnROCeHx4RWEddf9tvr9aLb7cb6+nqsr6/H/fv3Y2trK2azWQkrRqNRnJycXPs+Pj6O4XAYh4eH5f9gMIizs7OYTqcl0dWKiHRrqjR5Y2Mjtra24v79+/Ho0aPY3d2N27dvx8bGRty6dSvW19dja2srNjc3ixL1er04Pz+PZ8+exXA4LIrDWMczV3zEaxZouwdaxhiWmoJF1IPmLDhm38TuDkWykimKC6lbcPdE7ikcOuo60jXzWpli+Bg5f6cXldjhH/877b14HKVxuRGQQrAOYZbQjuRyd3c3xuNxvH79OiaTSRwfH8fZ2Vkx4i9fvoyjo6P4/e9/H/v7+3F4eFju9nxTqSrLsrK6uhrb29vxrW99K+7fvx+PHz+O3d3d2Nvbi83Nzdje3o719fXY2dmJXq8XR0dHcXh4GMfHxwWmyeNEXAmdIJIrCy1kVmrWyi29+qrBFv3PvIr3ldXjbwq2x2SO1x27s69lc2Ps5dArU8LavFx5HEKJN75RlcKt8xy3Z80yxckgl47Le/C/gnR5kMePH8fGxkaBVPIKkrfnz5/H559/Hr/5zW/i4OAghsPhtTG8bfkfKYuXTqcTW1tb8Td/8zfx+PHjeOedd+LWrVtx69at2Nraitu3b5eY5/Xr1/Hs2bMYDAYxGAyK0hCSSXlU3PJnuF31XBgdDqkNMs/XPXQsyyIRRmaCyfqLxdVuAh+je46aMGm8LA4l+TuLYdgvjyvWyBRS/YjeHm+wPmGUw2X36tkYHYJFXMqU1jc6nctXOa6ursbW1lbs7u7Go0ePYjabFeXY39+Pk5OTePnyZbx8+TJ+/etfx2effRanp6cpTf8n5Y+iLF7W1tbi8ePH8YMf/CDu3bsX9+7di52dnbh9+3Zsbm7Gzs5ORET84Q9/iJOTk0ZqWsIo1yhmUWCcaTpWs8K8hpaSDMqwuyvDsmNcQMsUwRWe2aU3BeC6hoqhuXgfDm2cVvQAThc3Jk6zmkdZZngyA+CGQX1r3ArO5U2U1n3w4EGsr68Xz3F+fh6ff/55HB0dxccffxy/+93v4j/+4z+qW4n+t+VLURaWbrcbH3zwQTx58iS+8Y1vxJ07d+LOnTuxtbVVYp7Dw8P49NNPYzwel8yDAisJhhOAzHMv5B7GGctryDSuAei8r1O029cfnRQRb5VVywqVZll5U2y2rE42Nlc0rrF4oiEzTt7OMkWteRH9p7KsrKyULSibm5uxubkZ7733Xkyn0zg7Oyse5MWLF8WD/P73v/9fwau3LV+6snhpt9vx/vvvx7e//e148uRJ7O3txb1792Jvby/W1tZisVjEwcFB7O/vl7Sddg5w3SbieiKgBt303y0thYRpZApdFqS6EnqftcC61h6vf1toVoutvH0KcE2Zat7Nlcy9YUZPQjLSxLNZjEkEsfr9fqysrMR7770Xa2trcXp6Gufn5/Hq1at49uxZvHz5Mn75y1/GJ5988pUoh5evXFlYtre34/3334/vfve78d577zUybRsbG3F4eBivXr0qwRvjGb/fg0KQWXgpBovDGl+MU/u1eEDFM0hZWjmDMDpfg4ysyyDZA3kVKrx7SJ7LAnUVXk9F4OKgaOf0IhTkKjsVREqi8fV6vbKC/t5770W73Y7Dw8M4OzuLly9fxuHhYXz00Ufxk5/8JI6Pj5d6uS+7/EmVRaXdbsf3vve9+Ku/+qv45je/Gbdu3Yq9vb3Y3t6OnZ2dGI/HJSlwfn5eFouUbuYuAQpXFics26bv+8o8LeqCzudTqZ7qeApXxZUiiyuyTBnn5YE62yJc9DGIRtxMyP+c99tCKvdKnm5mLMKMVrfbje3t7djc3IzHjx/HdDqNg4ODODk5if39/Tg4OIhf/epX8eGHH8br169Tnn3V5WuhLCwPHz6MDz74ID744IPY3d2NBw8exM7OTty6dSsWi0XJcAyHw7JPTRCN3xFXXsFLzYJzgx6tMNuqpX71zdVtKhkhUKYwXMPhOVcOL1mgXYNKWfo3y2J5NjEL9j1jpt88Lw+iJ98rcN/e3i4GUYuBR0dH8eLFi3j16lX8/Oc/j08++aSx9vZ1KF87ZVHZ2NiI999/P773ve/F7du345133onNzc3Y29uLlZWV4qK5U4Dbaxhz+O5ZCqeORVzPdDn08Jgoy7oR2mWQiyWLTxxKZV4qs/Iu8Owj80YZTOPGS17jmUOHmvrmvR+KRRS0r66uxs7OTty7dy96vV4MBoN49epVnJycxNOnT+PVq1fxz//8z7G/v/8nhVrLytdWWVQ6nU584xvfiB/84Adx9+7dePz4cfE0a2trBduenp427r/hXjT3NsuCdmW7VNchC0vmWdSW7wxwT6Jx0RpLQHlPUa1v9ZfBQ4dw2TH3du12uzxPgellX0ciZFObZQv7F+PQfsJOpxP9fj9u374dDx48KPuvtC3q6dOn8fz58/jJT34S5+fnbyUPf8rytVeW/9/e1fUmsUXRNaDMF4yDQ4slpNWHplEfjIn+/59gojYR00RqrFQEHKbDMDQVfbhZh83ptNKr10vbs15IKQwDnMXZe6299xCWZSGKIrx8+RLtdhtbW1sIggBhGML3fQBAr9dTZQ6SOMDyDsOdR1ds5MKTIZk0IPlcqZwV7Sb6IuX/9QXKY/H4cqHqjVW6IMFjyM9I3l4kNevJPhvOSHCZd8jPQL5HkkUShe56pVLB3bt38eDBA0RRhDRNkaapqr06PDxEt9vFq1ev1i7UugzXhiwSnufhxYsX2N7eRrvdRhAESkVzXRfD4RDHx8c4PT1VxOEvN3ccPUbX655kqKbnIcD5CSVFC7nob31X0x34ixb4Kj6LfkzuAjx/XUIuek265iSIrsJJw5Gdh9xNWFTbbrfhOA6SJFHeyHg8xuHhITqdDjqdztqGWpfhWpKFKJfLeP78OXZ2dhRpWJ9WrVaR5zk+f/6Mk5OTJdJIg1OWz8g8hzG8vkDZQaiHUECxZM3jFUnOumIl71+VGDw+cF6p4nvSZV2et9xdZVmOPF/djef9sqOQDjtLUE5OTpZI8uHDB7x79w4fP35c+T2tI641WST29vawu7uLdruNe/fuodFowPM8BEGA2WyGOI6RJImqDGBNmhyJJBeO7mdIQnDIh2wBBs5LzDJJJ/TQ77K/pRRc9Bj5OP096I8jGDbJK67xfj5Hz4N0ZYt1W7ZtK29sPp8jjmNlIsZxjIODA+zv7+Pbt29X+i7XFTeGLESz2cSTJ0+wvb2Ner2OjY0NhGEIz/NQLpcRxzGGw+G5dgFgQRLuHEBx+Yw+VVPmKDLP0Bc7H1/0PD2X0Y3FItFAEusyUhX5L3LUj34+zGPm87ka6sCedOYksk5rMplgNBqh3+8jjmO8ffsWBwcHyPP8D3yj64MbRxaJO3fu4OnTp9jd3UUURdjY2FCFnI7jwLIsjMdj1dPAYR0cmseOOS4kOVyCt0ULVPopvNXDG0lAokiOlvmCropJtUy+jiSnfo56qCaTeSpYwKKn3fM8VCoVNJtNeJ6HPM8xnU5Ve3m/38dgMMD+/j663e6f+NrWFjeaLESlUkGr1cLjx49x//59bG5uwvd9RZpqtYrv37+j1+thNpshz/NzraUyn6FQoOccekgGXLxYpfxaRATg4hCtKNQiaaSapp8P8y2GVHyu9ETorruuC8/zsLm5iR8/fqjOQoZaX758wWAwwOvXrzEaja5lwn5V3AqyEJZlIQgCPHv2DFEUodlswvd91azGGiU2EaVpuuTbyOvAkEhccProJv1XXK8GkC56UW7xK0hhQS56nlO5vLiymWwdoJtOMLxi52G9XkcYhiiVSpjNZkiSBFmWIUkSTCYT9Ho9HB8f482bNyt3GN4U3CqySJTLZSUItFot+L6vcptarYZKpQLbtnF2doZ+v4+zszNMp9OlZjUAqtxG1lXR3OOOJBdxURIuyaWrVLp3U5TncOeSQw+pbElFj0PjqGKxZ71SqaDRaACA6i1ixS+FkaOjI3S7XXz69OnvfEFriFtLFokwDLGzs4OHDx8uGZ2+76sOT9u2MZ/PkWWZao+mqgZAlYwzt6FEzV/yi8y3y6oJLttx5PPojUjDUMrFzM9YCm/bNur1OhzHUaOAsizDbDY7ZyB2Oh0cHR2pPqPbDEMWAcuyEIYh9vb2EEURGo2G8mwcx4HneWryDSdrxnGsem7m87kSCWTJDHcO3aMhpGAgQyb5OGkQcjfRr1bFXYTNU47jqJIT13URBIEqp+EooCzL1PSTJEnw9etXDAYDvH//HlmW/c2Pf+1hyHIBLMtCq9VCs9nE1taWGs7mOA5831fTDFlJy193qkWTyUSRB1jI0nJIOXegy7wVYDkXkQRh2EWSeJ6HUqmkKhls2wYAJZPPZjNMJhPVdZjnOcbjsQqzer0eRqPR3/yYrxUMWVZAqVRCrVbDo0ePEEWRCmGq1Spc11VhmhwLatv2UhLOlgI52UaWokiHXRYoyhyFci4LFV3XRblcVh2mwOIKAhw9xdG8JDHnZw2HQ/T7/f+t6/A6wpDlX8B1XdTrdWV8kjjMbzh4Wt4Ci0nuVKh4X5H/UmRekliyDUEOLszzfIkkeZ4jz3OkaarG73a7XVXJYHA1GLL8Jizrnzm6zWYTYRgq8tRqtaVRuNxxACg1igQhmaTzDyznO+zVsazF1QwAqJ2DJDk9PV0iRxzHqjXb4PdgyPIfgJM85dTOarWqyCPDNGBBHj1XobolBxIyL5IV1WmaqpKTLMswnU6vVIhpsBoMWdYAUibWy2KI2+CQrzsMWQwMVsSvRyEaGBgAMGQxMFgZhiwGBivCkMXAYEUYshgYrAhDFgODFWHIYmCwIgxZDAxWhCGLgcGK+AlvjLK/4v9pyAAAAABJRU5ErkJggg==" y="-35.3755"/>

   </g>

   <g id="matplotlib.axis_3">

    <g id="xtick_7">

     <g id="line2d_13">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="276.778409" xlink:href="#m8736a96668" y="280.3755"/>

      </g>

     </g>

     <g id="text_14">

      <!-- 0 -->

      <g transform="translate(273.597159 294.973937)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_8">

     <g id="line2d_14">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="333.142045" xlink:href="#m8736a96668" y="280.3755"/>

      </g>

     </g>

     <g id="text_15">

      <!-- 50 -->

      <g transform="translate(326.779545 294.973937)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-53"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_9">

     <g id="line2d_15">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="389.505682" xlink:href="#m8736a96668" y="280.3755"/>

      </g>

     </g>

     <g id="text_16">

      <!-- 100 -->

      <g transform="translate(379.961932 294.973937)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_10">

     <g id="line2d_16">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="445.869318" xlink:href="#m8736a96668" y="280.3755"/>

      </g>

     </g>

     <g id="text_17">

      <!-- 150 -->

      <g transform="translate(436.325568 294.973937)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-53"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="text_18">

     <!-- Projection angle (deg) -->

     <defs>

      <path d="M 19.671875 64.796875 

L 19.671875 37.40625 

L 32.078125 37.40625 

Q 38.96875 37.40625 42.71875 40.96875 

Q 46.484375 44.53125 46.484375 51.125 

Q 46.484375 57.671875 42.71875 61.234375 

Q 38.96875 64.796875 32.078125 64.796875 

z

M 9.8125 72.90625 

L 32.078125 72.90625 

Q 44.34375 72.90625 50.609375 67.359375 

Q 56.890625 61.8125 56.890625 51.125 

Q 56.890625 40.328125 50.609375 34.8125 

Q 44.34375 29.296875 32.078125 29.296875 

L 19.671875 29.296875 

L 19.671875 0 

L 9.8125 0 

z

" id="DejaVuSans-80"/>

      <path d="M 30.609375 48.390625 

Q 23.390625 48.390625 19.1875 42.75 

Q 14.984375 37.109375 14.984375 27.296875 

Q 14.984375 17.484375 19.15625 11.84375 

Q 23.34375 6.203125 30.609375 6.203125 

Q 37.796875 6.203125 41.984375 11.859375 

Q 46.1875 17.53125 46.1875 27.296875 

Q 46.1875 37.015625 41.984375 42.703125 

Q 37.796875 48.390625 30.609375 48.390625 

z

M 30.609375 56 

Q 42.328125 56 49.015625 48.375 

Q 55.71875 40.765625 55.71875 27.296875 

Q 55.71875 13.875 49.015625 6.21875 

Q 42.328125 -1.421875 30.609375 -1.421875 

Q 18.84375 -1.421875 12.171875 6.21875 

Q 5.515625 13.875 5.515625 27.296875 

Q 5.515625 40.765625 12.171875 48.375 

Q 18.84375 56 30.609375 56 

z

" id="DejaVuSans-111"/>

      <path d="M 9.421875 54.6875 

L 18.40625 54.6875 

L 18.40625 -0.984375 

Q 18.40625 -11.421875 14.421875 -16.109375 

Q 10.453125 -20.796875 1.609375 -20.796875 

L -1.8125 -20.796875 

L -1.8125 -13.1875 

L 0.59375 -13.1875 

Q 5.71875 -13.1875 7.5625 -10.8125 

Q 9.421875 -8.453125 9.421875 -0.984375 

z

M 9.421875 75.984375 

L 18.40625 75.984375 

L 18.40625 64.59375 

L 9.421875 64.59375 

z

" id="DejaVuSans-106"/>

      <path d="M 56.203125 29.59375 

L 56.203125 25.203125 

L 14.890625 25.203125 

Q 15.484375 15.921875 20.484375 11.0625 

Q 25.484375 6.203125 34.421875 6.203125 

Q 39.59375 6.203125 44.453125 7.46875 

Q 49.3125 8.734375 54.109375 11.28125 

L 54.109375 2.78125 

Q 49.265625 0.734375 44.1875 -0.34375 

Q 39.109375 -1.421875 33.890625 -1.421875 

Q 20.796875 -1.421875 13.15625 6.1875 

Q 5.515625 13.8125 5.515625 26.8125 

Q 5.515625 40.234375 12.765625 48.109375 

Q 20.015625 56 32.328125 56 

Q 43.359375 56 49.78125 48.890625 

Q 56.203125 41.796875 56.203125 29.59375 

z

M 47.21875 32.234375 

Q 47.125 39.59375 43.09375 43.984375 

Q 39.0625 48.390625 32.421875 48.390625 

Q 24.90625 48.390625 20.390625 44.140625 

Q 15.875 39.890625 15.1875 32.171875 

z

" id="DejaVuSans-101"/>

      <path d="M 48.78125 52.59375 

L 48.78125 44.1875 

Q 44.96875 46.296875 41.140625 47.34375 

Q 37.3125 48.390625 33.40625 48.390625 

Q 24.65625 48.390625 19.8125 42.84375 

Q 14.984375 37.3125 14.984375 27.296875 

Q 14.984375 17.28125 19.8125 11.734375 

Q 24.65625 6.203125 33.40625 6.203125 

Q 37.3125 6.203125 41.140625 7.25 

Q 44.96875 8.296875 48.78125 10.40625 

L 48.78125 2.09375 

Q 45.015625 0.34375 40.984375 -0.53125 

Q 36.96875 -1.421875 32.421875 -1.421875 

Q 20.0625 -1.421875 12.78125 6.34375 

Q 5.515625 14.109375 5.515625 27.296875 

Q 5.515625 40.671875 12.859375 48.328125 

Q 20.21875 56 33.015625 56 

Q 37.15625 56 41.109375 55.140625 

Q 45.0625 54.296875 48.78125 52.59375 

z

" id="DejaVuSans-99"/>

      <path d="M 18.3125 70.21875 

L 18.3125 54.6875 

L 36.8125 54.6875 

L 36.8125 47.703125 

L 18.3125 47.703125 

L 18.3125 18.015625 

Q 18.3125 11.328125 20.140625 9.421875 

Q 21.96875 7.515625 27.59375 7.515625 

L 36.8125 7.515625 

L 36.8125 0 

L 27.59375 0 

Q 17.1875 0 13.234375 3.875 

Q 9.28125 7.765625 9.28125 18.015625 

L 9.28125 47.703125 

L 2.6875 47.703125 

L 2.6875 54.6875 

L 9.28125 54.6875 

L 9.28125 70.21875 

z

" id="DejaVuSans-116"/>

      <path id="DejaVuSans-32"/>

      <path d="M 31 75.875 

Q 24.46875 64.65625 21.28125 53.65625 

Q 18.109375 42.671875 18.109375 31.390625 

Q 18.109375 20.125 21.3125 9.0625 

Q 24.515625 -2 31 -13.1875 

L 23.1875 -13.1875 

Q 15.875 -1.703125 12.234375 9.375 

Q 8.59375 20.453125 8.59375 31.390625 

Q 8.59375 42.28125 12.203125 53.3125 

Q 15.828125 64.359375 23.1875 75.875 

z

" id="DejaVuSans-40"/>

      <path d="M 45.40625 46.390625 

L 45.40625 75.984375 

L 54.390625 75.984375 

L 54.390625 0 

L 45.40625 0 

L 45.40625 8.203125 

Q 42.578125 3.328125 38.25 0.953125 

Q 33.9375 -1.421875 27.875 -1.421875 

Q 17.96875 -1.421875 11.734375 6.484375 

Q 5.515625 14.40625 5.515625 27.296875 

Q 5.515625 40.1875 11.734375 48.09375 

Q 17.96875 56 27.875 56 

Q 33.9375 56 38.25 53.625 

Q 42.578125 51.265625 45.40625 46.390625 

z

M 14.796875 27.296875 

Q 14.796875 17.390625 18.875 11.75 

Q 22.953125 6.109375 30.078125 6.109375 

Q 37.203125 6.109375 41.296875 11.75 

Q 45.40625 17.390625 45.40625 27.296875 

Q 45.40625 37.203125 41.296875 42.84375 

Q 37.203125 48.484375 30.078125 48.484375 

Q 22.953125 48.484375 18.875 42.84375 

Q 14.796875 37.203125 14.796875 27.296875 

z

" id="DejaVuSans-100"/>

      <path d="M 8.015625 75.875 

L 15.828125 75.875 

Q 23.140625 64.359375 26.78125 53.3125 

Q 30.421875 42.28125 30.421875 31.390625 

Q 30.421875 20.453125 26.78125 9.375 

Q 23.140625 -1.703125 15.828125 -13.1875 

L 8.015625 -13.1875 

Q 14.5 -2 17.703125 9.0625 

Q 20.90625 20.125 20.90625 31.390625 

Q 20.90625 42.671875 17.703125 53.65625 

Q 14.5 64.65625 8.015625 75.875 

z

" id="DejaVuSans-41"/>

     </defs>

     <g transform="translate(322.93608 308.652062)scale(0.1 -0.1)">

      <use xlink:href="#DejaVuSans-80"/>

      <use x="60.287109" xlink:href="#DejaVuSans-114"/>

      <use x="101.369141" xlink:href="#DejaVuSans-111"/>

      <use x="162.550781" xlink:href="#DejaVuSans-106"/>

      <use x="190.333984" xlink:href="#DejaVuSans-101"/>

      <use x="251.857422" xlink:href="#DejaVuSans-99"/>

      <use x="306.837891" xlink:href="#DejaVuSans-116"/>

      <use x="346.046875" xlink:href="#DejaVuSans-105"/>

      <use x="373.830078" xlink:href="#DejaVuSans-111"/>

      <use x="435.011719" xlink:href="#DejaVuSans-110"/>

      <use x="498.390625" xlink:href="#DejaVuSans-32"/>

      <use x="530.177734" xlink:href="#DejaVuSans-97"/>

      <use x="591.457031" xlink:href="#DejaVuSans-110"/>

      <use x="654.835938" xlink:href="#DejaVuSans-103"/>

      <use x="718.3125" xlink:href="#DejaVuSans-108"/>

      <use x="746.095703" xlink:href="#DejaVuSans-101"/>

      <use x="807.619141" xlink:href="#DejaVuSans-32"/>

      <use x="839.40625" xlink:href="#DejaVuSans-40"/>

      <use x="878.419922" xlink:href="#DejaVuSans-100"/>

      <use x="941.896484" xlink:href="#DejaVuSans-101"/>

      <use x="1003.419922" xlink:href="#DejaVuSans-103"/>

      <use x="1066.896484" xlink:href="#DejaVuSans-41"/>

     </g>

    </g>

   </g>

   <g id="matplotlib.axis_4">

    <g id="ytick_7">

     <g id="line2d_17">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="276.778409" xlink:href="#mf2ae93be4b" y="280.3755"/>

      </g>

     </g>

     <g id="text_19">

      <!-- 0 -->

      <g transform="translate(263.415909 284.174719)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_8">

     <g id="line2d_18">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="276.778409" xlink:href="#mf2ae93be4b" y="232.598156"/>

      </g>

     </g>

     <g id="text_20">

      <!-- 100 -->

      <g transform="translate(250.690909 236.397375)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_9">

     <g id="line2d_19">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="276.778409" xlink:href="#mf2ae93be4b" y="184.820812"/>

      </g>

     </g>

     <g id="text_21">

      <!-- 200 -->

      <g transform="translate(250.690909 188.620031)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-50"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_10">

     <g id="line2d_20">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="276.778409" xlink:href="#mf2ae93be4b" y="137.043469"/>

      </g>

     </g>

     <g id="text_22">

      <!-- 300 -->

      <g transform="translate(250.690909 140.842687)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-51"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_11">

     <g id="line2d_21">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="276.778409" xlink:href="#mf2ae93be4b" y="89.266125"/>

      </g>

     </g>

     <g id="text_23">

      <!-- 400 -->

      <g transform="translate(250.690909 93.065344)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-52"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_12">

     <g id="line2d_22">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="276.778409" xlink:href="#mf2ae93be4b" y="41.488781"/>

      </g>

     </g>

     <g id="text_24">

      <!-- 500 -->

      <g transform="translate(250.690909 45.288)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-53"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="text_25">

     <!-- Projection position (pixels) -->

     <defs>

      <path d="M 18.109375 8.203125 

L 18.109375 -20.796875 

L 9.078125 -20.796875 

L 9.078125 54.6875 

L 18.109375 54.6875 

L 18.109375 46.390625 

Q 20.953125 51.265625 25.265625 53.625 

Q 29.59375 56 35.59375 56 

Q 45.5625 56 51.78125 48.09375 

Q 58.015625 40.1875 58.015625 27.296875 

Q 58.015625 14.40625 51.78125 6.484375 

Q 45.5625 -1.421875 35.59375 -1.421875 

Q 29.59375 -1.421875 25.265625 0.953125 

Q 20.953125 3.328125 18.109375 8.203125 

z

M 48.6875 27.296875 

Q 48.6875 37.203125 44.609375 42.84375 

Q 40.53125 48.484375 33.40625 48.484375 

Q 26.265625 48.484375 22.1875 42.84375 

Q 18.109375 37.203125 18.109375 27.296875 

Q 18.109375 17.390625 22.1875 11.75 

Q 26.265625 6.109375 33.40625 6.109375 

Q 40.53125 6.109375 44.609375 11.75 

Q 48.6875 17.390625 48.6875 27.296875 

z

" id="DejaVuSans-112"/>

      <path d="M 44.28125 53.078125 

L 44.28125 44.578125 

Q 40.484375 46.53125 36.375 47.5 

Q 32.28125 48.484375 27.875 48.484375 

Q 21.1875 48.484375 17.84375 46.4375 

Q 14.5 44.390625 14.5 40.28125 

Q 14.5 37.15625 16.890625 35.375 

Q 19.28125 33.59375 26.515625 31.984375 

L 29.59375 31.296875 

Q 39.15625 29.25 43.1875 25.515625 

Q 47.21875 21.78125 47.21875 15.09375 

Q 47.21875 7.46875 41.1875 3.015625 

Q 35.15625 -1.421875 24.609375 -1.421875 

Q 20.21875 -1.421875 15.453125 -0.5625 

Q 10.6875 0.296875 5.421875 2 

L 5.421875 11.28125 

Q 10.40625 8.6875 15.234375 7.390625 

Q 20.0625 6.109375 24.8125 6.109375 

Q 31.15625 6.109375 34.5625 8.28125 

Q 37.984375 10.453125 37.984375 14.40625 

Q 37.984375 18.0625 35.515625 20.015625 

Q 33.0625 21.96875 24.703125 23.78125 

L 21.578125 24.515625 

Q 13.234375 26.265625 9.515625 29.90625 

Q 5.8125 33.546875 5.8125 39.890625 

Q 5.8125 47.609375 11.28125 51.796875 

Q 16.75 56 26.8125 56 

Q 31.78125 56 36.171875 55.265625 

Q 40.578125 54.546875 44.28125 53.078125 

z

" id="DejaVuSans-115"/>

      <path d="M 54.890625 54.6875 

L 35.109375 28.078125 

L 55.90625 0 

L 45.3125 0 

L 29.390625 21.484375 

L 13.484375 0 

L 2.875 0 

L 24.125 28.609375 

L 4.6875 54.6875 

L 15.28125 54.6875 

L 29.78125 35.203125 

L 44.28125 54.6875 

z

" id="DejaVuSans-120"/>

     </defs>

     <g transform="translate(244.611222 224.460031)rotate(-90)scale(0.1 -0.1)">

      <use xlink:href="#DejaVuSans-80"/>

      <use x="60.287109" xlink:href="#DejaVuSans-114"/>

      <use x="101.369141" xlink:href="#DejaVuSans-111"/>

      <use x="162.550781" xlink:href="#DejaVuSans-106"/>

      <use x="190.333984" xlink:href="#DejaVuSans-101"/>

      <use x="251.857422" xlink:href="#DejaVuSans-99"/>

      <use x="306.837891" xlink:href="#DejaVuSans-116"/>

      <use x="346.046875" xlink:href="#DejaVuSans-105"/>

      <use x="373.830078" xlink:href="#DejaVuSans-111"/>

      <use x="435.011719" xlink:href="#DejaVuSans-110"/>

      <use x="498.390625" xlink:href="#DejaVuSans-32"/>

      <use x="530.177734" xlink:href="#DejaVuSans-112"/>

      <use x="593.654297" xlink:href="#DejaVuSans-111"/>

      <use x="654.835938" xlink:href="#DejaVuSans-115"/>

      <use x="706.935547" xlink:href="#DejaVuSans-105"/>

      <use x="734.71875" xlink:href="#DejaVuSans-116"/>

      <use x="773.927734" xlink:href="#DejaVuSans-105"/>

      <use x="801.710938" xlink:href="#DejaVuSans-111"/>

      <use x="862.892578" xlink:href="#DejaVuSans-110"/>

      <use x="926.271484" xlink:href="#DejaVuSans-32"/>

      <use x="958.058594" xlink:href="#DejaVuSans-40"/>

      <use x="997.072266" xlink:href="#DejaVuSans-112"/>

      <use x="1060.548828" xlink:href="#DejaVuSans-105"/>

      <use x="1088.332031" xlink:href="#DejaVuSans-120"/>

      <use x="1147.464844" xlink:href="#DejaVuSans-101"/>

      <use x="1208.988281" xlink:href="#DejaVuSans-108"/>

      <use x="1236.771484" xlink:href="#DejaVuSans-115"/>

      <use x="1288.871094" xlink:href="#DejaVuSans-41"/>

     </g>

    </g>

   </g>

   <g id="patch_8">

    <path d="M 276.778409 280.3755 

L 276.778409 35.7555 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_9">

    <path d="M 479.6875 280.3755 

L 479.6875 35.7555 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_10">

    <path d="M 276.778409 280.3755 

L 479.6875 280.3755 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_11">

    <path d="M 276.778409 35.7555 

L 479.6875 35.7555 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="text_26">

    <!-- Radon transform -->

    <defs>

     <path d="M 44.390625 34.1875 

Q 47.5625 33.109375 50.5625 29.59375 

Q 53.5625 26.078125 56.59375 19.921875 

L 66.609375 0 

L 56 0 

L 46.6875 18.703125 

Q 43.0625 26.03125 39.671875 28.421875 

Q 36.28125 30.8125 30.421875 30.8125 

L 19.671875 30.8125 

L 19.671875 0 

L 9.8125 0 

L 9.8125 72.90625 

L 32.078125 72.90625 

Q 44.578125 72.90625 50.734375 67.671875 

Q 56.890625 62.453125 56.890625 51.90625 

Q 56.890625 45.015625 53.6875 40.46875 

Q 50.484375 35.9375 44.390625 34.1875 

z

M 19.671875 64.796875 

L 19.671875 38.921875 

L 32.078125 38.921875 

Q 39.203125 38.921875 42.84375 42.21875 

Q 46.484375 45.515625 46.484375 51.90625 

Q 46.484375 58.296875 42.84375 61.546875 

Q 39.203125 64.796875 32.078125 64.796875 

z

" id="DejaVuSans-82"/>

     <path d="M 37.109375 75.984375 

L 37.109375 68.5 

L 28.515625 68.5 

Q 23.6875 68.5 21.796875 66.546875 

Q 19.921875 64.59375 19.921875 59.515625 

L 19.921875 54.6875 

L 34.71875 54.6875 

L 34.71875 47.703125 

L 19.921875 47.703125 

L 19.921875 0 

L 10.890625 0 

L 10.890625 47.703125 

L 2.296875 47.703125 

L 2.296875 54.6875 

L 10.890625 54.6875 

L 10.890625 58.5 

Q 10.890625 67.625 15.140625 71.796875 

Q 19.390625 75.984375 28.609375 75.984375 

z

" id="DejaVuSans-102"/>

     <path d="M 52 44.1875 

Q 55.375 50.25 60.0625 53.125 

Q 64.75 56 71.09375 56 

Q 79.640625 56 84.28125 50.015625 

Q 88.921875 44.046875 88.921875 33.015625 

L 88.921875 0 

L 79.890625 0 

L 79.890625 32.71875 

Q 79.890625 40.578125 77.09375 44.375 

Q 74.3125 48.1875 68.609375 48.1875 

Q 61.625 48.1875 57.5625 43.546875 

Q 53.515625 38.921875 53.515625 30.90625 

L 53.515625 0 

L 44.484375 0 

L 44.484375 32.71875 

Q 44.484375 40.625 41.703125 44.40625 

Q 38.921875 48.1875 33.109375 48.1875 

Q 26.21875 48.1875 22.15625 43.53125 

Q 18.109375 38.875 18.109375 30.90625 

L 18.109375 0 

L 9.078125 0 

L 9.078125 54.6875 

L 18.109375 54.6875 

L 18.109375 46.1875 

Q 21.1875 51.21875 25.484375 53.609375 

Q 29.78125 56 35.6875 56 

Q 41.65625 56 45.828125 52.96875 

Q 50 49.953125 52 44.1875 

z

" id="DejaVuSans-109"/>

    </defs>

    <g transform="translate(327.682017 16.318125)scale(0.12 -0.12)">

     <use xlink:href="#DejaVuSans-82"/>

     <use x="69.451172" xlink:href="#DejaVuSans-97"/>

     <use x="130.730469" xlink:href="#DejaVuSans-100"/>

     <use x="194.207031" xlink:href="#DejaVuSans-111"/>

     <use x="255.388672" xlink:href="#DejaVuSans-110"/>

     <use x="318.767578" xlink:href="#DejaVuSans-32"/>

     <use x="350.554688" xlink:href="#DejaVuSans-116"/>

     <use x="389.763672" xlink:href="#DejaVuSans-114"/>

     <use x="430.876953" xlink:href="#DejaVuSans-97"/>

     <use x="492.15625" xlink:href="#DejaVuSans-110"/>

     <use x="555.535156" xlink:href="#DejaVuSans-115"/>

     <use x="607.634766" xlink:href="#DejaVuSans-102"/>

     <use x="642.839844" xlink:href="#DejaVuSans-111"/>

     <use x="704.021484" xlink:href="#DejaVuSans-114"/>

     <use x="745.119141" xlink:href="#DejaVuSans-109"/>

    </g>

    <!-- (Sinogram) -->

    <defs>

     <path d="M 53.515625 70.515625 

L 53.515625 60.890625 

Q 47.90625 63.578125 42.921875 64.890625 

Q 37.9375 66.21875 33.296875 66.21875 

Q 25.25 66.21875 20.875 63.09375 

Q 16.5 59.96875 16.5 54.203125 

Q 16.5 49.359375 19.40625 46.890625 

Q 22.3125 44.4375 30.421875 42.921875 

L 36.375 41.703125 

Q 47.40625 39.59375 52.65625 34.296875 

Q 57.90625 29 57.90625 20.125 

Q 57.90625 9.515625 50.796875 4.046875 

Q 43.703125 -1.421875 29.984375 -1.421875 

Q 24.8125 -1.421875 18.96875 -0.25 

Q 13.140625 0.921875 6.890625 3.21875 

L 6.890625 13.375 

Q 12.890625 10.015625 18.65625 8.296875 

Q 24.421875 6.59375 29.984375 6.59375 

Q 38.421875 6.59375 43.015625 9.90625 

Q 47.609375 13.234375 47.609375 19.390625 

Q 47.609375 24.75 44.3125 27.78125 

Q 41.015625 30.8125 33.5 32.328125 

L 27.484375 33.5 

Q 16.453125 35.6875 11.515625 40.375 

Q 6.59375 45.0625 6.59375 53.421875 

Q 6.59375 63.09375 13.40625 68.65625 

Q 20.21875 74.21875 32.171875 74.21875 

Q 37.3125 74.21875 42.625 73.28125 

Q 47.953125 72.359375 53.515625 70.515625 

z

" id="DejaVuSans-83"/>

    </defs>

    <g transform="translate(344.804517 29.7555)scale(0.12 -0.12)">

     <use xlink:href="#DejaVuSans-40"/>

     <use x="39.013672" xlink:href="#DejaVuSans-83"/>

     <use x="102.490234" xlink:href="#DejaVuSans-105"/>

     <use x="130.273438" xlink:href="#DejaVuSans-110"/>

     <use x="193.652344" xlink:href="#DejaVuSans-111"/>

     <use x="254.833984" xlink:href="#DejaVuSans-103"/>

     <use x="318.310547" xlink:href="#DejaVuSans-114"/>

     <use x="359.423828" xlink:href="#DejaVuSans-97"/>

     <use x="420.703125" xlink:href="#DejaVuSans-109"/>

     <use x="518.115234" xlink:href="#DejaVuSans-41"/>

    </g>

   </g>

  </g>

 </g>

 <defs>

  <clipPath id="pcb845ba5ce">

   <rect height="202.909091" width="202.909091" x="33.2875" y="56.610955"/>

  </clipPath>

  <clipPath id="p10a7be7180">

   <rect height="244.62" width="202.909091" x="276.778409" y="35.7555"/>

  </clipPath>

 </defs>

</svg>


</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="-Relationship-with-the-Fourier-transform"><center> Relationship with the Fourier transform</center><a class="anchor-link" href="#-Relationship-with-the-Fourier-transform">&#182;</a></h3><p>The Radon transform is closely related to the Fourier transform. We define the 2D Fourier transform here as
$$F(k_x,k_y)=\int\limits_{-\infty}^{\infty}\int\limits_{-\infty}^{\infty} f(x,y) e^{-i (k_x x + k_y y)} dx dy.$$
Denote $\vec{k}=(k_x,k_y)=\omega(\cos\alpha,\sin\alpha)$ and introduce new variables $s=x\cos\alpha+y\sin\alpha,   z=-x\sin\alpha+y\cos\alpha$. 
Thus,
$$F(\omega\cos\alpha,\omega\sin\alpha)=\int\limits_{-\infty}^{\infty} \left( \int\limits_{-\infty}^{\infty} f(s\cos\alpha-z\sin\alpha, s\sin\alpha+z\cos\alpha) e^{-i\omega s} dz \right) ds $$
and
$$F(\omega\cos\alpha,\omega\sin\alpha)= \int\limits_{-\infty}^{\infty} e^{-i\omega s} R(s,\alpha) ds.$$
Thus the <b>two-dimensional</b> Fourier transform of the initial function along a line at the inclination angle $\alpha$ is the <b>one-dimensional</b> Fourier transform of the Radon transform (acquired at angle $\alpha$) of that function. This fact can be used to compute both the Radon transform and its inverse.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="-Radon-Inversion-Formula-(FBP)-"><center> Radon Inversion Formula (FBP) </center><a class="anchor-link" href="#-Radon-Inversion-Formula-(FBP)-">&#182;</a></h3><p>Since Fourier transform is  invertible,
$$f(x,y)=\frac{1 }{(2\pi)^2} \int\limits_0^{2\pi} d \alpha\int\limits_{0}^{\infty} e^{i \omega(x\cos\alpha+y\sin\alpha)}\ \tilde{R}(\omega,\alpha) \omega d\omega,$$ 
where $\tilde{R}(\omega,\alpha)=\int\limits_{-\infty}^{\infty} R(s,\alpha)e^{-i\omega s} ds$.
<img src='FBP.png' width=60%></p>
<h4 id="Why-Filtered-Back-Projection?">Why Filtered Back Projection?<a class="anchor-link" href="#Why-Filtered-Back-Projection?">&#182;</a></h4><ol>
<li>The radial integral is interpreted as a filter applied to the Radon transform. The filter acts only the affine parameter; </li>
<li>The angular integral is then interpreted as the back-projection of the filtered Radon transform.</li>
</ol>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="-Projection-slice-theorem-"><center> Projection-slice theorem </center><a class="anchor-link" href="#-Projection-slice-theorem-">&#182;</a></h3><p>Apply the direct Fourier transform operation to the Radon transform of $f(x,y)$:</p>
$$\int\limits_{-\infty}^{\infty} R(s,\alpha) e^{-i \omega s}  ds = 
 \int\limits_{-\infty}^{\infty} \left( \int\limits_{-\infty}^{\infty} \int\limits_{-\infty}^{\infty} f(x,y) \delta(s - x \cos\alpha - y \sin\alpha) dx dy \right) e^{-i \omega s}  ds .$$<p>Then,</p>
$$\int\limits_{-\infty}^{\infty} R(s,\alpha) e^{-i \omega s}  ds =   \int\limits_{-\infty}^{\infty}  \int\limits_{-\infty}^{\infty} \left( \int\limits_{-\infty}^{\infty} e^{-i \omega s} \delta(s - x \cos\alpha - y \sin\alpha) ) ds \right)  f(x,y) dx dy =
\int\limits_{-\infty}^{\infty}  \int\limits_{-\infty}^{\infty} f(x,y) e^{-i \omega (x \cos\alpha + y \sin\alpha)} dx dy $$<p>Thus, the Fourier transform of the projection is the central section of the two-dimensional Fourier transform of the function $f(x, y)$.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[4]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Filtered Back Projection</span>
<span class="n">reconstruction_fbp</span> <span class="o">=</span> <span class="n">iradon</span><span class="p">(</span><span class="n">sinogram2d</span><span class="p">,</span> <span class="n">theta</span><span class="o">=</span><span class="n">theta2d</span><span class="p">,</span> <span class="n">circle</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>

<span class="n">fig</span><span class="p">,</span> <span class="p">(</span><span class="n">ax1</span><span class="p">,</span> <span class="n">ax2</span><span class="p">)</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">8</span><span class="p">,</span> <span class="mf">4.5</span><span class="p">),</span> <span class="n">sharex</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span> <span class="n">sharey</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">ax1</span><span class="o">.</span><span class="n">set_title</span><span class="p">(</span><span class="s2">&quot;Reconstruction</span><span class="se">\n</span><span class="s2">Filtered back projection&quot;</span><span class="p">);</span>
<span class="n">ax1</span><span class="o">.</span><span class="n">imshow</span><span class="p">(</span><span class="n">reconstruction_fbp</span><span class="p">,</span> <span class="n">cmap</span><span class="o">=</span><span class="s1">&#39;gray&#39;</span><span class="p">);</span>
<span class="n">ax2</span><span class="o">.</span><span class="n">set_title</span><span class="p">(</span><span class="s2">&quot;Reconstruction error</span><span class="se">\n</span><span class="s2">Filtered back projection&quot;</span><span class="p">);</span>
<span class="n">ax2</span><span class="o">.</span><span class="n">imshow</span><span class="p">(</span><span class="n">reconstruction_fbp</span> <span class="o">-</span> <span class="n">phantom2d</span><span class="p">,</span> <span class="n">cmap</span><span class="o">=</span><span class="s1">&#39;gray&#39;</span><span class="p">);</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt"></div>


<div class="output_svg output_subarea ">
<?xml version="1.0" encoding="utf-8" standalone="no"?>

<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN"

  "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">

<!-- Created with matplotlib (https://matplotlib.org/) -->

<svg height="262.542716pt" version="1.1" viewBox="0 0 491.873722 262.542716" width="491.873722pt" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">

 <defs>

  <style type="text/css">

*{stroke-linecap:butt;stroke-linejoin:round;}

  </style>

 </defs>

 <g id="figure_1">

  <g id="patch_1">

   <path d="M 0 262.542716 

L 491.873722 262.542716 

L 491.873722 0 

L 0 0 

z

" style="fill:none;"/>

  </g>

  <g id="axes_1">

   <g id="patch_2">

    <path d="M 33.2875 238.664591 

L 236.196591 238.664591 

L 236.196591 35.7555 

L 33.2875 35.7555 

z

" style="fill:#ffffff;"/>

   </g>

   <g clip-path="url(#p47ba5aa6ba)">

    <image height="203" id="image972ee34275" transform="scale(1 -1)translate(0 -203)" width="203" x="33.2875" xlink:href="data:image/png;base64,

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" y="-35.664591"/>

   </g>

   <g id="matplotlib.axis_1">

    <g id="xtick_1">

     <g id="line2d_1">

      <defs>

       <path d="M 0 0 

L 0 3.5 

" id="m8b0a97d421" style="stroke:#000000;stroke-width:0.8;"/>

      </defs>

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.485653" xlink:href="#m8b0a97d421" y="238.664591"/>

      </g>

     </g>

     <g id="text_1">

      <!-- 0 -->

      <defs>

       <path d="M 31.78125 66.40625 

Q 24.171875 66.40625 20.328125 58.90625 

Q 16.5 51.421875 16.5 36.375 

Q 16.5 21.390625 20.328125 13.890625 

Q 24.171875 6.390625 31.78125 6.390625 

Q 39.453125 6.390625 43.28125 13.890625 

Q 47.125 21.390625 47.125 36.375 

Q 47.125 51.421875 43.28125 58.90625 

Q 39.453125 66.40625 31.78125 66.40625 

z

M 31.78125 74.21875 

Q 44.046875 74.21875 50.515625 64.515625 

Q 56.984375 54.828125 56.984375 36.375 

Q 56.984375 17.96875 50.515625 8.265625 

Q 44.046875 -1.421875 31.78125 -1.421875 

Q 19.53125 -1.421875 13.0625 8.265625 

Q 6.59375 17.96875 6.59375 36.375 

Q 6.59375 54.828125 13.0625 64.515625 

Q 19.53125 74.21875 31.78125 74.21875 

z

" id="DejaVuSans-48"/>

      </defs>

      <g transform="translate(30.304403 253.263028)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_2">

     <g id="line2d_2">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="73.116335" xlink:href="#m8b0a97d421" y="238.664591"/>

      </g>

     </g>

     <g id="text_2">

      <!-- 100 -->

      <defs>

       <path d="M 12.40625 8.296875 

L 28.515625 8.296875 

L 28.515625 63.921875 

L 10.984375 60.40625 

L 10.984375 69.390625 

L 28.421875 72.90625 

L 38.28125 72.90625 

L 38.28125 8.296875 

L 54.390625 8.296875 

L 54.390625 0 

L 12.40625 0 

z

" id="DejaVuSans-49"/>

      </defs>

      <g transform="translate(63.572585 253.263028)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_3">

     <g id="line2d_3">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="112.747017" xlink:href="#m8b0a97d421" y="238.664591"/>

      </g>

     </g>

     <g id="text_3">

      <!-- 200 -->

      <defs>

       <path d="M 19.1875 8.296875 

L 53.609375 8.296875 

L 53.609375 0 

L 7.328125 0 

L 7.328125 8.296875 

Q 12.9375 14.109375 22.625 23.890625 

Q 32.328125 33.6875 34.8125 36.53125 

Q 39.546875 41.84375 41.421875 45.53125 

Q 43.3125 49.21875 43.3125 52.78125 

Q 43.3125 58.59375 39.234375 62.25 

Q 35.15625 65.921875 28.609375 65.921875 

Q 23.96875 65.921875 18.8125 64.3125 

Q 13.671875 62.703125 7.8125 59.421875 

L 7.8125 69.390625 

Q 13.765625 71.78125 18.9375 73 

Q 24.125 74.21875 28.421875 74.21875 

Q 39.75 74.21875 46.484375 68.546875 

Q 53.21875 62.890625 53.21875 53.421875 

Q 53.21875 48.921875 51.53125 44.890625 

Q 49.859375 40.875 45.40625 35.40625 

Q 44.1875 33.984375 37.640625 27.21875 

Q 31.109375 20.453125 19.1875 8.296875 

z

" id="DejaVuSans-50"/>

      </defs>

      <g transform="translate(103.203267 253.263028)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-50"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_4">

     <g id="line2d_4">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="152.377699" xlink:href="#m8b0a97d421" y="238.664591"/>

      </g>

     </g>

     <g id="text_4">

      <!-- 300 -->

      <defs>

       <path d="M 40.578125 39.3125 

Q 47.65625 37.796875 51.625 33 

Q 55.609375 28.21875 55.609375 21.1875 

Q 55.609375 10.40625 48.1875 4.484375 

Q 40.765625 -1.421875 27.09375 -1.421875 

Q 22.515625 -1.421875 17.65625 -0.515625 

Q 12.796875 0.390625 7.625 2.203125 

L 7.625 11.71875 

Q 11.71875 9.328125 16.59375 8.109375 

Q 21.484375 6.890625 26.8125 6.890625 

Q 36.078125 6.890625 40.9375 10.546875 

Q 45.796875 14.203125 45.796875 21.1875 

Q 45.796875 27.640625 41.28125 31.265625 

Q 36.765625 34.90625 28.71875 34.90625 

L 20.21875 34.90625 

L 20.21875 43.015625 

L 29.109375 43.015625 

Q 36.375 43.015625 40.234375 45.921875 

Q 44.09375 48.828125 44.09375 54.296875 

Q 44.09375 59.90625 40.109375 62.90625 

Q 36.140625 65.921875 28.71875 65.921875 

Q 24.65625 65.921875 20.015625 65.03125 

Q 15.375 64.15625 9.8125 62.3125 

L 9.8125 71.09375 

Q 15.4375 72.65625 20.34375 73.4375 

Q 25.25 74.21875 29.59375 74.21875 

Q 40.828125 74.21875 47.359375 69.109375 

Q 53.90625 64.015625 53.90625 55.328125 

Q 53.90625 49.265625 50.4375 45.09375 

Q 46.96875 40.921875 40.578125 39.3125 

z

" id="DejaVuSans-51"/>

      </defs>

      <g transform="translate(142.833949 253.263028)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-51"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_5">

     <g id="line2d_5">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="192.008381" xlink:href="#m8b0a97d421" y="238.664591"/>

      </g>

     </g>

     <g id="text_5">

      <!-- 400 -->

      <defs>

       <path d="M 37.796875 64.3125 

L 12.890625 25.390625 

L 37.796875 25.390625 

z

M 35.203125 72.90625 

L 47.609375 72.90625 

L 47.609375 25.390625 

L 58.015625 25.390625 

L 58.015625 17.1875 

L 47.609375 17.1875 

L 47.609375 0 

L 37.796875 0 

L 37.796875 17.1875 

L 4.890625 17.1875 

L 4.890625 26.703125 

z

" id="DejaVuSans-52"/>

      </defs>

      <g transform="translate(182.464631 253.263028)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-52"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_6">

     <g id="line2d_6">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="231.639062" xlink:href="#m8b0a97d421" y="238.664591"/>

      </g>

     </g>

     <g id="text_6">

      <!-- 500 -->

      <defs>

       <path d="M 10.796875 72.90625 

L 49.515625 72.90625 

L 49.515625 64.59375 

L 19.828125 64.59375 

L 19.828125 46.734375 

Q 21.96875 47.46875 24.109375 47.828125 

Q 26.265625 48.1875 28.421875 48.1875 

Q 40.625 48.1875 47.75 41.5 

Q 54.890625 34.8125 54.890625 23.390625 

Q 54.890625 11.625 47.5625 5.09375 

Q 40.234375 -1.421875 26.90625 -1.421875 

Q 22.3125 -1.421875 17.546875 -0.640625 

Q 12.796875 0.140625 7.71875 1.703125 

L 7.71875 11.625 

Q 12.109375 9.234375 16.796875 8.0625 

Q 21.484375 6.890625 26.703125 6.890625 

Q 35.15625 6.890625 40.078125 11.328125 

Q 45.015625 15.765625 45.015625 23.390625 

Q 45.015625 31 40.078125 35.4375 

Q 35.15625 39.890625 26.703125 39.890625 

Q 22.75 39.890625 18.8125 39.015625 

Q 14.890625 38.140625 10.796875 36.28125 

z

" id="DejaVuSans-53"/>

      </defs>

      <g transform="translate(222.095312 253.263028)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-53"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

   </g>

   <g id="matplotlib.axis_2">

    <g id="ytick_1">

     <g id="line2d_7">

      <defs>

       <path d="M 0 0 

L -3.5 0 

" id="m7c4965ee86" style="stroke:#000000;stroke-width:0.8;"/>

      </defs>

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#m7c4965ee86" y="35.953653"/>

      </g>

     </g>

     <g id="text_7">

      <!-- 0 -->

      <g transform="translate(19.925 39.752872)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_2">

     <g id="line2d_8">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#m7c4965ee86" y="75.584335"/>

      </g>

     </g>

     <g id="text_8">

      <!-- 100 -->

      <g transform="translate(7.2 79.383554)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_3">

     <g id="line2d_9">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#m7c4965ee86" y="115.215017"/>

      </g>

     </g>

     <g id="text_9">

      <!-- 200 -->

      <g transform="translate(7.2 119.014236)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-50"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_4">

     <g id="line2d_10">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#m7c4965ee86" y="154.845699"/>

      </g>

     </g>

     <g id="text_10">

      <!-- 300 -->

      <g transform="translate(7.2 158.644918)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-51"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_5">

     <g id="line2d_11">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#m7c4965ee86" y="194.476381"/>

      </g>

     </g>

     <g id="text_11">

      <!-- 400 -->

      <g transform="translate(7.2 198.275599)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-52"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_6">

     <g id="line2d_12">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#m7c4965ee86" y="234.107062"/>

      </g>

     </g>

     <g id="text_12">

      <!-- 500 -->

      <g transform="translate(7.2 237.906281)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-53"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

   </g>

   <g id="patch_3">

    <path d="M 33.2875 238.664591 

L 33.2875 35.7555 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_4">

    <path d="M 236.196591 238.664591 

L 236.196591 35.7555 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_5">

    <path d="M 33.2875 238.664591 

L 236.196591 238.664591 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_6">

    <path d="M 33.2875 35.7555 

L 236.196591 35.7555 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="text_13">

    <!-- Reconstruction -->

    <defs>

     <path d="M 44.390625 34.1875 

Q 47.5625 33.109375 50.5625 29.59375 

Q 53.5625 26.078125 56.59375 19.921875 

L 66.609375 0 

L 56 0 

L 46.6875 18.703125 

Q 43.0625 26.03125 39.671875 28.421875 

Q 36.28125 30.8125 30.421875 30.8125 

L 19.671875 30.8125 

L 19.671875 0 

L 9.8125 0 

L 9.8125 72.90625 

L 32.078125 72.90625 

Q 44.578125 72.90625 50.734375 67.671875 

Q 56.890625 62.453125 56.890625 51.90625 

Q 56.890625 45.015625 53.6875 40.46875 

Q 50.484375 35.9375 44.390625 34.1875 

z

M 19.671875 64.796875 

L 19.671875 38.921875 

L 32.078125 38.921875 

Q 39.203125 38.921875 42.84375 42.21875 

Q 46.484375 45.515625 46.484375 51.90625 

Q 46.484375 58.296875 42.84375 61.546875 

Q 39.203125 64.796875 32.078125 64.796875 

z

" id="DejaVuSans-82"/>

     <path d="M 56.203125 29.59375 

L 56.203125 25.203125 

L 14.890625 25.203125 

Q 15.484375 15.921875 20.484375 11.0625 

Q 25.484375 6.203125 34.421875 6.203125 

Q 39.59375 6.203125 44.453125 7.46875 

Q 49.3125 8.734375 54.109375 11.28125 

L 54.109375 2.78125 

Q 49.265625 0.734375 44.1875 -0.34375 

Q 39.109375 -1.421875 33.890625 -1.421875 

Q 20.796875 -1.421875 13.15625 6.1875 

Q 5.515625 13.8125 5.515625 26.8125 

Q 5.515625 40.234375 12.765625 48.109375 

Q 20.015625 56 32.328125 56 

Q 43.359375 56 49.78125 48.890625 

Q 56.203125 41.796875 56.203125 29.59375 

z

M 47.21875 32.234375 

Q 47.125 39.59375 43.09375 43.984375 

Q 39.0625 48.390625 32.421875 48.390625 

Q 24.90625 48.390625 20.390625 44.140625 

Q 15.875 39.890625 15.1875 32.171875 

z

" id="DejaVuSans-101"/>

     <path d="M 48.78125 52.59375 

L 48.78125 44.1875 

Q 44.96875 46.296875 41.140625 47.34375 

Q 37.3125 48.390625 33.40625 48.390625 

Q 24.65625 48.390625 19.8125 42.84375 

Q 14.984375 37.3125 14.984375 27.296875 

Q 14.984375 17.28125 19.8125 11.734375 

Q 24.65625 6.203125 33.40625 6.203125 

Q 37.3125 6.203125 41.140625 7.25 

Q 44.96875 8.296875 48.78125 10.40625 

L 48.78125 2.09375 

Q 45.015625 0.34375 40.984375 -0.53125 

Q 36.96875 -1.421875 32.421875 -1.421875 

Q 20.0625 -1.421875 12.78125 6.34375 

Q 5.515625 14.109375 5.515625 27.296875 

Q 5.515625 40.671875 12.859375 48.328125 

Q 20.21875 56 33.015625 56 

Q 37.15625 56 41.109375 55.140625 

Q 45.0625 54.296875 48.78125 52.59375 

z

" id="DejaVuSans-99"/>

     <path d="M 30.609375 48.390625 

Q 23.390625 48.390625 19.1875 42.75 

Q 14.984375 37.109375 14.984375 27.296875 

Q 14.984375 17.484375 19.15625 11.84375 

Q 23.34375 6.203125 30.609375 6.203125 

Q 37.796875 6.203125 41.984375 11.859375 

Q 46.1875 17.53125 46.1875 27.296875 

Q 46.1875 37.015625 41.984375 42.703125 

Q 37.796875 48.390625 30.609375 48.390625 

z

M 30.609375 56 

Q 42.328125 56 49.015625 48.375 

Q 55.71875 40.765625 55.71875 27.296875 

Q 55.71875 13.875 49.015625 6.21875 

Q 42.328125 -1.421875 30.609375 -1.421875 

Q 18.84375 -1.421875 12.171875 6.21875 

Q 5.515625 13.875 5.515625 27.296875 

Q 5.515625 40.765625 12.171875 48.375 

Q 18.84375 56 30.609375 56 

z

" id="DejaVuSans-111"/>

     <path d="M 54.890625 33.015625 

L 54.890625 0 

L 45.90625 0 

L 45.90625 32.71875 

Q 45.90625 40.484375 42.875 44.328125 

Q 39.84375 48.1875 33.796875 48.1875 

Q 26.515625 48.1875 22.3125 43.546875 

Q 18.109375 38.921875 18.109375 30.90625 

L 18.109375 0 

L 9.078125 0 

L 9.078125 54.6875 

L 18.109375 54.6875 

L 18.109375 46.1875 

Q 21.34375 51.125 25.703125 53.5625 

Q 30.078125 56 35.796875 56 

Q 45.21875 56 50.046875 50.171875 

Q 54.890625 44.34375 54.890625 33.015625 

z

" id="DejaVuSans-110"/>

     <path d="M 44.28125 53.078125 

L 44.28125 44.578125 

Q 40.484375 46.53125 36.375 47.5 

Q 32.28125 48.484375 27.875 48.484375 

Q 21.1875 48.484375 17.84375 46.4375 

Q 14.5 44.390625 14.5 40.28125 

Q 14.5 37.15625 16.890625 35.375 

Q 19.28125 33.59375 26.515625 31.984375 

L 29.59375 31.296875 

Q 39.15625 29.25 43.1875 25.515625 

Q 47.21875 21.78125 47.21875 15.09375 

Q 47.21875 7.46875 41.1875 3.015625 

Q 35.15625 -1.421875 24.609375 -1.421875 

Q 20.21875 -1.421875 15.453125 -0.5625 

Q 10.6875 0.296875 5.421875 2 

L 5.421875 11.28125 

Q 10.40625 8.6875 15.234375 7.390625 

Q 20.0625 6.109375 24.8125 6.109375 

Q 31.15625 6.109375 34.5625 8.28125 

Q 37.984375 10.453125 37.984375 14.40625 

Q 37.984375 18.0625 35.515625 20.015625 

Q 33.0625 21.96875 24.703125 23.78125 

L 21.578125 24.515625 

Q 13.234375 26.265625 9.515625 29.90625 

Q 5.8125 33.546875 5.8125 39.890625 

Q 5.8125 47.609375 11.28125 51.796875 

Q 16.75 56 26.8125 56 

Q 31.78125 56 36.171875 55.265625 

Q 40.578125 54.546875 44.28125 53.078125 

z

" id="DejaVuSans-115"/>

     <path d="M 18.3125 70.21875 

L 18.3125 54.6875 

L 36.8125 54.6875 

L 36.8125 47.703125 

L 18.3125 47.703125 

L 18.3125 18.015625 

Q 18.3125 11.328125 20.140625 9.421875 

Q 21.96875 7.515625 27.59375 7.515625 

L 36.8125 7.515625 

L 36.8125 0 

L 27.59375 0 

Q 17.1875 0 13.234375 3.875 

Q 9.28125 7.765625 9.28125 18.015625 

L 9.28125 47.703125 

L 2.6875 47.703125 

L 2.6875 54.6875 

L 9.28125 54.6875 

L 9.28125 70.21875 

z

" id="DejaVuSans-116"/>

     <path d="M 41.109375 46.296875 

Q 39.59375 47.171875 37.8125 47.578125 

Q 36.03125 48 33.890625 48 

Q 26.265625 48 22.1875 43.046875 

Q 18.109375 38.09375 18.109375 28.8125 

L 18.109375 0 

L 9.078125 0 

L 9.078125 54.6875 

L 18.109375 54.6875 

L 18.109375 46.1875 

Q 20.953125 51.171875 25.484375 53.578125 

Q 30.03125 56 36.53125 56 

Q 37.453125 56 38.578125 55.875 

Q 39.703125 55.765625 41.0625 55.515625 

z

" id="DejaVuSans-114"/>

     <path d="M 8.5 21.578125 

L 8.5 54.6875 

L 17.484375 54.6875 

L 17.484375 21.921875 

Q 17.484375 14.15625 20.5 10.265625 

Q 23.53125 6.390625 29.59375 6.390625 

Q 36.859375 6.390625 41.078125 11.03125 

Q 45.3125 15.671875 45.3125 23.6875 

L 45.3125 54.6875 

L 54.296875 54.6875 

L 54.296875 0 

L 45.3125 0 

L 45.3125 8.40625 

Q 42.046875 3.421875 37.71875 1 

Q 33.40625 -1.421875 27.6875 -1.421875 

Q 18.265625 -1.421875 13.375 4.4375 

Q 8.5 10.296875 8.5 21.578125 

z

M 31.109375 56 

z

" id="DejaVuSans-117"/>

     <path d="M 9.421875 54.6875 

L 18.40625 54.6875 

L 18.40625 0 

L 9.421875 0 

z

M 9.421875 75.984375 

L 18.40625 75.984375 

L 18.40625 64.59375 

L 9.421875 64.59375 

z

" id="DejaVuSans-105"/>

    </defs>

    <g transform="translate(89.573295 16.318125)scale(0.12 -0.12)">

     <use xlink:href="#DejaVuSans-82"/>

     <use x="69.419922" xlink:href="#DejaVuSans-101"/>

     <use x="130.943359" xlink:href="#DejaVuSans-99"/>

     <use x="185.923828" xlink:href="#DejaVuSans-111"/>

     <use x="247.105469" xlink:href="#DejaVuSans-110"/>

     <use x="310.484375" xlink:href="#DejaVuSans-115"/>

     <use x="362.583984" xlink:href="#DejaVuSans-116"/>

     <use x="401.792969" xlink:href="#DejaVuSans-114"/>

     <use x="442.90625" xlink:href="#DejaVuSans-117"/>

     <use x="506.285156" xlink:href="#DejaVuSans-99"/>

     <use x="561.265625" xlink:href="#DejaVuSans-116"/>

     <use x="600.474609" xlink:href="#DejaVuSans-105"/>

     <use x="628.257812" xlink:href="#DejaVuSans-111"/>

     <use x="689.439453" xlink:href="#DejaVuSans-110"/>

    </g>

    <!-- Filtered back projection -->

    <defs>

     <path d="M 9.8125 72.90625 

L 51.703125 72.90625 

L 51.703125 64.59375 

L 19.671875 64.59375 

L 19.671875 43.109375 

L 48.578125 43.109375 

L 48.578125 34.8125 

L 19.671875 34.8125 

L 19.671875 0 

L 9.8125 0 

z

" id="DejaVuSans-70"/>

     <path d="M 9.421875 75.984375 

L 18.40625 75.984375 

L 18.40625 0 

L 9.421875 0 

z

" id="DejaVuSans-108"/>

     <path d="M 45.40625 46.390625 

L 45.40625 75.984375 

L 54.390625 75.984375 

L 54.390625 0 

L 45.40625 0 

L 45.40625 8.203125 

Q 42.578125 3.328125 38.25 0.953125 

Q 33.9375 -1.421875 27.875 -1.421875 

Q 17.96875 -1.421875 11.734375 6.484375 

Q 5.515625 14.40625 5.515625 27.296875 

Q 5.515625 40.1875 11.734375 48.09375 

Q 17.96875 56 27.875 56 

Q 33.9375 56 38.25 53.625 

Q 42.578125 51.265625 45.40625 46.390625 

z

M 14.796875 27.296875 

Q 14.796875 17.390625 18.875 11.75 

Q 22.953125 6.109375 30.078125 6.109375 

Q 37.203125 6.109375 41.296875 11.75 

Q 45.40625 17.390625 45.40625 27.296875 

Q 45.40625 37.203125 41.296875 42.84375 

Q 37.203125 48.484375 30.078125 48.484375 

Q 22.953125 48.484375 18.875 42.84375 

Q 14.796875 37.203125 14.796875 27.296875 

z

" id="DejaVuSans-100"/>

     <path id="DejaVuSans-32"/>

     <path d="M 48.6875 27.296875 

Q 48.6875 37.203125 44.609375 42.84375 

Q 40.53125 48.484375 33.40625 48.484375 

Q 26.265625 48.484375 22.1875 42.84375 

Q 18.109375 37.203125 18.109375 27.296875 

Q 18.109375 17.390625 22.1875 11.75 

Q 26.265625 6.109375 33.40625 6.109375 

Q 40.53125 6.109375 44.609375 11.75 

Q 48.6875 17.390625 48.6875 27.296875 

z

M 18.109375 46.390625 

Q 20.953125 51.265625 25.265625 53.625 

Q 29.59375 56 35.59375 56 

Q 45.5625 56 51.78125 48.09375 

Q 58.015625 40.1875 58.015625 27.296875 

Q 58.015625 14.40625 51.78125 6.484375 

Q 45.5625 -1.421875 35.59375 -1.421875 

Q 29.59375 -1.421875 25.265625 0.953125 

Q 20.953125 3.328125 18.109375 8.203125 

L 18.109375 0 

L 9.078125 0 

L 9.078125 75.984375 

L 18.109375 75.984375 

z

" id="DejaVuSans-98"/>

     <path d="M 34.28125 27.484375 

Q 23.390625 27.484375 19.1875 25 

Q 14.984375 22.515625 14.984375 16.5 

Q 14.984375 11.71875 18.140625 8.90625 

Q 21.296875 6.109375 26.703125 6.109375 

Q 34.1875 6.109375 38.703125 11.40625 

Q 43.21875 16.703125 43.21875 25.484375 

L 43.21875 27.484375 

z

M 52.203125 31.203125 

L 52.203125 0 

L 43.21875 0 

L 43.21875 8.296875 

Q 40.140625 3.328125 35.546875 0.953125 

Q 30.953125 -1.421875 24.3125 -1.421875 

Q 15.921875 -1.421875 10.953125 3.296875 

Q 6 8.015625 6 15.921875 

Q 6 25.140625 12.171875 29.828125 

Q 18.359375 34.515625 30.609375 34.515625 

L 43.21875 34.515625 

L 43.21875 35.40625 

Q 43.21875 41.609375 39.140625 45 

Q 35.0625 48.390625 27.6875 48.390625 

Q 23 48.390625 18.546875 47.265625 

Q 14.109375 46.140625 10.015625 43.890625 

L 10.015625 52.203125 

Q 14.9375 54.109375 19.578125 55.046875 

Q 24.21875 56 28.609375 56 

Q 40.484375 56 46.34375 49.84375 

Q 52.203125 43.703125 52.203125 31.203125 

z

" id="DejaVuSans-97"/>

     <path d="M 9.078125 75.984375 

L 18.109375 75.984375 

L 18.109375 31.109375 

L 44.921875 54.6875 

L 56.390625 54.6875 

L 27.390625 29.109375 

L 57.625 0 

L 45.90625 0 

L 18.109375 26.703125 

L 18.109375 0 

L 9.078125 0 

z

" id="DejaVuSans-107"/>

     <path d="M 18.109375 8.203125 

L 18.109375 -20.796875 

L 9.078125 -20.796875 

L 9.078125 54.6875 

L 18.109375 54.6875 

L 18.109375 46.390625 

Q 20.953125 51.265625 25.265625 53.625 

Q 29.59375 56 35.59375 56 

Q 45.5625 56 51.78125 48.09375 

Q 58.015625 40.1875 58.015625 27.296875 

Q 58.015625 14.40625 51.78125 6.484375 

Q 45.5625 -1.421875 35.59375 -1.421875 

Q 29.59375 -1.421875 25.265625 0.953125 

Q 20.953125 3.328125 18.109375 8.203125 

z

M 48.6875 27.296875 

Q 48.6875 37.203125 44.609375 42.84375 

Q 40.53125 48.484375 33.40625 48.484375 

Q 26.265625 48.484375 22.1875 42.84375 

Q 18.109375 37.203125 18.109375 27.296875 

Q 18.109375 17.390625 22.1875 11.75 

Q 26.265625 6.109375 33.40625 6.109375 

Q 40.53125 6.109375 44.609375 11.75 

Q 48.6875 17.390625 48.6875 27.296875 

z

" id="DejaVuSans-112"/>

     <path d="M 9.421875 54.6875 

L 18.40625 54.6875 

L 18.40625 -0.984375 

Q 18.40625 -11.421875 14.421875 -16.109375 

Q 10.453125 -20.796875 1.609375 -20.796875 

L -1.8125 -20.796875 

L -1.8125 -13.1875 

L 0.59375 -13.1875 

Q 5.71875 -13.1875 7.5625 -10.8125 

Q 9.421875 -8.453125 9.421875 -0.984375 

z

M 9.421875 75.984375 

L 18.40625 75.984375 

L 18.40625 64.59375 

L 9.421875 64.59375 

z

" id="DejaVuSans-106"/>

    </defs>

    <g transform="translate(63.785483 29.7555)scale(0.12 -0.12)">

     <use xlink:href="#DejaVuSans-70"/>

     <use x="57.410156" xlink:href="#DejaVuSans-105"/>

     <use x="85.193359" xlink:href="#DejaVuSans-108"/>

     <use x="112.976562" xlink:href="#DejaVuSans-116"/>

     <use x="152.185547" xlink:href="#DejaVuSans-101"/>

     <use x="213.708984" xlink:href="#DejaVuSans-114"/>

     <use x="254.791016" xlink:href="#DejaVuSans-101"/>

     <use x="316.314453" xlink:href="#DejaVuSans-100"/>

     <use x="379.791016" xlink:href="#DejaVuSans-32"/>

     <use x="411.578125" xlink:href="#DejaVuSans-98"/>

     <use x="475.054688" xlink:href="#DejaVuSans-97"/>

     <use x="536.333984" xlink:href="#DejaVuSans-99"/>

     <use x="591.314453" xlink:href="#DejaVuSans-107"/>

     <use x="649.224609" xlink:href="#DejaVuSans-32"/>

     <use x="681.011719" xlink:href="#DejaVuSans-112"/>

     <use x="744.488281" xlink:href="#DejaVuSans-114"/>

     <use x="785.570312" xlink:href="#DejaVuSans-111"/>

     <use x="846.751953" xlink:href="#DejaVuSans-106"/>

     <use x="874.535156" xlink:href="#DejaVuSans-101"/>

     <use x="936.058594" xlink:href="#DejaVuSans-99"/>

     <use x="991.039062" xlink:href="#DejaVuSans-116"/>

     <use x="1030.248047" xlink:href="#DejaVuSans-105"/>

     <use x="1058.03125" xlink:href="#DejaVuSans-111"/>

     <use x="1119.212891" xlink:href="#DejaVuSans-110"/>

    </g>

   </g>

  </g>

  <g id="axes_2">

   <g id="patch_7">

    <path d="M 276.778409 238.664591 

L 479.6875 238.664591 

L 479.6875 35.7555 

L 276.778409 35.7555 

z

" style="fill:#ffffff;"/>

   </g>

   <g clip-path="url(#pacf1ecf3f8)">

    <image height="203" id="imagec7828ac2d2" transform="scale(1 -1)translate(0 -203)" width="203" x="276.778409" xlink:href="data:image/png;base64,

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" y="-35.664591"/>

   </g>

   <g id="matplotlib.axis_3">

    <g id="xtick_7">

     <g id="line2d_13">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="276.976562" xlink:href="#m8b0a97d421" y="238.664591"/>

      </g>

     </g>

     <g id="text_14">

      <!-- 0 -->

      <g transform="translate(273.795313 253.263028)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_8">

     <g id="line2d_14">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="316.607244" xlink:href="#m8b0a97d421" y="238.664591"/>

      </g>

     </g>

     <g id="text_15">

      <!-- 100 -->

      <g transform="translate(307.063494 253.263028)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_9">

     <g id="line2d_15">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="356.237926" xlink:href="#m8b0a97d421" y="238.664591"/>

      </g>

     </g>

     <g id="text_16">

      <!-- 200 -->

      <g transform="translate(346.694176 253.263028)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-50"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_10">

     <g id="line2d_16">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="395.868608" xlink:href="#m8b0a97d421" y="238.664591"/>

      </g>

     </g>

     <g id="text_17">

      <!-- 300 -->

      <g transform="translate(386.324858 253.263028)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-51"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_11">

     <g id="line2d_17">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="435.49929" xlink:href="#m8b0a97d421" y="238.664591"/>

      </g>

     </g>

     <g id="text_18">

      <!-- 400 -->

      <g transform="translate(425.95554 253.263028)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-52"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_12">

     <g id="line2d_18">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="475.129972" xlink:href="#m8b0a97d421" y="238.664591"/>

      </g>

     </g>

     <g id="text_19">

      <!-- 500 -->

      <g transform="translate(465.586222 253.263028)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-53"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

   </g>

   <g id="matplotlib.axis_4">

    <g id="ytick_7">

     <g id="line2d_19">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="276.778409" xlink:href="#m7c4965ee86" y="35.953653"/>

      </g>

     </g>

    </g>

    <g id="ytick_8">

     <g id="line2d_20">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="276.778409" xlink:href="#m7c4965ee86" y="75.584335"/>

      </g>

     </g>

    </g>

    <g id="ytick_9">

     <g id="line2d_21">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="276.778409" xlink:href="#m7c4965ee86" y="115.215017"/>

      </g>

     </g>

    </g>

    <g id="ytick_10">

     <g id="line2d_22">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="276.778409" xlink:href="#m7c4965ee86" y="154.845699"/>

      </g>

     </g>

    </g>

    <g id="ytick_11">

     <g id="line2d_23">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="276.778409" xlink:href="#m7c4965ee86" y="194.476381"/>

      </g>

     </g>

    </g>

    <g id="ytick_12">

     <g id="line2d_24">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="276.778409" xlink:href="#m7c4965ee86" y="234.107062"/>

      </g>

     </g>

    </g>

   </g>

   <g id="patch_8">

    <path d="M 276.778409 238.664591 

L 276.778409 35.7555 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_9">

    <path d="M 479.6875 238.664591 

L 479.6875 35.7555 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_10">

    <path d="M 276.778409 238.664591 

L 479.6875 238.664591 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_11">

    <path d="M 276.778409 35.7555 

L 479.6875 35.7555 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="text_20">

    <!-- Reconstruction error -->

    <g transform="translate(316.39733 16.318125)scale(0.12 -0.12)">

     <use xlink:href="#DejaVuSans-82"/>

     <use x="69.419922" xlink:href="#DejaVuSans-101"/>

     <use x="130.943359" xlink:href="#DejaVuSans-99"/>

     <use x="185.923828" xlink:href="#DejaVuSans-111"/>

     <use x="247.105469" xlink:href="#DejaVuSans-110"/>

     <use x="310.484375" xlink:href="#DejaVuSans-115"/>

     <use x="362.583984" xlink:href="#DejaVuSans-116"/>

     <use x="401.792969" xlink:href="#DejaVuSans-114"/>

     <use x="442.90625" xlink:href="#DejaVuSans-117"/>

     <use x="506.285156" xlink:href="#DejaVuSans-99"/>

     <use x="561.265625" xlink:href="#DejaVuSans-116"/>

     <use x="600.474609" xlink:href="#DejaVuSans-105"/>

     <use x="628.257812" xlink:href="#DejaVuSans-111"/>

     <use x="689.439453" xlink:href="#DejaVuSans-110"/>

     <use x="752.818359" xlink:href="#DejaVuSans-32"/>

     <use x="784.605469" xlink:href="#DejaVuSans-101"/>

     <use x="846.128906" xlink:href="#DejaVuSans-114"/>

     <use x="887.226562" xlink:href="#DejaVuSans-114"/>

     <use x="928.308594" xlink:href="#DejaVuSans-111"/>

     <use x="989.490234" xlink:href="#DejaVuSans-114"/>

    </g>

    <!-- Filtered back projection -->

    <g transform="translate(307.276392 29.7555)scale(0.12 -0.12)">

     <use xlink:href="#DejaVuSans-70"/>

     <use x="57.410156" xlink:href="#DejaVuSans-105"/>

     <use x="85.193359" xlink:href="#DejaVuSans-108"/>

     <use x="112.976562" xlink:href="#DejaVuSans-116"/>

     <use x="152.185547" xlink:href="#DejaVuSans-101"/>

     <use x="213.708984" xlink:href="#DejaVuSans-114"/>

     <use x="254.791016" xlink:href="#DejaVuSans-101"/>

     <use x="316.314453" xlink:href="#DejaVuSans-100"/>

     <use x="379.791016" xlink:href="#DejaVuSans-32"/>

     <use x="411.578125" xlink:href="#DejaVuSans-98"/>

     <use x="475.054688" xlink:href="#DejaVuSans-97"/>

     <use x="536.333984" xlink:href="#DejaVuSans-99"/>

     <use x="591.314453" xlink:href="#DejaVuSans-107"/>

     <use x="649.224609" xlink:href="#DejaVuSans-32"/>

     <use x="681.011719" xlink:href="#DejaVuSans-112"/>

     <use x="744.488281" xlink:href="#DejaVuSans-114"/>

     <use x="785.570312" xlink:href="#DejaVuSans-111"/>

     <use x="846.751953" xlink:href="#DejaVuSans-106"/>

     <use x="874.535156" xlink:href="#DejaVuSans-101"/>

     <use x="936.058594" xlink:href="#DejaVuSans-99"/>

     <use x="991.039062" xlink:href="#DejaVuSans-116"/>

     <use x="1030.248047" xlink:href="#DejaVuSans-105"/>

     <use x="1058.03125" xlink:href="#DejaVuSans-111"/>

     <use x="1119.212891" xlink:href="#DejaVuSans-110"/>

    </g>

   </g>

  </g>

 </g>

 <defs>

  <clipPath id="p47ba5aa6ba">

   <rect height="202.909091" width="202.909091" x="33.2875" y="35.7555"/>

  </clipPath>

  <clipPath id="pacf1ecf3f8">

   <rect height="202.909091" width="202.909091" x="276.778409" y="35.7555"/>

  </clipPath>

 </defs>

</svg>


</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="-TomoPy.-Reconstruction-Pipeline-"><center> TomoPy. Reconstruction Pipeline </center><a class="anchor-link" href="#-TomoPy.-Reconstruction-Pipeline-">&#182;</a></h3><p><img src='tomopy2.png'></p>
<p><strong><a href="https://tomopy.readthedocs.io/en/latest/">TomoPy</a></strong> is an open-source Python package for tomographic data processing and image reconstruction.</p>
<ul>
<li>Gursoy D, De Carlo F, Xiao X, Jacobsen C. (2014). <em>TomoPy: a framework for the analysis of synchrotron tomographic data</em>. J. Synchrotron Rad. 21. 1188-1193 doi:10.1107/S1600577514013939</li>
</ul>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[5]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">obj</span> <span class="o">=</span> <span class="n">tomopy</span><span class="o">.</span><span class="n">misc</span><span class="o">.</span><span class="n">phantom</span><span class="o">.</span><span class="n">shepp2d</span><span class="p">()</span> <span class="c1"># Generate an object.</span>
<span class="n">ang</span> <span class="o">=</span> <span class="n">tomopy</span><span class="o">.</span><span class="n">angles</span><span class="p">(</span><span class="mi">180</span><span class="p">)</span> <span class="c1"># Generate uniformly spaced tilt angles.</span>
<span class="n">sim</span> <span class="o">=</span> <span class="n">tomopy</span><span class="o">.</span><span class="n">project</span><span class="p">(</span><span class="n">obj</span><span class="p">,</span> <span class="n">ang</span><span class="p">)</span> <span class="c1"># Calculate projections.</span>
<span class="n">rec_fbp</span> <span class="o">=</span> <span class="n">tomopy</span><span class="o">.</span><span class="n">recon</span><span class="p">(</span><span class="n">sim</span><span class="p">,</span> <span class="n">ang</span><span class="p">,</span> <span class="n">algorithm</span><span class="o">=</span><span class="s1">&#39;fbp&#39;</span><span class="p">)</span> <span class="c1"># Reconstruct object (Filtered back-projection algorithm).</span>

<span class="c1"># Different algorithm</span>
<span class="c1"># rec = tomopy.recon(sim, ang, algorithm=&#39;gridrec&#39;) # Fourier grid reconstruction algorithm .</span>
<span class="n">rec_art</span> <span class="o">=</span> <span class="n">tomopy</span><span class="o">.</span><span class="n">recon</span><span class="p">(</span><span class="n">sim</span><span class="p">,</span> <span class="n">ang</span><span class="p">,</span> <span class="n">algorithm</span><span class="o">=</span><span class="s1">&#39;art&#39;</span><span class="p">)</span> <span class="c1"># Algebraic reconstruction technique.</span>
<span class="c1"># rec = tomopy.recon(sim, ang, algorithm=&#39;sirt&#39;) # Simultaneous algebraic reconstruction technique.</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[6]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Show results.</span>
<span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">12</span><span class="p">,</span><span class="mi">4</span><span class="p">))</span>
<span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">141</span><span class="p">);</span> <span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;Original&#39;</span><span class="p">);</span>
<span class="n">plt</span><span class="o">.</span><span class="n">imshow</span><span class="p">(</span><span class="n">obj</span><span class="o">.</span><span class="n">squeeze</span><span class="p">(),</span> <span class="n">cmap</span><span class="o">=</span><span class="s1">&#39;gray&#39;</span><span class="p">);</span> 
<span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">142</span><span class="p">);</span>  <span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;Sinogram&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">imshow</span><span class="p">(</span><span class="n">sim</span><span class="o">.</span><span class="n">squeeze</span><span class="p">(),</span> <span class="n">cmap</span><span class="o">=</span><span class="s1">&#39;gray&#39;</span><span class="p">);</span>
<span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">143</span><span class="p">);</span> <span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;FBP&#39;</span><span class="p">);</span>
<span class="n">plt</span><span class="o">.</span><span class="n">imshow</span><span class="p">(</span><span class="n">rec_fbp</span><span class="o">.</span><span class="n">squeeze</span><span class="p">(),</span> <span class="n">cmap</span><span class="o">=</span><span class="s1">&#39;gray&#39;</span><span class="p">);</span>
<span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">144</span><span class="p">);</span> <span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;ART&#39;</span><span class="p">);</span>
<span class="n">plt</span><span class="o">.</span><span class="n">imshow</span><span class="p">(</span><span class="n">rec_art</span><span class="o">.</span><span class="n">squeeze</span><span class="p">(),</span> <span class="n">cmap</span><span class="o">=</span><span class="s1">&#39;gray&#39;</span><span class="p">);</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt"></div>


<div class="output_svg output_subarea ">
<?xml version="1.0" encoding="utf-8" standalone="no"?>

<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN"

  "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">

<!-- Created with matplotlib (https://matplotlib.org/) -->

<svg height="191.761467pt" version="1.1" viewBox="0 0 713.5875 191.761467" width="713.5875pt" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">

 <defs>

  <style type="text/css">

*{stroke-linecap:butt;stroke-linejoin:round;}

  </style>

 </defs>

 <g id="figure_1">

  <g id="patch_1">

   <path d="M 0 191.761467 

L 713.5875 191.761467 

L 713.5875 0 

L 0 0 

z

" style="fill:none;"/>

  </g>

  <g id="axes_1">

   <g id="patch_2">

    <path d="M 33.2875 167.883342 

L 178.852717 167.883342 

L 178.852717 22.318125 

L 33.2875 22.318125 

z

" style="fill:#ffffff;"/>

   </g>

   <g clip-path="url(#pd8b1a94454)">

    <image height="146" id="imagef876c9edd3" transform="scale(1 -1)translate(0 -146)" width="146" x="33.2875" xlink:href="data:image/png;base64,

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" y="-21.883342"/>

   </g>

   <g id="matplotlib.axis_1">

    <g id="xtick_1">

     <g id="line2d_1">

      <defs>

       <path d="M 0 0 

L 0 3.5 

" id="ma727998dc9" style="stroke:#000000;stroke-width:0.8;"/>

      </defs>

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.429654" xlink:href="#ma727998dc9" y="167.883342"/>

      </g>

     </g>

     <g id="text_1">

      <!-- 0 -->

      <defs>

       <path d="M 31.78125 66.40625 

Q 24.171875 66.40625 20.328125 58.90625 

Q 16.5 51.421875 16.5 36.375 

Q 16.5 21.390625 20.328125 13.890625 

Q 24.171875 6.390625 31.78125 6.390625 

Q 39.453125 6.390625 43.28125 13.890625 

Q 47.125 21.390625 47.125 36.375 

Q 47.125 51.421875 43.28125 58.90625 

Q 39.453125 66.40625 31.78125 66.40625 

z

M 31.78125 74.21875 

Q 44.046875 74.21875 50.515625 64.515625 

Q 56.984375 54.828125 56.984375 36.375 

Q 56.984375 17.96875 50.515625 8.265625 

Q 44.046875 -1.421875 31.78125 -1.421875 

Q 19.53125 -1.421875 13.0625 8.265625 

Q 6.59375 17.96875 6.59375 36.375 

Q 6.59375 54.828125 13.0625 64.515625 

Q 19.53125 74.21875 31.78125 74.21875 

z

" id="DejaVuSans-48"/>

      </defs>

      <g transform="translate(30.248404 182.48178)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_2">

     <g id="line2d_2">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="90.291067" xlink:href="#ma727998dc9" y="167.883342"/>

      </g>

     </g>

     <g id="text_2">

      <!-- 200 -->

      <defs>

       <path d="M 19.1875 8.296875 

L 53.609375 8.296875 

L 53.609375 0 

L 7.328125 0 

L 7.328125 8.296875 

Q 12.9375 14.109375 22.625 23.890625 

Q 32.328125 33.6875 34.8125 36.53125 

Q 39.546875 41.84375 41.421875 45.53125 

Q 43.3125 49.21875 43.3125 52.78125 

Q 43.3125 58.59375 39.234375 62.25 

Q 35.15625 65.921875 28.609375 65.921875 

Q 23.96875 65.921875 18.8125 64.3125 

Q 13.671875 62.703125 7.8125 59.421875 

L 7.8125 69.390625 

Q 13.765625 71.78125 18.9375 73 

Q 24.125 74.21875 28.421875 74.21875 

Q 39.75 74.21875 46.484375 68.546875 

Q 53.21875 62.890625 53.21875 53.421875 

Q 53.21875 48.921875 51.53125 44.890625 

Q 49.859375 40.875 45.40625 35.40625 

Q 44.1875 33.984375 37.640625 27.21875 

Q 31.109375 20.453125 19.1875 8.296875 

z

" id="DejaVuSans-50"/>

      </defs>

      <g transform="translate(80.747317 182.48178)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-50"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_3">

     <g id="line2d_3">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="147.15248" xlink:href="#ma727998dc9" y="167.883342"/>

      </g>

     </g>

     <g id="text_3">

      <!-- 400 -->

      <defs>

       <path d="M 37.796875 64.3125 

L 12.890625 25.390625 

L 37.796875 25.390625 

z

M 35.203125 72.90625 

L 47.609375 72.90625 

L 47.609375 25.390625 

L 58.015625 25.390625 

L 58.015625 17.1875 

L 47.609375 17.1875 

L 47.609375 0 

L 37.796875 0 

L 37.796875 17.1875 

L 4.890625 17.1875 

L 4.890625 26.703125 

z

" id="DejaVuSans-52"/>

      </defs>

      <g transform="translate(137.60873 182.48178)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-52"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

   </g>

   <g id="matplotlib.axis_2">

    <g id="ytick_1">

     <g id="line2d_4">

      <defs>

       <path d="M 0 0 

L -3.5 0 

" id="m77dc7963b3" style="stroke:#000000;stroke-width:0.8;"/>

      </defs>

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#m77dc7963b3" y="22.460279"/>

      </g>

     </g>

     <g id="text_4">

      <!-- 0 -->

      <g transform="translate(19.925 26.259497)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_2">

     <g id="line2d_5">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#m77dc7963b3" y="50.890985"/>

      </g>

     </g>

     <g id="text_5">

      <!-- 100 -->

      <defs>

       <path d="M 12.40625 8.296875 

L 28.515625 8.296875 

L 28.515625 63.921875 

L 10.984375 60.40625 

L 10.984375 69.390625 

L 28.421875 72.90625 

L 38.28125 72.90625 

L 38.28125 8.296875 

L 54.390625 8.296875 

L 54.390625 0 

L 12.40625 0 

z

" id="DejaVuSans-49"/>

      </defs>

      <g transform="translate(7.2 54.690204)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_3">

     <g id="line2d_6">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#m77dc7963b3" y="79.321692"/>

      </g>

     </g>

     <g id="text_6">

      <!-- 200 -->

      <g transform="translate(7.2 83.12091)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-50"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_4">

     <g id="line2d_7">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#m77dc7963b3" y="107.752398"/>

      </g>

     </g>

     <g id="text_7">

      <!-- 300 -->

      <defs>

       <path d="M 40.578125 39.3125 

Q 47.65625 37.796875 51.625 33 

Q 55.609375 28.21875 55.609375 21.1875 

Q 55.609375 10.40625 48.1875 4.484375 

Q 40.765625 -1.421875 27.09375 -1.421875 

Q 22.515625 -1.421875 17.65625 -0.515625 

Q 12.796875 0.390625 7.625 2.203125 

L 7.625 11.71875 

Q 11.71875 9.328125 16.59375 8.109375 

Q 21.484375 6.890625 26.8125 6.890625 

Q 36.078125 6.890625 40.9375 10.546875 

Q 45.796875 14.203125 45.796875 21.1875 

Q 45.796875 27.640625 41.28125 31.265625 

Q 36.765625 34.90625 28.71875 34.90625 

L 20.21875 34.90625 

L 20.21875 43.015625 

L 29.109375 43.015625 

Q 36.375 43.015625 40.234375 45.921875 

Q 44.09375 48.828125 44.09375 54.296875 

Q 44.09375 59.90625 40.109375 62.90625 

Q 36.140625 65.921875 28.71875 65.921875 

Q 24.65625 65.921875 20.015625 65.03125 

Q 15.375 64.15625 9.8125 62.3125 

L 9.8125 71.09375 

Q 15.4375 72.65625 20.34375 73.4375 

Q 25.25 74.21875 29.59375 74.21875 

Q 40.828125 74.21875 47.359375 69.109375 

Q 53.90625 64.015625 53.90625 55.328125 

Q 53.90625 49.265625 50.4375 45.09375 

Q 46.96875 40.921875 40.578125 39.3125 

z

" id="DejaVuSans-51"/>

      </defs>

      <g transform="translate(7.2 111.551617)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-51"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_5">

     <g id="line2d_8">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#m77dc7963b3" y="136.183105"/>

      </g>

     </g>

     <g id="text_8">

      <!-- 400 -->

      <g transform="translate(7.2 139.982323)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-52"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_6">

     <g id="line2d_9">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#m77dc7963b3" y="164.613811"/>

      </g>

     </g>

     <g id="text_9">

      <!-- 500 -->

      <defs>

       <path d="M 10.796875 72.90625 

L 49.515625 72.90625 

L 49.515625 64.59375 

L 19.828125 64.59375 

L 19.828125 46.734375 

Q 21.96875 47.46875 24.109375 47.828125 

Q 26.265625 48.1875 28.421875 48.1875 

Q 40.625 48.1875 47.75 41.5 

Q 54.890625 34.8125 54.890625 23.390625 

Q 54.890625 11.625 47.5625 5.09375 

Q 40.234375 -1.421875 26.90625 -1.421875 

Q 22.3125 -1.421875 17.546875 -0.640625 

Q 12.796875 0.140625 7.71875 1.703125 

L 7.71875 11.625 

Q 12.109375 9.234375 16.796875 8.0625 

Q 21.484375 6.890625 26.703125 6.890625 

Q 35.15625 6.890625 40.078125 11.328125 

Q 45.015625 15.765625 45.015625 23.390625 

Q 45.015625 31 40.078125 35.4375 

Q 35.15625 39.890625 26.703125 39.890625 

Q 22.75 39.890625 18.8125 39.015625 

Q 14.890625 38.140625 10.796875 36.28125 

z

" id="DejaVuSans-53"/>

      </defs>

      <g transform="translate(7.2 168.41303)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-53"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

   </g>

   <g id="patch_3">

    <path d="M 33.2875 167.883342 

L 33.2875 22.318125 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_4">

    <path d="M 178.852717 167.883342 

L 178.852717 22.318125 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_5">

    <path d="M 33.2875 167.883342 

L 178.852717 167.883342 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_6">

    <path d="M 33.2875 22.318125 

L 178.852717 22.318125 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="text_10">

    <!-- Original -->

    <defs>

     <path d="M 39.40625 66.21875 

Q 28.65625 66.21875 22.328125 58.203125 

Q 16.015625 50.203125 16.015625 36.375 

Q 16.015625 22.609375 22.328125 14.59375 

Q 28.65625 6.59375 39.40625 6.59375 

Q 50.140625 6.59375 56.421875 14.59375 

Q 62.703125 22.609375 62.703125 36.375 

Q 62.703125 50.203125 56.421875 58.203125 

Q 50.140625 66.21875 39.40625 66.21875 

z

M 39.40625 74.21875 

Q 54.734375 74.21875 63.90625 63.9375 

Q 73.09375 53.65625 73.09375 36.375 

Q 73.09375 19.140625 63.90625 8.859375 

Q 54.734375 -1.421875 39.40625 -1.421875 

Q 24.03125 -1.421875 14.8125 8.828125 

Q 5.609375 19.09375 5.609375 36.375 

Q 5.609375 53.65625 14.8125 63.9375 

Q 24.03125 74.21875 39.40625 74.21875 

z

" id="DejaVuSans-79"/>

     <path d="M 41.109375 46.296875 

Q 39.59375 47.171875 37.8125 47.578125 

Q 36.03125 48 33.890625 48 

Q 26.265625 48 22.1875 43.046875 

Q 18.109375 38.09375 18.109375 28.8125 

L 18.109375 0 

L 9.078125 0 

L 9.078125 54.6875 

L 18.109375 54.6875 

L 18.109375 46.1875 

Q 20.953125 51.171875 25.484375 53.578125 

Q 30.03125 56 36.53125 56 

Q 37.453125 56 38.578125 55.875 

Q 39.703125 55.765625 41.0625 55.515625 

z

" id="DejaVuSans-114"/>

     <path d="M 9.421875 54.6875 

L 18.40625 54.6875 

L 18.40625 0 

L 9.421875 0 

z

M 9.421875 75.984375 

L 18.40625 75.984375 

L 18.40625 64.59375 

L 9.421875 64.59375 

z

" id="DejaVuSans-105"/>

     <path d="M 45.40625 27.984375 

Q 45.40625 37.75 41.375 43.109375 

Q 37.359375 48.484375 30.078125 48.484375 

Q 22.859375 48.484375 18.828125 43.109375 

Q 14.796875 37.75 14.796875 27.984375 

Q 14.796875 18.265625 18.828125 12.890625 

Q 22.859375 7.515625 30.078125 7.515625 

Q 37.359375 7.515625 41.375 12.890625 

Q 45.40625 18.265625 45.40625 27.984375 

z

M 54.390625 6.78125 

Q 54.390625 -7.171875 48.1875 -13.984375 

Q 42 -20.796875 29.203125 -20.796875 

Q 24.46875 -20.796875 20.265625 -20.09375 

Q 16.0625 -19.390625 12.109375 -17.921875 

L 12.109375 -9.1875 

Q 16.0625 -11.328125 19.921875 -12.34375 

Q 23.78125 -13.375 27.78125 -13.375 

Q 36.625 -13.375 41.015625 -8.765625 

Q 45.40625 -4.15625 45.40625 5.171875 

L 45.40625 9.625 

Q 42.625 4.78125 38.28125 2.390625 

Q 33.9375 0 27.875 0 

Q 17.828125 0 11.671875 7.65625 

Q 5.515625 15.328125 5.515625 27.984375 

Q 5.515625 40.671875 11.671875 48.328125 

Q 17.828125 56 27.875 56 

Q 33.9375 56 38.28125 53.609375 

Q 42.625 51.21875 45.40625 46.390625 

L 45.40625 54.6875 

L 54.390625 54.6875 

z

" id="DejaVuSans-103"/>

     <path d="M 54.890625 33.015625 

L 54.890625 0 

L 45.90625 0 

L 45.90625 32.71875 

Q 45.90625 40.484375 42.875 44.328125 

Q 39.84375 48.1875 33.796875 48.1875 

Q 26.515625 48.1875 22.3125 43.546875 

Q 18.109375 38.921875 18.109375 30.90625 

L 18.109375 0 

L 9.078125 0 

L 9.078125 54.6875 

L 18.109375 54.6875 

L 18.109375 46.1875 

Q 21.34375 51.125 25.703125 53.5625 

Q 30.078125 56 35.796875 56 

Q 45.21875 56 50.046875 50.171875 

Q 54.890625 44.34375 54.890625 33.015625 

z

" id="DejaVuSans-110"/>

     <path d="M 34.28125 27.484375 

Q 23.390625 27.484375 19.1875 25 

Q 14.984375 22.515625 14.984375 16.5 

Q 14.984375 11.71875 18.140625 8.90625 

Q 21.296875 6.109375 26.703125 6.109375 

Q 34.1875 6.109375 38.703125 11.40625 

Q 43.21875 16.703125 43.21875 25.484375 

L 43.21875 27.484375 

z

M 52.203125 31.203125 

L 52.203125 0 

L 43.21875 0 

L 43.21875 8.296875 

Q 40.140625 3.328125 35.546875 0.953125 

Q 30.953125 -1.421875 24.3125 -1.421875 

Q 15.921875 -1.421875 10.953125 3.296875 

Q 6 8.015625 6 15.921875 

Q 6 25.140625 12.171875 29.828125 

Q 18.359375 34.515625 30.609375 34.515625 

L 43.21875 34.515625 

L 43.21875 35.40625 

Q 43.21875 41.609375 39.140625 45 

Q 35.0625 48.390625 27.6875 48.390625 

Q 23 48.390625 18.546875 47.265625 

Q 14.109375 46.140625 10.015625 43.890625 

L 10.015625 52.203125 

Q 14.9375 54.109375 19.578125 55.046875 

Q 24.21875 56 28.609375 56 

Q 40.484375 56 46.34375 49.84375 

Q 52.203125 43.703125 52.203125 31.203125 

z

" id="DejaVuSans-97"/>

     <path d="M 9.421875 75.984375 

L 18.40625 75.984375 

L 18.40625 0 

L 9.421875 0 

z

" id="DejaVuSans-108"/>

    </defs>

    <g transform="translate(82.591359 16.318125)scale(0.12 -0.12)">

     <use xlink:href="#DejaVuSans-79"/>

     <use x="78.710938" xlink:href="#DejaVuSans-114"/>

     <use x="119.824219" xlink:href="#DejaVuSans-105"/>

     <use x="147.607422" xlink:href="#DejaVuSans-103"/>

     <use x="211.083984" xlink:href="#DejaVuSans-105"/>

     <use x="238.867188" xlink:href="#DejaVuSans-110"/>

     <use x="302.246094" xlink:href="#DejaVuSans-97"/>

     <use x="363.525391" xlink:href="#DejaVuSans-108"/>

    </g>

   </g>

  </g>

  <g id="axes_2">

   <g id="patch_7">

    <path d="M 207.965761 113.096434 

L 353.530978 113.096434 

L 353.530978 77.105034 

L 207.965761 77.105034 

z

" style="fill:#ffffff;"/>

   </g>

   <g clip-path="url(#p347483644c)">

    <image height="36" id="image3024103451" transform="scale(1 -1)translate(0 -36)" width="146" x="207.965761" xlink:href="data:image/png;base64,

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" y="-77.096434"/>

   </g>

   <g id="matplotlib.axis_3">

    <g id="xtick_4">

     <g id="line2d_10">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="208.065737" xlink:href="#ma727998dc9" y="113.096434"/>

      </g>

     </g>

     <g id="text_11">

      <!-- 0 -->

      <g transform="translate(204.884487 127.694871)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_5">

     <g id="line2d_11">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="248.056181" xlink:href="#ma727998dc9" y="113.096434"/>

      </g>

     </g>

     <g id="text_12">

      <!-- 200 -->

      <g transform="translate(238.512431 127.694871)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-50"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_6">

     <g id="line2d_12">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="288.046626" xlink:href="#ma727998dc9" y="113.096434"/>

      </g>

     </g>

     <g id="text_13">

      <!-- 400 -->

      <g transform="translate(278.502876 127.694871)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-52"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_7">

     <g id="line2d_13">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="328.03707" xlink:href="#ma727998dc9" y="113.096434"/>

      </g>

     </g>

     <g id="text_14">

      <!-- 600 -->

      <defs>

       <path d="M 33.015625 40.375 

Q 26.375 40.375 22.484375 35.828125 

Q 18.609375 31.296875 18.609375 23.390625 

Q 18.609375 15.53125 22.484375 10.953125 

Q 26.375 6.390625 33.015625 6.390625 

Q 39.65625 6.390625 43.53125 10.953125 

Q 47.40625 15.53125 47.40625 23.390625 

Q 47.40625 31.296875 43.53125 35.828125 

Q 39.65625 40.375 33.015625 40.375 

z

M 52.59375 71.296875 

L 52.59375 62.3125 

Q 48.875 64.0625 45.09375 64.984375 

Q 41.3125 65.921875 37.59375 65.921875 

Q 27.828125 65.921875 22.671875 59.328125 

Q 17.53125 52.734375 16.796875 39.40625 

Q 19.671875 43.65625 24.015625 45.921875 

Q 28.375 48.1875 33.59375 48.1875 

Q 44.578125 48.1875 50.953125 41.515625 

Q 57.328125 34.859375 57.328125 23.390625 

Q 57.328125 12.15625 50.6875 5.359375 

Q 44.046875 -1.421875 33.015625 -1.421875 

Q 20.359375 -1.421875 13.671875 8.265625 

Q 6.984375 17.96875 6.984375 36.375 

Q 6.984375 53.65625 15.1875 63.9375 

Q 23.390625 74.21875 37.203125 74.21875 

Q 40.921875 74.21875 44.703125 73.484375 

Q 48.484375 72.75 52.59375 71.296875 

z

" id="DejaVuSans-54"/>

      </defs>

      <g transform="translate(318.49332 127.694871)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-54"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

   </g>

   <g id="matplotlib.axis_4">

    <g id="ytick_7">

     <g id="line2d_14">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="207.965761" xlink:href="#m77dc7963b3" y="77.20501"/>

      </g>

     </g>

     <g id="text_15">

      <!-- 0 -->

      <g transform="translate(194.603261 81.004229)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_8">

     <g id="line2d_15">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="207.965761" xlink:href="#m77dc7963b3" y="97.200232"/>

      </g>

     </g>

     <g id="text_16">

      <!-- 100 -->

      <g transform="translate(181.878261 100.999451)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

   </g>

   <g id="patch_8">

    <path d="M 207.965761 113.096434 

L 207.965761 77.105034 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_9">

    <path d="M 353.530978 113.096434 

L 353.530978 77.105034 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_10">

    <path d="M 207.965761 113.096434 

L 353.530978 113.096434 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_11">

    <path d="M 207.965761 77.105034 

L 353.530978 77.105034 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="text_17">

    <!-- Sinogram -->

    <defs>

     <path d="M 53.515625 70.515625 

L 53.515625 60.890625 

Q 47.90625 63.578125 42.921875 64.890625 

Q 37.9375 66.21875 33.296875 66.21875 

Q 25.25 66.21875 20.875 63.09375 

Q 16.5 59.96875 16.5 54.203125 

Q 16.5 49.359375 19.40625 46.890625 

Q 22.3125 44.4375 30.421875 42.921875 

L 36.375 41.703125 

Q 47.40625 39.59375 52.65625 34.296875 

Q 57.90625 29 57.90625 20.125 

Q 57.90625 9.515625 50.796875 4.046875 

Q 43.703125 -1.421875 29.984375 -1.421875 

Q 24.8125 -1.421875 18.96875 -0.25 

Q 13.140625 0.921875 6.890625 3.21875 

L 6.890625 13.375 

Q 12.890625 10.015625 18.65625 8.296875 

Q 24.421875 6.59375 29.984375 6.59375 

Q 38.421875 6.59375 43.015625 9.90625 

Q 47.609375 13.234375 47.609375 19.390625 

Q 47.609375 24.75 44.3125 27.78125 

Q 41.015625 30.8125 33.5 32.328125 

L 27.484375 33.5 

Q 16.453125 35.6875 11.515625 40.375 

Q 6.59375 45.0625 6.59375 53.421875 

Q 6.59375 63.09375 13.40625 68.65625 

Q 20.21875 74.21875 32.171875 74.21875 

Q 37.3125 74.21875 42.625 73.28125 

Q 47.953125 72.359375 53.515625 70.515625 

z

" id="DejaVuSans-83"/>

     <path d="M 30.609375 48.390625 

Q 23.390625 48.390625 19.1875 42.75 

Q 14.984375 37.109375 14.984375 27.296875 

Q 14.984375 17.484375 19.15625 11.84375 

Q 23.34375 6.203125 30.609375 6.203125 

Q 37.796875 6.203125 41.984375 11.859375 

Q 46.1875 17.53125 46.1875 27.296875 

Q 46.1875 37.015625 41.984375 42.703125 

Q 37.796875 48.390625 30.609375 48.390625 

z

M 30.609375 56 

Q 42.328125 56 49.015625 48.375 

Q 55.71875 40.765625 55.71875 27.296875 

Q 55.71875 13.875 49.015625 6.21875 

Q 42.328125 -1.421875 30.609375 -1.421875 

Q 18.84375 -1.421875 12.171875 6.21875 

Q 5.515625 13.875 5.515625 27.296875 

Q 5.515625 40.765625 12.171875 48.375 

Q 18.84375 56 30.609375 56 

z

" id="DejaVuSans-111"/>

     <path d="M 52 44.1875 

Q 55.375 50.25 60.0625 53.125 

Q 64.75 56 71.09375 56 

Q 79.640625 56 84.28125 50.015625 

Q 88.921875 44.046875 88.921875 33.015625 

L 88.921875 0 

L 79.890625 0 

L 79.890625 32.71875 

Q 79.890625 40.578125 77.09375 44.375 

Q 74.3125 48.1875 68.609375 48.1875 

Q 61.625 48.1875 57.5625 43.546875 

Q 53.515625 38.921875 53.515625 30.90625 

L 53.515625 0 

L 44.484375 0 

L 44.484375 32.71875 

Q 44.484375 40.625 41.703125 44.40625 

Q 38.921875 48.1875 33.109375 48.1875 

Q 26.21875 48.1875 22.15625 43.53125 

Q 18.109375 38.875 18.109375 30.90625 

L 18.109375 0 

L 9.078125 0 

L 9.078125 54.6875 

L 18.109375 54.6875 

L 18.109375 46.1875 

Q 21.1875 51.21875 25.484375 53.609375 

Q 29.78125 56 35.6875 56 

Q 41.65625 56 45.828125 52.96875 

Q 50 49.953125 52 44.1875 

z

" id="DejaVuSans-109"/>

    </defs>

    <g transform="translate(252.001807 71.105034)scale(0.12 -0.12)">

     <use xlink:href="#DejaVuSans-83"/>

     <use x="63.476562" xlink:href="#DejaVuSans-105"/>

     <use x="91.259766" xlink:href="#DejaVuSans-110"/>

     <use x="154.638672" xlink:href="#DejaVuSans-111"/>

     <use x="215.820312" xlink:href="#DejaVuSans-103"/>

     <use x="279.296875" xlink:href="#DejaVuSans-114"/>

     <use x="320.410156" xlink:href="#DejaVuSans-97"/>

     <use x="381.689453" xlink:href="#DejaVuSans-109"/>

    </g>

   </g>

  </g>

  <g id="axes_3">

   <g id="patch_12">

    <path d="M 382.644022 167.883342 

L 528.209239 167.883342 

L 528.209239 22.318125 

L 382.644022 22.318125 

z

" style="fill:#ffffff;"/>

   </g>

   <g clip-path="url(#p3288cd0d13)">

    <image height="146" id="image28d3681912" transform="scale(1 -1)translate(0 -146)" width="146" x="382.644022" xlink:href="data:image/png;base64,

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" y="-21.883342"/>

   </g>

   <g id="matplotlib.axis_5">

    <g id="xtick_8">

     <g id="line2d_16">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="382.743998" xlink:href="#ma727998dc9" y="167.883342"/>

      </g>

     </g>

     <g id="text_18">

      <!-- 0 -->

      <g transform="translate(379.562748 182.48178)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_9">

     <g id="line2d_17">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="422.734442" xlink:href="#ma727998dc9" y="167.883342"/>

      </g>

     </g>

     <g id="text_19">

      <!-- 200 -->

      <g transform="translate(413.190692 182.48178)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-50"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_10">

     <g id="line2d_18">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="462.724887" xlink:href="#ma727998dc9" y="167.883342"/>

      </g>

     </g>

     <g id="text_20">

      <!-- 400 -->

      <g transform="translate(453.181137 182.48178)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-52"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_11">

     <g id="line2d_19">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="502.715331" xlink:href="#ma727998dc9" y="167.883342"/>

      </g>

     </g>

     <g id="text_21">

      <!-- 600 -->

      <g transform="translate(493.171581 182.48178)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-54"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

   </g>

   <g id="matplotlib.axis_6">

    <g id="ytick_9">

     <g id="line2d_20">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="382.644022" xlink:href="#m77dc7963b3" y="22.418101"/>

      </g>

     </g>

     <g id="text_22">

      <!-- 0 -->

      <g transform="translate(369.281522 26.21732)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_10">

     <g id="line2d_21">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="382.644022" xlink:href="#m77dc7963b3" y="62.408545"/>

      </g>

     </g>

     <g id="text_23">

      <!-- 200 -->

      <g transform="translate(356.556522 66.207764)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-50"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_11">

     <g id="line2d_22">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="382.644022" xlink:href="#m77dc7963b3" y="102.39899"/>

      </g>

     </g>

     <g id="text_24">

      <!-- 400 -->

      <g transform="translate(356.556522 106.198209)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-52"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_12">

     <g id="line2d_23">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="382.644022" xlink:href="#m77dc7963b3" y="142.389434"/>

      </g>

     </g>

     <g id="text_25">

      <!-- 600 -->

      <g transform="translate(356.556522 146.188653)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-54"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

   </g>

   <g id="patch_13">

    <path d="M 382.644022 167.883342 

L 382.644022 22.318125 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_14">

    <path d="M 528.209239 167.883342 

L 528.209239 22.318125 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_15">

    <path d="M 382.644022 167.883342 

L 528.209239 167.883342 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_16">

    <path d="M 382.644022 22.318125 

L 528.209239 22.318125 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="text_26">

    <!-- FBP -->

    <defs>

     <path d="M 9.8125 72.90625 

L 51.703125 72.90625 

L 51.703125 64.59375 

L 19.671875 64.59375 

L 19.671875 43.109375 

L 48.578125 43.109375 

L 48.578125 34.8125 

L 19.671875 34.8125 

L 19.671875 0 

L 9.8125 0 

z

" id="DejaVuSans-70"/>

     <path d="M 19.671875 34.8125 

L 19.671875 8.109375 

L 35.5 8.109375 

Q 43.453125 8.109375 47.28125 11.40625 

Q 51.125 14.703125 51.125 21.484375 

Q 51.125 28.328125 47.28125 31.5625 

Q 43.453125 34.8125 35.5 34.8125 

z

M 19.671875 64.796875 

L 19.671875 42.828125 

L 34.28125 42.828125 

Q 41.5 42.828125 45.03125 45.53125 

Q 48.578125 48.25 48.578125 53.8125 

Q 48.578125 59.328125 45.03125 62.0625 

Q 41.5 64.796875 34.28125 64.796875 

z

M 9.8125 72.90625 

L 35.015625 72.90625 

Q 46.296875 72.90625 52.390625 68.21875 

Q 58.5 63.53125 58.5 54.890625 

Q 58.5 48.1875 55.375 44.234375 

Q 52.25 40.28125 46.1875 39.3125 

Q 53.46875 37.75 57.5 32.78125 

Q 61.53125 27.828125 61.53125 20.40625 

Q 61.53125 10.640625 54.890625 5.3125 

Q 48.25 0 35.984375 0 

L 9.8125 0 

z

" id="DejaVuSans-66"/>

     <path d="M 19.671875 64.796875 

L 19.671875 37.40625 

L 32.078125 37.40625 

Q 38.96875 37.40625 42.71875 40.96875 

Q 46.484375 44.53125 46.484375 51.125 

Q 46.484375 57.671875 42.71875 61.234375 

Q 38.96875 64.796875 32.078125 64.796875 

z

M 9.8125 72.90625 

L 32.078125 72.90625 

Q 44.34375 72.90625 50.609375 67.359375 

Q 56.890625 61.8125 56.890625 51.125 

Q 56.890625 40.328125 50.609375 34.8125 

Q 44.34375 29.296875 32.078125 29.296875 

L 19.671875 29.296875 

L 19.671875 0 

L 9.8125 0 

z

" id="DejaVuSans-80"/>

    </defs>

    <g transform="translate(444.241318 16.318125)scale(0.12 -0.12)">

     <use xlink:href="#DejaVuSans-70"/>

     <use x="57.519531" xlink:href="#DejaVuSans-66"/>

     <use x="126.123047" xlink:href="#DejaVuSans-80"/>

    </g>

   </g>

  </g>

  <g id="axes_4">

   <g id="patch_17">

    <path d="M 557.322283 167.883342 

L 702.8875 167.883342 

L 702.8875 22.318125 

L 557.322283 22.318125 

z

" style="fill:#ffffff;"/>

   </g>

   <g clip-path="url(#p790632aec0)">

    <image height="146" id="image809d74c76a" transform="scale(1 -1)translate(0 -146)" width="146" x="557.322283" xlink:href="data:image/png;base64,

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" y="-21.883342"/>

   </g>

   <g id="matplotlib.axis_7">

    <g id="xtick_12">

     <g id="line2d_24">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="557.422259" xlink:href="#ma727998dc9" y="167.883342"/>

      </g>

     </g>

     <g id="text_27">

      <!-- 0 -->

      <g transform="translate(554.241009 182.48178)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_13">

     <g id="line2d_25">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="597.412703" xlink:href="#ma727998dc9" y="167.883342"/>

      </g>

     </g>

     <g id="text_28">

      <!-- 200 -->

      <g transform="translate(587.868953 182.48178)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-50"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_14">

     <g id="line2d_26">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="637.403147" xlink:href="#ma727998dc9" y="167.883342"/>

      </g>

     </g>

     <g id="text_29">

      <!-- 400 -->

      <g transform="translate(627.859397 182.48178)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-52"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_15">

     <g id="line2d_27">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="677.393592" xlink:href="#ma727998dc9" y="167.883342"/>

      </g>

     </g>

     <g id="text_30">

      <!-- 600 -->

      <g transform="translate(667.849842 182.48178)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-54"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

   </g>

   <g id="matplotlib.axis_8">

    <g id="ytick_13">

     <g id="line2d_28">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="557.322283" xlink:href="#m77dc7963b3" y="22.418101"/>

      </g>

     </g>

     <g id="text_31">

      <!-- 0 -->

      <g transform="translate(543.959783 26.21732)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_14">

     <g id="line2d_29">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="557.322283" xlink:href="#m77dc7963b3" y="62.408545"/>

      </g>

     </g>

     <g id="text_32">

      <!-- 200 -->

      <g transform="translate(531.234783 66.207764)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-50"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_15">

     <g id="line2d_30">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="557.322283" xlink:href="#m77dc7963b3" y="102.39899"/>

      </g>

     </g>

     <g id="text_33">

      <!-- 400 -->

      <g transform="translate(531.234783 106.198209)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-52"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_16">

     <g id="line2d_31">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="557.322283" xlink:href="#m77dc7963b3" y="142.389434"/>

      </g>

     </g>

     <g id="text_34">

      <!-- 600 -->

      <g transform="translate(531.234783 146.188653)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-54"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

   </g>

   <g id="patch_18">

    <path d="M 557.322283 167.883342 

L 557.322283 22.318125 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_19">

    <path d="M 702.8875 167.883342 

L 702.8875 22.318125 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_20">

    <path d="M 557.322283 167.883342 

L 702.8875 167.883342 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_21">

    <path d="M 557.322283 22.318125 

L 702.8875 22.318125 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="text_35">

    <!-- ART -->

    <defs>

     <path d="M 34.1875 63.1875 

L 20.796875 26.90625 

L 47.609375 26.90625 

z

M 28.609375 72.90625 

L 39.796875 72.90625 

L 67.578125 0 

L 57.328125 0 

L 50.6875 18.703125 

L 17.828125 18.703125 

L 11.1875 0 

L 0.78125 0 

z

" id="DejaVuSans-65"/>

     <path d="M 44.390625 34.1875 

Q 47.5625 33.109375 50.5625 29.59375 

Q 53.5625 26.078125 56.59375 19.921875 

L 66.609375 0 

L 56 0 

L 46.6875 18.703125 

Q 43.0625 26.03125 39.671875 28.421875 

Q 36.28125 30.8125 30.421875 30.8125 

L 19.671875 30.8125 

L 19.671875 0 

L 9.8125 0 

L 9.8125 72.90625 

L 32.078125 72.90625 

Q 44.578125 72.90625 50.734375 67.671875 

Q 56.890625 62.453125 56.890625 51.90625 

Q 56.890625 45.015625 53.6875 40.46875 

Q 50.484375 35.9375 44.390625 34.1875 

z

M 19.671875 64.796875 

L 19.671875 38.921875 

L 32.078125 38.921875 

Q 39.203125 38.921875 42.84375 42.21875 

Q 46.484375 45.515625 46.484375 51.90625 

Q 46.484375 58.296875 42.84375 61.546875 

Q 39.203125 64.796875 32.078125 64.796875 

z

" id="DejaVuSans-82"/>

     <path d="M -0.296875 72.90625 

L 61.375 72.90625 

L 61.375 64.59375 

L 35.5 64.59375 

L 35.5 0 

L 25.59375 0 

L 25.59375 64.59375 

L -0.296875 64.59375 

z

" id="DejaVuSans-84"/>

    </defs>

    <g transform="translate(618.173329 16.318125)scale(0.12 -0.12)">

     <use xlink:href="#DejaVuSans-65"/>

     <use x="68.408203" xlink:href="#DejaVuSans-82"/>

     <use x="137.78125" xlink:href="#DejaVuSans-84"/>

    </g>

   </g>

  </g>

 </g>

 <defs>

  <clipPath id="pd8b1a94454">

   <rect height="145.565217" width="145.565217" x="33.2875" y="22.318125"/>

  </clipPath>

  <clipPath id="p347483644c">

   <rect height="35.9914" width="145.565217" x="207.965761" y="77.105034"/>

  </clipPath>

  <clipPath id="p3288cd0d13">

   <rect height="145.565217" width="145.565217" x="382.644022" y="22.318125"/>

  </clipPath>

  <clipPath id="p790632aec0">

   <rect height="145.565217" width="145.565217" x="557.322283" y="22.318125"/>

  </clipPath>

 </defs>

</svg>


</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="-Astra-Toolbox.-Reconstruction-Pipeline-"><center> Astra Toolbox. Reconstruction Pipeline </center><a class="anchor-link" href="#-Astra-Toolbox.-Reconstruction-Pipeline-">&#182;</a></h3><p>The <strong><a href="https://www.astra-toolbox.com/">ASTRA Toolbox</a></strong> is a MATLAB and Python toolbox of high-performance GPU primitives for 2D and 3D tomography.</p>
<p><img src='astra.png'></p>
<ul>
<li><p>W. van Aarle, W J. Palenstijn, J. De Beenhouwer, T. Altantzis, S. Bals, K. J. Batenburg, and J. Sijbers, <em>“The ASTRA Toolbox: a platform for advanced algorithm development in electron tomography”</em>, Ultramicroscopy, Vol. 147, p. 35–47, (2015)</p>
</li>
<li><p>W J. Palenstijn, K J. Batenburg, and J. Sijbers, <em>“Performance improvements for iterative electron tomography reconstruction using graphics processing units (GPUs)”</em>, Journal of structural biology, vol. 176, issue 2, pp. 250-253, 2011</p>
</li>
</ul>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[7]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">n_size</span> <span class="o">=</span> <span class="mi">256</span>
<span class="n">obj</span> <span class="o">=</span> <span class="n">tomopy</span><span class="o">.</span><span class="n">misc</span><span class="o">.</span><span class="n">phantom</span><span class="o">.</span><span class="n">shepp2d</span><span class="p">(</span><span class="n">n_size</span><span class="p">)</span><span class="o">.</span><span class="n">squeeze</span><span class="p">()</span>

<span class="c1"># Create a basic 128x128 square volume geometry</span>
<span class="n">vol_geom</span> <span class="o">=</span> <span class="n">astra</span><span class="o">.</span><span class="n">create_vol_geom</span><span class="p">(</span><span class="n">n_size</span><span class="p">,</span> <span class="n">n_size</span><span class="p">)</span>

<span class="c1"># Create a parallel beam geometry with 180 angles between 0 and pi, and 384 detector pixels of width 1.</span>
<span class="n">proj_geom</span> <span class="o">=</span> <span class="n">astra</span><span class="o">.</span><span class="n">create_proj_geom</span><span class="p">(</span><span class="s1">&#39;parallel&#39;</span><span class="p">,</span> <span class="mi">1</span><span class="p">,</span> <span class="mi">384</span><span class="p">,</span> <span class="n">np</span><span class="o">.</span><span class="n">linspace</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span><span class="n">np</span><span class="o">.</span><span class="n">pi</span><span class="p">,</span><span class="mi">180</span><span class="p">,</span><span class="kc">False</span><span class="p">))</span>


<span class="c1"># Create a sinogram using the GPU or CPU.</span>
<span class="n">proj_id</span> <span class="o">=</span> <span class="n">astra</span><span class="o">.</span><span class="n">create_projector</span><span class="p">(</span><span class="s1">&#39;cuda&#39;</span><span class="p">,</span> <span class="n">proj_geom</span><span class="p">,</span> <span class="n">vol_geom</span><span class="p">)</span>
<span class="n">sinogram_id</span><span class="p">,</span> <span class="n">sinogram</span> <span class="o">=</span> <span class="n">astra</span><span class="o">.</span><span class="n">create_sino</span><span class="p">(</span><span class="n">obj</span><span class="p">,</span> <span class="n">proj_id</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[8]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#### GPU RECONSTRUCTION ####</span>

<span class="c1"># Create a data object for the reconstruction</span>
<span class="n">rec_id</span> <span class="o">=</span> <span class="n">astra</span><span class="o">.</span><span class="n">data2d</span><span class="o">.</span><span class="n">create</span><span class="p">(</span><span class="s1">&#39;-vol&#39;</span><span class="p">,</span> <span class="n">vol_geom</span><span class="p">)</span>

<span class="c1"># Set up the parameters for a reconstruction algorithm using the GPU</span>
<span class="c1"># Available algorithms:</span>
<span class="c1"># SIRT_CUDA, SART_CUDA, EM_CUDA, FBP_CUDA (see the FBP sample)</span>
<span class="n">cfg</span> <span class="o">=</span> <span class="n">astra</span><span class="o">.</span><span class="n">astra_dict</span><span class="p">(</span><span class="s1">&#39;SIRT_CUDA&#39;</span><span class="p">)</span>
<span class="n">cfg</span><span class="p">[</span><span class="s1">&#39;ReconstructionDataId&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">rec_id</span>
<span class="n">cfg</span><span class="p">[</span><span class="s1">&#39;ProjectionDataId&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">sinogram_id</span>


<span class="c1"># Create the algorithm object from the configuration structure</span>
<span class="n">alg_id</span> <span class="o">=</span> <span class="n">astra</span><span class="o">.</span><span class="n">algorithm</span><span class="o">.</span><span class="n">create</span><span class="p">(</span><span class="n">cfg</span><span class="p">)</span>

<span class="c1"># Run 150 iterations of the algorithm</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">&#39;GPU, 150 iterations:&#39;</span><span class="p">)</span>
<span class="o">%</span> <span class="n">time</span> <span class="n">astra</span><span class="o">.</span><span class="n">algorithm</span><span class="o">.</span><span class="n">run</span><span class="p">(</span><span class="n">alg_id</span><span class="p">,</span> <span class="mi">150</span><span class="p">)</span>

<span class="c1"># Get the result</span>
<span class="n">rec_sirt_cuda</span> <span class="o">=</span> <span class="n">astra</span><span class="o">.</span><span class="n">data2d</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="n">rec_id</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt"></div>

<div class="output_subarea output_stream output_stdout output_text">
<pre>GPU, 150 iterations:
Wall time: 1.53 s
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[9]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#### CPU RECONSTRUCTION ####</span>

<span class="c1"># Create a data object for the reconstruction</span>
<span class="n">rec_cpu_id</span> <span class="o">=</span> <span class="n">astra</span><span class="o">.</span><span class="n">data2d</span><span class="o">.</span><span class="n">create</span><span class="p">(</span><span class="s1">&#39;-vol&#39;</span><span class="p">,</span> <span class="n">vol_geom</span><span class="p">)</span>

<span class="c1"># Set up the parameters for a reconstruction algorithm using the CPU</span>
<span class="c1"># The main difference with the configuration of a GPU algorithm is the extra ProjectorId setting.</span>
<span class="c1"># Available algorithms:</span>
<span class="c1"># ART, SART, SIRT, CGLS, FBP</span>
<span class="n">cfg</span> <span class="o">=</span> <span class="n">astra</span><span class="o">.</span><span class="n">astra_dict</span><span class="p">(</span><span class="s1">&#39;SIRT&#39;</span><span class="p">)</span>
<span class="n">cfg</span><span class="p">[</span><span class="s1">&#39;ReconstructionDataId&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">rec_cpu_id</span>
<span class="n">cfg</span><span class="p">[</span><span class="s1">&#39;ProjectionDataId&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">sinogram_id</span>
<span class="n">cfg</span><span class="p">[</span><span class="s1">&#39;ProjectorId&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">proj_id</span>


<span class="c1"># Create the algorithm object from the configuration structure</span>
<span class="n">alg_cpu_id</span> <span class="o">=</span> <span class="n">astra</span><span class="o">.</span><span class="n">algorithm</span><span class="o">.</span><span class="n">create</span><span class="p">(</span><span class="n">cfg</span><span class="p">)</span>

<span class="c1"># Run 20 iterations of the algorithm. This will have a runtime in the order of 10 seconds.</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">&#39;CPU, 150 iterations:&#39;</span><span class="p">)</span>
<span class="o">%</span> <span class="n">time</span>  <span class="n">astra</span><span class="o">.</span><span class="n">algorithm</span><span class="o">.</span><span class="n">run</span><span class="p">(</span><span class="n">alg_cpu_id</span><span class="p">,</span> <span class="mi">150</span><span class="p">)</span>

<span class="c1"># Get the result</span>
<span class="n">rec_sirt</span> <span class="o">=</span> <span class="n">astra</span><span class="o">.</span><span class="n">data2d</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="n">rec_id</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt"></div>

<div class="output_subarea output_stream output_stdout output_text">
<pre>CPU, 150 iterations:
Wall time: 93.8 ms
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[10]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Clean up. Note that GPU memory is tied up in the algorithm object, and main RAM in the data objects.</span>
<span class="n">astra</span><span class="o">.</span><span class="n">algorithm</span><span class="o">.</span><span class="n">delete</span><span class="p">(</span><span class="n">alg_id</span><span class="p">)</span>
<span class="n">astra</span><span class="o">.</span><span class="n">algorithm</span><span class="o">.</span><span class="n">delete</span><span class="p">(</span><span class="n">alg_cpu_id</span><span class="p">)</span>
<span class="n">astra</span><span class="o">.</span><span class="n">data2d</span><span class="o">.</span><span class="n">delete</span><span class="p">(</span><span class="n">rec_id</span><span class="p">)</span>
<span class="n">astra</span><span class="o">.</span><span class="n">data2d</span><span class="o">.</span><span class="n">delete</span><span class="p">(</span><span class="n">rec_cpu_id</span><span class="p">)</span>
<span class="n">astra</span><span class="o">.</span><span class="n">data2d</span><span class="o">.</span><span class="n">delete</span><span class="p">(</span><span class="n">sinogram_id</span><span class="p">)</span>
<span class="n">astra</span><span class="o">.</span><span class="n">projector</span><span class="o">.</span><span class="n">delete</span><span class="p">(</span><span class="n">proj_id</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[11]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Show results.</span>
<span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">12</span><span class="p">,</span><span class="mi">4</span><span class="p">))</span>
<span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">141</span><span class="p">);</span> <span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;Original&#39;</span><span class="p">);</span>
<span class="n">plt</span><span class="o">.</span><span class="n">imshow</span><span class="p">(</span><span class="n">obj</span><span class="p">,</span> <span class="n">cmap</span><span class="o">=</span><span class="s1">&#39;gray&#39;</span><span class="p">);</span> 
<span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">142</span><span class="p">);</span>  <span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;Sinogram&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">imshow</span><span class="p">(</span><span class="n">sinogram</span><span class="p">,</span> <span class="n">cmap</span><span class="o">=</span><span class="s1">&#39;gray&#39;</span><span class="p">);</span>
<span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">143</span><span class="p">);</span>  <span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;SIRT_CUDA&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">imshow</span><span class="p">(</span><span class="n">rec_sirt_cuda</span><span class="p">,</span> <span class="n">cmap</span><span class="o">=</span><span class="s1">&#39;gray&#39;</span><span class="p">);</span>
<span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">144</span><span class="p">);</span>  <span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;SIRT&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">imshow</span><span class="p">(</span><span class="n">rec_sirt</span><span class="p">,</span> <span class="n">cmap</span><span class="o">=</span><span class="s1">&#39;gray&#39;</span><span class="p">);</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt"></div>


<div class="output_svg output_subarea ">
<?xml version="1.0" encoding="utf-8" standalone="no"?>

<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN"

  "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">

<!-- Created with matplotlib (https://matplotlib.org/) -->

<svg height="191.761467pt" version="1.1" viewBox="0 0 713.5875 191.761467" width="713.5875pt" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">

 <defs>

  <style type="text/css">

*{stroke-linecap:butt;stroke-linejoin:round;}

  </style>

 </defs>

 <g id="figure_1">

  <g id="patch_1">

   <path d="M 0 191.761467 

L 713.5875 191.761467 

L 713.5875 0 

L 0 0 

z

" style="fill:none;"/>

  </g>

  <g id="axes_1">

   <g id="patch_2">

    <path d="M 33.2875 167.883342 

L 178.852717 167.883342 

L 178.852717 22.318125 

L 33.2875 22.318125 

z

" style="fill:#ffffff;"/>

   </g>

   <g clip-path="url(#p3c320e4a05)">

    <image height="146" id="image9b9a75adaf" transform="scale(1 -1)translate(0 -146)" width="146" x="33.2875" xlink:href="data:image/png;base64,

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" y="-21.883342"/>

   </g>

   <g id="matplotlib.axis_1">

    <g id="xtick_1">

     <g id="line2d_1">

      <defs>

       <path d="M 0 0 

L 0 3.5 

" id="md4369562c1" style="stroke:#000000;stroke-width:0.8;"/>

      </defs>

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.571807" xlink:href="#md4369562c1" y="167.883342"/>

      </g>

     </g>

     <g id="text_1">

      <!-- 0 -->

      <defs>

       <path d="M 31.78125 66.40625 

Q 24.171875 66.40625 20.328125 58.90625 

Q 16.5 51.421875 16.5 36.375 

Q 16.5 21.390625 20.328125 13.890625 

Q 24.171875 6.390625 31.78125 6.390625 

Q 39.453125 6.390625 43.28125 13.890625 

Q 47.125 21.390625 47.125 36.375 

Q 47.125 51.421875 43.28125 58.90625 

Q 39.453125 66.40625 31.78125 66.40625 

z

M 31.78125 74.21875 

Q 44.046875 74.21875 50.515625 64.515625 

Q 56.984375 54.828125 56.984375 36.375 

Q 56.984375 17.96875 50.515625 8.265625 

Q 44.046875 -1.421875 31.78125 -1.421875 

Q 19.53125 -1.421875 13.0625 8.265625 

Q 6.59375 17.96875 6.59375 36.375 

Q 6.59375 54.828125 13.0625 64.515625 

Q 19.53125 74.21875 31.78125 74.21875 

z

" id="DejaVuSans-48"/>

      </defs>

      <g transform="translate(30.390557 182.48178)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_2">

     <g id="line2d_2">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="90.43322" xlink:href="#md4369562c1" y="167.883342"/>

      </g>

     </g>

     <g id="text_2">

      <!-- 100 -->

      <defs>

       <path d="M 12.40625 8.296875 

L 28.515625 8.296875 

L 28.515625 63.921875 

L 10.984375 60.40625 

L 10.984375 69.390625 

L 28.421875 72.90625 

L 38.28125 72.90625 

L 38.28125 8.296875 

L 54.390625 8.296875 

L 54.390625 0 

L 12.40625 0 

z

" id="DejaVuSans-49"/>

      </defs>

      <g transform="translate(80.88947 182.48178)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_3">

     <g id="line2d_3">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="147.294633" xlink:href="#md4369562c1" y="167.883342"/>

      </g>

     </g>

     <g id="text_3">

      <!-- 200 -->

      <defs>

       <path d="M 19.1875 8.296875 

L 53.609375 8.296875 

L 53.609375 0 

L 7.328125 0 

L 7.328125 8.296875 

Q 12.9375 14.109375 22.625 23.890625 

Q 32.328125 33.6875 34.8125 36.53125 

Q 39.546875 41.84375 41.421875 45.53125 

Q 43.3125 49.21875 43.3125 52.78125 

Q 43.3125 58.59375 39.234375 62.25 

Q 35.15625 65.921875 28.609375 65.921875 

Q 23.96875 65.921875 18.8125 64.3125 

Q 13.671875 62.703125 7.8125 59.421875 

L 7.8125 69.390625 

Q 13.765625 71.78125 18.9375 73 

Q 24.125 74.21875 28.421875 74.21875 

Q 39.75 74.21875 46.484375 68.546875 

Q 53.21875 62.890625 53.21875 53.421875 

Q 53.21875 48.921875 51.53125 44.890625 

Q 49.859375 40.875 45.40625 35.40625 

Q 44.1875 33.984375 37.640625 27.21875 

Q 31.109375 20.453125 19.1875 8.296875 

z

" id="DejaVuSans-50"/>

      </defs>

      <g transform="translate(137.750883 182.48178)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-50"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

   </g>

   <g id="matplotlib.axis_2">

    <g id="ytick_1">

     <g id="line2d_4">

      <defs>

       <path d="M 0 0 

L -3.5 0 

" id="m60fbb1ff4c" style="stroke:#000000;stroke-width:0.8;"/>

      </defs>

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#m60fbb1ff4c" y="22.602432"/>

      </g>

     </g>

     <g id="text_4">

      <!-- 0 -->

      <g transform="translate(19.925 26.401651)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_2">

     <g id="line2d_5">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#m60fbb1ff4c" y="51.033139"/>

      </g>

     </g>

     <g id="text_5">

      <!-- 50 -->

      <defs>

       <path d="M 10.796875 72.90625 

L 49.515625 72.90625 

L 49.515625 64.59375 

L 19.828125 64.59375 

L 19.828125 46.734375 

Q 21.96875 47.46875 24.109375 47.828125 

Q 26.265625 48.1875 28.421875 48.1875 

Q 40.625 48.1875 47.75 41.5 

Q 54.890625 34.8125 54.890625 23.390625 

Q 54.890625 11.625 47.5625 5.09375 

Q 40.234375 -1.421875 26.90625 -1.421875 

Q 22.3125 -1.421875 17.546875 -0.640625 

Q 12.796875 0.140625 7.71875 1.703125 

L 7.71875 11.625 

Q 12.109375 9.234375 16.796875 8.0625 

Q 21.484375 6.890625 26.703125 6.890625 

Q 35.15625 6.890625 40.078125 11.328125 

Q 45.015625 15.765625 45.015625 23.390625 

Q 45.015625 31 40.078125 35.4375 

Q 35.15625 39.890625 26.703125 39.890625 

Q 22.75 39.890625 18.8125 39.015625 

Q 14.890625 38.140625 10.796875 36.28125 

z

" id="DejaVuSans-53"/>

      </defs>

      <g transform="translate(13.5625 54.832357)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-53"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_3">

     <g id="line2d_6">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#m60fbb1ff4c" y="79.463845"/>

      </g>

     </g>

     <g id="text_6">

      <!-- 100 -->

      <g transform="translate(7.2 83.263064)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_4">

     <g id="line2d_7">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#m60fbb1ff4c" y="107.894552"/>

      </g>

     </g>

     <g id="text_7">

      <!-- 150 -->

      <g transform="translate(7.2 111.69377)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-53"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_5">

     <g id="line2d_8">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#m60fbb1ff4c" y="136.325258"/>

      </g>

     </g>

     <g id="text_8">

      <!-- 200 -->

      <g transform="translate(7.2 140.124477)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-50"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_6">

     <g id="line2d_9">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#m60fbb1ff4c" y="164.755965"/>

      </g>

     </g>

     <g id="text_9">

      <!-- 250 -->

      <g transform="translate(7.2 168.555183)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-50"/>

       <use x="63.623047" xlink:href="#DejaVuSans-53"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

   </g>

   <g id="patch_3">

    <path d="M 33.2875 167.883342 

L 33.2875 22.318125 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_4">

    <path d="M 178.852717 167.883342 

L 178.852717 22.318125 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_5">

    <path d="M 33.2875 167.883342 

L 178.852717 167.883342 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_6">

    <path d="M 33.2875 22.318125 

L 178.852717 22.318125 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="text_10">

    <!-- Original -->

    <defs>

     <path d="M 39.40625 66.21875 

Q 28.65625 66.21875 22.328125 58.203125 

Q 16.015625 50.203125 16.015625 36.375 

Q 16.015625 22.609375 22.328125 14.59375 

Q 28.65625 6.59375 39.40625 6.59375 

Q 50.140625 6.59375 56.421875 14.59375 

Q 62.703125 22.609375 62.703125 36.375 

Q 62.703125 50.203125 56.421875 58.203125 

Q 50.140625 66.21875 39.40625 66.21875 

z

M 39.40625 74.21875 

Q 54.734375 74.21875 63.90625 63.9375 

Q 73.09375 53.65625 73.09375 36.375 

Q 73.09375 19.140625 63.90625 8.859375 

Q 54.734375 -1.421875 39.40625 -1.421875 

Q 24.03125 -1.421875 14.8125 8.828125 

Q 5.609375 19.09375 5.609375 36.375 

Q 5.609375 53.65625 14.8125 63.9375 

Q 24.03125 74.21875 39.40625 74.21875 

z

" id="DejaVuSans-79"/>

     <path d="M 41.109375 46.296875 

Q 39.59375 47.171875 37.8125 47.578125 

Q 36.03125 48 33.890625 48 

Q 26.265625 48 22.1875 43.046875 

Q 18.109375 38.09375 18.109375 28.8125 

L 18.109375 0 

L 9.078125 0 

L 9.078125 54.6875 

L 18.109375 54.6875 

L 18.109375 46.1875 

Q 20.953125 51.171875 25.484375 53.578125 

Q 30.03125 56 36.53125 56 

Q 37.453125 56 38.578125 55.875 

Q 39.703125 55.765625 41.0625 55.515625 

z

" id="DejaVuSans-114"/>

     <path d="M 9.421875 54.6875 

L 18.40625 54.6875 

L 18.40625 0 

L 9.421875 0 

z

M 9.421875 75.984375 

L 18.40625 75.984375 

L 18.40625 64.59375 

L 9.421875 64.59375 

z

" id="DejaVuSans-105"/>

     <path d="M 45.40625 27.984375 

Q 45.40625 37.75 41.375 43.109375 

Q 37.359375 48.484375 30.078125 48.484375 

Q 22.859375 48.484375 18.828125 43.109375 

Q 14.796875 37.75 14.796875 27.984375 

Q 14.796875 18.265625 18.828125 12.890625 

Q 22.859375 7.515625 30.078125 7.515625 

Q 37.359375 7.515625 41.375 12.890625 

Q 45.40625 18.265625 45.40625 27.984375 

z

M 54.390625 6.78125 

Q 54.390625 -7.171875 48.1875 -13.984375 

Q 42 -20.796875 29.203125 -20.796875 

Q 24.46875 -20.796875 20.265625 -20.09375 

Q 16.0625 -19.390625 12.109375 -17.921875 

L 12.109375 -9.1875 

Q 16.0625 -11.328125 19.921875 -12.34375 

Q 23.78125 -13.375 27.78125 -13.375 

Q 36.625 -13.375 41.015625 -8.765625 

Q 45.40625 -4.15625 45.40625 5.171875 

L 45.40625 9.625 

Q 42.625 4.78125 38.28125 2.390625 

Q 33.9375 0 27.875 0 

Q 17.828125 0 11.671875 7.65625 

Q 5.515625 15.328125 5.515625 27.984375 

Q 5.515625 40.671875 11.671875 48.328125 

Q 17.828125 56 27.875 56 

Q 33.9375 56 38.28125 53.609375 

Q 42.625 51.21875 45.40625 46.390625 

L 45.40625 54.6875 

L 54.390625 54.6875 

z

" id="DejaVuSans-103"/>

     <path d="M 54.890625 33.015625 

L 54.890625 0 

L 45.90625 0 

L 45.90625 32.71875 

Q 45.90625 40.484375 42.875 44.328125 

Q 39.84375 48.1875 33.796875 48.1875 

Q 26.515625 48.1875 22.3125 43.546875 

Q 18.109375 38.921875 18.109375 30.90625 

L 18.109375 0 

L 9.078125 0 

L 9.078125 54.6875 

L 18.109375 54.6875 

L 18.109375 46.1875 

Q 21.34375 51.125 25.703125 53.5625 

Q 30.078125 56 35.796875 56 

Q 45.21875 56 50.046875 50.171875 

Q 54.890625 44.34375 54.890625 33.015625 

z

" id="DejaVuSans-110"/>

     <path d="M 34.28125 27.484375 

Q 23.390625 27.484375 19.1875 25 

Q 14.984375 22.515625 14.984375 16.5 

Q 14.984375 11.71875 18.140625 8.90625 

Q 21.296875 6.109375 26.703125 6.109375 

Q 34.1875 6.109375 38.703125 11.40625 

Q 43.21875 16.703125 43.21875 25.484375 

L 43.21875 27.484375 

z

M 52.203125 31.203125 

L 52.203125 0 

L 43.21875 0 

L 43.21875 8.296875 

Q 40.140625 3.328125 35.546875 0.953125 

Q 30.953125 -1.421875 24.3125 -1.421875 

Q 15.921875 -1.421875 10.953125 3.296875 

Q 6 8.015625 6 15.921875 

Q 6 25.140625 12.171875 29.828125 

Q 18.359375 34.515625 30.609375 34.515625 

L 43.21875 34.515625 

L 43.21875 35.40625 

Q 43.21875 41.609375 39.140625 45 

Q 35.0625 48.390625 27.6875 48.390625 

Q 23 48.390625 18.546875 47.265625 

Q 14.109375 46.140625 10.015625 43.890625 

L 10.015625 52.203125 

Q 14.9375 54.109375 19.578125 55.046875 

Q 24.21875 56 28.609375 56 

Q 40.484375 56 46.34375 49.84375 

Q 52.203125 43.703125 52.203125 31.203125 

z

" id="DejaVuSans-97"/>

     <path d="M 9.421875 75.984375 

L 18.40625 75.984375 

L 18.40625 0 

L 9.421875 0 

z

" id="DejaVuSans-108"/>

    </defs>

    <g transform="translate(82.591359 16.318125)scale(0.12 -0.12)">

     <use xlink:href="#DejaVuSans-79"/>

     <use x="78.710938" xlink:href="#DejaVuSans-114"/>

     <use x="119.824219" xlink:href="#DejaVuSans-105"/>

     <use x="147.607422" xlink:href="#DejaVuSans-103"/>

     <use x="211.083984" xlink:href="#DejaVuSans-105"/>

     <use x="238.867188" xlink:href="#DejaVuSans-110"/>

     <use x="302.246094" xlink:href="#DejaVuSans-97"/>

     <use x="363.525391" xlink:href="#DejaVuSans-108"/>

    </g>

   </g>

  </g>

  <g id="axes_2">

   <g id="patch_7">

    <path d="M 207.965761 129.217582 

L 353.530978 129.217582 

L 353.530978 60.983886 

L 207.965761 60.983886 

z

" style="fill:#ffffff;"/>

   </g>

   <g clip-path="url(#pe33ea7faeb)">

    <image height="69" id="imagef54d9e7121" transform="scale(1 -1)translate(0 -69)" width="146" x="207.965761" xlink:href="data:image/png;base64,

iVBORw0KGgoAAAANSUhEUgAAAJIAAABFCAYAAAChQL8ZAAAABHNCSVQICAgIfAhkiAAAGEtJREFUeJzlXU1vG1XUfuwZj8d2HCdpU2iagkpa0RaVCroAiZ8AQmLBlj0bFgiJ7fsjukaIZVfAEiEhQJHa8tFCq6ot0BaqJk0hqfPl7493kfe5ee7xuNAkji29R4ocj2fuXN/z3HOec8694xSALkZU8vk8rly5gkuXLqFaraLb7SKTySCdTiMIAgRBgEwmgzAM3f9BECCdTiMMQ6TTaaTTaSwuLqJSqaBer6PdbqPb7SKVSiEIAuRyOZRKJRQKBRw6dAhHjx5FOp3G2toaNjc30W63UavV0Gq10G630W630Wq1UK/X0Ww20e120Wg00Gw2sbm56fre7frDGgSBe81kMiiVSmi32+h0Omi1Wmg2m+h0Oq7NdrsNABgbG8O5c+dw9uxZVCqV/Rv8p5T0sDvwJMnn8wCARqPhBrbVajkldToddLtd98dz+Fmn0/Ha4zn863Q6DlydTgdRFLljvCcVm06nXRsAkEqlkMlkkEqlEIYhMpkMstksUqmUAymBzGv5GftH0eNBEKDT6bjrut0uwjB0YzGqMtJAmp2ddRYgnU47oFDxgA8mvu90Ok45fN/pdJw16na77hgtCq+v1+tYW1tDpVJxIGK7vL8ChVYwDEPEceysYyqVQjqd7gEWsAXGZrPpAQgA0uk0Op0OwjAEANfW2NgYZmdn92HEdy4jDaRz585hYWEBzWYTlUrFAUEtCgAHGLVOCigFEz8D4GZ+u93G2toaGo0GHj9+jI2NDTSbTefOWq0WWq2W1zcFSyaTQSaTQRRFyOVyzlIB8CyS9pWTg2CjhGHogTEIAmSzWZw7d27Qw70rGVkgpVIpzM3N4dGjR2i328hkMgDggYeilkZBRIXpuQo4zny6y+XlZVSrVc/9NZtNz2WSX7EfChJyN/ZVgWI5k/aF7pHfi+cHQYB2u41Go4G5uTnve4yajCyQjh49ijNnzmB5eRmdTge1Wg3NZhONRsMDQ6vV8iwN/1dwEQzKVYIgcCS32+2iWq1iaWkJ9XodtVoNtVoNjUbDs0oKVFojJe4AHF8ip0kCPgDPTSuY2PcgCNzxxcVFnDlzBkePHt2v4X9qGVkgvfbaazh48KBTIhUXRZE3uznYFCXZyo0AOAVRYcCWgqvVKqrVKur1OqrVqruG7lOtHa2FXs9jaoHomlSs9aJVtADV79VsNlEulzEzM4PXXnttACO9NxIA+J9hdyJJPvroIzQaDTx69AiNRqOHuAJwilAFAXCgIyDW1tbQbrd7Iia6qFqt5kDDqIlAUU6lgLJ/2p4Kr1cQ8nso2VaLGoahB+AoivDSSy+h3W7jiy++GNCI705G0iJNTk5ibm4O9+/fR61WAwCPp9j/6X6SUgGbm5se39DIq9VqoVqtOhdXrVYdT2IKgG6RLlVdqYII8AFKkGezWXd/Pc8ClMJ+8rx0Oo2NjQ0UCgWcPXsWk5OTezrWeyUjaZHeeustzM7O4u+///ZmrEZK+qdklqSV70me1eXx/Hq97hFzfsZ2Vfkq6oKs9VKLQ0mn014+Sl2hRpXatlq2TCaDOI5x4MAB3Lx5Ezdu3Nibgd5DGTmLNDMzg3feeQd379511kBzORTlP5y5JN9qeTR6A7a5R7VadRaHoX6j0UCj0UC5XEaz2XSEW1MBvB+P2RwW70FhBl4Bzs9JqDUSpJvW/1utFu7fv4/p6Wm88847Axv73cjIAentt9/GxMSEAxGBxEHXqEzdmeaYOKv1PGBbOSxHqKUiCBjyE2gEEAHH9mhxUqmUl9PiMb6yL0q+CSRNTTBByX4p72u1WqjVanjw4AGee+45TE9PD1gLTy8j5dpSqRQ+/vhj3L59GxsbGx6xBuBlh9X1qJL083a77eplBCCVomkEAkOTmO1220VU6jrV7fwbEdfj7Fej0XCTgoECo0lrYTkB6AKr1SpefvllAMC33347OEXsQEYKSO+99x5KpRJWVlZ6QnZbjwK2+YzOfLoQAM5VqcVg6UOJMyO8JDDofW2WnMf6kW4t1fA976VcjJ8RSHofBWK328XJkyfdPX/55ZeB6eJpZaRc2+uvv47l5WWPz7Daz/c6U9UdAdtWiJZHs9KpVMqBiNxGrQTdCZXJCj8ToerW9L42IUpXqK5OrRk5E9/b+qHNS3ES0c3eunULs7OzeP311weniB3IyADp3LlzKBQKLhzXGaqz1JYrlIzrsgxmtHkO27WK04Rmo9Fw7dbrddTrdWxsbDglqnVjH+1qAlsKYf8UJAQsXbVaRgCe1WNBudvtolarYXFxEceOHcMrr7wyUvW3kXBthUIBH374ocsbqXLVXdnZTNFkpboaAkAjNAtSYNsFKTDZvq4+ILchsNU6JuWFktwewZLJZJzltDyL/yupV1ebzWYxMzODIAjw/fffo9ls7rVKnlpGwiK9++67mJmZcRYBgDd7lav0K1PYRCRnMiv3GqprtMfr1QVqlpmWTUk7z6/X6wDg7qNRJYGqwOCrLZ+wLxoQaBJTLVSz2cTS0hKmpqZw7NgxvPvuu4NUzX+WoVukVCqFDz74AH/88QcqlUpPvSkMQw9UtAoEmCXibJOuiFlqgsm2b12cjdwo5FBK5u35Sqo1saifab+ZiuC9CCbLA3WiqKWemppCGIb48ssvB6ih/yZDt0ivvvoqAGB9fb2HY4Rh+MRVj6xJAT5f0gSkBY+SaRUCVO+lvKzT6aBSqfSQaQWwEm9Vvs2a8xXYcnHqwjSq44TRvnKCLC4uYmpqCkeOHHFjOEwZukV6//33sbS0hFqt5hFOwF/Po+E9C5uAX5tSssrFcBpt2SQmzwWQSJaT/tf8lSXr2p7lcGyDAInj2B1jOoLX8/varLe6+E6ngzNnzjjr+8033+xOEbuUoVqkubk5HDlyxBVW+yXzmEsC4KIdtURqbZhoZNFVybUNyS030Ve1RJrZ3tzcdC5YM+caEdpoUvNDdGsKWl20pxGhtq99ZT+uX7+O6elpnDp1CnNzc/ugsf4yVCC98cYbWFhY8FwR4JcYNHqyPMiCgdGLElZeqwDR2W8B2Q9M7GO9XveW/bJ9C0b9H9jmRrRodiVCkjVUMLG/BHWn08Hjx48RxzGmp6fxxhtv7LF2nk6G5tpefPFFvPnmm1haWvIAoGQa2C6LWH5Bkq2znp/bYqwCyAKQClZrRVFSruDmq7pXdVtJqQjdQkWLpG7VRpP2niT77KuWV0qlEtbX1/HXX3/hn3/+GZTKnihDs0ivvvoqisWil3AD4M10Ek+bn7Gz3c5YDb0VRNZ9AXBJS7UkalHs9bQIdJ20frw/xfaRx1i/U+4H9FrYpL7yuwZB4O5fLpcxNjaGAwcO4JVXXtl7Rf1HCf/9lMHI6dOn8fDhQ0/hDPUBePkj/R+A5+6UYAdB4BVjrSKSOBjbYRu8Nz/XTLS2QR7W7XaRzWYBwONxNuS3dbUkYf8pGnxwDAjmMAxRrVaxvr6O8fFxzMzM4PTp0ztVx65lKBbp2WefxfT0NB4/fuxliVUsP9HPlTdYUqukN8miWKvF9qyFs8tRbFvciKBlFbWEQC/XI+BsVAb467k1vaD341gxJ8YVARsbG5icnMSRI0fw7LPP7pWankqGAqTjx4+7YmhStKPRjfIUYLscAiTvtLWgsCSaYiNDnfFJn1t3p/eiZUqyeOxrJpPxwKz8Ts/VYxRaMztpGJUuLS0hjmOMjY3h+PHje6Gip5ahAOn06dNYWlpCq9Vy24I4SLplSJXiOvx/QLJhcbe7ve3IhvqA75L0mM58vuo9dQWBnqNhf6PRcOUSrftROCFsxMjvqf/b2pr22wYXwNbO4JWVFRSLRRSLxaG5t6EAaXx83IvUgN4dqUmiyTjLWQA/zFfR1QP2Gn2vLknfW5fFaywJ57n8nC6bBVpr9ZIskLrDfuAnN+Q96/W6s0jj4+NPHMNByb4DKZ1Oo1QquUX5Wj9TV2BdDLA9yBolqZvjq7UqCtCk6Mwq07pIVbiud7K5plqt5pU2uFlSybuKdcEq/frGcVAAM1CJ4xilUulfJ+QgZN/vmMvlMD4+3mNZgOTNjgosrYclcSB1a9quBZZNPPKcJNdj78H39lwl8LpJkuG+Atzmm9gnAImgs7zPlkxI+KMowvj4OHK53E5UsysZCpB0JtlBTcoZJVkquwxDz+3HRfhqw2rrCi0fSbJIFLv8RN/zMTcWNBakfLXcSv+359q+8julUqn/H0CKoshZFpYK7IBxcJR4W6tjTb6uWAS2B5u5qaQZrmUUEngFM8+1LkbB1w8cnDB6Tj9rynOSoji9J+9jrRqtIPlYFEVPVsIAZN+BxGRa0syzEYxKPxdoM8J6Trfb7bmXfqZWiRFks9n01hzxfL7yHF3uwTa0n+qG7f11s0FSjsy21c8V6nfXHTa69Ga/ZN+BpJVvtR6q3CS3ohnufgOfRLztuiOez4HX5B8VkkTYKSxR2CQqa2/ZbBZRFKHRaHjJTL2/fk/rWq3rtX1PijBTqZS3FKXfDuFByr4DaXNz0w1y0mApkCzB7CfWZdjwXR98ZS0YB91GdkAv/9E+qxXgg7EIJLahgNHv1090AiVNKh0f3oOknvm4er3uPctyv2TfgcQFbEAvYdZBswPOmZdESJMsRz+OofftF14DcCE1z0vqD1/JT7hYjdckLY2xfenHi2zOyY6BtqNciWmI/ZZ9B1K9Xsf6+rq30tBGZXbwrHug2GKuJbFq1TThaUNuW0dLWpvN+/FPHzYaBAHy+byn2CRCn2SNrGW2CU3LB/WVEkUR2u2tp++ura25LPt+ylAy2ysrKygUCp5PT7IYtvKtKyX1UXlJ65NsW7wPpZ81shxJuRmvoxsLwxBRFKFYLHoP71IQ8Pyk6My6vSRuqJsbtPxCd8pHDfJhYSsrK0+njD2SoQBpeXkZ+XweURR563OA3kcIJ7kBXUhGSXJ7FAI2qQ6mQvJtQc17dTrby3yZtY6iKJH8ayBh+2bBqWL5kFpT+z0IpEKhgFarhUqlguXl5b7jPkgZCpCuXr2KQ4cOuYq4hv128X9SQpGiM50rBlXpSW7SPrpYwaruk1ZOrSbvwWdqx3GMQqHg2lVyrBZSw3F1w3Yi2MI1+6ETiNdokHDo0CGsra2hXC7j6tWrO9DI7mUoQLp79y4AeDkeKj1pizOlXyqAirS8IolbqUsE/AekA37UaKMugotupVAo9LWM+r8CyVooCyx1Yzyu3519onWMoghTU1PY3NzExsaGG9v9lqEAqVKp4P79+5iZmekJzfmqnEO3SmseiIOuvMnyDgqVkEqlEEVRX/em3EiVqrwok8m4R/DZR+oo37NtWZJuk4zMrCeBkeeqa42iyJH8lZUV/PXXX0P7mYmhrdm+ePGi93BzGxlZi2QJL7ANHH6uu3J5jOfzGlofdUUqSZGd5oniOMbBgwcdP1GLqICxoLLATOJJOilsn/Q6ToQwDDE5OYnV1VUsLCzg4sWLu1XLjmVoQPr555/x8OFD97hjG8IDfi7FuhlVGBWkSzZsW8rDWKZRnkGAaZqA4FRQFAqFHiuatJLTAlRXBajQ2tgNBHpPS/I5FnEc4/Dhww5IP//88471sVsZGpBWV1cxPz+Po0ePeooBtpOBapXsk0B4nmaWs9lsjyVQIWfSjDnPZR/UhRAgDLEnJiYQx7H3XEhLgC2n6udqgd6ELPuuAOf7brfrfnSH0eLk5CQOHTqExcVFzM/PY3V1dQ80szMZ6gbJ+fl5N8OB5PS/vrcAsa7BKlbF8p5ut+sB2AKI7fN9NptFPp93P2JjnxqnINJ7JIm6KbVsWgS2i/3UMnHyTE9PY3NzEw8fPsT8/PzOFbEHMlQgVatV/PrrryiVSshms95A2kjI1sTU3akLyufzPVzJ1u0oBJPyHbbP4/w5iKmpKXecLjTp2iSXm9RP/Q5cTWD7rBYR2Cb2cRwjn8/j2LFjePDgAa5evYpqtToQHf1XGfrTSD777DOcPHkSuVzO8aWkZJ1W9NUtAX4GfGxsDNlsNtEyqWtTiePYU6JaoVwuh4MHDyKKIuc6qVx1q/reWiZaXPbRApzHbLae/xNU6XQa2WwW2WwW09PTWFxcxN27d/HZZ5/tXhG7lKEDqVwuY2FhARMTE54JB3yrpNujNXzWpCEVSYthCbCCU3/fhJZHLQzfx3GMbDbr2lV+ZCMw3sO6O1paLeLyOFdC6HHNidlID9gC/okTJ/DPP//g3r17KJfLe66Xp5WhAwkALly4gMOHDyOO4x63oAlCwOc6nNG6NjoIAhSLRQcEwC/82s2H3FZkAcR2dMNhFEWIosj75UiKWqekRKY9xv7YCUKxaQRa2Fwuh+npaURRhBs3buDChQsD1Mx/l5EA0qVLl3Dr1i3k83kvj8KBVY6QFBVZLkELQmXb861QablczimNOzLYLmtqvBeBq+Ah2Ln9SM+zBFwLt2rNrOtU902Qnzp1CsvLy7h16xYuXbq0t8rYoYwEkLrdLs6fP4+zZ896ILBcxkZCSXklWidaDo2wuKxDUwB2icfY2Bjy+TwKhQKKxaJrL5vNej87Suul6Ql1zf0Az/9JsG1yUrmRXQKTyWTcgzdu376N8+fP940M91uG9hAJK6urq/jhhx9QLBZRLpe9DQA6wEpqAb8GpSF5Npt1kQxdiK545KtaKBZjoyjCxMSEAzQ5l1oIK8rt7DGtHXLhmY3O2u22K2Kzr+omaSVPnDiB3377Dd99991Q80ZWRsIiUb766is8//zzXnSk5r5fZpthPLC9S0WjKQr/1+cLAOiJvOI4xtTUlDvG5S7KY/iZ8hfrNlkb1FyYBhLW7eqk0Cy7JkVnZ2dx584dfPXVV4NSw45kpIB0+fJlrK+vu1qWAgXorZNR9AENwJaSx8fHXU1KFZ3JZJw1s2F6Or31C5UEUi6Xw9jYmBe9UaFaOqHYviWlIOwaK+VIGg3agm82m8XExAT+/PNPfP3117h8+fIANLBzGSkgAVs1uBdeeMG5E7sWR9cbqZWiZdAZb0sUnOlJP6muLpMg4ZojfRyNTUBawq+gtK5Of6Jd0wdA725gy5+iKMLs7Czu37+Pzz//fOB6eFoZOSB98sknuH37tlseoY+4o8KoIH6mCUlaGxJjCxK1TBYUbI9Am5qaQqFQcIlJWiILGpuOUAIObJN8tYQUzWPZRCslDEMUi0UcPnwYP/74I/7+++/BKmEHMnJAajQa+PTTT3HmzBkUCgV3nEqma9AckYIA2F4yy+uoKG1H3RhBpUDN5XKI4xiTk5PI5XKOhPezSMptWFxmzoqbL23WW60lv4vyKhLxMAxx+vRp3Lt3D59++uk+aeLpZOSABADXr19HJpNBLpfzyKgqWwHEzwE416R79Hk+ORPzMbp0VsNumwTk+vIkMFDUnSmn023k7MuT6obcEcJzCKZSqYQHDx7g+vXrAxv33chIAqndbuPq1auuBkeFKi+yyTrlHsD2o28ULAzvNR/Ez+I4dknHOI5Rr9fdNfl8HuPj445sq1UCeh/iRfBwwyIBYjc6WLKvy2R0uUyhUMDi4iJ++umnoWzH/i8ykkACtsomXHfDp3qotVA+Yt0S61pKjnX7EAuffM/royjC2NgYUqmtR8WwvhaGIfL5PHK5XGItD/AfbEogcaMi2wa214jb8kq/LeJhGKJUKuHOnTsjUw5JkpEF0s2bN7GwsOAUTlGepO4oCVBKoi3hJrA0nKf7i+PYKwTzr1gsOqtlw3quciQn4jOLbOabbaoFI+gVSHTNQRDgwIEDePDgAW7evDm4Ad+ljCyQ1tbWcOXKFTzzzDPeuiGglw/RQgFbM153mmpSkZaEVomhPXlTsVj0FF8ulz1uFkWR52rpgpJ+HYBVfc0bKVhs5KZFZX1QRafTwdTUFK5cuYK1tbV9GfudyMgCCQB+//13HD58GLlcLjF8t4SayuGD1Hk+lULOQ0BpxZ/8xz5PqVKpePkcAomWUbkNH+ZOa0Q+w+sJKiXXFPueHI+u9/fffx/8gO9CRqbWliTXrl1DqVTyojB1KwoetRDqVniOVt0VGOn01qpKkm1ew7VCtVoNExMTrr1cLod8Pu/qeCTV/A1dbgdSl2ifr60lExvua8KV/V1fX8e1a9f2Y8h3LCNtkR49euTxG7UYSVllAN5PmSoXYtREPqTH4zh277m4n1Kv17G6uuoBdnJy0nNH5ET8lUn7VDl9SgnF5p30T10lf1P30aNH+zDiO5eRBlK1WvUWvKslSVo8BviF0qTaV1KB1i4L0bJFKrX1dP1yuewsla7MpDXir1RqtV83FFAIFIpaHl3WAsAtNWk2m0Nfk/1v8r+gy4aIyN+8VgAAAABJRU5ErkJggg==" y="-60.217582"/>

   </g>

   <g id="matplotlib.axis_3">

    <g id="xtick_4">

     <g id="line2d_10">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="208.155299" xlink:href="#md4369562c1" y="129.217582"/>

      </g>

     </g>

     <g id="text_11">

      <!-- 0 -->

      <g transform="translate(204.974049 143.816019)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_5">

     <g id="line2d_11">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="246.062908" xlink:href="#md4369562c1" y="129.217582"/>

      </g>

     </g>

     <g id="text_12">

      <!-- 100 -->

      <g transform="translate(236.519158 143.816019)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_6">

     <g id="line2d_12">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="283.970516" xlink:href="#md4369562c1" y="129.217582"/>

      </g>

     </g>

     <g id="text_13">

      <!-- 200 -->

      <g transform="translate(274.426766 143.816019)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-50"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_7">

     <g id="line2d_13">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="321.878125" xlink:href="#md4369562c1" y="129.217582"/>

      </g>

     </g>

     <g id="text_14">

      <!-- 300 -->

      <defs>

       <path d="M 40.578125 39.3125 

Q 47.65625 37.796875 51.625 33 

Q 55.609375 28.21875 55.609375 21.1875 

Q 55.609375 10.40625 48.1875 4.484375 

Q 40.765625 -1.421875 27.09375 -1.421875 

Q 22.515625 -1.421875 17.65625 -0.515625 

Q 12.796875 0.390625 7.625 2.203125 

L 7.625 11.71875 

Q 11.71875 9.328125 16.59375 8.109375 

Q 21.484375 6.890625 26.8125 6.890625 

Q 36.078125 6.890625 40.9375 10.546875 

Q 45.796875 14.203125 45.796875 21.1875 

Q 45.796875 27.640625 41.28125 31.265625 

Q 36.765625 34.90625 28.71875 34.90625 

L 20.21875 34.90625 

L 20.21875 43.015625 

L 29.109375 43.015625 

Q 36.375 43.015625 40.234375 45.921875 

Q 44.09375 48.828125 44.09375 54.296875 

Q 44.09375 59.90625 40.109375 62.90625 

Q 36.140625 65.921875 28.71875 65.921875 

Q 24.65625 65.921875 20.015625 65.03125 

Q 15.375 64.15625 9.8125 62.3125 

L 9.8125 71.09375 

Q 15.4375 72.65625 20.34375 73.4375 

Q 25.25 74.21875 29.59375 74.21875 

Q 40.828125 74.21875 47.359375 69.109375 

Q 53.90625 64.015625 53.90625 55.328125 

Q 53.90625 49.265625 50.4375 45.09375 

Q 46.96875 40.921875 40.578125 39.3125 

z

" id="DejaVuSans-51"/>

      </defs>

      <g transform="translate(312.334375 143.816019)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-51"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

   </g>

   <g id="matplotlib.axis_4">

    <g id="ytick_7">

     <g id="line2d_14">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="207.965761" xlink:href="#m60fbb1ff4c" y="61.173424"/>

      </g>

     </g>

     <g id="text_15">

      <!-- 0 -->

      <g transform="translate(194.603261 64.972643)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_8">

     <g id="line2d_15">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="207.965761" xlink:href="#m60fbb1ff4c" y="99.081033"/>

      </g>

     </g>

     <g id="text_16">

      <!-- 100 -->

      <g transform="translate(181.878261 102.880251)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

   </g>

   <g id="patch_8">

    <path d="M 207.965761 129.217582 

L 207.965761 60.983886 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_9">

    <path d="M 353.530978 129.217582 

L 353.530978 60.983886 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_10">

    <path d="M 207.965761 129.217582 

L 353.530978 129.217582 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_11">

    <path d="M 207.965761 60.983886 

L 353.530978 60.983886 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="text_17">

    <!-- Sinogram -->

    <defs>

     <path d="M 53.515625 70.515625 

L 53.515625 60.890625 

Q 47.90625 63.578125 42.921875 64.890625 

Q 37.9375 66.21875 33.296875 66.21875 

Q 25.25 66.21875 20.875 63.09375 

Q 16.5 59.96875 16.5 54.203125 

Q 16.5 49.359375 19.40625 46.890625 

Q 22.3125 44.4375 30.421875 42.921875 

L 36.375 41.703125 

Q 47.40625 39.59375 52.65625 34.296875 

Q 57.90625 29 57.90625 20.125 

Q 57.90625 9.515625 50.796875 4.046875 

Q 43.703125 -1.421875 29.984375 -1.421875 

Q 24.8125 -1.421875 18.96875 -0.25 

Q 13.140625 0.921875 6.890625 3.21875 

L 6.890625 13.375 

Q 12.890625 10.015625 18.65625 8.296875 

Q 24.421875 6.59375 29.984375 6.59375 

Q 38.421875 6.59375 43.015625 9.90625 

Q 47.609375 13.234375 47.609375 19.390625 

Q 47.609375 24.75 44.3125 27.78125 

Q 41.015625 30.8125 33.5 32.328125 

L 27.484375 33.5 

Q 16.453125 35.6875 11.515625 40.375 

Q 6.59375 45.0625 6.59375 53.421875 

Q 6.59375 63.09375 13.40625 68.65625 

Q 20.21875 74.21875 32.171875 74.21875 

Q 37.3125 74.21875 42.625 73.28125 

Q 47.953125 72.359375 53.515625 70.515625 

z

" id="DejaVuSans-83"/>

     <path d="M 30.609375 48.390625 

Q 23.390625 48.390625 19.1875 42.75 

Q 14.984375 37.109375 14.984375 27.296875 

Q 14.984375 17.484375 19.15625 11.84375 

Q 23.34375 6.203125 30.609375 6.203125 

Q 37.796875 6.203125 41.984375 11.859375 

Q 46.1875 17.53125 46.1875 27.296875 

Q 46.1875 37.015625 41.984375 42.703125 

Q 37.796875 48.390625 30.609375 48.390625 

z

M 30.609375 56 

Q 42.328125 56 49.015625 48.375 

Q 55.71875 40.765625 55.71875 27.296875 

Q 55.71875 13.875 49.015625 6.21875 

Q 42.328125 -1.421875 30.609375 -1.421875 

Q 18.84375 -1.421875 12.171875 6.21875 

Q 5.515625 13.875 5.515625 27.296875 

Q 5.515625 40.765625 12.171875 48.375 

Q 18.84375 56 30.609375 56 

z

" id="DejaVuSans-111"/>

     <path d="M 52 44.1875 

Q 55.375 50.25 60.0625 53.125 

Q 64.75 56 71.09375 56 

Q 79.640625 56 84.28125 50.015625 

Q 88.921875 44.046875 88.921875 33.015625 

L 88.921875 0 

L 79.890625 0 

L 79.890625 32.71875 

Q 79.890625 40.578125 77.09375 44.375 

Q 74.3125 48.1875 68.609375 48.1875 

Q 61.625 48.1875 57.5625 43.546875 

Q 53.515625 38.921875 53.515625 30.90625 

L 53.515625 0 

L 44.484375 0 

L 44.484375 32.71875 

Q 44.484375 40.625 41.703125 44.40625 

Q 38.921875 48.1875 33.109375 48.1875 

Q 26.21875 48.1875 22.15625 43.53125 

Q 18.109375 38.875 18.109375 30.90625 

L 18.109375 0 

L 9.078125 0 

L 9.078125 54.6875 

L 18.109375 54.6875 

L 18.109375 46.1875 

Q 21.1875 51.21875 25.484375 53.609375 

Q 29.78125 56 35.6875 56 

Q 41.65625 56 45.828125 52.96875 

Q 50 49.953125 52 44.1875 

z

" id="DejaVuSans-109"/>

    </defs>

    <g transform="translate(252.001807 54.983886)scale(0.12 -0.12)">

     <use xlink:href="#DejaVuSans-83"/>

     <use x="63.476562" xlink:href="#DejaVuSans-105"/>

     <use x="91.259766" xlink:href="#DejaVuSans-110"/>

     <use x="154.638672" xlink:href="#DejaVuSans-111"/>

     <use x="215.820312" xlink:href="#DejaVuSans-103"/>

     <use x="279.296875" xlink:href="#DejaVuSans-114"/>

     <use x="320.410156" xlink:href="#DejaVuSans-97"/>

     <use x="381.689453" xlink:href="#DejaVuSans-109"/>

    </g>

   </g>

  </g>

  <g id="axes_3">

   <g id="patch_12">

    <path d="M 382.644022 167.883342 

L 528.209239 167.883342 

L 528.209239 22.318125 

L 382.644022 22.318125 

z

" style="fill:#ffffff;"/>

   </g>

   <g clip-path="url(#pa394763eca)">

    <image height="146" id="imageaa165d161b" transform="scale(1 -1)translate(0 -146)" width="146" x="382.644022" xlink:href="data:image/png;base64,

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" y="-21.883342"/>

   </g>

   <g id="matplotlib.axis_5">

    <g id="xtick_8">

     <g id="line2d_16">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="382.928329" xlink:href="#md4369562c1" y="167.883342"/>

      </g>

     </g>

     <g id="text_18">

      <!-- 0 -->

      <g transform="translate(379.747079 182.48178)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_9">

     <g id="line2d_17">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="439.789742" xlink:href="#md4369562c1" y="167.883342"/>

      </g>

     </g>

     <g id="text_19">

      <!-- 100 -->

      <g transform="translate(430.245992 182.48178)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_10">

     <g id="line2d_18">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="496.651155" xlink:href="#md4369562c1" y="167.883342"/>

      </g>

     </g>

     <g id="text_20">

      <!-- 200 -->

      <g transform="translate(487.107405 182.48178)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-50"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

   </g>

   <g id="matplotlib.axis_6">

    <g id="ytick_9">

     <g id="line2d_19">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="382.644022" xlink:href="#m60fbb1ff4c" y="22.602432"/>

      </g>

     </g>

     <g id="text_21">

      <!-- 0 -->

      <g transform="translate(369.281522 26.401651)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_10">

     <g id="line2d_20">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="382.644022" xlink:href="#m60fbb1ff4c" y="51.033139"/>

      </g>

     </g>

     <g id="text_22">

      <!-- 50 -->

      <g transform="translate(362.919022 54.832357)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-53"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_11">

     <g id="line2d_21">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="382.644022" xlink:href="#m60fbb1ff4c" y="79.463845"/>

      </g>

     </g>

     <g id="text_23">

      <!-- 100 -->

      <g transform="translate(356.556522 83.263064)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_12">

     <g id="line2d_22">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="382.644022" xlink:href="#m60fbb1ff4c" y="107.894552"/>

      </g>

     </g>

     <g id="text_24">

      <!-- 150 -->

      <g transform="translate(356.556522 111.69377)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-53"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_13">

     <g id="line2d_23">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="382.644022" xlink:href="#m60fbb1ff4c" y="136.325258"/>

      </g>

     </g>

     <g id="text_25">

      <!-- 200 -->

      <g transform="translate(356.556522 140.124477)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-50"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_14">

     <g id="line2d_24">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="382.644022" xlink:href="#m60fbb1ff4c" y="164.755965"/>

      </g>

     </g>

     <g id="text_26">

      <!-- 250 -->

      <g transform="translate(356.556522 168.555183)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-50"/>

       <use x="63.623047" xlink:href="#DejaVuSans-53"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

   </g>

   <g id="patch_13">

    <path d="M 382.644022 167.883342 

L 382.644022 22.318125 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_14">

    <path d="M 528.209239 167.883342 

L 528.209239 22.318125 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_15">

    <path d="M 382.644022 167.883342 

L 528.209239 167.883342 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_16">

    <path d="M 382.644022 22.318125 

L 528.209239 22.318125 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="text_27">

    <!-- SIRT_CUDA -->

    <defs>

     <path d="M 9.8125 72.90625 

L 19.671875 72.90625 

L 19.671875 0 

L 9.8125 0 

z

" id="DejaVuSans-73"/>

     <path d="M 44.390625 34.1875 

Q 47.5625 33.109375 50.5625 29.59375 

Q 53.5625 26.078125 56.59375 19.921875 

L 66.609375 0 

L 56 0 

L 46.6875 18.703125 

Q 43.0625 26.03125 39.671875 28.421875 

Q 36.28125 30.8125 30.421875 30.8125 

L 19.671875 30.8125 

L 19.671875 0 

L 9.8125 0 

L 9.8125 72.90625 

L 32.078125 72.90625 

Q 44.578125 72.90625 50.734375 67.671875 

Q 56.890625 62.453125 56.890625 51.90625 

Q 56.890625 45.015625 53.6875 40.46875 

Q 50.484375 35.9375 44.390625 34.1875 

z

M 19.671875 64.796875 

L 19.671875 38.921875 

L 32.078125 38.921875 

Q 39.203125 38.921875 42.84375 42.21875 

Q 46.484375 45.515625 46.484375 51.90625 

Q 46.484375 58.296875 42.84375 61.546875 

Q 39.203125 64.796875 32.078125 64.796875 

z

" id="DejaVuSans-82"/>

     <path d="M -0.296875 72.90625 

L 61.375 72.90625 

L 61.375 64.59375 

L 35.5 64.59375 

L 35.5 0 

L 25.59375 0 

L 25.59375 64.59375 

L -0.296875 64.59375 

z

" id="DejaVuSans-84"/>

     <path d="M 50.984375 -16.609375 

L 50.984375 -23.578125 

L -0.984375 -23.578125 

L -0.984375 -16.609375 

z

" id="DejaVuSans-95"/>

     <path d="M 64.40625 67.28125 

L 64.40625 56.890625 

Q 59.421875 61.53125 53.78125 63.8125 

Q 48.140625 66.109375 41.796875 66.109375 

Q 29.296875 66.109375 22.65625 58.46875 

Q 16.015625 50.828125 16.015625 36.375 

Q 16.015625 21.96875 22.65625 14.328125 

Q 29.296875 6.6875 41.796875 6.6875 

Q 48.140625 6.6875 53.78125 8.984375 

Q 59.421875 11.28125 64.40625 15.921875 

L 64.40625 5.609375 

Q 59.234375 2.09375 53.4375 0.328125 

Q 47.65625 -1.421875 41.21875 -1.421875 

Q 24.65625 -1.421875 15.125 8.703125 

Q 5.609375 18.84375 5.609375 36.375 

Q 5.609375 53.953125 15.125 64.078125 

Q 24.65625 74.21875 41.21875 74.21875 

Q 47.75 74.21875 53.53125 72.484375 

Q 59.328125 70.75 64.40625 67.28125 

z

" id="DejaVuSans-67"/>

     <path d="M 8.6875 72.90625 

L 18.609375 72.90625 

L 18.609375 28.609375 

Q 18.609375 16.890625 22.84375 11.734375 

Q 27.09375 6.59375 36.625 6.59375 

Q 46.09375 6.59375 50.34375 11.734375 

Q 54.59375 16.890625 54.59375 28.609375 

L 54.59375 72.90625 

L 64.5 72.90625 

L 64.5 27.390625 

Q 64.5 13.140625 57.4375 5.859375 

Q 50.390625 -1.421875 36.625 -1.421875 

Q 22.796875 -1.421875 15.734375 5.859375 

Q 8.6875 13.140625 8.6875 27.390625 

z

" id="DejaVuSans-85"/>

     <path d="M 19.671875 64.796875 

L 19.671875 8.109375 

L 31.59375 8.109375 

Q 46.6875 8.109375 53.6875 14.9375 

Q 60.6875 21.78125 60.6875 36.53125 

Q 60.6875 51.171875 53.6875 57.984375 

Q 46.6875 64.796875 31.59375 64.796875 

z

M 9.8125 72.90625 

L 30.078125 72.90625 

Q 51.265625 72.90625 61.171875 64.09375 

Q 71.09375 55.28125 71.09375 36.53125 

Q 71.09375 17.671875 61.125 8.828125 

Q 51.171875 0 30.078125 0 

L 9.8125 0 

z

" id="DejaVuSans-68"/>

     <path d="M 34.1875 63.1875 

L 20.796875 26.90625 

L 47.609375 26.90625 

z

M 28.609375 72.90625 

L 39.796875 72.90625 

L 67.578125 0 

L 57.328125 0 

L 50.6875 18.703125 

L 17.828125 18.703125 

L 11.1875 0 

L 0.78125 0 

z

" id="DejaVuSans-65"/>

    </defs>

    <g transform="translate(421.716005 16.318125)scale(0.12 -0.12)">

     <use xlink:href="#DejaVuSans-83"/>

     <use x="63.476562" xlink:href="#DejaVuSans-73"/>

     <use x="92.96875" xlink:href="#DejaVuSans-82"/>

     <use x="162.341797" xlink:href="#DejaVuSans-84"/>

     <use x="223.425781" xlink:href="#DejaVuSans-95"/>

     <use x="273.425781" xlink:href="#DejaVuSans-67"/>

     <use x="343.25" xlink:href="#DejaVuSans-85"/>

     <use x="416.443359" xlink:href="#DejaVuSans-68"/>

     <use x="493.429688" xlink:href="#DejaVuSans-65"/>

    </g>

   </g>

  </g>

  <g id="axes_4">

   <g id="patch_17">

    <path d="M 557.322283 167.883342 

L 702.8875 167.883342 

L 702.8875 22.318125 

L 557.322283 22.318125 

z

" style="fill:#ffffff;"/>

   </g>

   <g clip-path="url(#p4510fef9b7)">

    <image height="146" id="image5490641d67" transform="scale(1 -1)translate(0 -146)" width="146" x="557.322283" xlink:href="data:image/png;base64,

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" y="-21.883342"/>

   </g>

   <g id="matplotlib.axis_7">

    <g id="xtick_11">

     <g id="line2d_25">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="557.60659" xlink:href="#md4369562c1" y="167.883342"/>

      </g>

     </g>

     <g id="text_28">

      <!-- 0 -->

      <g transform="translate(554.42534 182.48178)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_12">

     <g id="line2d_26">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="614.468003" xlink:href="#md4369562c1" y="167.883342"/>

      </g>

     </g>

     <g id="text_29">

      <!-- 100 -->

      <g transform="translate(604.924253 182.48178)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_13">

     <g id="line2d_27">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="671.329416" xlink:href="#md4369562c1" y="167.883342"/>

      </g>

     </g>

     <g id="text_30">

      <!-- 200 -->

      <g transform="translate(661.785666 182.48178)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-50"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

   </g>

   <g id="matplotlib.axis_8">

    <g id="ytick_15">

     <g id="line2d_28">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="557.322283" xlink:href="#m60fbb1ff4c" y="22.602432"/>

      </g>

     </g>

     <g id="text_31">

      <!-- 0 -->

      <g transform="translate(543.959783 26.401651)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_16">

     <g id="line2d_29">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="557.322283" xlink:href="#m60fbb1ff4c" y="51.033139"/>

      </g>

     </g>

     <g id="text_32">

      <!-- 50 -->

      <g transform="translate(537.597283 54.832357)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-53"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_17">

     <g id="line2d_30">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="557.322283" xlink:href="#m60fbb1ff4c" y="79.463845"/>

      </g>

     </g>

     <g id="text_33">

      <!-- 100 -->

      <g transform="translate(531.234783 83.263064)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_18">

     <g id="line2d_31">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="557.322283" xlink:href="#m60fbb1ff4c" y="107.894552"/>

      </g>

     </g>

     <g id="text_34">

      <!-- 150 -->

      <g transform="translate(531.234783 111.69377)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-53"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_19">

     <g id="line2d_32">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="557.322283" xlink:href="#m60fbb1ff4c" y="136.325258"/>

      </g>

     </g>

     <g id="text_35">

      <!-- 200 -->

      <g transform="translate(531.234783 140.124477)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-50"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_20">

     <g id="line2d_33">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="557.322283" xlink:href="#m60fbb1ff4c" y="164.755965"/>

      </g>

     </g>

     <g id="text_36">

      <!-- 250 -->

      <g transform="translate(531.234783 168.555183)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-50"/>

       <use x="63.623047" xlink:href="#DejaVuSans-53"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

   </g>

   <g id="patch_18">

    <path d="M 557.322283 167.883342 

L 557.322283 22.318125 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_19">

    <path d="M 702.8875 167.883342 

L 702.8875 22.318125 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_20">

    <path d="M 557.322283 167.883342 

L 702.8875 167.883342 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_21">

    <path d="M 557.322283 22.318125 

L 702.8875 22.318125 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="text_37">

    <!-- SIRT -->

    <g transform="translate(616.698641 16.318125)scale(0.12 -0.12)">

     <use xlink:href="#DejaVuSans-83"/>

     <use x="63.476562" xlink:href="#DejaVuSans-73"/>

     <use x="92.96875" xlink:href="#DejaVuSans-82"/>

     <use x="162.341797" xlink:href="#DejaVuSans-84"/>

    </g>

   </g>

  </g>

 </g>

 <defs>

  <clipPath id="p3c320e4a05">

   <rect height="145.565217" width="145.565217" x="33.2875" y="22.318125"/>

  </clipPath>

  <clipPath id="pe33ea7faeb">

   <rect height="68.233696" width="145.565217" x="207.965761" y="60.983886"/>

  </clipPath>

  <clipPath id="pa394763eca">

   <rect height="145.565217" width="145.565217" x="382.644022" y="22.318125"/>

  </clipPath>

  <clipPath id="p4510fef9b7">

   <rect height="145.565217" width="145.565217" x="557.322283" y="22.318125"/>

  </clipPath>

 </defs>

</svg>


</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="-Astra-Toolbox.-3D-Geometry-"><center> Astra Toolbox. 3D Geometry </center><a class="anchor-link" href="#-Astra-Toolbox.-3D-Geometry-">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[12]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">n_size</span> <span class="o">=</span> <span class="mi">128</span>
<span class="n">vol_geom</span> <span class="o">=</span> <span class="n">astra</span><span class="o">.</span><span class="n">create_vol_geom</span><span class="p">(</span><span class="n">n_size</span><span class="p">,</span> <span class="n">n_size</span><span class="p">,</span> <span class="n">n_size</span><span class="p">)</span>

<span class="c1"># create geometry</span>
<span class="n">angles</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">linspace</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="n">np</span><span class="o">.</span><span class="n">pi</span><span class="p">,</span> <span class="mi">180</span><span class="p">,</span><span class="kc">False</span><span class="p">)</span>
<span class="c1"># create_proj_geom(&#39;parallel3d&#39;, detector_spacing_x, detector_spacing_y, det_row_count, det_col_count, angles)</span>
<span class="n">proj_geom</span> <span class="o">=</span> <span class="n">astra</span><span class="o">.</span><span class="n">create_proj_geom</span><span class="p">(</span><span class="s1">&#39;parallel3d&#39;</span><span class="p">,</span> <span class="mf">1.0</span><span class="p">,</span> <span class="mf">1.0</span><span class="p">,</span> <span class="mi">128</span><span class="p">,</span> <span class="mi">192</span><span class="p">,</span> <span class="n">angles</span><span class="p">)</span>

<span class="c1"># Create phantom</span>
<span class="n">obj</span> <span class="o">=</span> <span class="n">tomopy</span><span class="o">.</span><span class="n">misc</span><span class="o">.</span><span class="n">phantom</span><span class="o">.</span><span class="n">shepp3d</span><span class="p">(</span><span class="n">n_size</span><span class="p">)</span>

<span class="c1"># Create projection data from this</span>
<span class="n">proj_id</span><span class="p">,</span> <span class="n">proj_data</span> <span class="o">=</span> <span class="n">astra</span><span class="o">.</span><span class="n">create_sino3d_gpu</span><span class="p">(</span><span class="n">obj</span><span class="p">,</span> <span class="n">proj_geom</span><span class="p">,</span> <span class="n">vol_geom</span><span class="p">)</span>

<span class="c1"># Create a data object for the reconstruction</span>
<span class="n">rec_id</span> <span class="o">=</span> <span class="n">astra</span><span class="o">.</span><span class="n">data3d</span><span class="o">.</span><span class="n">create</span><span class="p">(</span><span class="s1">&#39;-vol&#39;</span><span class="p">,</span> <span class="n">vol_geom</span><span class="p">)</span>

<span class="c1"># Set up the parameters for a reconstruction algorithm using the GPU</span>
<span class="n">cfg</span> <span class="o">=</span> <span class="n">astra</span><span class="o">.</span><span class="n">astra_dict</span><span class="p">(</span><span class="s1">&#39;SIRT3D_CUDA&#39;</span><span class="p">)</span>
<span class="n">cfg</span><span class="p">[</span><span class="s1">&#39;ReconstructionDataId&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">rec_id</span>
<span class="n">cfg</span><span class="p">[</span><span class="s1">&#39;ProjectionDataId&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">proj_id</span>


<span class="c1"># Create the algorithm object from the configuration structure</span>
<span class="n">alg_id</span> <span class="o">=</span> <span class="n">astra</span><span class="o">.</span><span class="n">algorithm</span><span class="o">.</span><span class="n">create</span><span class="p">(</span><span class="n">cfg</span><span class="p">)</span>

<span class="c1"># Run 150 iterations of the algorithm</span>
<span class="c1"># Note that this requires about 750MB of GPU memory, and has a runtime</span>
<span class="c1"># in the order of 10 seconds.</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">&#39;GPU, 150 iterations:&#39;</span><span class="p">)</span>
<span class="o">%</span> <span class="n">time</span>  <span class="n">astra</span><span class="o">.</span><span class="n">algorithm</span><span class="o">.</span><span class="n">run</span><span class="p">(</span><span class="n">alg_id</span><span class="p">,</span> <span class="mi">150</span><span class="p">)</span>

<span class="c1"># Get the result</span>
<span class="n">rec</span> <span class="o">=</span> <span class="n">astra</span><span class="o">.</span><span class="n">data3d</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="n">rec_id</span><span class="p">)</span>

<span class="c1"># Clean up. Note that GPU memory is tied up in the algorithm object,</span>
<span class="c1"># and main RAM in the data objects.</span>
<span class="n">astra</span><span class="o">.</span><span class="n">algorithm</span><span class="o">.</span><span class="n">delete</span><span class="p">(</span><span class="n">alg_id</span><span class="p">)</span>
<span class="n">astra</span><span class="o">.</span><span class="n">data3d</span><span class="o">.</span><span class="n">delete</span><span class="p">(</span><span class="n">rec_id</span><span class="p">)</span>
<span class="n">astra</span><span class="o">.</span><span class="n">data3d</span><span class="o">.</span><span class="n">delete</span><span class="p">(</span><span class="n">proj_id</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt"></div>

<div class="output_subarea output_stream output_stdout output_text">
<pre>GPU, 150 iterations:
Wall time: 1min
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[20]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Show results.</span>
<span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">12</span><span class="p">,</span><span class="mi">4</span><span class="p">))</span>
<span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">131</span><span class="p">);</span> <span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;Phantom&#39;</span><span class="p">);</span>
<span class="n">plt</span><span class="o">.</span><span class="n">imshow</span><span class="p">(</span><span class="n">obj</span><span class="p">[</span><span class="mi">64</span><span class="p">,:,:],</span> <span class="n">cmap</span><span class="o">=</span><span class="s1">&#39;gray&#39;</span><span class="p">);</span> 
<span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">132</span><span class="p">);</span>  <span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;Single projection image&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">imshow</span><span class="p">(</span><span class="n">proj_data</span><span class="p">[</span><span class="mi">64</span><span class="p">,:,:],</span> <span class="n">cmap</span><span class="o">=</span><span class="s1">&#39;gray&#39;</span><span class="p">);</span>
<span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">133</span><span class="p">);</span>  <span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;SIRT3D_CUDA&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">imshow</span><span class="p">(</span><span class="n">rec</span><span class="p">[</span><span class="mi">64</span><span class="p">,:,:],</span> <span class="n">cmap</span><span class="o">=</span><span class="s1">&#39;gray&#39;</span><span class="p">);</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt"></div>


<div class="output_svg output_subarea ">
<?xml version="1.0" encoding="utf-8" standalone="no"?>

<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN"

  "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">

<!-- Created with matplotlib (https://matplotlib.org/) -->

<svg height="243.137426pt" version="1.1" viewBox="0 0 715.784743 243.137426" width="715.784743pt" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">

 <defs>

  <style type="text/css">

*{stroke-linecap:butt;stroke-linejoin:round;}

  </style>

 </defs>

 <g id="figure_1">

  <g id="patch_1">

   <path d="M 0 243.137426 

L 715.784743 243.137426 

L 715.784743 0 

L 0 0 

z

" style="fill:none;"/>

  </g>

  <g id="axes_1">

   <g id="patch_2">

    <path d="M 33.2875 219.259301 

L 230.228676 219.259301 

L 230.228676 22.318125 

L 33.2875 22.318125 

z

" style="fill:#ffffff;"/>

   </g>

   <g clip-path="url(#p689e081778)">

    <image height="197" id="image58a22ba204" transform="scale(1 -1)translate(0 -197)" width="197" x="33.2875" xlink:href="data:image/png;base64,

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" y="-22.259301"/>

   </g>

   <g id="matplotlib.axis_1">

    <g id="xtick_1">

     <g id="line2d_1">

      <defs>

       <path d="M 0 0 

L 0 3.5 

" id="mcb3674a554" style="stroke:#000000;stroke-width:0.8;"/>

      </defs>

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="34.056801" xlink:href="#mcb3674a554" y="219.259301"/>

      </g>

     </g>

     <g id="text_1">

      <!-- 0 -->

      <defs>

       <path d="M 31.78125 66.40625 

Q 24.171875 66.40625 20.328125 58.90625 

Q 16.5 51.421875 16.5 36.375 

Q 16.5 21.390625 20.328125 13.890625 

Q 24.171875 6.390625 31.78125 6.390625 

Q 39.453125 6.390625 43.28125 13.890625 

Q 47.125 21.390625 47.125 36.375 

Q 47.125 51.421875 43.28125 58.90625 

Q 39.453125 66.40625 31.78125 66.40625 

z

M 31.78125 74.21875 

Q 44.046875 74.21875 50.515625 64.515625 

Q 56.984375 54.828125 56.984375 36.375 

Q 56.984375 17.96875 50.515625 8.265625 

Q 44.046875 -1.421875 31.78125 -1.421875 

Q 19.53125 -1.421875 13.0625 8.265625 

Q 6.59375 17.96875 6.59375 36.375 

Q 6.59375 54.828125 13.0625 64.515625 

Q 19.53125 74.21875 31.78125 74.21875 

z

" id="DejaVuSans-48"/>

      </defs>

      <g transform="translate(30.875551 233.857739)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_2">

     <g id="line2d_2">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="72.521875" xlink:href="#mcb3674a554" y="219.259301"/>

      </g>

     </g>

     <g id="text_2">

      <!-- 25 -->

      <defs>

       <path d="M 19.1875 8.296875 

L 53.609375 8.296875 

L 53.609375 0 

L 7.328125 0 

L 7.328125 8.296875 

Q 12.9375 14.109375 22.625 23.890625 

Q 32.328125 33.6875 34.8125 36.53125 

Q 39.546875 41.84375 41.421875 45.53125 

Q 43.3125 49.21875 43.3125 52.78125 

Q 43.3125 58.59375 39.234375 62.25 

Q 35.15625 65.921875 28.609375 65.921875 

Q 23.96875 65.921875 18.8125 64.3125 

Q 13.671875 62.703125 7.8125 59.421875 

L 7.8125 69.390625 

Q 13.765625 71.78125 18.9375 73 

Q 24.125 74.21875 28.421875 74.21875 

Q 39.75 74.21875 46.484375 68.546875 

Q 53.21875 62.890625 53.21875 53.421875 

Q 53.21875 48.921875 51.53125 44.890625 

Q 49.859375 40.875 45.40625 35.40625 

Q 44.1875 33.984375 37.640625 27.21875 

Q 31.109375 20.453125 19.1875 8.296875 

z

" id="DejaVuSans-50"/>

       <path d="M 10.796875 72.90625 

L 49.515625 72.90625 

L 49.515625 64.59375 

L 19.828125 64.59375 

L 19.828125 46.734375 

Q 21.96875 47.46875 24.109375 47.828125 

Q 26.265625 48.1875 28.421875 48.1875 

Q 40.625 48.1875 47.75 41.5 

Q 54.890625 34.8125 54.890625 23.390625 

Q 54.890625 11.625 47.5625 5.09375 

Q 40.234375 -1.421875 26.90625 -1.421875 

Q 22.3125 -1.421875 17.546875 -0.640625 

Q 12.796875 0.140625 7.71875 1.703125 

L 7.71875 11.625 

Q 12.109375 9.234375 16.796875 8.0625 

Q 21.484375 6.890625 26.703125 6.890625 

Q 35.15625 6.890625 40.078125 11.328125 

Q 45.015625 15.765625 45.015625 23.390625 

Q 45.015625 31 40.078125 35.4375 

Q 35.15625 39.890625 26.703125 39.890625 

Q 22.75 39.890625 18.8125 39.015625 

Q 14.890625 38.140625 10.796875 36.28125 

z

" id="DejaVuSans-53"/>

      </defs>

      <g transform="translate(66.159375 233.857739)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-50"/>

       <use x="63.623047" xlink:href="#DejaVuSans-53"/>

      </g>

     </g>

    </g>

    <g id="xtick_3">

     <g id="line2d_3">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="110.986949" xlink:href="#mcb3674a554" y="219.259301"/>

      </g>

     </g>

     <g id="text_3">

      <!-- 50 -->

      <g transform="translate(104.624449 233.857739)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-53"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_4">

     <g id="line2d_4">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="149.452022" xlink:href="#mcb3674a554" y="219.259301"/>

      </g>

     </g>

     <g id="text_4">

      <!-- 75 -->

      <defs>

       <path d="M 8.203125 72.90625 

L 55.078125 72.90625 

L 55.078125 68.703125 

L 28.609375 0 

L 18.3125 0 

L 43.21875 64.59375 

L 8.203125 64.59375 

z

" id="DejaVuSans-55"/>

      </defs>

      <g transform="translate(143.089522 233.857739)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-55"/>

       <use x="63.623047" xlink:href="#DejaVuSans-53"/>

      </g>

     </g>

    </g>

    <g id="xtick_5">

     <g id="line2d_5">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="187.917096" xlink:href="#mcb3674a554" y="219.259301"/>

      </g>

     </g>

     <g id="text_5">

      <!-- 100 -->

      <defs>

       <path d="M 12.40625 8.296875 

L 28.515625 8.296875 

L 28.515625 63.921875 

L 10.984375 60.40625 

L 10.984375 69.390625 

L 28.421875 72.90625 

L 38.28125 72.90625 

L 38.28125 8.296875 

L 54.390625 8.296875 

L 54.390625 0 

L 12.40625 0 

z

" id="DejaVuSans-49"/>

      </defs>

      <g transform="translate(178.373346 233.857739)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_6">

     <g id="line2d_6">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="226.382169" xlink:href="#mcb3674a554" y="219.259301"/>

      </g>

     </g>

     <g id="text_6">

      <!-- 125 -->

      <g transform="translate(216.838419 233.857739)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-50"/>

       <use x="127.246094" xlink:href="#DejaVuSans-53"/>

      </g>

     </g>

    </g>

   </g>

   <g id="matplotlib.axis_2">

    <g id="ytick_1">

     <g id="line2d_7">

      <defs>

       <path d="M 0 0 

L -3.5 0 

" id="mfc78c67cd4" style="stroke:#000000;stroke-width:0.8;"/>

      </defs>

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#mfc78c67cd4" y="23.087426"/>

      </g>

     </g>

     <g id="text_7">

      <!-- 0 -->

      <g transform="translate(19.925 26.886645)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_2">

     <g id="line2d_8">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#mfc78c67cd4" y="53.859485"/>

      </g>

     </g>

     <g id="text_8">

      <!-- 20 -->

      <g transform="translate(13.5625 57.658704)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-50"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_3">

     <g id="line2d_9">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#mfc78c67cd4" y="84.631544"/>

      </g>

     </g>

     <g id="text_9">

      <!-- 40 -->

      <defs>

       <path d="M 37.796875 64.3125 

L 12.890625 25.390625 

L 37.796875 25.390625 

z

M 35.203125 72.90625 

L 47.609375 72.90625 

L 47.609375 25.390625 

L 58.015625 25.390625 

L 58.015625 17.1875 

L 47.609375 17.1875 

L 47.609375 0 

L 37.796875 0 

L 37.796875 17.1875 

L 4.890625 17.1875 

L 4.890625 26.703125 

z

" id="DejaVuSans-52"/>

      </defs>

      <g transform="translate(13.5625 88.430763)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-52"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_4">

     <g id="line2d_10">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#mfc78c67cd4" y="115.403603"/>

      </g>

     </g>

     <g id="text_10">

      <!-- 60 -->

      <defs>

       <path d="M 33.015625 40.375 

Q 26.375 40.375 22.484375 35.828125 

Q 18.609375 31.296875 18.609375 23.390625 

Q 18.609375 15.53125 22.484375 10.953125 

Q 26.375 6.390625 33.015625 6.390625 

Q 39.65625 6.390625 43.53125 10.953125 

Q 47.40625 15.53125 47.40625 23.390625 

Q 47.40625 31.296875 43.53125 35.828125 

Q 39.65625 40.375 33.015625 40.375 

z

M 52.59375 71.296875 

L 52.59375 62.3125 

Q 48.875 64.0625 45.09375 64.984375 

Q 41.3125 65.921875 37.59375 65.921875 

Q 27.828125 65.921875 22.671875 59.328125 

Q 17.53125 52.734375 16.796875 39.40625 

Q 19.671875 43.65625 24.015625 45.921875 

Q 28.375 48.1875 33.59375 48.1875 

Q 44.578125 48.1875 50.953125 41.515625 

Q 57.328125 34.859375 57.328125 23.390625 

Q 57.328125 12.15625 50.6875 5.359375 

Q 44.046875 -1.421875 33.015625 -1.421875 

Q 20.359375 -1.421875 13.671875 8.265625 

Q 6.984375 17.96875 6.984375 36.375 

Q 6.984375 53.65625 15.1875 63.9375 

Q 23.390625 74.21875 37.203125 74.21875 

Q 40.921875 74.21875 44.703125 73.484375 

Q 48.484375 72.75 52.59375 71.296875 

z

" id="DejaVuSans-54"/>

      </defs>

      <g transform="translate(13.5625 119.202822)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-54"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_5">

     <g id="line2d_11">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#mfc78c67cd4" y="146.175662"/>

      </g>

     </g>

     <g id="text_11">

      <!-- 80 -->

      <defs>

       <path d="M 31.78125 34.625 

Q 24.75 34.625 20.71875 30.859375 

Q 16.703125 27.09375 16.703125 20.515625 

Q 16.703125 13.921875 20.71875 10.15625 

Q 24.75 6.390625 31.78125 6.390625 

Q 38.8125 6.390625 42.859375 10.171875 

Q 46.921875 13.96875 46.921875 20.515625 

Q 46.921875 27.09375 42.890625 30.859375 

Q 38.875 34.625 31.78125 34.625 

z

M 21.921875 38.8125 

Q 15.578125 40.375 12.03125 44.71875 

Q 8.5 49.078125 8.5 55.328125 

Q 8.5 64.0625 14.71875 69.140625 

Q 20.953125 74.21875 31.78125 74.21875 

Q 42.671875 74.21875 48.875 69.140625 

Q 55.078125 64.0625 55.078125 55.328125 

Q 55.078125 49.078125 51.53125 44.71875 

Q 48 40.375 41.703125 38.8125 

Q 48.828125 37.15625 52.796875 32.3125 

Q 56.78125 27.484375 56.78125 20.515625 

Q 56.78125 9.90625 50.3125 4.234375 

Q 43.84375 -1.421875 31.78125 -1.421875 

Q 19.734375 -1.421875 13.25 4.234375 

Q 6.78125 9.90625 6.78125 20.515625 

Q 6.78125 27.484375 10.78125 32.3125 

Q 14.796875 37.15625 21.921875 38.8125 

z

M 18.3125 54.390625 

Q 18.3125 48.734375 21.84375 45.5625 

Q 25.390625 42.390625 31.78125 42.390625 

Q 38.140625 42.390625 41.71875 45.5625 

Q 45.3125 48.734375 45.3125 54.390625 

Q 45.3125 60.0625 41.71875 63.234375 

Q 38.140625 66.40625 31.78125 66.40625 

Q 25.390625 66.40625 21.84375 63.234375 

Q 18.3125 60.0625 18.3125 54.390625 

z

" id="DejaVuSans-56"/>

      </defs>

      <g transform="translate(13.5625 149.974881)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-56"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_6">

     <g id="line2d_12">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#mfc78c67cd4" y="176.947721"/>

      </g>

     </g>

     <g id="text_12">

      <!-- 100 -->

      <g transform="translate(7.2 180.746939)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_7">

     <g id="line2d_13">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#mfc78c67cd4" y="207.719779"/>

      </g>

     </g>

     <g id="text_13">

      <!-- 120 -->

      <g transform="translate(7.2 211.518998)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-50"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

   </g>

   <g id="patch_3">

    <path d="M 33.2875 219.259301 

L 33.2875 22.318125 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_4">

    <path d="M 230.228676 219.259301 

L 230.228676 22.318125 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_5">

    <path d="M 33.2875 219.259301 

L 230.228676 219.259301 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_6">

    <path d="M 33.2875 22.318125 

L 230.228676 22.318125 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="text_14">

    <!-- Phantom -->

    <defs>

     <path d="M 19.671875 64.796875 

L 19.671875 37.40625 

L 32.078125 37.40625 

Q 38.96875 37.40625 42.71875 40.96875 

Q 46.484375 44.53125 46.484375 51.125 

Q 46.484375 57.671875 42.71875 61.234375 

Q 38.96875 64.796875 32.078125 64.796875 

z

M 9.8125 72.90625 

L 32.078125 72.90625 

Q 44.34375 72.90625 50.609375 67.359375 

Q 56.890625 61.8125 56.890625 51.125 

Q 56.890625 40.328125 50.609375 34.8125 

Q 44.34375 29.296875 32.078125 29.296875 

L 19.671875 29.296875 

L 19.671875 0 

L 9.8125 0 

z

" id="DejaVuSans-80"/>

     <path d="M 54.890625 33.015625 

L 54.890625 0 

L 45.90625 0 

L 45.90625 32.71875 

Q 45.90625 40.484375 42.875 44.328125 

Q 39.84375 48.1875 33.796875 48.1875 

Q 26.515625 48.1875 22.3125 43.546875 

Q 18.109375 38.921875 18.109375 30.90625 

L 18.109375 0 

L 9.078125 0 

L 9.078125 75.984375 

L 18.109375 75.984375 

L 18.109375 46.1875 

Q 21.34375 51.125 25.703125 53.5625 

Q 30.078125 56 35.796875 56 

Q 45.21875 56 50.046875 50.171875 

Q 54.890625 44.34375 54.890625 33.015625 

z

" id="DejaVuSans-104"/>

     <path d="M 34.28125 27.484375 

Q 23.390625 27.484375 19.1875 25 

Q 14.984375 22.515625 14.984375 16.5 

Q 14.984375 11.71875 18.140625 8.90625 

Q 21.296875 6.109375 26.703125 6.109375 

Q 34.1875 6.109375 38.703125 11.40625 

Q 43.21875 16.703125 43.21875 25.484375 

L 43.21875 27.484375 

z

M 52.203125 31.203125 

L 52.203125 0 

L 43.21875 0 

L 43.21875 8.296875 

Q 40.140625 3.328125 35.546875 0.953125 

Q 30.953125 -1.421875 24.3125 -1.421875 

Q 15.921875 -1.421875 10.953125 3.296875 

Q 6 8.015625 6 15.921875 

Q 6 25.140625 12.171875 29.828125 

Q 18.359375 34.515625 30.609375 34.515625 

L 43.21875 34.515625 

L 43.21875 35.40625 

Q 43.21875 41.609375 39.140625 45 

Q 35.0625 48.390625 27.6875 48.390625 

Q 23 48.390625 18.546875 47.265625 

Q 14.109375 46.140625 10.015625 43.890625 

L 10.015625 52.203125 

Q 14.9375 54.109375 19.578125 55.046875 

Q 24.21875 56 28.609375 56 

Q 40.484375 56 46.34375 49.84375 

Q 52.203125 43.703125 52.203125 31.203125 

z

" id="DejaVuSans-97"/>

     <path d="M 54.890625 33.015625 

L 54.890625 0 

L 45.90625 0 

L 45.90625 32.71875 

Q 45.90625 40.484375 42.875 44.328125 

Q 39.84375 48.1875 33.796875 48.1875 

Q 26.515625 48.1875 22.3125 43.546875 

Q 18.109375 38.921875 18.109375 30.90625 

L 18.109375 0 

L 9.078125 0 

L 9.078125 54.6875 

L 18.109375 54.6875 

L 18.109375 46.1875 

Q 21.34375 51.125 25.703125 53.5625 

Q 30.078125 56 35.796875 56 

Q 45.21875 56 50.046875 50.171875 

Q 54.890625 44.34375 54.890625 33.015625 

z

" id="DejaVuSans-110"/>

     <path d="M 18.3125 70.21875 

L 18.3125 54.6875 

L 36.8125 54.6875 

L 36.8125 47.703125 

L 18.3125 47.703125 

L 18.3125 18.015625 

Q 18.3125 11.328125 20.140625 9.421875 

Q 21.96875 7.515625 27.59375 7.515625 

L 36.8125 7.515625 

L 36.8125 0 

L 27.59375 0 

Q 17.1875 0 13.234375 3.875 

Q 9.28125 7.765625 9.28125 18.015625 

L 9.28125 47.703125 

L 2.6875 47.703125 

L 2.6875 54.6875 

L 9.28125 54.6875 

L 9.28125 70.21875 

z

" id="DejaVuSans-116"/>

     <path d="M 30.609375 48.390625 

Q 23.390625 48.390625 19.1875 42.75 

Q 14.984375 37.109375 14.984375 27.296875 

Q 14.984375 17.484375 19.15625 11.84375 

Q 23.34375 6.203125 30.609375 6.203125 

Q 37.796875 6.203125 41.984375 11.859375 

Q 46.1875 17.53125 46.1875 27.296875 

Q 46.1875 37.015625 41.984375 42.703125 

Q 37.796875 48.390625 30.609375 48.390625 

z

M 30.609375 56 

Q 42.328125 56 49.015625 48.375 

Q 55.71875 40.765625 55.71875 27.296875 

Q 55.71875 13.875 49.015625 6.21875 

Q 42.328125 -1.421875 30.609375 -1.421875 

Q 18.84375 -1.421875 12.171875 6.21875 

Q 5.515625 13.875 5.515625 27.296875 

Q 5.515625 40.765625 12.171875 48.375 

Q 18.84375 56 30.609375 56 

z

" id="DejaVuSans-111"/>

     <path d="M 52 44.1875 

Q 55.375 50.25 60.0625 53.125 

Q 64.75 56 71.09375 56 

Q 79.640625 56 84.28125 50.015625 

Q 88.921875 44.046875 88.921875 33.015625 

L 88.921875 0 

L 79.890625 0 

L 79.890625 32.71875 

Q 79.890625 40.578125 77.09375 44.375 

Q 74.3125 48.1875 68.609375 48.1875 

Q 61.625 48.1875 57.5625 43.546875 

Q 53.515625 38.921875 53.515625 30.90625 

L 53.515625 0 

L 44.484375 0 

L 44.484375 32.71875 

Q 44.484375 40.625 41.703125 44.40625 

Q 38.921875 48.1875 33.109375 48.1875 

Q 26.21875 48.1875 22.15625 43.53125 

Q 18.109375 38.875 18.109375 30.90625 

L 18.109375 0 

L 9.078125 0 

L 9.078125 54.6875 

L 18.109375 54.6875 

L 18.109375 46.1875 

Q 21.1875 51.21875 25.484375 53.609375 

Q 29.78125 56 35.6875 56 

Q 41.65625 56 45.828125 52.96875 

Q 50 49.953125 52 44.1875 

z

" id="DejaVuSans-109"/>

    </defs>

    <g transform="translate(104.990588 16.318125)scale(0.12 -0.12)">

     <use xlink:href="#DejaVuSans-80"/>

     <use x="60.302734" xlink:href="#DejaVuSans-104"/>

     <use x="123.681641" xlink:href="#DejaVuSans-97"/>

     <use x="184.960938" xlink:href="#DejaVuSans-110"/>

     <use x="248.339844" xlink:href="#DejaVuSans-116"/>

     <use x="287.548828" xlink:href="#DejaVuSans-111"/>

     <use x="348.730469" xlink:href="#DejaVuSans-109"/>

    </g>

   </g>

  </g>

  <g id="axes_2">

   <g id="patch_7">

    <path d="M 269.616912 213.10489 

L 466.558088 213.10489 

L 466.558088 28.472537 

L 269.616912 28.472537 

z

" style="fill:#ffffff;"/>

   </g>

   <g clip-path="url(#p82095d2861)">

    <image height="185" id="image5127b7eb58" transform="scale(1 -1)translate(0 -185)" width="197" x="269.616912" xlink:href="data:image/png;base64,

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" y="-28.10489"/>

   </g>

   <g id="matplotlib.axis_3">

    <g id="xtick_7">

     <g id="line2d_14">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="270.129779" xlink:href="#mcb3674a554" y="213.10489"/>

      </g>

     </g>

     <g id="text_15">

      <!-- 0 -->

      <g transform="translate(266.948529 227.703327)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_8">

     <g id="line2d_15">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="321.416544" xlink:href="#mcb3674a554" y="213.10489"/>

      </g>

     </g>

     <g id="text_16">

      <!-- 50 -->

      <g transform="translate(315.054044 227.703327)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-53"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_9">

     <g id="line2d_16">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="372.703309" xlink:href="#mcb3674a554" y="213.10489"/>

      </g>

     </g>

     <g id="text_17">

      <!-- 100 -->

      <g transform="translate(363.159559 227.703327)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_10">

     <g id="line2d_17">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="423.990074" xlink:href="#mcb3674a554" y="213.10489"/>

      </g>

     </g>

     <g id="text_18">

      <!-- 150 -->

      <g transform="translate(414.446324 227.703327)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-53"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

   </g>

   <g id="matplotlib.axis_4">

    <g id="ytick_8">

     <g id="line2d_18">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="269.616912" xlink:href="#mfc78c67cd4" y="28.985404"/>

      </g>

     </g>

     <g id="text_19">

      <!-- 0 -->

      <g transform="translate(256.254412 32.784623)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_9">

     <g id="line2d_19">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="269.616912" xlink:href="#mfc78c67cd4" y="49.50011"/>

      </g>

     </g>

     <g id="text_20">

      <!-- 20 -->

      <g transform="translate(249.891912 53.299329)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-50"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_10">

     <g id="line2d_20">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="269.616912" xlink:href="#mfc78c67cd4" y="70.014816"/>

      </g>

     </g>

     <g id="text_21">

      <!-- 40 -->

      <g transform="translate(249.891912 73.814035)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-52"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_11">

     <g id="line2d_21">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="269.616912" xlink:href="#mfc78c67cd4" y="90.529522"/>

      </g>

     </g>

     <g id="text_22">

      <!-- 60 -->

      <g transform="translate(249.891912 94.328741)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-54"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_12">

     <g id="line2d_22">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="269.616912" xlink:href="#mfc78c67cd4" y="111.044228"/>

      </g>

     </g>

     <g id="text_23">

      <!-- 80 -->

      <g transform="translate(249.891912 114.843447)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-56"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_13">

     <g id="line2d_23">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="269.616912" xlink:href="#mfc78c67cd4" y="131.558934"/>

      </g>

     </g>

     <g id="text_24">

      <!-- 100 -->

      <g transform="translate(243.529412 135.358153)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_14">

     <g id="line2d_24">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="269.616912" xlink:href="#mfc78c67cd4" y="152.07364"/>

      </g>

     </g>

     <g id="text_25">

      <!-- 120 -->

      <g transform="translate(243.529412 155.872858)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-50"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_15">

     <g id="line2d_25">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="269.616912" xlink:href="#mfc78c67cd4" y="172.588346"/>

      </g>

     </g>

     <g id="text_26">

      <!-- 140 -->

      <g transform="translate(243.529412 176.387564)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-52"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_16">

     <g id="line2d_26">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="269.616912" xlink:href="#mfc78c67cd4" y="193.103051"/>

      </g>

     </g>

     <g id="text_27">

      <!-- 160 -->

      <g transform="translate(243.529412 196.90227)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-54"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

   </g>

   <g id="patch_8">

    <path d="M 269.616912 213.10489 

L 269.616912 28.472537 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_9">

    <path d="M 466.558088 213.10489 

L 466.558088 28.472537 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_10">

    <path d="M 269.616912 213.10489 

L 466.558088 213.10489 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_11">

    <path d="M 269.616912 28.472537 

L 466.558088 28.472537 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="text_28">

    <!-- Single projection image -->

    <defs>

     <path d="M 53.515625 70.515625 

L 53.515625 60.890625 

Q 47.90625 63.578125 42.921875 64.890625 

Q 37.9375 66.21875 33.296875 66.21875 

Q 25.25 66.21875 20.875 63.09375 

Q 16.5 59.96875 16.5 54.203125 

Q 16.5 49.359375 19.40625 46.890625 

Q 22.3125 44.4375 30.421875 42.921875 

L 36.375 41.703125 

Q 47.40625 39.59375 52.65625 34.296875 

Q 57.90625 29 57.90625 20.125 

Q 57.90625 9.515625 50.796875 4.046875 

Q 43.703125 -1.421875 29.984375 -1.421875 

Q 24.8125 -1.421875 18.96875 -0.25 

Q 13.140625 0.921875 6.890625 3.21875 

L 6.890625 13.375 

Q 12.890625 10.015625 18.65625 8.296875 

Q 24.421875 6.59375 29.984375 6.59375 

Q 38.421875 6.59375 43.015625 9.90625 

Q 47.609375 13.234375 47.609375 19.390625 

Q 47.609375 24.75 44.3125 27.78125 

Q 41.015625 30.8125 33.5 32.328125 

L 27.484375 33.5 

Q 16.453125 35.6875 11.515625 40.375 

Q 6.59375 45.0625 6.59375 53.421875 

Q 6.59375 63.09375 13.40625 68.65625 

Q 20.21875 74.21875 32.171875 74.21875 

Q 37.3125 74.21875 42.625 73.28125 

Q 47.953125 72.359375 53.515625 70.515625 

z

" id="DejaVuSans-83"/>

     <path d="M 9.421875 54.6875 

L 18.40625 54.6875 

L 18.40625 0 

L 9.421875 0 

z

M 9.421875 75.984375 

L 18.40625 75.984375 

L 18.40625 64.59375 

L 9.421875 64.59375 

z

" id="DejaVuSans-105"/>

     <path d="M 45.40625 27.984375 

Q 45.40625 37.75 41.375 43.109375 

Q 37.359375 48.484375 30.078125 48.484375 

Q 22.859375 48.484375 18.828125 43.109375 

Q 14.796875 37.75 14.796875 27.984375 

Q 14.796875 18.265625 18.828125 12.890625 

Q 22.859375 7.515625 30.078125 7.515625 

Q 37.359375 7.515625 41.375 12.890625 

Q 45.40625 18.265625 45.40625 27.984375 

z

M 54.390625 6.78125 

Q 54.390625 -7.171875 48.1875 -13.984375 

Q 42 -20.796875 29.203125 -20.796875 

Q 24.46875 -20.796875 20.265625 -20.09375 

Q 16.0625 -19.390625 12.109375 -17.921875 

L 12.109375 -9.1875 

Q 16.0625 -11.328125 19.921875 -12.34375 

Q 23.78125 -13.375 27.78125 -13.375 

Q 36.625 -13.375 41.015625 -8.765625 

Q 45.40625 -4.15625 45.40625 5.171875 

L 45.40625 9.625 

Q 42.625 4.78125 38.28125 2.390625 

Q 33.9375 0 27.875 0 

Q 17.828125 0 11.671875 7.65625 

Q 5.515625 15.328125 5.515625 27.984375 

Q 5.515625 40.671875 11.671875 48.328125 

Q 17.828125 56 27.875 56 

Q 33.9375 56 38.28125 53.609375 

Q 42.625 51.21875 45.40625 46.390625 

L 45.40625 54.6875 

L 54.390625 54.6875 

z

" id="DejaVuSans-103"/>

     <path d="M 9.421875 75.984375 

L 18.40625 75.984375 

L 18.40625 0 

L 9.421875 0 

z

" id="DejaVuSans-108"/>

     <path d="M 56.203125 29.59375 

L 56.203125 25.203125 

L 14.890625 25.203125 

Q 15.484375 15.921875 20.484375 11.0625 

Q 25.484375 6.203125 34.421875 6.203125 

Q 39.59375 6.203125 44.453125 7.46875 

Q 49.3125 8.734375 54.109375 11.28125 

L 54.109375 2.78125 

Q 49.265625 0.734375 44.1875 -0.34375 

Q 39.109375 -1.421875 33.890625 -1.421875 

Q 20.796875 -1.421875 13.15625 6.1875 

Q 5.515625 13.8125 5.515625 26.8125 

Q 5.515625 40.234375 12.765625 48.109375 

Q 20.015625 56 32.328125 56 

Q 43.359375 56 49.78125 48.890625 

Q 56.203125 41.796875 56.203125 29.59375 

z

M 47.21875 32.234375 

Q 47.125 39.59375 43.09375 43.984375 

Q 39.0625 48.390625 32.421875 48.390625 

Q 24.90625 48.390625 20.390625 44.140625 

Q 15.875 39.890625 15.1875 32.171875 

z

" id="DejaVuSans-101"/>

     <path id="DejaVuSans-32"/>

     <path d="M 18.109375 8.203125 

L 18.109375 -20.796875 

L 9.078125 -20.796875 

L 9.078125 54.6875 

L 18.109375 54.6875 

L 18.109375 46.390625 

Q 20.953125 51.265625 25.265625 53.625 

Q 29.59375 56 35.59375 56 

Q 45.5625 56 51.78125 48.09375 

Q 58.015625 40.1875 58.015625 27.296875 

Q 58.015625 14.40625 51.78125 6.484375 

Q 45.5625 -1.421875 35.59375 -1.421875 

Q 29.59375 -1.421875 25.265625 0.953125 

Q 20.953125 3.328125 18.109375 8.203125 

z

M 48.6875 27.296875 

Q 48.6875 37.203125 44.609375 42.84375 

Q 40.53125 48.484375 33.40625 48.484375 

Q 26.265625 48.484375 22.1875 42.84375 

Q 18.109375 37.203125 18.109375 27.296875 

Q 18.109375 17.390625 22.1875 11.75 

Q 26.265625 6.109375 33.40625 6.109375 

Q 40.53125 6.109375 44.609375 11.75 

Q 48.6875 17.390625 48.6875 27.296875 

z

" id="DejaVuSans-112"/>

     <path d="M 41.109375 46.296875 

Q 39.59375 47.171875 37.8125 47.578125 

Q 36.03125 48 33.890625 48 

Q 26.265625 48 22.1875 43.046875 

Q 18.109375 38.09375 18.109375 28.8125 

L 18.109375 0 

L 9.078125 0 

L 9.078125 54.6875 

L 18.109375 54.6875 

L 18.109375 46.1875 

Q 20.953125 51.171875 25.484375 53.578125 

Q 30.03125 56 36.53125 56 

Q 37.453125 56 38.578125 55.875 

Q 39.703125 55.765625 41.0625 55.515625 

z

" id="DejaVuSans-114"/>

     <path d="M 9.421875 54.6875 

L 18.40625 54.6875 

L 18.40625 -0.984375 

Q 18.40625 -11.421875 14.421875 -16.109375 

Q 10.453125 -20.796875 1.609375 -20.796875 

L -1.8125 -20.796875 

L -1.8125 -13.1875 

L 0.59375 -13.1875 

Q 5.71875 -13.1875 7.5625 -10.8125 

Q 9.421875 -8.453125 9.421875 -0.984375 

z

M 9.421875 75.984375 

L 18.40625 75.984375 

L 18.40625 64.59375 

L 9.421875 64.59375 

z

" id="DejaVuSans-106"/>

     <path d="M 48.78125 52.59375 

L 48.78125 44.1875 

Q 44.96875 46.296875 41.140625 47.34375 

Q 37.3125 48.390625 33.40625 48.390625 

Q 24.65625 48.390625 19.8125 42.84375 

Q 14.984375 37.3125 14.984375 27.296875 

Q 14.984375 17.28125 19.8125 11.734375 

Q 24.65625 6.203125 33.40625 6.203125 

Q 37.3125 6.203125 41.140625 7.25 

Q 44.96875 8.296875 48.78125 10.40625 

L 48.78125 2.09375 

Q 45.015625 0.34375 40.984375 -0.53125 

Q 36.96875 -1.421875 32.421875 -1.421875 

Q 20.0625 -1.421875 12.78125 6.34375 

Q 5.515625 14.109375 5.515625 27.296875 

Q 5.515625 40.671875 12.859375 48.328125 

Q 20.21875 56 33.015625 56 

Q 37.15625 56 41.109375 55.140625 

Q 45.0625 54.296875 48.78125 52.59375 

z

" id="DejaVuSans-99"/>

    </defs>

    <g transform="translate(297.042813 22.472537)scale(0.12 -0.12)">

     <use xlink:href="#DejaVuSans-83"/>

     <use x="63.476562" xlink:href="#DejaVuSans-105"/>

     <use x="91.259766" xlink:href="#DejaVuSans-110"/>

     <use x="154.638672" xlink:href="#DejaVuSans-103"/>

     <use x="218.115234" xlink:href="#DejaVuSans-108"/>

     <use x="245.898438" xlink:href="#DejaVuSans-101"/>

     <use x="307.421875" xlink:href="#DejaVuSans-32"/>

     <use x="339.208984" xlink:href="#DejaVuSans-112"/>

     <use x="402.685547" xlink:href="#DejaVuSans-114"/>

     <use x="443.767578" xlink:href="#DejaVuSans-111"/>

     <use x="504.949219" xlink:href="#DejaVuSans-106"/>

     <use x="532.732422" xlink:href="#DejaVuSans-101"/>

     <use x="594.255859" xlink:href="#DejaVuSans-99"/>

     <use x="649.236328" xlink:href="#DejaVuSans-116"/>

     <use x="688.445312" xlink:href="#DejaVuSans-105"/>

     <use x="716.228516" xlink:href="#DejaVuSans-111"/>

     <use x="777.410156" xlink:href="#DejaVuSans-110"/>

     <use x="840.789062" xlink:href="#DejaVuSans-32"/>

     <use x="872.576172" xlink:href="#DejaVuSans-105"/>

     <use x="900.359375" xlink:href="#DejaVuSans-109"/>

     <use x="997.771484" xlink:href="#DejaVuSans-97"/>

     <use x="1059.050781" xlink:href="#DejaVuSans-103"/>

     <use x="1122.527344" xlink:href="#DejaVuSans-101"/>

    </g>

   </g>

  </g>

  <g id="axes_3">

   <g id="patch_12">

    <path d="M 505.946324 219.259301 

L 702.8875 219.259301 

L 702.8875 22.318125 

L 505.946324 22.318125 

z

" style="fill:#ffffff;"/>

   </g>

   <g clip-path="url(#pbcd47cb0ec)">

    <image height="197" id="imagec6a98c8742" transform="scale(1 -1)translate(0 -197)" width="197" x="505.946324" xlink:href="data:image/png;base64,

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" y="-22.259301"/>

   </g>

   <g id="matplotlib.axis_5">

    <g id="xtick_11">

     <g id="line2d_27">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="506.715625" xlink:href="#mcb3674a554" y="219.259301"/>

      </g>

     </g>

     <g id="text_29">

      <!-- 0 -->

      <g transform="translate(503.534375 233.857739)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_12">

     <g id="line2d_28">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="545.180699" xlink:href="#mcb3674a554" y="219.259301"/>

      </g>

     </g>

     <g id="text_30">

      <!-- 25 -->

      <g transform="translate(538.818199 233.857739)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-50"/>

       <use x="63.623047" xlink:href="#DejaVuSans-53"/>

      </g>

     </g>

    </g>

    <g id="xtick_13">

     <g id="line2d_29">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="583.645772" xlink:href="#mcb3674a554" y="219.259301"/>

      </g>

     </g>

     <g id="text_31">

      <!-- 50 -->

      <g transform="translate(577.283272 233.857739)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-53"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_14">

     <g id="line2d_30">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="622.110846" xlink:href="#mcb3674a554" y="219.259301"/>

      </g>

     </g>

     <g id="text_32">

      <!-- 75 -->

      <g transform="translate(615.748346 233.857739)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-55"/>

       <use x="63.623047" xlink:href="#DejaVuSans-53"/>

      </g>

     </g>

    </g>

    <g id="xtick_15">

     <g id="line2d_31">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="660.575919" xlink:href="#mcb3674a554" y="219.259301"/>

      </g>

     </g>

     <g id="text_33">

      <!-- 100 -->

      <g transform="translate(651.032169 233.857739)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_16">

     <g id="line2d_32">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="699.040993" xlink:href="#mcb3674a554" y="219.259301"/>

      </g>

     </g>

     <g id="text_34">

      <!-- 125 -->

      <g transform="translate(689.497243 233.857739)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-50"/>

       <use x="127.246094" xlink:href="#DejaVuSans-53"/>

      </g>

     </g>

    </g>

   </g>

   <g id="matplotlib.axis_6">

    <g id="ytick_17">

     <g id="line2d_33">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="505.946324" xlink:href="#mfc78c67cd4" y="23.087426"/>

      </g>

     </g>

     <g id="text_35">

      <!-- 0 -->

      <g transform="translate(492.583824 26.886645)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_18">

     <g id="line2d_34">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="505.946324" xlink:href="#mfc78c67cd4" y="53.859485"/>

      </g>

     </g>

     <g id="text_36">

      <!-- 20 -->

      <g transform="translate(486.221324 57.658704)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-50"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_19">

     <g id="line2d_35">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="505.946324" xlink:href="#mfc78c67cd4" y="84.631544"/>

      </g>

     </g>

     <g id="text_37">

      <!-- 40 -->

      <g transform="translate(486.221324 88.430763)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-52"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_20">

     <g id="line2d_36">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="505.946324" xlink:href="#mfc78c67cd4" y="115.403603"/>

      </g>

     </g>

     <g id="text_38">

      <!-- 60 -->

      <g transform="translate(486.221324 119.202822)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-54"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_21">

     <g id="line2d_37">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="505.946324" xlink:href="#mfc78c67cd4" y="146.175662"/>

      </g>

     </g>

     <g id="text_39">

      <!-- 80 -->

      <g transform="translate(486.221324 149.974881)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-56"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_22">

     <g id="line2d_38">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="505.946324" xlink:href="#mfc78c67cd4" y="176.947721"/>

      </g>

     </g>

     <g id="text_40">

      <!-- 100 -->

      <g transform="translate(479.858824 180.746939)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_23">

     <g id="line2d_39">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="505.946324" xlink:href="#mfc78c67cd4" y="207.719779"/>

      </g>

     </g>

     <g id="text_41">

      <!-- 120 -->

      <g transform="translate(479.858824 211.518998)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-50"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

   </g>

   <g id="patch_13">

    <path d="M 505.946324 219.259301 

L 505.946324 22.318125 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_14">

    <path d="M 702.8875 219.259301 

L 702.8875 22.318125 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_15">

    <path d="M 505.946324 219.259301 

L 702.8875 219.259301 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_16">

    <path d="M 505.946324 22.318125 

L 702.8875 22.318125 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="text_42">

    <!-- SIRT3D_CUDA -->

    <defs>

     <path d="M 9.8125 72.90625 

L 19.671875 72.90625 

L 19.671875 0 

L 9.8125 0 

z

" id="DejaVuSans-73"/>

     <path d="M 44.390625 34.1875 

Q 47.5625 33.109375 50.5625 29.59375 

Q 53.5625 26.078125 56.59375 19.921875 

L 66.609375 0 

L 56 0 

L 46.6875 18.703125 

Q 43.0625 26.03125 39.671875 28.421875 

Q 36.28125 30.8125 30.421875 30.8125 

L 19.671875 30.8125 

L 19.671875 0 

L 9.8125 0 

L 9.8125 72.90625 

L 32.078125 72.90625 

Q 44.578125 72.90625 50.734375 67.671875 

Q 56.890625 62.453125 56.890625 51.90625 

Q 56.890625 45.015625 53.6875 40.46875 

Q 50.484375 35.9375 44.390625 34.1875 

z

M 19.671875 64.796875 

L 19.671875 38.921875 

L 32.078125 38.921875 

Q 39.203125 38.921875 42.84375 42.21875 

Q 46.484375 45.515625 46.484375 51.90625 

Q 46.484375 58.296875 42.84375 61.546875 

Q 39.203125 64.796875 32.078125 64.796875 

z

" id="DejaVuSans-82"/>

     <path d="M -0.296875 72.90625 

L 61.375 72.90625 

L 61.375 64.59375 

L 35.5 64.59375 

L 35.5 0 

L 25.59375 0 

L 25.59375 64.59375 

L -0.296875 64.59375 

z

" id="DejaVuSans-84"/>

     <path d="M 40.578125 39.3125 

Q 47.65625 37.796875 51.625 33 

Q 55.609375 28.21875 55.609375 21.1875 

Q 55.609375 10.40625 48.1875 4.484375 

Q 40.765625 -1.421875 27.09375 -1.421875 

Q 22.515625 -1.421875 17.65625 -0.515625 

Q 12.796875 0.390625 7.625 2.203125 

L 7.625 11.71875 

Q 11.71875 9.328125 16.59375 8.109375 

Q 21.484375 6.890625 26.8125 6.890625 

Q 36.078125 6.890625 40.9375 10.546875 

Q 45.796875 14.203125 45.796875 21.1875 

Q 45.796875 27.640625 41.28125 31.265625 

Q 36.765625 34.90625 28.71875 34.90625 

L 20.21875 34.90625 

L 20.21875 43.015625 

L 29.109375 43.015625 

Q 36.375 43.015625 40.234375 45.921875 

Q 44.09375 48.828125 44.09375 54.296875 

Q 44.09375 59.90625 40.109375 62.90625 

Q 36.140625 65.921875 28.71875 65.921875 

Q 24.65625 65.921875 20.015625 65.03125 

Q 15.375 64.15625 9.8125 62.3125 

L 9.8125 71.09375 

Q 15.4375 72.65625 20.34375 73.4375 

Q 25.25 74.21875 29.59375 74.21875 

Q 40.828125 74.21875 47.359375 69.109375 

Q 53.90625 64.015625 53.90625 55.328125 

Q 53.90625 49.265625 50.4375 45.09375 

Q 46.96875 40.921875 40.578125 39.3125 

z

" id="DejaVuSans-51"/>

     <path d="M 19.671875 64.796875 

L 19.671875 8.109375 

L 31.59375 8.109375 

Q 46.6875 8.109375 53.6875 14.9375 

Q 60.6875 21.78125 60.6875 36.53125 

Q 60.6875 51.171875 53.6875 57.984375 

Q 46.6875 64.796875 31.59375 64.796875 

z

M 9.8125 72.90625 

L 30.078125 72.90625 

Q 51.265625 72.90625 61.171875 64.09375 

Q 71.09375 55.28125 71.09375 36.53125 

Q 71.09375 17.671875 61.125 8.828125 

Q 51.171875 0 30.078125 0 

L 9.8125 0 

z

" id="DejaVuSans-68"/>

     <path d="M 50.984375 -16.609375 

L 50.984375 -23.578125 

L -0.984375 -23.578125 

L -0.984375 -16.609375 

z

" id="DejaVuSans-95"/>

     <path d="M 64.40625 67.28125 

L 64.40625 56.890625 

Q 59.421875 61.53125 53.78125 63.8125 

Q 48.140625 66.109375 41.796875 66.109375 

Q 29.296875 66.109375 22.65625 58.46875 

Q 16.015625 50.828125 16.015625 36.375 

Q 16.015625 21.96875 22.65625 14.328125 

Q 29.296875 6.6875 41.796875 6.6875 

Q 48.140625 6.6875 53.78125 8.984375 

Q 59.421875 11.28125 64.40625 15.921875 

L 64.40625 5.609375 

Q 59.234375 2.09375 53.4375 0.328125 

Q 47.65625 -1.421875 41.21875 -1.421875 

Q 24.65625 -1.421875 15.125 8.703125 

Q 5.609375 18.84375 5.609375 36.375 

Q 5.609375 53.953125 15.125 64.078125 

Q 24.65625 74.21875 41.21875 74.21875 

Q 47.75 74.21875 53.53125 72.484375 

Q 59.328125 70.75 64.40625 67.28125 

z

" id="DejaVuSans-67"/>

     <path d="M 8.6875 72.90625 

L 18.609375 72.90625 

L 18.609375 28.609375 

Q 18.609375 16.890625 22.84375 11.734375 

Q 27.09375 6.59375 36.625 6.59375 

Q 46.09375 6.59375 50.34375 11.734375 

Q 54.59375 16.890625 54.59375 28.609375 

L 54.59375 72.90625 

L 64.5 72.90625 

L 64.5 27.390625 

Q 64.5 13.140625 57.4375 5.859375 

Q 50.390625 -1.421875 36.625 -1.421875 

Q 22.796875 -1.421875 15.734375 5.859375 

Q 8.6875 13.140625 8.6875 27.390625 

z

" id="DejaVuSans-85"/>

     <path d="M 34.1875 63.1875 

L 20.796875 26.90625 

L 47.609375 26.90625 

z

M 28.609375 72.90625 

L 39.796875 72.90625 

L 67.578125 0 

L 57.328125 0 

L 50.6875 18.703125 

L 17.828125 18.703125 

L 11.1875 0 

L 0.78125 0 

z

" id="DejaVuSans-65"/>

    </defs>

    <g transform="translate(562.268787 16.318125)scale(0.12 -0.12)">

     <use xlink:href="#DejaVuSans-83"/>

     <use x="63.476562" xlink:href="#DejaVuSans-73"/>

     <use x="92.96875" xlink:href="#DejaVuSans-82"/>

     <use x="162.341797" xlink:href="#DejaVuSans-84"/>

     <use x="223.425781" xlink:href="#DejaVuSans-51"/>

     <use x="287.048828" xlink:href="#DejaVuSans-68"/>

     <use x="364.050781" xlink:href="#DejaVuSans-95"/>

     <use x="414.050781" xlink:href="#DejaVuSans-67"/>

     <use x="483.875" xlink:href="#DejaVuSans-85"/>

     <use x="557.068359" xlink:href="#DejaVuSans-68"/>

     <use x="634.054688" xlink:href="#DejaVuSans-65"/>

    </g>

   </g>

  </g>

 </g>

 <defs>

  <clipPath id="p689e081778">

   <rect height="196.941176" width="196.941176" x="33.2875" y="22.318125"/>

  </clipPath>

  <clipPath id="p82095d2861">

   <rect height="184.632353" width="196.941176" x="269.616912" y="28.472537"/>

  </clipPath>

  <clipPath id="pbcd47cb0ec">

   <rect height="196.941176" width="196.941176" x="505.946324" y="22.318125"/>

  </clipPath>

 </defs>

</svg>


</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="-TomoPy-+-Astra-"><center> TomoPy + Astra </center><a class="anchor-link" href="#-TomoPy-+-Astra-">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[14]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">obj</span> <span class="o">=</span> <span class="n">tomopy</span><span class="o">.</span><span class="n">shepp2d</span><span class="p">()</span> <span class="c1"># Generate an object.</span>
<span class="n">ang</span> <span class="o">=</span> <span class="n">tomopy</span><span class="o">.</span><span class="n">angles</span><span class="p">(</span><span class="mi">180</span><span class="p">)</span> <span class="c1"># Generate uniformly spaced tilt angles.</span>
<span class="n">sim</span> <span class="o">=</span> <span class="n">tomopy</span><span class="o">.</span><span class="n">project</span><span class="p">(</span><span class="n">obj</span><span class="p">,</span> <span class="n">ang</span><span class="p">)</span> <span class="c1"># Calculate projections.</span>

<span class="c1"># Reconstruct object:</span>
<span class="n">options</span> <span class="o">=</span> <span class="p">{</span><span class="s1">&#39;proj_type&#39;</span><span class="p">:</span><span class="s1">&#39;linear&#39;</span><span class="p">,</span> <span class="s1">&#39;method&#39;</span><span class="p">:</span><span class="s1">&#39;FBP&#39;</span><span class="p">}</span>
<span class="n">rec_fbp</span> <span class="o">=</span> <span class="n">tomopy</span><span class="o">.</span><span class="n">recon</span><span class="p">(</span><span class="n">sim</span><span class="p">,</span> <span class="n">ang</span><span class="p">,</span> <span class="n">algorithm</span><span class="o">=</span><span class="n">tomopy</span><span class="o">.</span><span class="n">astra</span><span class="p">,</span> <span class="n">options</span><span class="o">=</span><span class="n">options</span><span class="p">)</span>

<span class="n">options</span> <span class="o">=</span> <span class="n">options</span><span class="o">=</span><span class="p">{</span><span class="s1">&#39;method&#39;</span><span class="p">:</span><span class="s1">&#39;SART&#39;</span><span class="p">,</span> <span class="s1">&#39;num_iter&#39;</span><span class="p">:</span><span class="mi">10</span><span class="o">*</span><span class="mi">180</span><span class="p">,</span> <span class="s1">&#39;proj_type&#39;</span><span class="p">:</span><span class="s1">&#39;linear&#39;</span><span class="p">,</span> <span class="s1">&#39;extra_options&#39;</span><span class="p">:{</span><span class="s1">&#39;MinConstraint&#39;</span><span class="p">:</span><span class="mi">0</span><span class="p">}}</span>
<span class="n">rec_sart</span> <span class="o">=</span> <span class="n">tomopy</span><span class="o">.</span><span class="n">recon</span><span class="p">(</span><span class="n">sim</span><span class="p">,</span> <span class="n">ang</span><span class="p">,</span> <span class="n">algorithm</span><span class="o">=</span><span class="n">tomopy</span><span class="o">.</span><span class="n">astra</span><span class="p">,</span> <span class="n">options</span><span class="o">=</span><span class="n">options</span><span class="p">)</span>


<span class="c1"># Show results.</span>
<span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">12</span><span class="p">,</span><span class="mi">4</span><span class="p">))</span>
<span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">141</span><span class="p">);</span> <span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;Original&#39;</span><span class="p">);</span>
<span class="n">plt</span><span class="o">.</span><span class="n">imshow</span><span class="p">(</span><span class="n">obj</span><span class="o">.</span><span class="n">squeeze</span><span class="p">(),</span> <span class="n">cmap</span><span class="o">=</span><span class="s1">&#39;gray&#39;</span><span class="p">);</span> 
<span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">142</span><span class="p">);</span>  <span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;Sinogram&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">imshow</span><span class="p">(</span><span class="n">sim</span><span class="o">.</span><span class="n">squeeze</span><span class="p">(),</span> <span class="n">cmap</span><span class="o">=</span><span class="s1">&#39;gray&#39;</span><span class="p">);</span>
<span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">143</span><span class="p">);</span> <span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;FBP&#39;</span><span class="p">);</span>
<span class="n">plt</span><span class="o">.</span><span class="n">imshow</span><span class="p">(</span><span class="n">rec_fbp</span><span class="o">.</span><span class="n">squeeze</span><span class="p">(),</span> <span class="n">cmap</span><span class="o">=</span><span class="s1">&#39;gray&#39;</span><span class="p">);</span>
<span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">144</span><span class="p">);</span> <span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;SART&#39;</span><span class="p">);</span>
<span class="n">plt</span><span class="o">.</span><span class="n">imshow</span><span class="p">(</span><span class="n">rec_sart</span><span class="o">.</span><span class="n">squeeze</span><span class="p">(),</span> <span class="n">cmap</span><span class="o">=</span><span class="s1">&#39;gray&#39;</span><span class="p">);</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt"></div>


<div class="output_svg output_subarea ">
<?xml version="1.0" encoding="utf-8" standalone="no"?>

<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN"

  "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">

<!-- Created with matplotlib (https://matplotlib.org/) -->

<svg height="191.761467pt" version="1.1" viewBox="0 0 713.5875 191.761467" width="713.5875pt" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">

 <defs>

  <style type="text/css">

*{stroke-linecap:butt;stroke-linejoin:round;}

  </style>

 </defs>

 <g id="figure_1">

  <g id="patch_1">

   <path d="M 0 191.761467 

L 713.5875 191.761467 

L 713.5875 0 

L 0 0 

z

" style="fill:none;"/>

  </g>

  <g id="axes_1">

   <g id="patch_2">

    <path d="M 33.2875 167.883342 

L 178.852717 167.883342 

L 178.852717 22.318125 

L 33.2875 22.318125 

z

" style="fill:#ffffff;"/>

   </g>

   <g clip-path="url(#p8ff3dca968)">

    <image height="146" id="imagec4711b93f2" transform="scale(1 -1)translate(0 -146)" width="146" x="33.2875" xlink:href="data:image/png;base64,

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" y="-21.883342"/>

   </g>

   <g id="matplotlib.axis_1">

    <g id="xtick_1">

     <g id="line2d_1">

      <defs>

       <path d="M 0 0 

L 0 3.5 

" id="m03a7e2e9af" style="stroke:#000000;stroke-width:0.8;"/>

      </defs>

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.429654" xlink:href="#m03a7e2e9af" y="167.883342"/>

      </g>

     </g>

     <g id="text_1">

      <!-- 0 -->

      <defs>

       <path d="M 31.78125 66.40625 

Q 24.171875 66.40625 20.328125 58.90625 

Q 16.5 51.421875 16.5 36.375 

Q 16.5 21.390625 20.328125 13.890625 

Q 24.171875 6.390625 31.78125 6.390625 

Q 39.453125 6.390625 43.28125 13.890625 

Q 47.125 21.390625 47.125 36.375 

Q 47.125 51.421875 43.28125 58.90625 

Q 39.453125 66.40625 31.78125 66.40625 

z

M 31.78125 74.21875 

Q 44.046875 74.21875 50.515625 64.515625 

Q 56.984375 54.828125 56.984375 36.375 

Q 56.984375 17.96875 50.515625 8.265625 

Q 44.046875 -1.421875 31.78125 -1.421875 

Q 19.53125 -1.421875 13.0625 8.265625 

Q 6.59375 17.96875 6.59375 36.375 

Q 6.59375 54.828125 13.0625 64.515625 

Q 19.53125 74.21875 31.78125 74.21875 

z

" id="DejaVuSans-48"/>

      </defs>

      <g transform="translate(30.248404 182.48178)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_2">

     <g id="line2d_2">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="90.291067" xlink:href="#m03a7e2e9af" y="167.883342"/>

      </g>

     </g>

     <g id="text_2">

      <!-- 200 -->

      <defs>

       <path d="M 19.1875 8.296875 

L 53.609375 8.296875 

L 53.609375 0 

L 7.328125 0 

L 7.328125 8.296875 

Q 12.9375 14.109375 22.625 23.890625 

Q 32.328125 33.6875 34.8125 36.53125 

Q 39.546875 41.84375 41.421875 45.53125 

Q 43.3125 49.21875 43.3125 52.78125 

Q 43.3125 58.59375 39.234375 62.25 

Q 35.15625 65.921875 28.609375 65.921875 

Q 23.96875 65.921875 18.8125 64.3125 

Q 13.671875 62.703125 7.8125 59.421875 

L 7.8125 69.390625 

Q 13.765625 71.78125 18.9375 73 

Q 24.125 74.21875 28.421875 74.21875 

Q 39.75 74.21875 46.484375 68.546875 

Q 53.21875 62.890625 53.21875 53.421875 

Q 53.21875 48.921875 51.53125 44.890625 

Q 49.859375 40.875 45.40625 35.40625 

Q 44.1875 33.984375 37.640625 27.21875 

Q 31.109375 20.453125 19.1875 8.296875 

z

" id="DejaVuSans-50"/>

      </defs>

      <g transform="translate(80.747317 182.48178)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-50"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_3">

     <g id="line2d_3">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="147.15248" xlink:href="#m03a7e2e9af" y="167.883342"/>

      </g>

     </g>

     <g id="text_3">

      <!-- 400 -->

      <defs>

       <path d="M 37.796875 64.3125 

L 12.890625 25.390625 

L 37.796875 25.390625 

z

M 35.203125 72.90625 

L 47.609375 72.90625 

L 47.609375 25.390625 

L 58.015625 25.390625 

L 58.015625 17.1875 

L 47.609375 17.1875 

L 47.609375 0 

L 37.796875 0 

L 37.796875 17.1875 

L 4.890625 17.1875 

L 4.890625 26.703125 

z

" id="DejaVuSans-52"/>

      </defs>

      <g transform="translate(137.60873 182.48178)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-52"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

   </g>

   <g id="matplotlib.axis_2">

    <g id="ytick_1">

     <g id="line2d_4">

      <defs>

       <path d="M 0 0 

L -3.5 0 

" id="m4b2e90d108" style="stroke:#000000;stroke-width:0.8;"/>

      </defs>

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#m4b2e90d108" y="22.460279"/>

      </g>

     </g>

     <g id="text_4">

      <!-- 0 -->

      <g transform="translate(19.925 26.259497)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_2">

     <g id="line2d_5">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#m4b2e90d108" y="50.890985"/>

      </g>

     </g>

     <g id="text_5">

      <!-- 100 -->

      <defs>

       <path d="M 12.40625 8.296875 

L 28.515625 8.296875 

L 28.515625 63.921875 

L 10.984375 60.40625 

L 10.984375 69.390625 

L 28.421875 72.90625 

L 38.28125 72.90625 

L 38.28125 8.296875 

L 54.390625 8.296875 

L 54.390625 0 

L 12.40625 0 

z

" id="DejaVuSans-49"/>

      </defs>

      <g transform="translate(7.2 54.690204)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_3">

     <g id="line2d_6">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#m4b2e90d108" y="79.321692"/>

      </g>

     </g>

     <g id="text_6">

      <!-- 200 -->

      <g transform="translate(7.2 83.12091)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-50"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_4">

     <g id="line2d_7">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#m4b2e90d108" y="107.752398"/>

      </g>

     </g>

     <g id="text_7">

      <!-- 300 -->

      <defs>

       <path d="M 40.578125 39.3125 

Q 47.65625 37.796875 51.625 33 

Q 55.609375 28.21875 55.609375 21.1875 

Q 55.609375 10.40625 48.1875 4.484375 

Q 40.765625 -1.421875 27.09375 -1.421875 

Q 22.515625 -1.421875 17.65625 -0.515625 

Q 12.796875 0.390625 7.625 2.203125 

L 7.625 11.71875 

Q 11.71875 9.328125 16.59375 8.109375 

Q 21.484375 6.890625 26.8125 6.890625 

Q 36.078125 6.890625 40.9375 10.546875 

Q 45.796875 14.203125 45.796875 21.1875 

Q 45.796875 27.640625 41.28125 31.265625 

Q 36.765625 34.90625 28.71875 34.90625 

L 20.21875 34.90625 

L 20.21875 43.015625 

L 29.109375 43.015625 

Q 36.375 43.015625 40.234375 45.921875 

Q 44.09375 48.828125 44.09375 54.296875 

Q 44.09375 59.90625 40.109375 62.90625 

Q 36.140625 65.921875 28.71875 65.921875 

Q 24.65625 65.921875 20.015625 65.03125 

Q 15.375 64.15625 9.8125 62.3125 

L 9.8125 71.09375 

Q 15.4375 72.65625 20.34375 73.4375 

Q 25.25 74.21875 29.59375 74.21875 

Q 40.828125 74.21875 47.359375 69.109375 

Q 53.90625 64.015625 53.90625 55.328125 

Q 53.90625 49.265625 50.4375 45.09375 

Q 46.96875 40.921875 40.578125 39.3125 

z

" id="DejaVuSans-51"/>

      </defs>

      <g transform="translate(7.2 111.551617)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-51"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_5">

     <g id="line2d_8">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#m4b2e90d108" y="136.183105"/>

      </g>

     </g>

     <g id="text_8">

      <!-- 400 -->

      <g transform="translate(7.2 139.982323)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-52"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_6">

     <g id="line2d_9">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="33.2875" xlink:href="#m4b2e90d108" y="164.613811"/>

      </g>

     </g>

     <g id="text_9">

      <!-- 500 -->

      <defs>

       <path d="M 10.796875 72.90625 

L 49.515625 72.90625 

L 49.515625 64.59375 

L 19.828125 64.59375 

L 19.828125 46.734375 

Q 21.96875 47.46875 24.109375 47.828125 

Q 26.265625 48.1875 28.421875 48.1875 

Q 40.625 48.1875 47.75 41.5 

Q 54.890625 34.8125 54.890625 23.390625 

Q 54.890625 11.625 47.5625 5.09375 

Q 40.234375 -1.421875 26.90625 -1.421875 

Q 22.3125 -1.421875 17.546875 -0.640625 

Q 12.796875 0.140625 7.71875 1.703125 

L 7.71875 11.625 

Q 12.109375 9.234375 16.796875 8.0625 

Q 21.484375 6.890625 26.703125 6.890625 

Q 35.15625 6.890625 40.078125 11.328125 

Q 45.015625 15.765625 45.015625 23.390625 

Q 45.015625 31 40.078125 35.4375 

Q 35.15625 39.890625 26.703125 39.890625 

Q 22.75 39.890625 18.8125 39.015625 

Q 14.890625 38.140625 10.796875 36.28125 

z

" id="DejaVuSans-53"/>

      </defs>

      <g transform="translate(7.2 168.41303)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-53"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

   </g>

   <g id="patch_3">

    <path d="M 33.2875 167.883342 

L 33.2875 22.318125 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_4">

    <path d="M 178.852717 167.883342 

L 178.852717 22.318125 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_5">

    <path d="M 33.2875 167.883342 

L 178.852717 167.883342 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_6">

    <path d="M 33.2875 22.318125 

L 178.852717 22.318125 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="text_10">

    <!-- Original -->

    <defs>

     <path d="M 39.40625 66.21875 

Q 28.65625 66.21875 22.328125 58.203125 

Q 16.015625 50.203125 16.015625 36.375 

Q 16.015625 22.609375 22.328125 14.59375 

Q 28.65625 6.59375 39.40625 6.59375 

Q 50.140625 6.59375 56.421875 14.59375 

Q 62.703125 22.609375 62.703125 36.375 

Q 62.703125 50.203125 56.421875 58.203125 

Q 50.140625 66.21875 39.40625 66.21875 

z

M 39.40625 74.21875 

Q 54.734375 74.21875 63.90625 63.9375 

Q 73.09375 53.65625 73.09375 36.375 

Q 73.09375 19.140625 63.90625 8.859375 

Q 54.734375 -1.421875 39.40625 -1.421875 

Q 24.03125 -1.421875 14.8125 8.828125 

Q 5.609375 19.09375 5.609375 36.375 

Q 5.609375 53.65625 14.8125 63.9375 

Q 24.03125 74.21875 39.40625 74.21875 

z

" id="DejaVuSans-79"/>

     <path d="M 41.109375 46.296875 

Q 39.59375 47.171875 37.8125 47.578125 

Q 36.03125 48 33.890625 48 

Q 26.265625 48 22.1875 43.046875 

Q 18.109375 38.09375 18.109375 28.8125 

L 18.109375 0 

L 9.078125 0 

L 9.078125 54.6875 

L 18.109375 54.6875 

L 18.109375 46.1875 

Q 20.953125 51.171875 25.484375 53.578125 

Q 30.03125 56 36.53125 56 

Q 37.453125 56 38.578125 55.875 

Q 39.703125 55.765625 41.0625 55.515625 

z

" id="DejaVuSans-114"/>

     <path d="M 9.421875 54.6875 

L 18.40625 54.6875 

L 18.40625 0 

L 9.421875 0 

z

M 9.421875 75.984375 

L 18.40625 75.984375 

L 18.40625 64.59375 

L 9.421875 64.59375 

z

" id="DejaVuSans-105"/>

     <path d="M 45.40625 27.984375 

Q 45.40625 37.75 41.375 43.109375 

Q 37.359375 48.484375 30.078125 48.484375 

Q 22.859375 48.484375 18.828125 43.109375 

Q 14.796875 37.75 14.796875 27.984375 

Q 14.796875 18.265625 18.828125 12.890625 

Q 22.859375 7.515625 30.078125 7.515625 

Q 37.359375 7.515625 41.375 12.890625 

Q 45.40625 18.265625 45.40625 27.984375 

z

M 54.390625 6.78125 

Q 54.390625 -7.171875 48.1875 -13.984375 

Q 42 -20.796875 29.203125 -20.796875 

Q 24.46875 -20.796875 20.265625 -20.09375 

Q 16.0625 -19.390625 12.109375 -17.921875 

L 12.109375 -9.1875 

Q 16.0625 -11.328125 19.921875 -12.34375 

Q 23.78125 -13.375 27.78125 -13.375 

Q 36.625 -13.375 41.015625 -8.765625 

Q 45.40625 -4.15625 45.40625 5.171875 

L 45.40625 9.625 

Q 42.625 4.78125 38.28125 2.390625 

Q 33.9375 0 27.875 0 

Q 17.828125 0 11.671875 7.65625 

Q 5.515625 15.328125 5.515625 27.984375 

Q 5.515625 40.671875 11.671875 48.328125 

Q 17.828125 56 27.875 56 

Q 33.9375 56 38.28125 53.609375 

Q 42.625 51.21875 45.40625 46.390625 

L 45.40625 54.6875 

L 54.390625 54.6875 

z

" id="DejaVuSans-103"/>

     <path d="M 54.890625 33.015625 

L 54.890625 0 

L 45.90625 0 

L 45.90625 32.71875 

Q 45.90625 40.484375 42.875 44.328125 

Q 39.84375 48.1875 33.796875 48.1875 

Q 26.515625 48.1875 22.3125 43.546875 

Q 18.109375 38.921875 18.109375 30.90625 

L 18.109375 0 

L 9.078125 0 

L 9.078125 54.6875 

L 18.109375 54.6875 

L 18.109375 46.1875 

Q 21.34375 51.125 25.703125 53.5625 

Q 30.078125 56 35.796875 56 

Q 45.21875 56 50.046875 50.171875 

Q 54.890625 44.34375 54.890625 33.015625 

z

" id="DejaVuSans-110"/>

     <path d="M 34.28125 27.484375 

Q 23.390625 27.484375 19.1875 25 

Q 14.984375 22.515625 14.984375 16.5 

Q 14.984375 11.71875 18.140625 8.90625 

Q 21.296875 6.109375 26.703125 6.109375 

Q 34.1875 6.109375 38.703125 11.40625 

Q 43.21875 16.703125 43.21875 25.484375 

L 43.21875 27.484375 

z

M 52.203125 31.203125 

L 52.203125 0 

L 43.21875 0 

L 43.21875 8.296875 

Q 40.140625 3.328125 35.546875 0.953125 

Q 30.953125 -1.421875 24.3125 -1.421875 

Q 15.921875 -1.421875 10.953125 3.296875 

Q 6 8.015625 6 15.921875 

Q 6 25.140625 12.171875 29.828125 

Q 18.359375 34.515625 30.609375 34.515625 

L 43.21875 34.515625 

L 43.21875 35.40625 

Q 43.21875 41.609375 39.140625 45 

Q 35.0625 48.390625 27.6875 48.390625 

Q 23 48.390625 18.546875 47.265625 

Q 14.109375 46.140625 10.015625 43.890625 

L 10.015625 52.203125 

Q 14.9375 54.109375 19.578125 55.046875 

Q 24.21875 56 28.609375 56 

Q 40.484375 56 46.34375 49.84375 

Q 52.203125 43.703125 52.203125 31.203125 

z

" id="DejaVuSans-97"/>

     <path d="M 9.421875 75.984375 

L 18.40625 75.984375 

L 18.40625 0 

L 9.421875 0 

z

" id="DejaVuSans-108"/>

    </defs>

    <g transform="translate(82.591359 16.318125)scale(0.12 -0.12)">

     <use xlink:href="#DejaVuSans-79"/>

     <use x="78.710938" xlink:href="#DejaVuSans-114"/>

     <use x="119.824219" xlink:href="#DejaVuSans-105"/>

     <use x="147.607422" xlink:href="#DejaVuSans-103"/>

     <use x="211.083984" xlink:href="#DejaVuSans-105"/>

     <use x="238.867188" xlink:href="#DejaVuSans-110"/>

     <use x="302.246094" xlink:href="#DejaVuSans-97"/>

     <use x="363.525391" xlink:href="#DejaVuSans-108"/>

    </g>

   </g>

  </g>

  <g id="axes_2">

   <g id="patch_7">

    <path d="M 207.965761 113.096434 

L 353.530978 113.096434 

L 353.530978 77.105034 

L 207.965761 77.105034 

z

" style="fill:#ffffff;"/>

   </g>

   <g clip-path="url(#p45d2a0dba5)">

    <image height="36" id="image6ef0b3372e" transform="scale(1 -1)translate(0 -36)" width="146" x="207.965761" xlink:href="data:image/png;base64,

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" y="-77.096434"/>

   </g>

   <g id="matplotlib.axis_3">

    <g id="xtick_4">

     <g id="line2d_10">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="208.065737" xlink:href="#m03a7e2e9af" y="113.096434"/>

      </g>

     </g>

     <g id="text_11">

      <!-- 0 -->

      <g transform="translate(204.884487 127.694871)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_5">

     <g id="line2d_11">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="248.056181" xlink:href="#m03a7e2e9af" y="113.096434"/>

      </g>

     </g>

     <g id="text_12">

      <!-- 200 -->

      <g transform="translate(238.512431 127.694871)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-50"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_6">

     <g id="line2d_12">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="288.046626" xlink:href="#m03a7e2e9af" y="113.096434"/>

      </g>

     </g>

     <g id="text_13">

      <!-- 400 -->

      <g transform="translate(278.502876 127.694871)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-52"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_7">

     <g id="line2d_13">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="328.03707" xlink:href="#m03a7e2e9af" y="113.096434"/>

      </g>

     </g>

     <g id="text_14">

      <!-- 600 -->

      <defs>

       <path d="M 33.015625 40.375 

Q 26.375 40.375 22.484375 35.828125 

Q 18.609375 31.296875 18.609375 23.390625 

Q 18.609375 15.53125 22.484375 10.953125 

Q 26.375 6.390625 33.015625 6.390625 

Q 39.65625 6.390625 43.53125 10.953125 

Q 47.40625 15.53125 47.40625 23.390625 

Q 47.40625 31.296875 43.53125 35.828125 

Q 39.65625 40.375 33.015625 40.375 

z

M 52.59375 71.296875 

L 52.59375 62.3125 

Q 48.875 64.0625 45.09375 64.984375 

Q 41.3125 65.921875 37.59375 65.921875 

Q 27.828125 65.921875 22.671875 59.328125 

Q 17.53125 52.734375 16.796875 39.40625 

Q 19.671875 43.65625 24.015625 45.921875 

Q 28.375 48.1875 33.59375 48.1875 

Q 44.578125 48.1875 50.953125 41.515625 

Q 57.328125 34.859375 57.328125 23.390625 

Q 57.328125 12.15625 50.6875 5.359375 

Q 44.046875 -1.421875 33.015625 -1.421875 

Q 20.359375 -1.421875 13.671875 8.265625 

Q 6.984375 17.96875 6.984375 36.375 

Q 6.984375 53.65625 15.1875 63.9375 

Q 23.390625 74.21875 37.203125 74.21875 

Q 40.921875 74.21875 44.703125 73.484375 

Q 48.484375 72.75 52.59375 71.296875 

z

" id="DejaVuSans-54"/>

      </defs>

      <g transform="translate(318.49332 127.694871)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-54"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

   </g>

   <g id="matplotlib.axis_4">

    <g id="ytick_7">

     <g id="line2d_14">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="207.965761" xlink:href="#m4b2e90d108" y="77.20501"/>

      </g>

     </g>

     <g id="text_15">

      <!-- 0 -->

      <g transform="translate(194.603261 81.004229)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_8">

     <g id="line2d_15">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="207.965761" xlink:href="#m4b2e90d108" y="97.200232"/>

      </g>

     </g>

     <g id="text_16">

      <!-- 100 -->

      <g transform="translate(181.878261 100.999451)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-49"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

   </g>

   <g id="patch_8">

    <path d="M 207.965761 113.096434 

L 207.965761 77.105034 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_9">

    <path d="M 353.530978 113.096434 

L 353.530978 77.105034 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_10">

    <path d="M 207.965761 113.096434 

L 353.530978 113.096434 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_11">

    <path d="M 207.965761 77.105034 

L 353.530978 77.105034 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="text_17">

    <!-- Sinogram -->

    <defs>

     <path d="M 53.515625 70.515625 

L 53.515625 60.890625 

Q 47.90625 63.578125 42.921875 64.890625 

Q 37.9375 66.21875 33.296875 66.21875 

Q 25.25 66.21875 20.875 63.09375 

Q 16.5 59.96875 16.5 54.203125 

Q 16.5 49.359375 19.40625 46.890625 

Q 22.3125 44.4375 30.421875 42.921875 

L 36.375 41.703125 

Q 47.40625 39.59375 52.65625 34.296875 

Q 57.90625 29 57.90625 20.125 

Q 57.90625 9.515625 50.796875 4.046875 

Q 43.703125 -1.421875 29.984375 -1.421875 

Q 24.8125 -1.421875 18.96875 -0.25 

Q 13.140625 0.921875 6.890625 3.21875 

L 6.890625 13.375 

Q 12.890625 10.015625 18.65625 8.296875 

Q 24.421875 6.59375 29.984375 6.59375 

Q 38.421875 6.59375 43.015625 9.90625 

Q 47.609375 13.234375 47.609375 19.390625 

Q 47.609375 24.75 44.3125 27.78125 

Q 41.015625 30.8125 33.5 32.328125 

L 27.484375 33.5 

Q 16.453125 35.6875 11.515625 40.375 

Q 6.59375 45.0625 6.59375 53.421875 

Q 6.59375 63.09375 13.40625 68.65625 

Q 20.21875 74.21875 32.171875 74.21875 

Q 37.3125 74.21875 42.625 73.28125 

Q 47.953125 72.359375 53.515625 70.515625 

z

" id="DejaVuSans-83"/>

     <path d="M 30.609375 48.390625 

Q 23.390625 48.390625 19.1875 42.75 

Q 14.984375 37.109375 14.984375 27.296875 

Q 14.984375 17.484375 19.15625 11.84375 

Q 23.34375 6.203125 30.609375 6.203125 

Q 37.796875 6.203125 41.984375 11.859375 

Q 46.1875 17.53125 46.1875 27.296875 

Q 46.1875 37.015625 41.984375 42.703125 

Q 37.796875 48.390625 30.609375 48.390625 

z

M 30.609375 56 

Q 42.328125 56 49.015625 48.375 

Q 55.71875 40.765625 55.71875 27.296875 

Q 55.71875 13.875 49.015625 6.21875 

Q 42.328125 -1.421875 30.609375 -1.421875 

Q 18.84375 -1.421875 12.171875 6.21875 

Q 5.515625 13.875 5.515625 27.296875 

Q 5.515625 40.765625 12.171875 48.375 

Q 18.84375 56 30.609375 56 

z

" id="DejaVuSans-111"/>

     <path d="M 52 44.1875 

Q 55.375 50.25 60.0625 53.125 

Q 64.75 56 71.09375 56 

Q 79.640625 56 84.28125 50.015625 

Q 88.921875 44.046875 88.921875 33.015625 

L 88.921875 0 

L 79.890625 0 

L 79.890625 32.71875 

Q 79.890625 40.578125 77.09375 44.375 

Q 74.3125 48.1875 68.609375 48.1875 

Q 61.625 48.1875 57.5625 43.546875 

Q 53.515625 38.921875 53.515625 30.90625 

L 53.515625 0 

L 44.484375 0 

L 44.484375 32.71875 

Q 44.484375 40.625 41.703125 44.40625 

Q 38.921875 48.1875 33.109375 48.1875 

Q 26.21875 48.1875 22.15625 43.53125 

Q 18.109375 38.875 18.109375 30.90625 

L 18.109375 0 

L 9.078125 0 

L 9.078125 54.6875 

L 18.109375 54.6875 

L 18.109375 46.1875 

Q 21.1875 51.21875 25.484375 53.609375 

Q 29.78125 56 35.6875 56 

Q 41.65625 56 45.828125 52.96875 

Q 50 49.953125 52 44.1875 

z

" id="DejaVuSans-109"/>

    </defs>

    <g transform="translate(252.001807 71.105034)scale(0.12 -0.12)">

     <use xlink:href="#DejaVuSans-83"/>

     <use x="63.476562" xlink:href="#DejaVuSans-105"/>

     <use x="91.259766" xlink:href="#DejaVuSans-110"/>

     <use x="154.638672" xlink:href="#DejaVuSans-111"/>

     <use x="215.820312" xlink:href="#DejaVuSans-103"/>

     <use x="279.296875" xlink:href="#DejaVuSans-114"/>

     <use x="320.410156" xlink:href="#DejaVuSans-97"/>

     <use x="381.689453" xlink:href="#DejaVuSans-109"/>

    </g>

   </g>

  </g>

  <g id="axes_3">

   <g id="patch_12">

    <path d="M 382.644022 167.883342 

L 528.209239 167.883342 

L 528.209239 22.318125 

L 382.644022 22.318125 

z

" style="fill:#ffffff;"/>

   </g>

   <g clip-path="url(#pfcafcdf142)">

    <image height="146" id="image000e75056c" transform="scale(1 -1)translate(0 -146)" width="146" x="382.644022" xlink:href="data:image/png;base64,

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" y="-21.883342"/>

   </g>

   <g id="matplotlib.axis_5">

    <g id="xtick_8">

     <g id="line2d_16">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="382.743998" xlink:href="#m03a7e2e9af" y="167.883342"/>

      </g>

     </g>

     <g id="text_18">

      <!-- 0 -->

      <g transform="translate(379.562748 182.48178)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_9">

     <g id="line2d_17">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="422.734442" xlink:href="#m03a7e2e9af" y="167.883342"/>

      </g>

     </g>

     <g id="text_19">

      <!-- 200 -->

      <g transform="translate(413.190692 182.48178)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-50"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_10">

     <g id="line2d_18">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="462.724887" xlink:href="#m03a7e2e9af" y="167.883342"/>

      </g>

     </g>

     <g id="text_20">

      <!-- 400 -->

      <g transform="translate(453.181137 182.48178)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-52"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_11">

     <g id="line2d_19">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="502.715331" xlink:href="#m03a7e2e9af" y="167.883342"/>

      </g>

     </g>

     <g id="text_21">

      <!-- 600 -->

      <g transform="translate(493.171581 182.48178)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-54"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

   </g>

   <g id="matplotlib.axis_6">

    <g id="ytick_9">

     <g id="line2d_20">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="382.644022" xlink:href="#m4b2e90d108" y="22.418101"/>

      </g>

     </g>

     <g id="text_22">

      <!-- 0 -->

      <g transform="translate(369.281522 26.21732)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_10">

     <g id="line2d_21">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="382.644022" xlink:href="#m4b2e90d108" y="62.408545"/>

      </g>

     </g>

     <g id="text_23">

      <!-- 200 -->

      <g transform="translate(356.556522 66.207764)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-50"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_11">

     <g id="line2d_22">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="382.644022" xlink:href="#m4b2e90d108" y="102.39899"/>

      </g>

     </g>

     <g id="text_24">

      <!-- 400 -->

      <g transform="translate(356.556522 106.198209)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-52"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_12">

     <g id="line2d_23">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="382.644022" xlink:href="#m4b2e90d108" y="142.389434"/>

      </g>

     </g>

     <g id="text_25">

      <!-- 600 -->

      <g transform="translate(356.556522 146.188653)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-54"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

   </g>

   <g id="patch_13">

    <path d="M 382.644022 167.883342 

L 382.644022 22.318125 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_14">

    <path d="M 528.209239 167.883342 

L 528.209239 22.318125 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_15">

    <path d="M 382.644022 167.883342 

L 528.209239 167.883342 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_16">

    <path d="M 382.644022 22.318125 

L 528.209239 22.318125 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="text_26">

    <!-- FBP -->

    <defs>

     <path d="M 9.8125 72.90625 

L 51.703125 72.90625 

L 51.703125 64.59375 

L 19.671875 64.59375 

L 19.671875 43.109375 

L 48.578125 43.109375 

L 48.578125 34.8125 

L 19.671875 34.8125 

L 19.671875 0 

L 9.8125 0 

z

" id="DejaVuSans-70"/>

     <path d="M 19.671875 34.8125 

L 19.671875 8.109375 

L 35.5 8.109375 

Q 43.453125 8.109375 47.28125 11.40625 

Q 51.125 14.703125 51.125 21.484375 

Q 51.125 28.328125 47.28125 31.5625 

Q 43.453125 34.8125 35.5 34.8125 

z

M 19.671875 64.796875 

L 19.671875 42.828125 

L 34.28125 42.828125 

Q 41.5 42.828125 45.03125 45.53125 

Q 48.578125 48.25 48.578125 53.8125 

Q 48.578125 59.328125 45.03125 62.0625 

Q 41.5 64.796875 34.28125 64.796875 

z

M 9.8125 72.90625 

L 35.015625 72.90625 

Q 46.296875 72.90625 52.390625 68.21875 

Q 58.5 63.53125 58.5 54.890625 

Q 58.5 48.1875 55.375 44.234375 

Q 52.25 40.28125 46.1875 39.3125 

Q 53.46875 37.75 57.5 32.78125 

Q 61.53125 27.828125 61.53125 20.40625 

Q 61.53125 10.640625 54.890625 5.3125 

Q 48.25 0 35.984375 0 

L 9.8125 0 

z

" id="DejaVuSans-66"/>

     <path d="M 19.671875 64.796875 

L 19.671875 37.40625 

L 32.078125 37.40625 

Q 38.96875 37.40625 42.71875 40.96875 

Q 46.484375 44.53125 46.484375 51.125 

Q 46.484375 57.671875 42.71875 61.234375 

Q 38.96875 64.796875 32.078125 64.796875 

z

M 9.8125 72.90625 

L 32.078125 72.90625 

Q 44.34375 72.90625 50.609375 67.359375 

Q 56.890625 61.8125 56.890625 51.125 

Q 56.890625 40.328125 50.609375 34.8125 

Q 44.34375 29.296875 32.078125 29.296875 

L 19.671875 29.296875 

L 19.671875 0 

L 9.8125 0 

z

" id="DejaVuSans-80"/>

    </defs>

    <g transform="translate(444.241318 16.318125)scale(0.12 -0.12)">

     <use xlink:href="#DejaVuSans-70"/>

     <use x="57.519531" xlink:href="#DejaVuSans-66"/>

     <use x="126.123047" xlink:href="#DejaVuSans-80"/>

    </g>

   </g>

  </g>

  <g id="axes_4">

   <g id="patch_17">

    <path d="M 557.322283 167.883342 

L 702.8875 167.883342 

L 702.8875 22.318125 

L 557.322283 22.318125 

z

" style="fill:#ffffff;"/>

   </g>

   <g clip-path="url(#p0a8bcd5d6e)">

    <image height="146" id="image072a50cca7" transform="scale(1 -1)translate(0 -146)" width="146" x="557.322283" xlink:href="data:image/png;base64,

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" y="-21.883342"/>

   </g>

   <g id="matplotlib.axis_7">

    <g id="xtick_12">

     <g id="line2d_24">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="557.422259" xlink:href="#m03a7e2e9af" y="167.883342"/>

      </g>

     </g>

     <g id="text_27">

      <!-- 0 -->

      <g transform="translate(554.241009 182.48178)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_13">

     <g id="line2d_25">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="597.412703" xlink:href="#m03a7e2e9af" y="167.883342"/>

      </g>

     </g>

     <g id="text_28">

      <!-- 200 -->

      <g transform="translate(587.868953 182.48178)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-50"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_14">

     <g id="line2d_26">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="637.403147" xlink:href="#m03a7e2e9af" y="167.883342"/>

      </g>

     </g>

     <g id="text_29">

      <!-- 400 -->

      <g transform="translate(627.859397 182.48178)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-52"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="xtick_15">

     <g id="line2d_27">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="677.393592" xlink:href="#m03a7e2e9af" y="167.883342"/>

      </g>

     </g>

     <g id="text_30">

      <!-- 600 -->

      <g transform="translate(667.849842 182.48178)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-54"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

   </g>

   <g id="matplotlib.axis_8">

    <g id="ytick_13">

     <g id="line2d_28">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="557.322283" xlink:href="#m4b2e90d108" y="22.418101"/>

      </g>

     </g>

     <g id="text_31">

      <!-- 0 -->

      <g transform="translate(543.959783 26.21732)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_14">

     <g id="line2d_29">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="557.322283" xlink:href="#m4b2e90d108" y="62.408545"/>

      </g>

     </g>

     <g id="text_32">

      <!-- 200 -->

      <g transform="translate(531.234783 66.207764)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-50"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_15">

     <g id="line2d_30">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="557.322283" xlink:href="#m4b2e90d108" y="102.39899"/>

      </g>

     </g>

     <g id="text_33">

      <!-- 400 -->

      <g transform="translate(531.234783 106.198209)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-52"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

    <g id="ytick_16">

     <g id="line2d_31">

      <g>

       <use style="stroke:#000000;stroke-width:0.8;" x="557.322283" xlink:href="#m4b2e90d108" y="142.389434"/>

      </g>

     </g>

     <g id="text_34">

      <!-- 600 -->

      <g transform="translate(531.234783 146.188653)scale(0.1 -0.1)">

       <use xlink:href="#DejaVuSans-54"/>

       <use x="63.623047" xlink:href="#DejaVuSans-48"/>

       <use x="127.246094" xlink:href="#DejaVuSans-48"/>

      </g>

     </g>

    </g>

   </g>

   <g id="patch_18">

    <path d="M 557.322283 167.883342 

L 557.322283 22.318125 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_19">

    <path d="M 702.8875 167.883342 

L 702.8875 22.318125 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_20">

    <path d="M 557.322283 167.883342 

L 702.8875 167.883342 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="patch_21">

    <path d="M 557.322283 22.318125 

L 702.8875 22.318125 

" style="fill:none;stroke:#000000;stroke-linecap:square;stroke-linejoin:miter;stroke-width:0.8;"/>

   </g>

   <g id="text_35">

    <!-- SART -->

    <defs>

     <path d="M 34.1875 63.1875 

L 20.796875 26.90625 

L 47.609375 26.90625 

z

M 28.609375 72.90625 

L 39.796875 72.90625 

L 67.578125 0 

L 57.328125 0 

L 50.6875 18.703125 

L 17.828125 18.703125 

L 11.1875 0 

L 0.78125 0 

z

" id="DejaVuSans-65"/>

     <path d="M 44.390625 34.1875 

Q 47.5625 33.109375 50.5625 29.59375 

Q 53.5625 26.078125 56.59375 19.921875 

L 66.609375 0 

L 56 0 

L 46.6875 18.703125 

Q 43.0625 26.03125 39.671875 28.421875 

Q 36.28125 30.8125 30.421875 30.8125 

L 19.671875 30.8125 

L 19.671875 0 

L 9.8125 0 

L 9.8125 72.90625 

L 32.078125 72.90625 

Q 44.578125 72.90625 50.734375 67.671875 

Q 56.890625 62.453125 56.890625 51.90625 

Q 56.890625 45.015625 53.6875 40.46875 

Q 50.484375 35.9375 44.390625 34.1875 

z

M 19.671875 64.796875 

L 19.671875 38.921875 

L 32.078125 38.921875 

Q 39.203125 38.921875 42.84375 42.21875 

Q 46.484375 45.515625 46.484375 51.90625 

Q 46.484375 58.296875 42.84375 61.546875 

Q 39.203125 64.796875 32.078125 64.796875 

z

" id="DejaVuSans-82"/>

     <path d="M -0.296875 72.90625 

L 61.375 72.90625 

L 61.375 64.59375 

L 35.5 64.59375 

L 35.5 0 

L 25.59375 0 

L 25.59375 64.59375 

L -0.296875 64.59375 

z

" id="DejaVuSans-84"/>

    </defs>

    <g transform="translate(614.363329 16.318125)scale(0.12 -0.12)">

     <use xlink:href="#DejaVuSans-83"/>

     <use x="63.492188" xlink:href="#DejaVuSans-65"/>

     <use x="131.900391" xlink:href="#DejaVuSans-82"/>

     <use x="201.273438" xlink:href="#DejaVuSans-84"/>

    </g>

   </g>

  </g>

 </g>

 <defs>

  <clipPath id="p8ff3dca968">

   <rect height="145.565217" width="145.565217" x="33.2875" y="22.318125"/>

  </clipPath>

  <clipPath id="p45d2a0dba5">

   <rect height="35.9914" width="145.565217" x="207.965761" y="77.105034"/>

  </clipPath>

  <clipPath id="pfcafcdf142">

   <rect height="145.565217" width="145.565217" x="382.644022" y="22.318125"/>

  </clipPath>

  <clipPath id="p0a8bcd5d6e">

   <rect height="145.565217" width="145.565217" x="557.322283" y="22.318125"/>

  </clipPath>

 </defs>

</svg>


</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="-Reconstruction-Methods-"><center> Reconstruction Methods </center><a class="anchor-link" href="#-Reconstruction-Methods-">&#182;</a></h3><p><img src='methods.png'></p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<ul>
<li><strong>Analytical</strong>: BP, BPF, FBP</li>
</ul>
<p>Reference: <a href="http://file.scirp.org/Html/13-9101545_27659.htm">Asl, Mahsa Noori, and Alireza Sadremomtaz. "Analytical image reconstruction methods in emission tomography." Journal of Biomedical Science and Engineering 6.01 (2013): 100.</a></p>
<ul>
<li><strong>Algebraic</strong></li>
</ul>
<p>The algebraic reconstruction technique (ART) is a class of iterative algorithms used in computed tomography.
ART can be considered as an iterative solver of a system of linear equations $ A x = b $. The values of the pixels are considered as variables collected in a vector $ x $, and the image process is described by a matrix $ A $. The measured angular projections are collected in a vector $ b $. Given a real or complex  $m \times n $
matrix 
$ A $
and a real or complex vector 
$ b $
respectively, the method computes an approximation of the solution of the linear 
systems of equations as in the following formula,</p>
$$
  x^{k+1} 
  = 
  x^{k} 
  + 
  \lambda_k 
  \frac{b_{i} - \langle a_{i}, x^{k} \rangle}{\lVert a_{i} \rVert^2} a_{i}^{T}
$$<p>where 
$ i = k \, \bmod \, m + 1 $,
$ a_i$ 
is the $i$-th row of the matrix 
$ A $, 
$ b_i $
is the $i$-th component of the vector
$ b $, 
and
$ \lambda_k $
is a relaxation parameter. The above formulae gives a simple iteration routine.</p>
<p>An advantage of ART over other reconstruction methods (such as FBP) is that it is relatively easy to incorporate prior knowledge into the reconstruction process.</p>
<p>See, <a href="http://itas2012.iitp.ru/pdf/1569605161.pdf"><em>e.g.</em></a></p>
<ul>
<li><strong>Statistical</strong></li>
</ul>

</div>
</div>
</div>
    </div>
  </div>
</body>

 


</html>
