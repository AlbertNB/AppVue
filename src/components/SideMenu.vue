<template>
    <v-navigation-drawer app
    dark
    permanent
    >
      <v-list>
         <v-list-tile avatar>
           <v-list-tile-avatar>
             <img v-bind:src= "user.picture">
           </v-list-tile-avatar>
           <v-list-tile-content>
             <v-list-tile-title>{{user.name}}</v-list-tile-title>
             <v-list-tile-sub-title>{{user.role}}</v-list-tile-sub-title>
           </v-list-tile-content>
         </v-list-tile>
         <v-divider></v-divider>

        <v-list-tile
        v-for="item in menu"
        :key="item.title"
        class="my-1"
        @click=""
      >
        <v-list-tile-action>
          <v-icon>{{ item.icon }}</v-icon>
        </v-list-tile-action>

        <v-list-tile-content>
          <v-list-tile-title>{{ item.title }}</v-list-tile-title>
        </v-list-tile-content>
      </v-list-tile>
      </v-list>  
    </v-navigation-drawer> 
</template>

<script>

export default {
  data () {
    return {
      user: {name: 'Jorge da Borracharia', picture: 'https://randomuser.me/api/portraits/men/85.jpg',role: 'Gerente'},
      menu: [
          { title: 'Pagina Inicial', icon: 'fas fa-republican' },
          { title: 'Usuarios', icon: 'fas fa-user' },
          { title: 'Clientes', icon: 'fas fa-users' },
          { title: 'Produtos', icon: 'fas fa-gift' },
          { title: 'Vendas', icon: 'fas fa-shopping-cart' },
          { title: 'Relatórios', icon: 'fas fa-chart-bar' }
        ]
    }
  }
}
</script>