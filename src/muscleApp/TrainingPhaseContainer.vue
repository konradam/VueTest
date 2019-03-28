<template>
    <div style="background: red">
        <h1>{{title}}</h1>
    </div>
</template>

<script>
export default {
    props: {
        title: {
            type: String
        }
    }
}
</script>
