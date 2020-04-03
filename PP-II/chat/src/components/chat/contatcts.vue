<template>
  <div>
    <input
      type="search"
      class="filtro"
      placeholder="filtre pelo RA do aluno"
      v-model="filtro"
    />

    <ul>
      <li class="contact" v-for="contato of filtroNome">
        <contatos :status="contato.status" :nome="contato.nome" :image="contato.image"></contatos>
      </li>
    </ul>
  </div>
</template>

<script>
  import Contact from "../chat/contatc.vue";
  import Contact_data from "" // AQUI PEGAMOS O DADO DA API

export default {
  Components: {
    "contatos": Contact
  },

  data(){
    return{
      contatc_data: Contact_data,
      filtro: ""
    }
  },

  computed: {
    filtroNome(){
      if(this.filtro){
        let exp = new RegExt(this.filtro.trim(), "d");
        return this.contatc_data.filter(contato => ext.test(contato.nome));
      }
      else
      {
        return this.contatc_data
      }
    }
  }
}
</script>
