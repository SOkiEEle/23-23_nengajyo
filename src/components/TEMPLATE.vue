<template>
    <!-- <div id="COMPONENT_NAME">
        any HTML you want

        <button id="example" @click="select('example')">{{ t("Example.button") }}</button>

        <SUB_COMPONENT :sub_component_props_name:"example_parameter" @event_name="function_name()"/>

        <SOMETHING v-for="example in example_list" :key="example.id" :example_props_name="example">
    </div> -->
</template>

<script>
export default Vue.defineComponent({
    name: 'COMOPNENT_NAME',
    components: {
        //"SUB_COMPONENT": Vue.defineAsyncComponent(() => loadModule("src/components/SUB_COMPONENT.vue", options)),
    },
    setup() {
        //一番最初に走るjavascript

        //i18n設定
        const { t } = VueI18n.useI18n()
        return { t }
    },
    mounted() {
        //マウントされたときに走るjavascript。setup()より基本的にこれを使う。
    },
    updated() {
        //表示内容が更新されたときに走るjavascript
    },
    data() {
        //プライベート変数
        return {
            //example_variable: "example"
        }
    },
    props: {
        //コンポーネントの引数

        // example_parameter: {
        //     type: String,
        //     required: true
        // }
    },
    methods: {
        // このコンポーネントのメソッド
        // select(example) {
        //     this.$emit("onSelected", example)
        // },
        // example_method() {
        //   
        // }
    },
    watch: {
        // 変化監視
        // example_variable: {
        //     handler: function (newVal, oldVal) {
        //         //script called when example_variable is changed
        //     },
        //     deep: true
        // }
    },
    computed: {
        // プライベート変数の一種。
        // 中身の計算に使われている変数が更新されると、これを検知してこちらも更新される。
        // example_computed() {
        //      
        //     return this.example_variable + " computed"
        // }
    }
})
</script>

<i18n>
    {
        "en": {
            "Example": {
                "button": "example"
            }
        },
        "ja": {
            "Example": {
                "button": "例"
            }
        }
    }
</i18n>

<style>
/*.COMPONENT_NAME {
    font-size: 1.5em;
    font-weight: bold;     
}*/
</style>
