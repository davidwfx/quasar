<template>
  <div class="q-layout-padding">
    <template v-for="b in bp">
      <h5 :key="`h${ b }`">Breakpoint {{ b || 'NONE' }}</h5>
      <div class="row items-center" :key="`h${ b }`">
        <div class="box" v-for="s in sz" :key="`b${ b }-${ s }`">
          <div :class="`q-pa${ b }-${ s } q-ma${ b }-${ s }`"/>
        </div>
      </div>
    </template>
  </div>
</template>

<style lang="stylus">
  .box
    position relative
    display inline-flex
    margin 2em
    background rgba(255, 150, 0, .3)
    width 200px
    height 200px
    div
      flex 1 1 100%
      background rgba(0, 200, 0, .3)
      &:before
        content ''
        display block
        width 100%
        height 100%
        background rgba(0, 0, 255, .3)
      &:after
        content attr(class)
        position absolute
        bottom 0
        left 0
        right 0
        transform translateY(100%)
        padding .5em
        background rgba(100, 100, 100, .1)
        text-align center

</style>

<script>
export default {
  data () {
    return {
      bp: ['', '-xs', '-sm', '-md', '-lg', '-xl'],
      sz: ['xs', 'sm', 'md', 'lg', 'xl']
    }
  },
  created () {
    import('./flex-addon.styl')
  }
}
</script>
