<template>
    <div>
       Component 2

       <h2 @mouseover="performAddition">on mouse hover {{count}} </h2>
    </div>
</template>

<script>
import addition from './addition'

    export default {
        name : 'MyComp2',
        mixins : [addition]
    }
</script>


<style>

</style>
