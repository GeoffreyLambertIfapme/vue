<template>
    <div class="row">
        <div class="col">
            <ActionComponent label="-" @action="decrease()"/>
        </div>
        <div class="col">
            <CounterValue :value="this.counter" />
        </div>
        <div class="col">
            <CounterValue :value="this.counterMore10" />
        </div>
        <div class="col">
            <ActionComponent label="+" @action="increase()"/>
        </div>
    </div>
   
</template>

<script>
// @ is an alias to /src
import CounterValue from '@/components/Counter.vue';
import ActionComponent from '@/components/Action.vue';


export default {
    name: 'CptView',
    components: {
        CounterValue,
        ActionComponent
    },
    data() {
        return {
            counter: 5
        }
    },
    computed: {
        counterMore10() {
            return this.counter + 10;
        }
    },
    methods: {
        decrease() {
            if(this.counter <= 0){
                return;
            }
            this.counter--;
        },
        increase() {
            if(this.counter >= 10){
                return;
            }
            this.counter++;
        }
    }
}
</script>

<style>
</style>