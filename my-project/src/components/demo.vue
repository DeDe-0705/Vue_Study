<template>
    <div>
        <p>文本插值 {{message}}</p>
        <p>JS 表达式 {{flag ? 'yes' : 'no'}} 只能是表达式，不能是js语句</p>

        <p :id="dynamicId">动态属性</p>
        <hr/>
        <p>如下有xss风险，看不见子元素</p>
        <p v-html="rawHtml">
            <span>【注意】使用v-html之后，将会覆盖子元素</span>
        </p>
    </div>
</template>
// 导出组件
<script>
export default {
    data() {
        return {
            message: "hello vue",
            flag: true,
            rawHtml: '指令 - 原始 html <b>加粗</b> <i>斜体</i>',
            dynamicId: `id-${Date.now()}`
        }
    }
}
</script>