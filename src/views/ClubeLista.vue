<template>
  <v-container>
      <h2 class="text-h5 text-center mb-3 mt5">
          Classificação
      </h2>

  <v-simple-table>
    <template v-slot:default>
      <thead>
        <tr>
            
          <th colspan="2" class="text-left">
            Clubes
          </th>
          <th class="text-left">
            Pontos
          </th>
        </tr>
        
      </thead>
      <tbody>
        <tr v-for="(clube, index) of clubesLista" :key="clube.id">
           <td>{{index+1}}</td>
           <td> </td>
          <td><v-avatar>
                <img
                    :src="clube.escudo"
                    :alt="clube.nome"
                >
                </v-avatar>{{ clube.nome  }}</td>
            <td>{{ clube.pontos  }}</td>
        </tr>
      </tbody>
    </template>
  </v-simple-table>

  </v-container>
</template>

<script>
export default {
    name: 'ClubeLista',
    data() {
        return {
            clubesLista: []
        }
    },
    created() {
        fetch('https://hackthon-decola.firebaseio.com/clubes-lista.json')
        .then(resposta => resposta.json())
        .then(json =>
                this.clubesLista = json)
                console.log(this.clubesLista)
            }

}
</script>

<style scoped>

</style>