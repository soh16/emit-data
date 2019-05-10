<template>
  <div id="app">

    <form id="search">

      <input name="query" v-model="searchQuery" placeholder="Search" />

    </form>

    <userTable
      :heroes="gridData"
      :columns="gridColumns"
      :filterKey="searchQuery"/>

  </div>
</template>

<script>
import userTable from '@/components/userTable.vue'

export default {
  name: 'app',
  components: {
    userTable
  },
  data() {
    return {
      searchQuery: '',
      gridColumns: ['username', 'role', 'fascias', 'services'],
      gridData: [{
        username: 'first.last@jdplc.com',
        role: 'Edit',
        fascias: 'JDSPORTS',
        services: 'Content Editor'
      },{
        username: 'joe.bloggs@jdplc.com',
        role: 'Manage',
        fascias: 'JDSPORTS',
        services: 'Image'
      },{
        username: 'ste.last@jdplc.com',
        role: 'Admin',
        fascias: 'JDSPORTS, JDSPORTS_IE, JDSPORTS_BE',
        services: 'Content Editor',
      },
      {
        username: 'joe.bloggs@jdplc.com',
        role: 'Admin',
        fascias: 'JDSPORTS, JDSPORTS_IE, JDSPORTS_BE',
        services: 'Content Editor, Image, Email, Raffle',
      },
      {
        username: 'joe.bloggs@jdplc.com',
        role: 'Edit',
        fascias: 'JDSPORTS',
        services: 'Content Editor, Image, Email, Raffle',
      },
      {
        username: 'ste.bloggs@jdplc.com',
        role: 'Manage',
        fascias: 'JDSPORTS',
        services: 'Content Editor, Image, Email, Raffle',
      },
      {
        username: 'joe.bloggs@jdplc.com',
        role: 'Admin',
        fascias: 'JDSPORTS',
        services: 'Content Editor, Image, Email, Raffle',
      },
      {
        username: 'DELETE.ME@jdplc.com',
        role: 'Manage',
        fascias: 'JDSPORTS_BE',
        services: 'Raffle',
      }]
    }
  },
  computed: {

        // searchList() {
        //     return this.search ? this.items.filter(item => {
        //     for(let key in item) {
        //         if(item[key].toLowerCase().match(this.search.toLowerCase())) {
        //             return true
        //         }
        //     }
        // })
        // : this.items
        // }

    }
}
</script>

<style>
table, tr, td, th{
    border: 1px solid #000;
}

</style>
