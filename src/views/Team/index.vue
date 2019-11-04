<template>
  <div class="team">
    <!--h1 class="subheading grey--text">This is team page</h1-->

    <v-container class="my-5">
      <v-layout row wrap my-3>
        <v-flex xs12 sm6 md4 lg3 v-for="person in team" :key="person.name" my-3 mx-3>
          <v-card flat class="text-center ma-3" outlined>
            <v-responsive class="pt-4">
              <v-avatar size="100">
                <img :src="person.avatar">
              </v-avatar>
            </v-responsive>
            <v-card-text>
              <div class="subheading">{{person.name}}</div>
              <div class="grey--text">{{person.role}}</div>
            </v-card-text>
            <v-card-actions>
              <v-btn class=" message v-btn--flat theme--light grey--text">
                <v-icon small right >message</v-icon>
                <span class="pa-3 grey--text">message</span>
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
  </div>
</template>


<script>
// @ is an alias to /src

export default {
  data() {
    return {
      team: [
        {
          name: "Yan",
          role: "CEO",
          avatar:'https://png.pngtree.com/svg/20161212/f93e57629c.svg'
        },
        {
          name: "Anna",
          role: "Project Manager",
          avatar:'https://png.pngtree.com/svg/20161212/f93e57629c.svg'
        },
        { 
          name: "George", 
          role: "Designer",
          avatar:'https://png.pngtree.com/svg/20161212/f93e57629c.svg'
         },
        {
          name: "Veronika",
          role: "Software Font-end Developer",
          avatar:'https://png.pngtree.com/svg/20161212/f93e57629c.svg'
        },
        {
          name: "David",
          role: "Software Developer",
          avatar:'https://png.pngtree.com/svg/20161212/f93e57629c.svg'
        },
        {
          name: "Den",
          role: "Software Developer",
          avatar:'https://png.pngtree.com/svg/20161212/f93e57629c.svg'
        },
        {
          name: "Elison",
          role: "Software Developer",
          avatar:'https://png.pngtree.com/svg/20161212/f93e57629c.svg'
        },
        {
          name: "Nicole",
          role: "Software Developer",
          avatar:'https://png.pngtree.com/svg/20161212/f93e57629c.svg'
        },
        {
          name: "Lee",
          role: "Automation Tester",
          avatar:'https://png.pngtree.com/svg/20161212/f93e57629c.svg'        },
        {
          name: "Brandon",
          role: "Automation Tester",
          avatar:'https://png.pngtree.com/svg/20161212/f93e57629c.svg'
        },
        {
          name: "Peter",
          role: "Manual QA",
          avatar:'https://png.pngtree.com/svg/20161212/f93e57629c.svg'
        },
        {
          name: "Jessica",
          role: "Manual QA",
          avatar:'https://png.pngtree.com/svg/20161212/f93e57629c.svg'
        }
      ]
    };
  }
};
</script>