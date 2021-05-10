<template>
  <div class="art">
    <h1>Art</h1>

    <div v-for="art in artWorks" :key="art.title">
        <div>{{art.title}}</div>
        <div>{{art.artist}}</div>
        <img :src="`../assets/${art.img}`"/>
    </div>

  </div>
</template>

<script>
export default {
    name: 'Art',
    data(){
        return{
            artWorks:[
                
                {title:'Tink',artist:'Demonyia Lewis',img:'Tink.png'},
                {title:'Lindsey',artist:'Demonyia Lewis',img:'Tink.png'},
                {title:'Bystander',artist:'Demonyia Lewis',img:'Tink.png'},

            ],

            alignments: [
            'start',
            'center',
            'end',
            ],
        }
    }
}
</script>

