<template>
  <div class="q-pa-md q-gutter-md">
    <div class="row justify-center">
      <q-date
        v-model="date"
        first-day-of-week="1"
      />
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      date: '2019/02/01'
    }
  }
}
</script>
