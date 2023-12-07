<template>
    <div id="app">

        <Potato />
        <Tamago />
        <Potato />
        <br>
        <textform />
        <img src="src/components/Pictures/sample.png" alt="サンプル画像が表示されます。" >

    </div>
</template>


<script>
export default Vue.defineComponent({
    name: 'App',
    components: {

        "Tamago": Vue.defineAsyncComponent(() => loadModule("src/components/Tamago.vue", options)),
        "Potato": Vue.defineAsyncComponent(() => loadModule("src/components/Potato.vue", options)),
        "textform": Vue.defineAsyncComponent(() => loadModule("src/components/textform.vue", options)),

    },
})
</script>
