<template>
    <div class="user-table">

        <table>

            <tr>
                <th>Username</th>
                <th>Role</th>
                <th>Fascia</th>
                <th>Services</th>
            </tr>

            <tr 
                v-for="(item, index) in items"
                :key="index"
            >
                <td>{{ item.username }}</td>
                <td>{{ item.role }}</td>
                <td>{{ item.fascias }}</td>
                <td>{{ item.services }}</td>
            </tr>
            
        </table>

    </div>
</template>

<script>
export default {
    name: 'userTable',
    props: {
        items: {
            type: Array,
            default: () => [],
            required: true
        }
    }
}
</script>

<style>
table, tr, td, th{
    border: 1px solid #000;
}

</style>

