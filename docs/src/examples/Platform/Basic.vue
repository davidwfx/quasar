<template>
  <div class="q-pa-md">
    <q-markup-table>
      <thead>
        <tr>
          <th class="text-left">Property</th>
          <th class="text-left">Value</th>
        </tr>
      </thead>

      <tbody>
        <tr v-for="(value, prop) in $q.platform.is" :key="prop">
          <td>{{ prop }}</td>
          <td>{{ value }}</td>
        </tr>
      </tbody>
    </q-markup-table>

    <div class="q-mt-md">
      The device which are using to view this website <strong>{{ touch }}</strong> touch capability.
    </div>
  </div>
</template>

<script>
export default {
  computed: {
    touch () {
      return this.$q.platform.has.touch ? 'has' : 'does not have'
    }
  }
}
</script>
