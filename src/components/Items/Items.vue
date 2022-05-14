<template>
    <div class="grid grid-cols-4 gap-4">
        <div class="border p-2 shadow-lg rounded" v-for="(item, index) in items">
            <SingleItem :item="item" />
        </div>
    </div>
</template>

<script>
import SingleItem from '../../components/Items/SingleItem.vue'
export default {
    props: {
        items: Array,
    },
    components: { SingleItem }
}
</script>
