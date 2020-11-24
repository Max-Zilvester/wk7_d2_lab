<template>
<div>
<h1>My Shopping List</h1>
<shopping-list-item v-for="(item, index) in items" :key="index" :item="item"></shopping-list-item>
</div>               <!-- :key helps to bind items. could be index -->
    <!-- app should only be responsible for rendering info to DOM -->


</template>

<script>
import ShoppingListItem from './components/ShoppingListItem.vue'
export default {
    name: 'app',
    data() {
        return{   
            items: [
                {name: 'Milk', isPurchased: false},
                {name: 'Bread', isPurchased: true},
                {name: 'Apples', isPurchased: false},
            ] 

        }
    },
    components: { 
        'shopping-list-item': ShoppingListItem
    }

}
</script>

<style>

</style>