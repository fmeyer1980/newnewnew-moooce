<template>
    <img :src="$urlFor(asset).width(800)" :alt="asset.alt" />
</template>

<script>
	export default {
		name: "ContentImage",
        props:{
            asset:Object,
            default: () => {
                return {}
            }
        }
    }
</script>
