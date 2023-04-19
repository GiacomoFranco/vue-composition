<template>
    <div>{{ fullName }}</div>
</template>

<script>
import { ref, computed } from 'vue';

    export default {
        setup(){
            
            const firstName = ref('Santy')
            const lastName = ref('Gil')

            const fullName = computed(()=>{
                return `${firstName.value} ${lastName.value}`
            })


            // const obj =  reactive({count: 0});

            // setInterval(() => obj.count++, 500)

            // watch(() => obj.count, (newValue,prevValue) => {
            //     console.log(newValue,prevValue);
            // })

            // return {
            //     obj
            // };

            
            return{
                fullName
            }
        },
    };
</script>