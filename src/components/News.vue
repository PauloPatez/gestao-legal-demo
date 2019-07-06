<template>
    <v-card>
        <v-card-title primary-title v-for="i in news" :key={i}>

            <v-subheader>{{i.date}}</v-subheader>
          <v-divider/>

            <h3 class="headline mb-0" style="cursor: pointer">{{i.title}}</h3>
            <br/>
            <div>
              {{i.text}}
            </div>

        </v-card-title>
        <v-divider/>
        <br/>
        <v-card-actions>
          <v-spacer/>
          <v-btn>Ver Tudo</v-btn>
        </v-card-actions>
    </v-card>
</template>

<script>
export default {
    data: () => ({
      news: [
        {
          title: "Cronograma de implantação do eSocial dos eventos de Segurança e Saúde no Trabalho é prorrogado",
          text: "O Ministério da Economia publicou no Diário Oficial da União em 05/07/2019 a Portaria SEPREVT nº 716/2019 que prorroga o cronograma de entrega do eSocial referente a obrigatoriedade de envio dos eventos periódicos para as empresas constantes no Grupo 3 e de todos os eventos de SST...",
          date: "05/07/2019"
        },
        {
          title: "Representantes do eSocial propõem simplificação e prorrogação das obrigatoriedades relativas à prestação das informações de Saúde e Segurança...",
          text: "Durante encontro dos representantes envolvidos no eSocial na ENAP - Escola Nacional de Administração Pública foram definidas mudanças previstas para a simplificação da plataforma. Estava na pauta dos debatedores a revisão de todo o leiaute, de forma a eliminar informações redundan...",
          date: "28/06/2019"
        },
        {
          title: "Alteração no Processo de Licenciamento Simplificado – PTS – Corpo de Bombeiros da Bahia",
          text: "A partir do dia 10/06/2019 (segunda-feira), os Processos de Licenciamento Simplificado (PTS) deverão ser apresentados em no mínimo duas vias, sendo uma em meio físico e uma em meio eletrônico no formato PDF, contendo todos os documentos pertinentes ao processo devidamente preenchi...",
          date: "18/06/2019"
        },
      ]
    }),
}
</script>