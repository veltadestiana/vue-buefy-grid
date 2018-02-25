<template>
  <div id="app">
    <main-content></main-content>
  </div>
</template>

<script>
import { MainContent, InfoBar } from 'components/layout/'

export default {
  components: {
    'main-content': MainContent,
    'info-bar': InfoBar
  }
}
</script>

<style lang="scss">
@import '~animate.css';
.animated {
  animation-duration: .377s;
}

// Import Bulma's core
@import "~bulma/sass/utilities/_all";

// Set your colors
$primary: #8c67ef;
$primary-invert: findColorInvert($primary);

// Setup $colors to use as bulma classes (e.g. 'is-twitter')
$colors: (
    "white": ($white, $black),
    "black": ($black, $white),
    "light": ($light, $light-invert),
    "dark": ($dark, $dark-invert),
    "primary": ($primary, $primary-invert),
    "info": ($info, $info-invert),
    "success": ($success, $success-invert),
    "warning": ($warning, $warning-invert),
    "danger": ($danger, $danger-invert)
);

// Links
$link: $primary;
$link-invert: $primary-invert;
$link-focus-border: $primary;

// Import Bulma and Buefy styles
@import "~bulma";
@import "~buefy/src/scss/buefy";

$fa-font-path: '~font-awesome/fonts/';
@import '~font-awesome/scss/font-awesome';

// Global custom style
.has-shadow {
     box-shadow: 0 2px 3px hsla(0,0%,4%,.1);
}
 .title {
     margin: 20px;
}
 .title-site {
     color: white;
     margin-top: 20px;
}
 .container {
     margin-top: -35px;
}
 .image {
     height:60px;
     width:100%;
}
 .card {
     margin: 0 20px 20px 15px;
}
 .card:hover {
     top: -2px;
     box-shadow: 0 4px 5px rgba(0,0,0,0.2);
}
 .is-grouped {
     margin-left: 0 30px 0 30px;
     display: flex;
     justify-content: center;
}
 .search-box input {
     border-radius: 20px;
}
 figure {
     position: relative;
     padding: 50px;
     margin: 5px auto;
}
.list-tags {
     display: inline-flex;
     text-align: center;
     justify-content: center;
}
 .ribbon {
     width: 150px;
     height: 150px;
     overflow: hidden;
     position: absolute;
     opacity: 0.95;
}
 .ribbon::before, .ribbon::after {
     position: absolute;
     z-index: -1;
     content: '';
     display: block;
     border: 5px solid #2980b9;
}
 .ribbon span {
     position: absolute;
     display: block;
     width: 225px;
     padding: 15px 0;
     background-color: #3498db;
     color: #fff;
     font: 600 18px/1 'Open Sans', sans-serif;
     text-transform: uppercase;
     text-align: center;
}
 .ribbon-top-right {
     top: -10px;
     right: -10px;
}
 .ribbon-top-right::before, .ribbon-top-right::after {
     border-top-color: transparent;
     border-right-color: transparent;
}
 .ribbon-top-right::before {
     top: 0;
     left: 0;
}
 .ribbon-top-right::after {
     bottom: 0;
     right: 0;
}
 .ribbon-top-right span {
     left: -25px;
     top: 30px;
     transform: rotate(45deg);
}
 *, *:active, *:focus{
     outline: none;
}
.button-detail {
  margin-top: 0;
  border-radius: 0;
  letter-spacing: 0.7px;
}
 .searchbox{
     position: relative;
     height: 40px;
     width: 60%;
     margin: 50px auto;
     overflow: hidden;
     border-bottom: 2px solid #fff;
     background: none;
     color: #fff;
     transition: all 0.4s cubic-bezier(.25, .8, .25, 1);
     &--active{
         color: #000;
    }
     &:after{
         position: absolute;
         content: "";
         z-index: 1;
         width: 100%;
         height: 100%;
         top: 20px;
         left: 0px;
         transform: rotateX(90deg);
         background: #fff;
         transition: all 0.4s cubic-bezier(.25, .8, .25, 1);
    }
     &--active:after{
         top: 0px;
         left: 0px;
         transform: rotateX(0deg);
    }
     input {
         z-index: 1;
         height: 100%;
         width: 100%;
         border: none;
         font-size: 1em;
         color: inherit;
         background: none;
    }
     ::placeholder {
         color: white;
    }
     button{
         position: absolute;
         z-index: 1;
         right: 0px;
         top: 0px;
         height: 100%;
         border: none;
         background: none;
         font-size: 1.4em;
         color: inherit;
    }
}

</style>
