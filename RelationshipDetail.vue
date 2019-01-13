<template>
    <section> 
        <div v-if="relationship">
            <h2>{{relationship.name}}</h2>
            <p>{{relationship.attribute}}</p>
            <img v-bind:src="relationship.image">
        </div>
        <div v-else>What type of relationship do you select?</div>
    </section>
</template>

<script>
export default {
    props: { 
        relationship: Object
    }
};
</script>

<style scoped>
.donut-detail {
    height: 60%;
    width: 200px;
    position: absolute;
    bottom: 10px;
    left: 0;
    right: 0;
    /* margin: auto; */
    margin-bottom: 100px;
}
img {
    width: 300px;
    
}
</style>

