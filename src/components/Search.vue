<template>
    <form id="search">

      <input name="query" v-model="searchQuery" placeholder="Search" />

    </form>
</template>

<script>
export default {
    name: 'Search',
    data() {
        return {
            search: ''
        }
    },
    methods: {

        isSearch() {
            this.$emit('this.search')
        },

        searchList() {
            return this.search ? this.items.filter(item => {
            for(let key in item) {
                if(item[key].toLowerCase().match(this.search.toLowerCase())) {
                    return true
                }
            }
        })
        : this.items
        }

    }

}
</script>

<style>

</style>
