<template>
  <q-page >
    <div class="q-pa-md">
      <div style="max-width:300px">
        <q-from @submit="submitForm">
          <div>
            <q-input outlined rounded clearable clear-icon="close" color="teal" label="Your Name" v-model="formData.textInput" 
            :rules="[val => !!val || 'Field is required']" 
            />
          </div>
          <div class="q-pt-md">
            <q-btn type="submit" label="Submit"/>
          </div>
        </q-from>
      </div>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'IndexPage',
  data() {
    return {
     formData: {
      textInput: null
     }
    }
  },
  methods: {
    submitForm() {
      alert('You name is:' + this,formData.textInput);
    }
  }
})
</script>
