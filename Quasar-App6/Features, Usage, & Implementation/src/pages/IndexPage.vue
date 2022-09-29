<template>
  <q-page class="flex flex-center">
    <div>
      <q-table
        dense
        separator="none"
        title="People"
        :rows="rows"
        :colomns="columns"
        row-kay="firstName"
        no-data-label="I didn't find anything for you"
      />  
    </div>
    <div class="q-px-md">
      <q-card>
        <q-card-section>
          <q-list separator>
            <q-item clickable v-ripple>
              <q-item-section>
                Sample content here
              </q-item-section>
              <q-item-section side top>
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
  </q-page>
</template>

<script>
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'IndexPage',
  data() {
    return {
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
