<template>
    <div class="search-container">

        <input type="text" v-model="search" placeholder="Search" />

    </div>
</template>

<script>
export default {
    name: 'Search',
    props: {
        items: {
            type: Array,
            default: () => [],
            required: true
        }
    },
    data() {
        return {
            search: ''
        }
    },
    methods: {
        
        // searchList(item) {
        //     this.$emit('update-cart', item)
        // },

        searchList() {
            return this.search ? this.items.filter(item => {
            for(let key in item) {
                if(item[key].toLowerCase().include(this.search.toLowerCase())) {
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
