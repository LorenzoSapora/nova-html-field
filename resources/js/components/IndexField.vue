<template>
    <div :class="`text-${field.textAlign}`">
        <template v-if="hasValue">
            <div v-html="field.value"></div>
        </template>
        <p v-else>&mdash;</p>
    </div>
</template>

<script>
export default {
    props: ['resourceName', 'field'],

    computed: {
        /**
         * Determine if the field has a value other than null.
         */
        hasValue() {
            return this.field.value !== null
        },
    },
}
</script>
