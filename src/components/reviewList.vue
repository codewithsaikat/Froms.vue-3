<template>
    <div class="review-container">
        <h3>Reviews:</h3>
        <ul>
            <li v-for="(review, index) in reviews" :key="index">
                {{ review.name }} gave this {{ review.rating }} stars
                <br />
                "{{ review.review }}"
                <br />
                Recommended: {{ review.recommend }}
            </li>

        </ul>

    </div>
</template>
<script>
    export default {
        props: {
            reviews: {
                type: Array,
                required: true
            }
        }
    }
</script>