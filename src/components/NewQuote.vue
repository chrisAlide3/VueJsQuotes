<template>
    <div class="row">
        <div class="col-sm-6 mx-auto text-center">
            <div class="form-group">
                <label for="newQuote">Quote:</label>
                <textarea v-model="quote" class="form-control" id="newQuote" rows="3" v-focus></textarea>
            </div>
            <button @click="addQuote" type="button" class="btn btn-primary">Add quote</button>    
        </div>
    </div>
</template>

<script>
export default {
    data: function() {
        return {
            quote: "",
        }
    },

    methods: {
        addQuote() {
            if (this.quote != "") {
                this.$emit("quoteAdded", this.quote);
                this.quote = "";
            }
        }
    },
    
    directives: {
        focus: {
            // directive definition
            inserted: function (el) {
            el.focus()
            }
        }
    },

}
</script>