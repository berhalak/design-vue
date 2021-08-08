<template>
	<div class="absolute inset-0 bg-gray-500 bg-opacity-40" v-if="show">
		<div
			class="
				absolute
				inset-5
				bg-white
				p-4
				border
				rounded
				overflow-y-auto
			"
		>
			<slot />
		</div>
	</div>
</template>

<script>
export default {
	data() {
		return {
			show: false,
		};
	},
	methods: {
		open() {
			this.show = true;
		},
		close() {
			this.show = false;
		},
	},
};
</script>