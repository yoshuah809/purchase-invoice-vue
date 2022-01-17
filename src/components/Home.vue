<template>
	<b-container>
		<b-row>
			<b-col>
				<h1>Welcome to this course</h1>
			</b-col>
		</b-row>
		<b-row>
			<b-col v-for="net in network" :key="net.net" class="text-center">
				<b-link :href="net.url" target="_blank">
					<b-alert :variant="net.color" show> {{ net.net }}</b-alert>
				</b-link>
			</b-col>
		</b-row>
	</b-container>
</template>

<script>
export default {
	name: "Home",
	data() {
		return {
			network: [
				{
					net: "Facebook",
					url: "https://facebook.com",
					color: "info",
				},
				{
					net: "tweeter",
					url: "https://tweeter.com",
					color: "danger",
				},
			],
		};
	},
};
</script>

<style lang="stylus" scoped></style>
