<template>
    <div>
       Component 1

       <h2 @click="performAddition">on mouse click {{count}} </h2>
    </div>
</template>

<script>
    import addition from './addition'
    export default {
        name : 'MyComp1',
        mixins : [addition]
    }
</script>


<style>

</style>
