<template>
    <v-navigation-drawer v-model="drawer" fixed app mobile-break-point=720>
        <!-- list -->
        <v-list dense>
            <!-- home tile -->
            <v-list-tile @click="">
                <v-list-tile-action>
                    <v-icon>home</v-icon>
                </v-list-tile-action>
                <v-list-tile-title>Visão Geral</v-list-tile-title>
            </v-list-tile>
            <!-- group -->
            <v-list-group v-for="section in sections" :key="section.text" :prepend-icon="section.icon">
                <!-- group name -->
                <template v-slot:activator>
                    <v-list-tile>
                        <v-list-tile-title>{{section.text}}</v-list-tile-title>
                    </v-list-tile>
                </template>
                <!-- group item -->
                <v-list-tile v-for="item in section.items" :key="item" @click="">
                    <v-list-tile-title>{{item}}</v-list-tile-title>
                </v-list-tile>
            </v-list-group>
            <!-- item -->
            <v-list-tile @click="">
                <v-list-tile-action>
                    <v-icon>dns</v-icon>
                </v-list-tile-action>
                <v-list-tile-title>Requisitos</v-list-tile-title>
            </v-list-tile>
            <!-- item -->
            <v-list-tile @click="">
                <v-list-tile-action>
                    <v-icon>poll</v-icon>
                </v-list-tile-action>
                <v-list-tile-title>Relatórios</v-list-tile-title>
            </v-list-tile>
            <v-divider></v-divider>
            <!-- item -->
            <v-list-tile @click="">
                <v-list-tile-action>
                    <v-icon>donut_small</v-icon>
                </v-list-tile-action>
                <v-list-tile-title>GAP - Gestão de Aspectos e Perigos</v-list-tile-title>
            </v-list-tile>
            <!-- item -->
            <!-- item -->
            <v-list-tile @click="">
                <v-list-tile-action>
                    <v-icon>feedback</v-icon>
                </v-list-tile-action>
                <v-list-tile-title>Notícias</v-list-tile-title>
            </v-list-tile>
            <!-- item -->
            <v-list-tile @click="">
                <v-list-tile-action>
                    <v-icon>help</v-icon>
                </v-list-tile-action>
                <v-list-tile-title>Ajuda</v-list-tile-title>
            </v-list-tile>
            <!-- item -->
            <v-list-tile @click="">
                <v-list-tile-action>
                    <v-icon>info</v-icon>
                </v-list-tile-action>
                <v-list-tile-title>Sobre</v-list-tile-title>
            </v-list-tile>
        </v-list>
        

    </v-navigation-drawer>
    
</template>
<script>
  export default {
    data: () => ({
      drawer: null,
      sections: [
          { text: 'Ações', icon: 'assignment_turned_in', items: ['Documentos Legais', 'Monitoramento', 'Adequação']},
          { text: 'Manutenção de Dados', icon: 'library_books', items: ['Clientes', 'Fornecedores', 'Documentos']},
          { text: 'Levantamentos', icon: 'assignment', items: ['Aspectos', 'Perigos']},
      ]
    }),
    props: {
      source: String
    }
    
  }
</script>