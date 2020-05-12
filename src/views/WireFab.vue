<template>
	<v-app>
		<v-content>
			<v-container>
				<v-row>
					<div class="display-1">Calculator for wire fabrication</div>
				</v-row>
				<v-form>
					<v-row class="pt-5">
						<v-col class="align-self-center">
							<div class="body-1">Precursor diameter (mm)</div>
						</v-col>
						<v-col class="align-self-center">
							<v-text-field label="Enter Precursor diameter" v-model="predia" required></v-text-field>
						</v-col>
						<v-col class="align-self-center">
							<div class="body-1">(mm)</div>
						</v-col>
					</v-row>

					<v-row class="">
						<v-col class="align-self-center">
							<div class="body-1">Precursor length (mm)</div>
						</v-col>
						<v-col class="align-self-center">
							<v-text-field label="Enter Precursor length" required v-model="prelen"></v-text-field>
						</v-col>
						<v-col class="align-self-center">
							<div class="body-1">(mm)</div>
						</v-col>
					</v-row>

					<v-row class="">
						<v-col class="align-self-center">
							<div class="body-1">Fabricated diameter (mm)</div>
						</v-col>
						<v-col class="align-self-center">
							<v-text-field label="Enter Fabricated diameter" required v-model="fabdia"></v-text-field>
						</v-col>
						<v-col class="align-self-center">
							<div class="body-1">(mm)</div>
						</v-col>
					</v-row>

					<v-row >
						<v-col class="align-self-center">
										<v-dialog v-model="dialog" width="500">
												<template v-slot:activator="{ on }">
														<v-btn v-on="on" color='deep-purple white--text' v-on:click="pForm">Submit</v-btn>
												</template>
												<v-card class="text-left">
																<v-card-title primary-title class="headline grey lighten-2">
																				Result
																</v-card-title>
																<v-card-text class="pt-5">
																				The fabricated wire's length is <span class="title">{{ respfablen }}</span> (mm) !!
																</v-card-text>
																<v-divider></v-divider>
																<v-card-actions>
																	<v-spacer></v-spacer>
																		<v-btn text @click="dialog = false">
																						Close
																		</v-btn>
																</v-card-actions>
												</v-card>
										</v-dialog>
						</v-col>
					</v-row>
				</v-form>

			</v-container>
		</v-content>

	</v-app>

</template>

<script>
import axios from 'axios'

export default {
				data: () => ({
								dialog: false,
								predia: null,
								prelen: null,
								fabdia: null,
								respfablen: null,
				}),

				methods: {
								pForm: function() {
												let params = new URLSearchParams()
												params.append("predia", this.predia)
												params.append("prelen", this.prelen)
												params.append("fabdia", this.fabdia)
												axios.post('http://localhost:1000', params
												).then((response) => {
																console.log(response)
																this.respfablen = response.data.Fablen
												})

								}
				}
}
</script>
