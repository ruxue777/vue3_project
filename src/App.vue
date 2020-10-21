<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld :msg="msg" />
</template>

<script lang="ts">
import { defineComponent,reactive } from 'vue'
import HelloWorld from './components/HelloWorld.vue'

interface title_Data {
    msg:string
}

export default defineComponent({
   name: 'App',
   components: {
    HelloWorld
    },
    setup(){
        const data:title_Data = reactive({
            msg:'Welcome ~'
        })

        return {
            ...data
        }
    }
})
</script>
