

<template>
  <div class="dashboard">
    <h1 class="subheading grey--text">This is an dashboard page</h1>

    <v-container class="my-5">
      <v-card flat class="pa-3" v-for="project in projects" :key="project.title">
        <v-layout row wrap :class="`pa-3 project ${project.status}`">

          <v-flex xs12 md6 bl1>
            <div class="caption grey--text" >Project title</div>
            <div>{{project.title}}</div>
          </v-flex>

          <v-flex xs6 sm4 md2 bl2>
            <div class="caption grey--text">Person</div>
            <div>{{project.person}}</div>
          </v-flex>

          <v-flex xs6 sm4 md2 bl2>
            <div class="caption grey--text">Due by</div>
            <div>{{project.due}}</div>
          </v-flex>

          <v-flex xs6 sm4 md2 bl2>
            <div class="caption grey--text"><span>status</span></div>
            <div><span :class="`status ${project.status}`">{{project.status}}</span></div>
          </v-flex>
        </v-layout>
      </v-card>
    </v-container>
  </div>
</template> 

<script>
export default {
  data() {
    return {
      projects: [
        {
          title: "Amadey",
          person: "John",
          due: "1st Jan 2016",
          status: "in_progress",
          content:
            "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Obcaecati illo, dolorum quia praesentium quam totam quo magni architecto numquam necessitatibus pariatur dolor! Eveniet iure repellendus magni explicabo tempore similique nisi."
        },
        {
          title: "Google",
          person: "Anna",
          due: "1st Jan 2011",
          status: "complete",
          content:
            "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Obcaecati illo, dolorum quia praesentium quam totam quo magni architecto numquam necessitatibus pariatur dolor! Eveniet iure repellendus magni explicabo tempore similique nisi."
        },
        {
          title: "Sabryn",
          person: "David",
          due: "10st Dec 2007",
          status: "not_started",
          content:
            "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Obcaecati illo, dolorum quia praesentium quam totam quo magni architecto numquam necessitatibus pariatur dolor! Eveniet iure repellendus magni explicabo tempore similique nisi."
        },
        {
          title: "Foldex",
          person: "Yan",
          due: "1st Jul 2017",
          status: "complete",
          content:
            "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Obcaecati illo, dolorum quia praesentium quam totam quo magni architecto numquam necessitatibus pariatur dolor! Eveniet iure repellendus magni explicabo tempore similique nisi."
        },
        {
          title: "Google",
          person: "Brian",
          due: "1st Sep  2019",
          status: "pending",
          content:
            "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Obcaecati illo, dolorum quia praesentium quam totam quo magni architecto numquam necessitatibus pariatur dolor! Eveniet iure repellendus magni explicabo tempore similique nisi."
        },
        {
          title: "Scambler",
          person: "Garry",
          status_bg: "red",
          due: "1st Sep  2007",
          status: "failure",
          content:
            "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Obcaecati illo, dolorum quia praesentium quam totam quo magni architecto numquam necessitatibus pariatur dolor! Eveniet iure repellendus magni explicabo tempore similique nisi."
        }
        
      ]
    };
  }
};
</script>

<style>
</style>