
import { message } from 'laravel-mix/src/Log';
<template>
    <div class="container">
        <h1>Nggawe To Do</h1>
        <form class="form">
            <input type="text" v-model="input">
            <button type="button" @click="addList">Submit</button>
        </form>
        <ul class="list">
            <li v-for="(item, index) in list" :key="index">
                {{item.title}}<button class="delete" @click="deleteList(index)">Hapus</button>
            </li>
        </ul>
    </div>
</template>
<script>
export default {
    data:function(){
        return {
         list: [
            {title:"menyapu"},
            {title:"cuci piring"},
            {title:"ngepel"},
         ],
         input:""
        }
    },
    methods: {
                addList () {
                    let newList= {
                        title : this.input 
                    }
                    this.list.push (newList)
                    this.input = ""
                },
                deleteList(index){
                    this.list.splice(index,1)
                }
            },
            mounted() {
    console.log('Component mounted.')
    },
}
   
</script>

