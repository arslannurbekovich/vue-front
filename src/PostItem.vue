<template>
    <div class="post">
        <div>
            <div><strong>Название:</strong> {{post.title}} </div>
            <div><strong>Описание:</strong> {{post.body}} </div>
        </div>
        <div class="post__btns">
            <my-button>Удалить</my-button>
        </div>
    </div>
</template>

<script>
import MyButton from './UI/MyButton.vue'
export default {
  components: { MyButton },
    props:{
        posts:{
            type: Object,
            required: true
        }
    }

}
</script>

<style>

</style>