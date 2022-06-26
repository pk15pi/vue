<template>
<div>
    <h2>
        template refs are used to give focus to any DOM component or any child component.
        let say we want to give focus to any input box on page load.
    </h2>
    <input type="text" ref="inputRef" />
    <PostList ref="postListRef"/>
</div>
</template>


<script>
import PostList from './CallOnPageLoad.vue'
export default {
    name : 'TempRef',
    components : {
        PostList,
    },

    // since we want to give focus to input on created
    // we need to do it on mounted method, as DOM is mounted at its place when mounted gets executed
    mounted() {
        console.log(this.$refs.postListRef)
        this.$refs.inputRef.focus()
    }

}

</script>