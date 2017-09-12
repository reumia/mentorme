<template>
<div class="mentors">
  <div class="mentor">
    userId<br/>
    topicId<br/>
    level
  </div>
  <div class="mentor">
    userId<br/>
    topicId<br/>
    level
  </div>
  <div class="mentor">
    userId<br/>
    topicId<br/>
    level
  </div>
  <div class="mentor">
    userId<br/>
    topicId<br/>
    level
  </div>
</div>
</template>

<script>
export default {
  name: 'mentors',
  props: ['data'],
  data () {
    return {}
  }
}
</script>

<style scoped lang="scss">
@import 'init';

.mentors {
  margin: ($space-unit * 2) 0;
  border-top: 1px solid $color-border;
}
.mentor {
  padding: $space-unit 0;
  border-bottom: 1px solid $color-border;
  text-align: left;
}
</style>
