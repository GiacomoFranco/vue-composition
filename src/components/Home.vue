<template>
    <div>Fullname: {{ fullName }}</div>
    <div>username: {{ username }}</div>
</template>
<script>
import { toRefs, computed, inject } from 'vue';

    export default {
        props: {
            firstName: String,
            lastName: String,
        },
        setup(props, { expose }){
            // console.log(context);
            
            const { firstName, lastName } = toRefs(props);
            
            // const firstName = ref('Santy')
            // const lastName = ref('Gil')
            const username = inject('username')

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

            expose({
                fullName,
            })
            
            return{
                fullName,
                username
            }
        },
    };
</script>