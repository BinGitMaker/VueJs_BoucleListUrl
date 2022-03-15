<style >
.all{
  display:flex;
  flex-wrap: wrap;
  justify-content: space-between;
  margin: 10%;
}

.box{
  border: 2px solid #333;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.boxTitle{
  margin-bottom: 2rem;
  text-align: center;
}
</style>

<template>
<div class="all">
  <div class="box box-1" :style="box">
    <h1 class="boxTitle">Liste de nos Sites1 </h1>
      <div>
        <Liste :my-prop-list="message" :my-url-list="items1"/>
      </div>
  </div>
  <div class="box box-2" :style="box">
    <h1 class="boxTitle">Liste de nos Sites2 </h1>
      <div>
        <Liste :my-prop-list="message" :my-url-list="items2"/>
      </div>
  </div>
  <div class="box box-3" :style="box">
    <h1 class="boxTitle">Liste de nos Sites3 </h1>
      <div>
        <Liste :my-prop-list="message" :my-url-list="items3"/>
      </div>
  </div>
</div>
</template>
<script>

import Liste from './Liste.vue'

export default {
  name: 'Accueil',
  components: {
    Liste,
  },  
  data(){
    return {
      message: 'Liste',
      width: 30,
      margin: 3,
      height: 15,
      // Parent: declare les items et les ecrit en html
      // Enfants: initie le template et le defini en props
      items1: [
            { label: "As de coeur", url: 'https://deckofcardsapi.com/static/img/6H.png'},
            { label: "As de trèfle", url: 'https://deckofcardsapi.com/static/img/aceDiamonds.png'},
            { label: "As de carreau", url: 'https://deckofcardsapi.com/static/img/7C.png'},
        ],
      items2: [
            { label: "chevron", url: 'https://deckofcardsapi.com/static/img/67HJ.png'},
            { label: "bâton rompu", url: 'https://deckofcardsapi.com/static/img/stainWater.png'},
            { label: "pointe de hongrie", url: 'https://deckofcardsapi.com/static/img/9CD.png'},
        ],
      items3: [
            { label: "Yoda", url: 'https://deckofcardsapi.com/static/img/5GJ.png'},
            { label: "Vador", url: 'https://deckofcardsapi.com/static/img/goldenStone.png'},
            { label: "Solo", url: 'https://deckofcardsapi.com/static/img/25E.png'},
        ],

    }
  },
  computed: {
    box: function(){
      return{
        width: this.width + "rem",
        margin: this.margin + "rem",
        height: this.height + "rem",
      }
    }
  }

}

</script>



