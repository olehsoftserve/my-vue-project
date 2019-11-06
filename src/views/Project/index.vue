<template>
  <div class="project">
   
    <div class="slot">Projects</div>

    <v-container class="my-5">

      <v-expansion-panels >
        
        <v-expansion-panel v-for="project in myProjects" :key="project.title" >
          
          <v-expansion-panel-header>{{ project.title }}</v-expansion-panel-header>
          
          <v-expansion-panel-content>

              <v-card-text class="px-4 grey--text">

                <div class="font-weight-bold">due by{{project.due}}</div>
                <div>{{project.content}}</div>

              </v-card-text>

          </v-expansion-panel-content>

        </v-expansion-panel>

      </v-expansion-panels>

    </v-container>
  
  </div>
  
</template>

<script>

export default {
  data() {
    return {
      projects: [
        
        {title: "Amadey",person: "David",due: "17st Jan 2016",status: "in_progress",content:"Lorem ipsum, dolor sit amet consectetur adipisicing elit. Obcaecati illo, dolorum quia praesentium quam totam quo magni architecto numquam necessitatibus pariatur dolor! Eveniet iure repellendus magni explicabo tempore similique nisi."},
        {title: "Google",person: "Anna",due: "10st Jan 2011",status: "complete",content:"Lorem ipsum, dolor sit amet consectetur adipisicing elit. Obcaecati illo, dolorum quia praesentium quam totam quo magni architecto numquam necessitatibus pariatur dolor! Eveniet iure repellendus magni explicabo tempore similique nisi."},
        {title: "Sabryn",person: "John",due: "10st Dec 2007",status: "not_started",content:"Lorem ipsum, dolor sit amet consectetur adipisicing elit. Obcaecati illo, dolorum quia praesentium quam totam quo magni architecto numquam necessitatibus pariatur dolor! Eveniet iure repellendus magni explicabo tempore similique nisi."},
        {title: "Foldex",person: "Yan",due: "27st Jul 2017", status: "complete",content:"Lorem ipsum, dolor sit amet consectetur adipisicing elit. Obcaecati illo, dolorum quia praesentium quam totam quo magni architecto numquam necessitatibus pariatur dolor! Eveniet iure repellendus magni explicabo tempore similique nisi."},
        {title: "Hubble",person: "John",due: "9st Sep  2019",status: "pending",content:"Lorem ipsum, dolor sit amet consectetur adipisicing elit. Obcaecati illo, dolorum quia praesentium quam totam quo magni architecto numquam necessitatibus pariatur dolor! Eveniet iure repellendus magni explicabo tempore similique nisi."},
        {title: "Scrambler",person: "Garry",due: "7st Sep  2007",status: "failure",content:"Lorem ipsum, dolor sit amet consectetur adipisicing elit. Obcaecati illo, dolorum quia praesentium quam totam quo magni architecto numquam necessitatibus pariatur dolor! Eveniet iure repellendus magni explicabo tempore similique nisi."}
      ]
  }
},
computed: {
  myProjects() {
    return this.projects.filter(project => {
      return project.person === "John"
      })
    }
   }
}
</script>

<style>
</style>