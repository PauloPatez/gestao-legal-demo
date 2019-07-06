<template>
  <v-content>
      <v-container fluid grid-list-md text-xs-center>
        <v-layout wrap>


          <v-flex md12 lg8>
            <v-layout wrap>

              <v-flex row grow v-for="i in 1" :key="`6${i}`" xs12>
                <!-- Calendar Card -->
                <v-card-title primary-title>
                    <div class="headline">Agenda de Tarefas</div>
                </v-card-title>
                <v-card color="">
                  
                  <div class="pa-2">
                    <Calendar/>
                      <v-card-actions>
                        <v-spacer></v-spacer>
                        <v-btn> Ver Tudo </v-btn>
                      </v-card-actions>
                  </div>
                </v-card>
                <!-- Calendar Card -->
              </v-flex>

              <v-flex row grow md12 lg6 v-for="i in 1" :key={i}>
                <v-card-title primary-title>
                  <div class="headline">Estatísticas de ações</div>
                </v-card-title>
                <v-card>
                  <ActionsChart/>
                  <!-- <v-card-title primary-title>
                    <div class="headline">Estatísticas de ações</div>
                  </v-card-title> -->
                </v-card>
              </v-flex>
              <v-flex row grow md12 lg6 v-for="i in 1" :key={i}>
                <v-card-title primary-title>
                  <div class="headline">Estatísticas de Requisitos</div>
                </v-card-title>
                <v-card>
                  <ReqChart/>
                  <!-- <v-card-title primary-title>
                    <div class="headline">Estatísticas de Requisitos</div>
                  </v-card-title> -->
                </v-card>
              </v-flex>
            </v-layout>
          </v-flex>

          <v-flex md12 lg4>
            <v-layout>
              <v-flex>
                <v-card-title primary-title>
                  <div class="headline">Últimas Notícias</div>
                </v-card-title>
                <News/>
              </v-flex>

            </v-layout>
          </v-flex>

        </v-layout>
        <br/>
        <br/>
      </v-container>
      
    </v-content>
</template>

<script>
  import Calendar from './Calendar'
  import ActionsChart from './ActionsChart'
  import ReqChart from './ReqChart'
  import News from './News'
  export default {
    data: () => ({

    }),
    components: {
      Calendar,
      ActionsChart,
      ReqChart,
      News
    }
  }
</script>

<style>

</style>
