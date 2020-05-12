<template>
  <div class="home">
	<v-app>
		<!--<div>
			<v-app-bar color="deep-purple accent-4" dense dark>
				<v-toolbar-title>Taro's Apps</v-toolbar-title>
				<v-spacer></v-spacer>
			</v-app-bar>
		</div> -->

		<v-content>
			<v-container class="text-left">
				<v-row>
					<v-col>
						<v-card class="pa-2" tile>
							<v-list-item three-line>
								<v-list-item-content>
									<div class="overline mb-4">application</div>
									<v-list-item-title class="headline mb-1">Wire Fab Calculator</v-list-item-title>
									<v-list-item-subtitle>Calculator for wire fabrication</v-list-item-subtitle>
								</v-list-item-content>
							</v-list-item>
							<v-card-actions>
									<v-btn to="/WireFab" text color='deep-purple accent-4'>
										Start
									</v-btn>
							</v-card-actions>
						</v-card>
					</v-col>
					<v-col>
						<v-card class="pa-2" tile>
							<v-list-item three-line>
								<v-list-item-content>
									<div class="overline mb-4">application</div>
									<v-list-item-title class="headline mb-1">Wire Fab Calculator</v-list-item-title>
									<v-list-item-subtitle>Calculator for wire fabrication</v-list-item-subtitle>
								</v-list-item-content>
							</v-list-item>
							<v-card-actions>
									<v-btn to="/WireFab" text color='deep-purple accent-4'>
										Start
									</v-btn>
							</v-card-actions>
						</v-card>
					</v-col>

				</v-row>
			</v-container>
		</v-content>
	</v-app>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Home',
  components: {
  }
}
</script>
