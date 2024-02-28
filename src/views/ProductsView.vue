<template>
    <div class="container">
        <div class="row">
            <div class="col">
                <input type="text" v-model="searchQuery" placeholder="Search product by name" class="form-control">
            </div>
            <div class="col">
                <button class="btn btn-sm btn-custom" @click="toggleSortOrder">Sorting by price</button>
            </div>
        </div>
        <div class="row" v-if="products">
            <Card v-for="product in filteredProducts" :key="product.prodID">
                <template #cardHeader>
                    <img :src="product.ProdUrl" class="car-img-top" alt="">
                    <h4 class="card-title">{{ product.prodName }}</h4>
                </template>
                <template #cardBody>
                    <p class="card-text text-dark bg-gradient bg-dark-subtle p-2">
                        Quantity: {{ product.prodQuantity }}
                    </p>
                    <p class="card-text text-dark bg-gradient bg-dark-subtle p-2">
                        Amount: R{{ product.prodAmount }}
                    </p>
                    <router-link :to="{name: 'product', params: {id: product.prodID}}">View More</router-link>
                </template>
            </Card>
        </div>
        <div class="row" v-else>
            <p class="lead">Loading</p>
        </div>
    </div>
</template>

<script>
import Card from '@/components/Card.vue';
export default {
    name: 'ProductsView.vue',
    components: {
        Card
    },
    data() {
        return {
            ascendingOrder: true, // Flag to track sorting order
            searchQuery: '' // Query for searching product by name
        };
    },
    computed:{
        products(){
            return this.$store.state.products;
        },
        sortedProducts() {
            // Create a copy of products array to avoid mutating the original array
            const sorted = [...this.products];
            // Sort the products by prodAmount
            sorted.sort((a, b) => (this.ascendingOrder ? a.prodAmount - b.prodAmount : b.prodAmount - a.prodAmount));
            return sorted;
        },
        filteredProducts() {
            // Filter products based on search query
            return this.sortedProducts.filter(product =>
                product.prodName.toLowerCase().includes(this.searchQuery.toLowerCase())
            );
        }
    },
    methods: {
        toggleSortOrder() {
            this.ascendingOrder = !this.ascendingOrder;
        }
    },
    mounted() {
        this.$store.dispatch('fetchProducts');
    }
}
</script>

<style scoped>
/* .btn-secondary {
    background-color: gray;
    color: white;
} */
.btn-custom {
    background-color: #918e8e;
    color: white;
}
</style>