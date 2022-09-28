<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-md-8">
                <div class="card">
                    <div class="card-header">Example Component</div>

                    <div class="card-body">
                        I'm an example component.
                    </div>
                    <h1>{{message}}</h1>
                    <span v-if="type=='A'">If type is A</span>
                    <span v-else-if="type=='B'">If type is B</span>
                    <span v-else>If type is other then A or B</span>
                    <br>
                    <ol>
                        <li v-for="(todo, index) in todos" :key="index">
                            {{todo.text}}
                        </li>
                    </ol>
                    <br>
                    <h4>input text</h4>
                    <input v-model="input" placeholder="Input Text">
                    <h4>Show User Input:</h4>
                    <p>{{input}}</p>
                    
                </div>
            </div>
        </div>
    </div>
</template>

<script>

    export default {
        data:function(){
            return{
                message:"Haiiii....ini data baru",
                type:"C",
                todos:[
                    {text:'learn javascript'},
                    {text:'learn vue'},
                    {text:'built something awasome'}
                ],
                input:null
            }
        },
        mounted() {
            console.log('Component mounted.')
        }
    }
</script>
