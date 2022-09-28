<template>
  <q-page class="flex flex-center">
    <div class="inline-block q-mx-lg">
      <q-card style="width: 300px">
        <q-parallax src="" :height="150"></q-parallax>

        <q-card-section>
          <div class="text-h6">Text Here</div>
          <div class="text-subtitle2">by someone</div>
        </q-card-section>

        <q-seperator/>

        <q-card-section>
          A very long textual content here.
        </q-card-section>

        <q-separator/>

        <q-card-actions :align="right">
          <q-btn flat label="Accept"/>
          <q-btn flat label="Regect"/>
        </q-card-actions>
      </q-card>
    </div>
    <div>
      <q-card>
        <q-card-section horizontal>
          <q-img src=""></q-img>

          <q-tabs v-model="tab" class="text-teal">
            <q-tab label="Tab one" name="one"/>
            <q-tab label="Tab two" name="two"/>
          </q-tabs>

          <q-tab-panels v-model="tab" animated>
            <q-tab-panel name="one">
              The QCard component is a great way to display important pieces of grouped content.
          </q-tab-panel>

          <q-tab-panel name="two">
            With so much content to display at once, and often so little screen real-estate,
            Cards have fast become the design pattern of choice for many companies, including
            the likes of Google and Twitter.
          </q-tab-panel>
          </q-tab-panels>
        </q-card-section>
      </q-card>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'IndexPage',
  data() {
    return {
      isLoading: true,
      useData: false,
      useWifi: false
    }
  }
})
</script>
