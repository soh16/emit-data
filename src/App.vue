<template>
  <div id="app">

    <Search @search="searchList"/>
    
    <user-table :items="items"/>
  
  </div>
</template>

<script>
import Search from '@/components/Search.vue'
import userTable from '@/components/userTable.vue'

export default {
  name: 'app',
  components: {
    Search, userTable
  },
  data() {
    return {
      items: [{
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
  }
}
</script>

<style>
</style>
