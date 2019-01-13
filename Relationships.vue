<template>
    <ul class=relationships>
        <li v-bind:class="{ relationship: true, selected: relationship === selected }"    
            v-for="relationship in relationships"
            v-bind:key="relationship.name"
            v-on:click="onSelect(relationship)">
            <h3>{{relationship.name}} the {{relationship.attribute}}</h3>
            <img v-bind:src="relationship.image">
        </li>
    </ul>
</template>
                                 
<script>
export default {
    props: {
        relationships: Array,  
        selected: Object, 
        onSelect: Function 
    }
};
</script>  

<style scoped>

.donuts {
    display: flex;
    flex-wrap: wrap;
}
.donut {
    list-style: none;
    width: 200px;
    text-align: center;
    cursor: pointer;
}
img {
    object-fit: cover;
    width: 100px;
    
}


</style>
