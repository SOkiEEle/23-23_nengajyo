<template>
    <div id="textform">
        記入お願いします
        <br>
        <textarea rows="5" cols="50">ここに記入してください</textarea>
        <br>
        <button type="submit">送信</button>
    </div>
</template>

<script>
    export default Vue.defineComponent({
        name: 'textform',
    })
</script>

<style>
#textform {
    font-size: 1.0em;
    font-weight: bold; 
    background-color: #1ac943;
    color: #ffffff; 
    padding-left: 5px;
    padding: 5px;
}
</style>