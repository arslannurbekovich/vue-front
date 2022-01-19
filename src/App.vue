<template>
    <div> 
        <div>
            Количество лайков: <strong>{{ likes }}</strong>
        </div>
        <div>
            <button @click="addLike">Like</button>
        </div>
    </div>
</template>

<script>
    export default {
        data(){
            return {
                likes: 0
            }
        } ,
        methods: {
            addLike() {
                this.likes += 1;
            }
        }
    }
</script>

<style> 

</style>

