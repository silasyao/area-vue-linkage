<template>
    <div class="code-area">
        <div class="area-left">
            <area-cascader :level="2"  type="text" placeholder="请选择地区" v-model="selected" :data="$pcaa"></area-cascader>
        </div>
            <div class="area-right">
            <pre><code>{{selected}}</code></pre>
        </div>
        <div class="original-code" ref="original" v-if="shown">
            <pre><code><span>//返回值是一个数组，数组项是行政区域文本</span><br /><span>&lt;</span>template<span>&gt;</span><br/>&nbsp;&nbsp;&nbsp;&nbsp;<span>&lt;</span>area-cascader&nbsp;:level="2"&nbsp;type="text"&nbsp;placeholder="请选择地区"&nbsp;v-model='selected'&gt;&lt;/area-cascader&gt;<br/>&lt;</span>/template<span>&gt;</span></code></pre>
        </div>
        <div class="show-code" @click="toggle">
            {{this.shown ? 'Hide Code' : 'Show Code'}}
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                selected: [],
                shown: false
            }
        },
        methods: {
            toggle() {
                this.shown = !this.shown;
            }
        }
    };
</script>
