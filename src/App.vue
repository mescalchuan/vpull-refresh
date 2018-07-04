<template>
    <div id="app">
        <Example/>
    </div>
</template>

<script>
import Example from './components/Example'

export default {
    name: 'App',
    components: {
        Example
    }
}
</script>

<style>
    html, body {
        margin: 0;
        padding: 0;
        height: 100%;
        background-color: #eeeeee;
    }
</style>
