<template>
    <div class="home-container">
        <listing-summary-group
            v-for="(group, country) in listing_groups"
            :key="country"
            :listings="group"
            :country="country"
            class="listing-summary-group">
        </listing-summary-group>
    </div>
</template>

<script>
    import { groupByCountry } from '../js/helpers';
    import ListingSummaryGroup from './ListingSummaryGroup.vue';

    export default {
        computed: {
            listing_groups() {
                return groupByCountry(this.$store.state.listing_summaries);
            }
        },
        components: {
            ListingSummaryGroup
        }
    }
</script>
