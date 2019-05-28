<template>
    <v-app>
        <v-content>
            <v-container fluid grid-list-md box>
                <v-layout row>
                    <v-flex d-flex xs8 fill-height >
                        <v-layout row wrap>
                            <v-flex d-flex xs12  >
                                <v-card min-height="50">
                                    <v-layout row wrap class="light--text mt-3">
                                        <v-flex xs2>Contract ID</v-flex>
                                        <v-flex xs3>Portfolio(SKU)</v-flex>
                                        <v-flex xs3>Stock container</v-flex>
                                        <v-flex xs2>Sort By Date</v-flex>
                                    </v-layout>
                                    <v-layout>
                                        <v-flex xs2>
                                            <v-checkbox label="Contract ID" v-model="checkbox"></v-checkbox>
                                        </v-flex>
                                        <v-flex xs3>
                                            <v-select :items="items" label="Portfolio(SKU)" outline></v-select>
                                        </v-flex>
                                        <v-flex xs3>
                                            <v-select
                                                :items="selectItems"
                                                :nudge-top="-8"
                                                content-class="menu__content--select"
                                                label="Stock container"
                                                offset-y
                                                outline
                                            ></v-select>
                                        </v-flex>
                                        <v-flex xs2>
                                            <v-select
                                                :items="selectItems"
                                                :nudge-top="-8"
                                                content-class="menu__content--select"
                                                label="Date"
                                                outline
                                                offset-y
                                            ></v-select>
                                        </v-flex>
                                        <v-flex xs2><v-btn color="red xs white--text small">Reset</v-btn></v-flex>
                                    </v-layout>
                                </v-card>
                            </v-flex>

                            <v-flex d-flex xs4 >
                                <v-card >
                                    <v-toolbar color="grey lighten-2" light>
                                        <v-toolbar-title class="text-xs-left body-1">Label-1</v-toolbar-title>
                                        <v-spacer></v-spacer>
                                        <v-toolbar-title class="text-xs-right body-1">#152521</v-toolbar-title>
                                    </v-toolbar>
                                    <v-flex>
                                        <v-card-text class="text-xs-left caption">54 SKU Types <v-card-text class="text-xs-right">500 Total Units</v-card-text></v-card-text>
                                    </v-flex>
                                    <v-card-text >Last outward date: 15 May 2019</v-card-text>
                                    <v-footer class="">
                                        <v-btn small  class="text-xs-left white--text ml-0 mr-0 caption pt-0 pb-0" color="red">Add full box to cart</v-btn>
                                        <v-btn small class="text-xs-right white--text ml-0 mr-0 " disabled>Select SKUs</v-btn>
                                    </v-footer>
                                </v-card>
                            </v-flex>
                            <v-flex d-flex xs4>
                                <v-card >
                                    <v-toolbar color="grey lighten-2" light>
                                        <v-toolbar-title class="text-xs-left body-1">Label-1</v-toolbar-title>
                                        <v-spacer></v-spacer>
                                        <v-toolbar-title class="text-xs-right body-1">#152521</v-toolbar-title>
                                    </v-toolbar>
                                    <v-card-text></v-card-text>
                                </v-card>
                            </v-flex>
                            <v-flex d-flex xs4 fill-heigh>
                                <v-card >
                                    <v-toolbar color="grey lighten-2" light>
                                        <v-toolbar-title class="text-xs-left body-1">Label-1</v-toolbar-title>
                                        <v-spacer></v-spacer>
                                        <v-toolbar-title class="text-xs-right body-1 ml-4">#152521</v-toolbar-title>
                                    </v-toolbar>
                                    <v-card-text></v-card-text>
                                </v-card>
                            </v-flex>

                        </v-layout>

                    </v-flex>

                    <v-flex d-flex xs4>
                        <div id="e3" style="max-width: 600px" class="grey lighten-1">
                            <v-toolbar color="grey lighten-2" light>
                                <v-spacer>
                                    <v-toolbar-title height="2px">ORDERS</v-toolbar-title>
                                </v-spacer>
                            </v-toolbar>
                    
                            <v-card>
                                <v-container fluid grid-list-lg>
                                    <div class="mt-0 mb-0">
                                        <v-list-tile-avatar>
                                            <v-icon :class="[item.iconClass]">{{ item.icon }}</v-icon>
                                        </v-list-tile-avatar>
                                        <v-list-tile-content>
                                            <v-list-tile-title class="text-xs-left">Box-1</v-list-tile-title>
                                            <v-list-tile-title class="text-xs-right">Select box</v-list-tile-title>
                                            <v-list-tile-sub-title class="subheading ">All items selected</v-list-tile-sub-title>
                                        </v-list-tile-content>
                                    </div>
                                    <v-divider></v-divider>
                                    <div class="mt-0 mb-0">
                                        <v-list-tile-avatar>
                                            <v-icon :class="[item.iconClass]">{{ item.icon }}</v-icon>
                                        </v-list-tile-avatar>
                                        <v-list-tile-content>
                                            <v-list-tile-title class="text-xs-left">Box-2</v-list-tile-title>
                                            <v-list-tile-title class="text-xs-right">Select box</v-list-tile-title>
                                            <v-list-tile-sub-title class="red--text">25 SKU ^</v-list-tile-sub-title>
                                        </v-list-tile-content>
                                    </div>
                                    <v-divider></v-divider>
                                    <div>
                                        <v-list-tile-avatar>
                                            <v-icon :class="[item.iconClass]">{{ item.icon }}</v-icon>
                                        </v-list-tile-avatar>
                                        <v-list-tile-content>
                                            <v-list-tile-title class="text-xs-left">Shampoo</v-list-tile-title>
                                            <v-list-tile-title class="text-xs-right red--text caption">Remove</v-list-tile-title>
                                            <v-list-tile-title class="text-xs-right black--text caption"><v-icon small dark>remove_circle</v-icon>1</v-list-tile-title>
                                            <v-list-tile-sub-title>Available Quantity  -  5</v-list-tile-sub-title>
                                        </v-list-tile-content>
                                    </div>
                                    <v-divider></v-divider>
                                    <div>
                                        <v-list-tile-avatar>
                                            <v-icon :class="[item.iconClass]">{{ item.icon }}</v-icon>
                                        </v-list-tile-avatar>
                                        <v-list-tile-content>
                                            <v-list-tile-title class="text-xs-left">Shampoo</v-list-tile-title>
                                            <v-list-tile-title class="text-xs-right red--text caption">Remove</v-list-tile-title>
                                            <v-list-tile-sub-title>Available Quantity  -  5</v-list-tile-sub-title>
                                        </v-list-tile-content>
                                    </div>
                                    <v-divider></v-divider>
                                    <div>
                                        <v-list-tile-avatar>
                                            <v-icon :class="[item.iconClass]">{{ item.icon }}</v-icon>
                                        </v-list-tile-avatar>
                                        <v-list-tile-content>
                                            <v-list-tile-title class="text-xs-left">Shampoo </v-list-tile-title>
                                            <v-list-tile-title class="text-xs-right red--text caption">Remove</v-list-tile-title>
                                            <v-list-tile-sub-title>Available Quantity  -  5</v-list-tile-sub-title>
                                        </v-list-tile-content>
                                        <v-list-tile-action>
                                            <v-btn icon>
                                                <v-icon color="grey lighten-1">select box</v-icon>
                                            </v-btn>
                                        </v-list-tile-action>
                                    </div>
                                    <v-divider></v-divider>
                            
                                    <v-card-actions class="mt-5">
                                        <v-btn color="red" block class="white--text">Next</v-btn>
                                    </v-card-actions>
                                </v-container>
                            </v-card>
                        </div>    
                    </v-flex>
                </v-layout>
            </v-container>
        </v-content>
    </v-app>
</template>

<script>
export default {
    name: 'Test',
    props: {
        msg: String
    },
    data () {
        return {
            checkbox: true,
            selectItems: [
                { text: "Portfolio(SKU)", value: 0 },
                { text: "Second Item", value: 1 },
                { text: "Third Item", value: 2 },
                { text: "Fourth Item", value: 3 },
            ],
            items: ['Portfolio(SKU)'],
            item: [
                { icon: 'folder', iconClass: 'grey lighten-1 white--text', title: 'Photos', subtitle: 'Jan 9, 2014' },
            ],
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

</style>
