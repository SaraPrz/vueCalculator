<template>
    <div>
        <input type="text" v-model="leftNumber">
        <select v-model="operator">
            <option v-for="(item, index) in items" :key="index + 1">
                {{ item }}
            </option>
        </select>
        <input type="text" v-model="rightNumber">
        <button @click="calculate">
            Calculate
        </button>
        {{ result }}
    </div>
</template>

<script>

export default {
    name: 'App',
    data() {
        return {
            leftNumber: 0,
            rightNumber: 0,
            items: ['+', '-', '*', '/'],
            operator: '+',
            result: 0
        }
    },
    methods: {
        calculate() {
            if (this.operator === '+') {
                this.result = +this.leftNumber + +this.rightNumber
            } else if (this.operator === '-') {
                this.result = this.leftNumber - this.rightNumber
            } else if (this.operator === '*') {
                this.result = this.leftNumber * this.rightNumber
            } else if (this.operator === '/') {
                this.result = this.leftNumber / this.rightNumber
            }
        }
    }
}
</script>

<style>
</style>
