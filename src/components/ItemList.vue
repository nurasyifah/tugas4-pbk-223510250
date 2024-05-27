<template>
    <div class="item-list">
        <h2><u>Item List</u></h2>
        <ul>
            <li v-for="item in items" :key="item.id">
                {{ item.name }} - {{ item.price }}
                <button @click="sendDataToParent(item)">Send Data to Parent</button>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'ItemList',
    data() {
        return {
            items: [
            { id: 9012901, name: 'Nike Dunk Low', price: 'Rp 1.999.000' },
            { id: 9918180, name: 'Kalibre Topi', price: 'Rp 145.000' },
            { id: 9810149, name: 'T Shirt Kaos Lacoste Black', price: 'Rp 90.000' },
            { id: 9310112, name: 'Uniqlo Pullover Sweat Hoodie', price: 'Rp 499.000' },
            { id: 9712105, name: 'Charles&Keith Saddle Bag', price: 'Rp 1.300.000' },
            ],
        };
    },
    methods: {
        sendDataToParent(item) {
            this.$emit('send-data', item);
        },
    },
};
</script>

<style>
.item-list {
    font-family: 'Century', sans-serif;
    background-color: #e3f2fd;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}
h2 {
    color: #1e88e5;
}
ul {
    list-style: none;
    padding: 0;
}
li {
    background-color: #bbdefb;
    margin: 10px 0;
    padding: 10px;
    border-radius: 5px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}
button {
    background-color: #1976d2;
    color: white;
    border: none;
    padding: 5px 10px;
    border-radius: 5px;
    cursor: pointer;
}
button:hover {
    background-color: #0d47a1;
}
</style>