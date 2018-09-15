<template>
    <div>
        <button class="btn btn-primary" @click="asyncIncrement({by:100,duration:300})">Increment</button>
        <button class="btn btn-primary" @click="asyncDecrement({by:100,duration:300})">Decrement</button>
    </div>
</template>

<script>
    import {mapActions} from 'vuex'
    import * as types from '../store/types';

    export default {
        methods: {
            ...mapActions({
                asyncIncrement: types.COUNTER_INCREMENT_ASYNC,
                asyncDecrement: types.COUNTER_DECREMENT_ASYNC
            })
        }
    }
</script>