<template>
<div class="home">
  <div class="search">
    <input class="search-input" v-model="query" placeholder="메세지를 입력하세요." />
    <Mentors :data={getMentors} />
  </div>
</div>
</template>

<script>
import Mentors from './Mentors'

export default {
  name: 'home',
  components: {
    Mentors
  },
  data () {
    return {
      query: ''
    }
  },
  computed: {
    getMentors: function () {
      this.$http
        .get(`/mentor_request/?query=${this.query}`, {
          withCredentials: false
        })
        .then(result => {
          return result
        })
    }
  }
}
</script>

<style scoped lang="scss">
@import 'init';

.search {

}
.search-input {
  @extend %form-init;
  @include transition(color, border-color);

  border-bottom-color: $color-border;
  border-bottom-width: 1px;
  padding: $space-unit;
  width: 100%;
  background-color: $color-background-dark;

  &:focus {
    border-bottom-color: $color-brand;
    color: $color-brand;
  }
}
</style>
