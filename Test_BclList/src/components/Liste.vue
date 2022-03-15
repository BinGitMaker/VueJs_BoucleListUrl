<style >
.urlText{
    overflow-wrap: anywhere;
    margin-right : 10%;
    text-align: start;
    text-decoration: none;
}

</style>

<template>

<div>
    <ul id="list-1">
        <template v-for="item in myUrlList" :key="item" >
            <li>
                <p v-html="hideUrl(item)"></p>
                </li>
            <!-- li class="urlText">{{ item.url }}</li> -->
        </template>
    </ul>
    
</div>

</template>

<script>


export default {
   name: 'Liste',
    data(){
        return{
            parentUrl:"Nos Listes",
            
        }
    },
    props: {
        myPropList:{
            type: String,
            default: () => ''
        },
        myUrlList:{
            type: Array,
            dafaut: () => []
        }
    },
  methods: {
    hideUrl: function(item) {
        return '<a href="'+item.url+'">'+ item.label +'</a>'
        /* console.log(item) */
      }
    }
}
</script>