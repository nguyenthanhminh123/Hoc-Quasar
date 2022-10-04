<template>
  <q-page >
    <div class="q-pa-md">
      <q-card style="max-width: 500px">
        <q-item>
          <q-item-section avatar>
            <q-skeleton type="QAvatar" animation="pulse" bordered class="bg-teal"/>
          </q-item-section>
          <q-item-section>
            <q-item-label>
              <q-skeleton type="text" animation="pulse"/>
            </q-item-label>
            <q-item-label caption>
              <q-skeleton type="text" animation="pulse"/>
            </q-item-label>
          </q-item-section>
        </q-item>

        <q-skeleton height="200px" square/>

        <q-card-actions :align="right" class="q-gutter-md">
          <q-skeleton type="QBtn" animation="pulse" class="bg-red"/>
          <q-skeleton type="QBtn" animation="pulse" class="bg-green"/>
        </q-card-actions>
      </q-card>
    </div>
    <!-- <div>
      <q-tabs v-model="tabs" outside-arrows dense switch-indicator-color="blue">
        <q-tab :ripple="{ color: 'orange'}" name="home" label="Home" icon="home"/>
        <q-tab :ripple="{ color: 'orange'}" name="mail" label="Mail" icon="mail">
          <q-badge color="red" floating></q-badge>
        </q-tab>
        <q-tab :ripple="{ color: 'orange'}" name="alarms" label="Alarms" icon="alarms"/>
        <q-btn-dropdown auto-close stretch flat label="More..">
          <q-list>
            <q-item clickable>
              <q-item-section>Movies</q-item-section>
            </q-item>
            <q-item>
              <q-item-section>Photos</q-item-section>
            </q-item>
          </q-list>
        </q-btn-dropdown>
      </q-tabs>
    </div>
    <div>
      <q-tab-panels v-model="tabs" animated>
        <q-tab-panel name="home">
          <div class="text-h6">Home</div>
          Lorem ipsum dolor sit amet consectetur adipisicing alit.
        </q-tab-panel>
        <q-tab-panel name="mail">
          <div class="text-h6">Mail</div>
          Lorem ipsum dolor sit amet consectetur adipisicing alit.
        </q-tab-panel>
        <q-tab-panel name="alarms">
          <div class="text-h6">Alarms</div>
          Lorem ipsum dolor sit amet consectetur adipisicing alit.
        </q-tab-panel>
      </q-tab-panels>
    </div>
    <div class="q-px-md" style="with: 400px">
      <q-carousel 
        animated 
        v-model="carousel" 
        class="rounded-borders bg-primary"
        transition-prev="scale"
        transition-next="scale"
        navigation
        padding
        arrows
        control-type="outline"
        navigation-position="top"
        infinete
        autoplay
      >
      <q-carousel-slide name="home" class="column no-wrap flex-center">
          <div class="text-h2 text-white">
            Home
          </div>
        </q-carousel-slide>
        <q-carousel-slide name="mail" class="column no-wrap flex-center">
          <div class="text-h2 text-white">
            Mail
          </div>
        </q-carousel-slide>
        <q-carousel-slide name="profile" class="column no-wrap flex-center">
          <div class="text-h2 text-white">
            Profile
          </div>
        </q-carousel-slide>
        <q-carousel-slide name="settings" class="column no-wrap flex-center">
          <div class="text-h2 text-white">
            Settings
          </div>
        </q-carousel-slide>
      </q-carousel>
      <div class="row justify-center">
        <q-btn-toggle
          glossy
          v-model="carousel"
          :options="[
            { label: 1, value: 'style' },
            { label: 2, value: 'mail' },
            { label: 3, value: 'profile' },
            { label: 4, value: 'settings' }
          ]"
        />
      </div>
    </div>
    <div class="q-px-md">
      <q-btn @click="showDialog = true" label="Open Dialog"/>
      <q-dialog v-model="showDialog">
        <q-card>
          <q-card-section>
            <div class="text-h6">Alert</div>
          </q-card-section>

          <q-card-section class="q-pt-none">
            Lorem ipsum dolor sit emet consectetur adipicing elit. rerum 
          </q-card-section>
          <q-card-actions :align="right">
            <q-btn flat label="OK" color="primary" v-close-popup/>
          </q-card-actions>
        </q-card>
      </q-dialog>
    </div>
    <div class="q-px-md">
      <q-table
        dense
        separator="none"
        title="People"
        :rows="rows"
        :columns="columns"
        row-kay="firstName"
        no-data-label="I didn't find anything for you"
      />  
    </div>
    <div class="q-px-md">
      <q-card style="...">
        <q-card-section>
          <q-list separator>
            <q-item clickable v-ripple :active="true" active-class="bg-teal-1">
              <q-item-section>
                <q-item-label>
                  First item label
                </q-item-label>
                <q-item-label caption>
                  secondary line text. Lorem ipsum dolor
                </q-item-label>
              </q-item-section>  

              <q-item-section side top>
                <q-item-label>1 min ago</q-item-label>
                <q-avatar color="teal" text-color="white" icon="home"/>
              </q-item-section>
            </q-item>

            <q-item clickable v-ripple>
              <q-item-section avatar>
                <q-avatar round>
                  <img src="https://cdn.quasar.dev/img/boy-avatar.png">
                </q-avatar>
              </q-item-section>

            <q-item-section>
              Sample 2 content here
            </q-item-section>
            </q-item>
          </q-list>
        </q-card-section>
      </q-card>
    </div>
    <div style="max-width: 300px;">
      <q-list bordered dark>
        <q-expansion-item>
          <teamplate>
            <q-item-section avatar>
              <q-avatar icon="bluetooth" color="primary" text-color="white"/>
            </q-item-section>

            <q-item-section>
              Bluetooth
            </q-item-section>

            <q-item-section side>
              <div class="row items-center">
              <q-icon name="star" color="red" size="24px" />
              <q-icon name="star" color="red" size="24px" />
              <q-icon name="star" color="red" size="24px" />
            </div>
            </q-item-section>
          </teamplate>
          <q-card>
            <q-card-section>
              Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quidem, eius reprehenderrit eos corrupti
              commoidi magni quaerat ex numquam, dolorum officiis modi facere maiores architecto suscipit q-item-section
              eveniet doloribus ullam aliquid.
            </q-card-section>
          </q-card>
        </q-expansion-item>

        <q-expansion-item  dense header-class="text-red" v-model="expandItem" expand-separator icon="mail" label="Mail">
          <q-icon name="mail" size="50px"/>
        </q-expansion-item>
      </q-list>
    </div>
    <div>
      <q-btn label="click me" @click="expandItem = !expandItem"/> 
    </div> -->
    <div>
      <q-btn-sticky position="bottom-right" :offset="[18, 18]">
        <q-fab square label="Options" color="blue" icon="keyboard_arrow_up" derection="up" :hide-label="hideLabel">
          <q-fab-action external-label color="red" icon="mail" label="Mail" />
          <q-fab-action external-label color="orange" icon="home" label="Home"/>
        </q-fab>
        <q-btn @click="hideLabel = !hideLabel" label="Hide FAB Labels"/>
      </q-btn-sticky>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'IndexPage',
  data() {
    return {
      tabs: "home",
      carousel: "home",
      fullscreen: false,
      hideLabel: false,
      expandItem:false,
      showDialog: false,
      alert: false,
      maximized: true,
      tab: 'one',
      isLoading: true,
      useData: false,
      useWifi: false,
      columns: [
        {
          name: 'name',
          label: 'First Name',
          field: 'name'
        },
        {
          name: 'lastname',
          label: 'Last Name',
          field: 'lastname'

        }
      ],
      rows: [
        {
          name: 'Minh',
          lastName: 'Jadia',
        },
        {
          name: 'Minquan',
          lastName: 'Jia',
        }
      ]
    }
  }
})
</script>
