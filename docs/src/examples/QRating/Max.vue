<template>
  <div class="q-pa-md q-gutter-md">
    <div class="row justify-center">
      <q-rating
        v-model="ratingModel"
        size="2em"
        :max="10"
      />
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      ratingModel: 3
    }
  },

  methods: {
  }
}
</script>
