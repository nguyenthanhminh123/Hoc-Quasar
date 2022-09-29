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
      />  
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
