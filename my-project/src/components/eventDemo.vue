<template>
    <div>
        <!-- 事件修饰符：
        capture：反冒泡
        stop：阻止向上冒泡
        prevent：阻止默认事件 -->
        <p>{{num}}</p>
        <p @click="increment1"> 
            <a>你好</a>
            <button @click ="increment1">+1</button>
            <!-- 体现了事件冒泡机制 -->
        </p>
        
        <button @click="increment2(2, $event)">2</button>
    </div>
</template>

<script>
export default {
    data() {
        return {
            num: 0
        }
    },
    methods: {
        increment1(event) {
            console.log('event', event, event.__proto__.constructor);
            console.log(event.target);// 指向触发事件的元素
            console.log(event.currentTarget);// 指向事件绑定的元素
            this.num++;
        },
        increment2(val, event) {
            console.log(event.target);
            this.num = this.num + val;
        },
        loadHandler() {

        }
    },
}
</script>