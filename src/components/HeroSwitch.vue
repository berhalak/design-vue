<template>
	<div style="display: contents">
		<div @click="$refs.modal.open()" style="display: contents">
			<hero :name="icon" class="click"  />
		</div>
		<modal ref="modal">
			<hero-gallery
				@click="
					x => {
						(icon = x), $refs.modal.close();
					}
				"
			/>
		</modal>
	</div>
</template>

<script>
export default {
	props : ["name"],
	data() {
		return {
			icon: this.name || "zoom-out",
		};
	},
};
</script>