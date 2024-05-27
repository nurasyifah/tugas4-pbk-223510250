<template>
    <div class="dashboard">
        <h1><u>Jastip Strach</u></h1>
        <h2>from @nurasyifah_</h2>
        <ItemList @send-data="receiveData"/>
        <OrderForm @send-data="receiveData"/>
        <p>Data from Component: {{ childData }}</p>
        <slot name="custom-slot"></slot>
    </div>
</template>

<script>
import ItemList from './ItemList.vue';
import OrderForm from './OrderForm.vue';

export default {
    name: 'JastipDashboard',
    components: {
        ItemList,
        OrderForm,
    },
    data() {
        return {
            childData: '',
        };
    },
    methods: {
        receiveData(data) {
            this.childData = data;
        },
    },
};
</script>

<style>
.dashboard {
    font-family: 'Edwardian Script ITC', sans-serif;
    background-color: #e0f7fa;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}
h1, p {
    font-family: 'Goudy Old Style', sans-serif;
    color: #007bb5;
}
</style>