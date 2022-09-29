<template>
  <q-page class="flex flex-center">
    <q-btn label="Alert" color="primary" @click="clert = true"/>

    <q-dialog v-model="alert">
      <q-card>
        <q-card-section>
          <q-bar>
            <q-icon name="network_wifi" />
            <q-icon name="network_cell" />
            <q-icon name="battery_full" />
            <div>9:34</div>

            <q-space/>

            <q-btn dense flat icon="close" v-close-popup>
              <q-tooltip>Close</q-tooltip>
            </q-btn>
          </q-bar>
        </q-card-section>
        
        <q-card-section class="q-pt-none">
          Lorem ipsum dolor sit amet consectotur adipicing elit. Rerum perellendus sit
        </q-card-section>

        <q-card-actions :align="right">
          <q-btn flat label="OK" color="primary" v-close-popup/>
        </q-card-actions>
      </q-card>
    </q-dialog>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'IndexPage',
  data() {
    return {
      alert: false,
      tab: 'one',
      isLoading: true,
      useData: false,
      useWifi: false
    }
  }
})
</script>
