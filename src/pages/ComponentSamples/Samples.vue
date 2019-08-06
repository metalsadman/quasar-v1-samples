<template>
  <q-page class="q-pa-md row justify-center">
    <div>
      <q-btn @click="dialog = true" label="Show Form Dialog"/>
      <e-dialog
        :maximized="$q.platform.is.mobile"
        v-model="dialog"
        @child-update="updateForm"
        :formData="formData"
      />
    </div>
    <div>{{ formData || '' }}</div>
  </q-page>
</template>

<style>
</style>

<script>
/* eslint-disable */
import EDialog from 'pages/ComponentSamples/DialogExtension'
export default {
  components: {
    EDialog
  },
  name: 'Samples',
  data() {
    return {
      dialog: false,
      formData: {
        amount: 0,
        account: 'Default',
        description: 'Default input',
        type: 'Savings',
        uppercase: '',
        password: ''
      }
    }
  },
  methods: {
    updateForm(data) {
      this.formData = data
    }
  }
}
</script>
