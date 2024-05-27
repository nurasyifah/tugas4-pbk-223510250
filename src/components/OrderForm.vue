<template>
    <div class="order-form">
        <h2><u>Order Form</u></h2>
        <button  @click="sendDataToParent">Send Data to Parent</button>
    </div>
</template>

<script>
 export default {
    name: 'OrderForm',
    methods: {
        sendDataToParent() {
            this.$emit('send-data', 'Data from OrderForm');
        },
    },
 };
</script>

<style>
.order-form {
    font-family: 'Goudy Old Style', sans-serif;
    background-color: #e3f2fd;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}
h2 {
    color: #1e88e5;
}
button {
    background-color: #1976d2;
    color: white;
    border: none;
    padding: 10px 20px;
    border-radius: 5px;
    cursor: pointer;
    margin-top: 10px;
}
button:hover {
    background-color: #0d47a1;
}
</style>