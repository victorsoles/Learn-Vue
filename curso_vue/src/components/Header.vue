<template>
    <div>
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">Projetos</a></li>
            <li><a href="#">Contatos</a></li>
        </ul>
    </div>
</template>

<script>
export default {
    name: "Header"
}
</script>

<style scoped>
    ul {
        list-style: none;
        display: flex;
        background: #999;
    }

    li {
        margin-right: 10px;
    }

    a {
        color: #ddd;
        text-decoration: none;
        transition: .5s;
    }

    a:hover {
        color: turquoise;
    }
</style>