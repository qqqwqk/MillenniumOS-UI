<style scoped>
.chart-height-limit {
	max-height: 320px;
}
</style>

<template>
	<div class="d-flex flex-column">
		<job-progress />

		<v-row class="mt-0" :dense="$vuetify.breakpoint.mobile">
			<v-col order="1" order-md="1" cols="12" sm="6" md="3" xl="2">
				<v-row align="center" :dense="$vuetify.breakpoint.mobile">
					<v-col cols="12">
						<job-control-panel />
					</v-col>
					<v-col cols="12" class="d-none d-sm-block d-md-none">
						<speed-factor-panel />
					</v-col>
				</v-row>
			</v-col>

			<v-col order="0" order-md="2" cols="12" md="5" xl="7" class="d-none d-sm-flex flex-column">
				<mos-job-code-panel class="mb-5" />

				<v-row class="flex-grow-0 flex-shrink-1 d-none d-md-flex">
					<v-col cols="12">
						<job-estimations-panel />
					</v-col>
					<v-col cols="12">
						<job-data-panel />
					</v-col>
				</v-row>

				<v-row class="flex-grow-0 flex-shrink-1 hidden-sm-and-up mt-3">
					<v-col cols="6" md="6">
						<speed-factor-panel />
					</v-col>
				</v-row>
			</v-col>

			<v-col order="2" order-md="3" cols="12" sm="6" md="4" xl="3">
				<v-row :dense="$vuetify.breakpoint.mobile">
					<v-col cols="12" class="hidden-md-and-up">
						<job-data-panel />
					</v-col>
					<v-col cols="12" class="hidden-md-and-up">
						<job-info-panel />
					</v-col>

					<v-col cols="12" class="hidden-sm-only">
						<speed-factor-panel />
					</v-col>
				</v-row>
			</v-col>
		</v-row>
	</div>
</template>

<script lang="ts">
import Vue from "vue";

import { defineComponent } from 'vue';

export default defineComponent({});
</script>
