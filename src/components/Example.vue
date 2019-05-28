<template>
    <v-app>
        <v-content>
            <v-container fluid grid-list-md box>
                <v-layout row>
                    <v-flex d-flex xs8 fill-height >
                        <v-layout row wrap>

                            <v-flex d-flex xs8 >
                                <div id="e3" style="max-width: 600px" class="grey lighten-1">
                                    <v-card >
                                        <v-toolbar color="grey lighten-2" light>
                                            <v-toolbar-title class="text-xs-left body-1">Box 1</v-toolbar-title>
                                            <v-spacer></v-spacer>
                                            <v-toolbar-title class="text-xs-center body-1">#6266161</v-toolbar-title><v-spacer></v-spacer>
                                            <v-toolbar-title class="text-xs-right"><v-icon>close</v-icon></v-toolbar-title>
                                        </v-toolbar>
                                        <v-flex>
                                            <v-card-text class="text-xs-left caption">50 SKU Types <v-card-text class="text-xs-right">Select All Items<i class="material-icons">check_box_outline_blank</i></v-card-text></v-card-text>
                                        </v-flex>
                                        <div class="mt-0 mb-0 ml-2 mr-2">
                                            <v-list-tile-avatar>
                                                <v-icon :class="[item.iconClass]">{{ item.icon }}</v-icon>
                                            </v-list-tile-avatar>
                                            <v-list-tile-content>
                                                <v-list-tile-title class="text-xs-left">Shampoo</v-list-tile-title>
                                                <v-list-tile-title class="text-xs-center">Quantity Available 25 Unit</v-list-tile-title>
                                                <v-list-tile-title class="text-xs-right"><i class="material-icons">remove_circle </i> 1 <i class="material-icons">add_circle</i><i class="material-icons">check_box</i></v-list-tile-title>
                                                <v-list-tile-sub-title class="subheading ">#15515</v-list-tile-sub-title>
                                            </v-list-tile-content>
                                        </div>
                                        <v-divider></v-divider>
                                        <div class="mt-0 mb-0 ml-2 mr-2">
                                            <v-list-tile-avatar>
                                                <v-icon :class="[item.iconClass]">{{ item.icon }}</v-icon>
                                            </v-list-tile-avatar>
                                            <v-list-tile-content>
                                                <v-list-tile-title class="text-xs-left">Shampoo</v-list-tile-title>
                                                <v-list-tile-title class="text-xs-center">Quantity Available 25 Unit</v-list-tile-title>
                                                <v-list-tile-title class="text-xs-right"><i class="material-icons">remove_circle </i> 1 <i class="material-icons">add_circle</i><i class="material-icons">check_box_outline_blank</i></v-list-tile-title>
                                                <v-list-tile-sub-title class="subheading ">#15515</v-list-tile-sub-title>
                                            </v-list-tile-content>
                                        </div>
                                        <v-divider></v-divider>
                                        <div class="mt-0 mb-0 ml-2 mr-2">
                                            <v-list-tile-avatar>
                                                <v-icon :class="[item.iconClass]">{{ item.icon }}</v-icon>
                                            </v-list-tile-avatar>
                                            <v-list-tile-content>
                                                <v-list-tile-title class="text-xs-left">Shampoo</v-list-tile-title>
                                                <v-list-tile-title class="text-xs-center">Quantity Available 25 Unit</v-list-tile-title>
                                                <v-list-tile-title class="text-xs-right"><i class="material-icons">remove_circle </i> 1 <i class="material-icons">add_circle</i><i class="material-icons">check_box</i></v-list-tile-title>
                                                <v-list-tile-sub-title class="subheading ">#15515</v-list-tile-sub-title>
                                            </v-list-tile-content>
                                        </div>
                                        <v-divider></v-divider>
                                        <v-footer class="mt-5">
                                            <v-btn  class="text-xs-left white--text caption" block color="red">Cancel   </v-btn>
                                            <v-btn  class="text-xs-right white--text " block disabled>Add to Cart</v-btn>
                                        </v-footer>
                                    </v-card>
                                </div>
                            </v-flex>
                        </v-layout>

                    </v-flex>
                </v-layout>
            </v-container>
        </v-content>
    </v-app>
</template>

<script>
export default {
    name: 'Exam',
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
