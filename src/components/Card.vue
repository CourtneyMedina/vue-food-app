<template>
    <div class="card">
    <img src="https://www.flaticon.com/svg/static/icons/svg/1377/1377194.svg" class="card-img-top" alt="Image Failed to Load">
        <div class="card-body">
            <h5 class="card-title" id="product-name">{{product}}</h5>
            <p class="card-text" id="brand">Manufacturer: {{manufacturer}}</p>
            <p class="card-text" id="rating">Rating: {{ratingValue}}</p>
            <p class="card-text" id="price">Price: ${{priceValue}}</p>
            <ButtonGroup></ButtonGroup>
            <!-- <a href="#" class="btn btn-primary">Go somewhere</a> -->
        </div>
    </div>
</template>

<script>
import ButtonGroup from "./ButtonGroup.vue"

export default {
    props: {
        key: String,
        product: String,
        manufacturer: String,
        rating: Number,
        price: Number,
    },

    setup(props){
        return {
            ButtonGroup,
            ratingValue: props.rating ? props.rating : "Not Rated",
            priceValue: props.price ? props.price.toFixed(2) : "0.00",
            // ternary operator tests value for T/F condition
            // conditionalState ? returnIfTrue : returnIfFalse
            ////// Redefining the property in returns
            }
    },
}
</script>

<style>
.card {
    width: 18rem;
    padding: 0.5rem;
    margin: 1rem 0rem;
}

p {
    text-align: left;
}

</style>