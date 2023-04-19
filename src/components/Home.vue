<template>
    <div>{{ obj }}</div>
</template>

<script>
import { reactive, watch } from 'vue';

    export default {
        setup(){

            const obj =  reactive({count: 0});

            setInterval(() => obj.count++, 500)

            watch(() => obj.count, (newValue,prevValue) => {
                console.log(newValue,prevValue);
            })

            return {
                obj
            };
        },
    };
</script>