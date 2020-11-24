<template>
<li v-bind:class="item.isPurchased ? 'purchased' : 'not-purchased'">{{item.name}}</li>
</template>  

<script>
export default {
    name: 'shopping-list-item',
    // props is the item property. passing info btw the compo. handles all other tasks
    props: ['item']

}
</script>

<style>
.not-purchased {
    background-color: lightgoldenrodyellow;
}

.purchased {
    text-decoration: line-through;
    background-color: red;
}
</style>