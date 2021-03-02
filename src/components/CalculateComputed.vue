<template>
    <div>
        <input type="text" v-model="leftNumber">
        <select v-model="operator">
            <option v-for="(item, index) in items" :key="index + 1">
                {{ item }}
            </option>
        </select>
        <input type="text" v-model="rightNumber">
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
        }
    },
    computed: {
        result() {
            switch (this.operator) {
            case "+":
                return (+this.leftNumber + +this.rightNumber);
            case "-":
                return (this.leftNumber - this.rightNumber);
            case "*":
                return (this.leftNumber * this.rightNumber);
            case "/":
                return (this.leftNumber / this.rightNumber);
            default: 
                return 0;
            }
        }
    }
}
</script>

<style>
</style>
