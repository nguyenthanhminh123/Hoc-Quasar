<template>
  <q-page class="flex flex-center">
    <div class="inline-block">
      <div>
        <q-btn stack color="primary" icon="mail" label="A Button" :disable="isLoading"/>
      </div>
      <div class="q-py-md">
        <q-btn size="150px" padding="xl" round icon="mail" color="green"/>
      </div>
      <div class="q-py-md">
        <q-btn round>
          <q-avatar size="50px">
            <img src="assets/quasar-logo-vertical.svg"/>
          </q-avatar>
        </q-btn>
      </div>
      <div class="q-py-md">
        <q-btn glossy no-caps color="secondary" label="Button"/>
      </div>
      <div class="q-py-md">
        <q-btn-group>
          <q-btn rounded label="Home"/>
          <q-btn rounded label="Profile"/>
          <q-btn rounded label="Messages"/>
        </q-btn-group>
      </div>
      <div class="q-py-md">
        <q-btn-dropdown color="primary" label="Dropdown">
          <q-list>
            <q-item clickable>
              <q-item-section>
                <q-item-label>
                  Home
                </q-item-label>
              </q-item-section>
            </q-item>
            <q-item clickable>
              <q-item-section>
                <q-item-label>
                  Profile
                </q-item-label>
              </q-item-section>
            </q-item>
            <q-item clickable>
              <q-item-section>
                <q-item-label>
                  Message
                </q-item-label>
              </q-item-section>
            </q-item>
          </q-list>
        </q-btn-dropdown>
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
      isLoading: true,
      useData: false,
      useWifi: false
    }
  }
})
</script>
