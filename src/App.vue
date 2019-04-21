<template>
  <div class="container">
    <!-- Progress -->
    <div class="mx-auto mt-5 mb-3">
      <h3>Quotes added</h3>
      <quote-progress :maxQuotes="maxQuotes" :quotesNbr="quotes.length"></quote-progress>
    </div>
    <!-- New Quote -->
    <div class="mb-3">
      <new-quote @quoteAdded="addQuote($event)"></new-quote>
    </div>
    <!-- Quote list -->
    <div>
      <quotes :quotes="quotes" :deleteQuote="deleteQuote"></quotes>
    </div>
    <!-- Footer -->
    <div class="alert alert-info text-center" role="alert">
        Info: Click on a Quote to delete it
    </div> 
  </div>  
</template>

<script>
import NewQuote from "./components/NewQuote";
import Quotes from "./components/Quotes"; 
import Progress from "./components/Progress";

export default {
  data: function() {
    return {
      quotes: [],
      maxQuotes: 10,
    }
  },

  methods: {
    addQuote(quote) {
      if (this.quotes.length >= this.maxQuotes) {
        return alert("You already added the maximum of 10 Quotes");
      };
      this.quotes.push(quote);
    },

    deleteQuote(index) {
      this.quotes.splice(index, 1);
    }
  },

  components: {
    "newQuote": NewQuote,
    "quotes": Quotes,
    "quote-progress": Progress,
  }
}
</script>