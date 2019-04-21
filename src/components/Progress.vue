<template>
    <div>
        <div class="progress">
            <div class="progress-bar" role="progressbar" style="width: 25%" aria-valuenow="25" aria-valuemin="0"           aria-valuemax="100"
                 v-bind:style="{width: (quotesNbr / maxQuotes) * 100 + '%'}">{{ quotesNbr }} / {{ maxQuotes }}
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        "maxQuotes": Number,
        "quotesNbr": Number,
    }
}
</script>