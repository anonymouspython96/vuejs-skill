<template>
    <div id="1">
        <h3>Lista della spesa</h3>
        <form @submit.prevent="addProduct">
            <input v-model="newProduct.name" type="text" placeholder="Nome prodotto" required>
            <input v-model.number="newProduct.quantity" type="number" placeholder="Quantità" required>
            <input v-model.number="newProduct.price" type="number" placeholder="Prezzo" step="0.01" required>
            <select v-model="newProduct.category">
                <option value="frutta">Frutta</option>
                <option value="verdura">Verdura</option>
                <option value="carne">Carne</option>
                <option value="pesce">Pesce</option>
                <option value="latticini">Latticini</option>
                <option value="cereali">Cereali</option>
                <option value="snack">Snack</option>
                <option value="bevande">Bevande</option>
                <option value="dolci">Dolci</option>
                <option value="altro">Altro</option>
            </select>
            <button type="submit">Aggiungi Prodotto</button>
        </form>
        <ul>
            <li v-for="product in products" :key="product.name">
                <input type="checkbox" v-model="product.inCart" />
                {{ product.name }} - {{ product.quantity }} - €{{ product.price }} - {{ product.category }}
            </li>
        </ul>
        <h4>Totale stimato: €{{ calculateTotal() }}</h4>
    </div>
</template>

<script>
export default {
    data() {
        return {
            newProduct: {
                name: '',
                quantity: 1,
                price: 0,
                category: 'frutta'
            },
            products: []
        };
    },
    methods: {
        addProduct() {
            this.products.push({ ...this.newProduct, inCart: false });
            this.newProduct.name = '';
            this.newProduct.quantity = 1;
            this.newProduct.price = 0;
        },
        calculateTotal() {
            return this.products.reduce((total, product) => {
                if (product.inCart) {
                    return total + (product.price * product.quantity);
                }
                return total;
            }, 0);
        }
    }
}
</script>

<style lang="css" scoped></style>