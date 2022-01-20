<template>
   <form @submit.prevent>
            <h3>Создание поста</h3>
            <input v-model="post.title" 
             class="input" type="text" placeholder="Название">
            <input v-model="post.body"
              class="input" type="text" placeholder="Описание">
            <my-button 
             style="align-self:flex-end"
             @click="createPost">Создать</my-button>
        </form>
</template>

<script>
import MyButton from '../UI/MyButton.vue';
export default {
  components: { MyButton },
    data(){
        return {
            post: {
                title: "",
                body: ""
            }
        }
    },
    methods: {
        createPost(){
            this.post.id = Date.now();
            this.$emit("create", this.post)
            this.post = {
                title: "",
                body: ""  
            }
        }
    }
}
</script>

<style>
    form {
        display: flex;
        flex-direction: column;
    }
    .input {
        width: 100%;
        padding: 10px 15px;
        border: 2px solid teal;
        margin-top: 15px;
    }
    h3 {
        color: teal;
    }
</style>