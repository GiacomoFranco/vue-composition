<template>
    <div>Fullname: {{ fullName }}</div>
</template>
<script>
import { toRefs, computed } from 'vue';

    export default {
        props: {
            firstName: String,
            lastName: String,
        },
        setup(props){
            
            const { firstName, lastName } = toRefs(props);
            
            // const firstName = ref('Santy')
            // const lastName = ref('Gil')

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
                fullName,
            }
        },
    };
</script>