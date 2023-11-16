<template>
  <v-app-bar flat>
    <template v-slot:prepend>
      <v-app-bar-nav-icon></v-app-bar-nav-icon>
    </template>
    <v-app-bar-title>Shopio</v-app-bar-title>
    <v-spacer></v-spacer>
    <v-text-field density="compact" variant="solo" label="Search products" append-inner-icon="mdi-maginify" single-line hide-details flat></v-text-field>
    <v-spacer></v-spacer>
    <button @click="downloadii(appi)">
        <v-icon color="success">mdi mdi-download-circle-outline</v-icon>
      {{ appi.name }}
    </button >
    <v-btn>
      Sign In / Login
    </v-btn>
 </v-app-bar>
</template>
<script>
import axios from "axios"
export default {
data(){
  return{
    appi:{
      name:'zoom',
      url:"https://zoom.us/client/latest/ZoomInstaller.exe"
    }
  }
},
methods:{
  forceFileDownload(response, item) {
    let headers = response.headers;
    let extension = item.url.substring(item.url.lastIndexOf('.' + 1))
    let blob = new Blob([response.data], {type: headers['content-type']})
    let link = document.createElement('a');
    link.href = window.URL.createObjectURL(blob);
    link.download = `${item.name}.${extension}`;
    link.click();
    link.remove();
  },
  downloadii:function(item) {
    axios({
      method: 'get',
      url: item.url,
      responseType: 'blob'
    })
    .then(response =>{
      this.forceFileDownload(response, this.appi)
    })
    .catch(() => console.log('error occured'))
  }
}
}
</script>

<style>

</style>
