<template>
    <div class="productList">
        <nav>
            <span style="margin-right: 20px">欢迎您：{{this.$store.state.loginuser}}</span>
        </nav>
        <div class="list">
            <product v-for="(item,index )in product":info="item" :key="index"></product>
        </div>
        <div class="page">
            <Page :total="total" :current="current" :page-size="size"
            prev-text="上一页" next-text="下一页" @on-change="change"/>
        </div>
    </div>
</template>

<script>
    import Product from "../components/Product";
    export default {
        name: "ProductList",
        components: {Product},
        path:'/productlist',
        component:ProductList
    }

</script>

<style scoped>

</style>