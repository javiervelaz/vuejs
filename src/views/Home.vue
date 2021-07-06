<template>
    <div class="home">
        home
        <p ref="p">mi nombre es  {{name }} y mi edad es {{ age}}</p>
        <button @click="handleClick">Click me</button>
        <button @click="age++">add 1 to age</button>
        <input type="text" v-model="name" />
    </div>
</template>

<script>
// @ is an alias to /src

    import { ref ,reactive} from 'vue'
export default {
        name: 'Home',
        setup() {
            console.log('setup')

            
            //const p = ref(null)
            const name = ref('mario')
            const age = ref(30)

            const handleClick = () => {
                name.value = 'javier'
                age.value = 89  
            }

            return {
                name, age, handleClick
            }
        },
        data() {
            return {
                
            }
        },
        created() {
            console.log('created')
        },
        mounted() {
            console.log('mounted')
        },
        components: {}
}
</script>
