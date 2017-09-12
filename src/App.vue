<template>
  <div class="site">
    <header class="site-header">
      Mentor Me.
    </header>
    <article class="site-body">
      <router-view></router-view>
    </article>
    <footer class="site-footer">
      <address class="copyright">
        &copy; 2017. MentorMe Allright Reserved.
      </address>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'app'
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css?family=Pacifico');
@import 'init';

$footer-height: $space-unit * 4;

.site {
  font-family: sans-serif;
  text-align: center;
  color: $color-text;
  font-size: $space-unit;
}

.site-header {
  background-color: $color-background;
  color: $color-brand;
  font-family: 'Pacifico', cursive;
  font-size: ($space-unit * 2);
  line-height: $space-unit * 8;
}

.site-body {
  margin: 0 auto;
  padding: $space-unit $space-unit ($space-unit + $footer-height);
  max-width: $space-unit * 30;
}

.site-footer {
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  color: $color-text-light;
  line-height: $footer-height;
}
</style>
