<template>
    <ul v-if="data && data.length" class="sub-menu">
        <Casitem
            v-for="(item, i) in data"
            :key="item.value + '_' + i"
            :data="item"
            :disabled="disabled"
            @on-change="change"
        >
        </Casitem>
    </ul>
</template>
<script>
    import Casitem from './casitem';

    export default {
        name: 'Caspanel',
        components: {Casitem},
        props: {
            data: Array,
            disabled: Boolean
        },
        data () {
            return {
                
            };
        },
        watch: {
            data () {
                
            }
        },
        methods: {
            change(data) {
                this.$emit('on-change', data);
            }
        },
    };
</script>
