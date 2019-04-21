<template>
    <div>
        <div class="row">
            <div v-for="(quote, index) in quotes" :key="index" 
                class="col-sm-3 mb-3">
                <quote @click.native="deleteQuote(index)">
                    {{ quote }}
                </quote>
            </div>
        </div>
    </div>
</template>

<script>
import Quote from "./Quote";

export default {
    components: {
        "quote": Quote,
    },

    props: {
        "quotes": Array,
        "deleteQuote": Function
    },

    methods: {
        
    },
}
</script>