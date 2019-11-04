
<template>
  <div class="dashboard">
    <!--h1 class="subheading grey--text">This is an dashboard page</h1-->

    <v-container class="my-5">
      <v-layout>
        <span class="caption text-lowercsase pa-1 grey--text mb-5"></span>
        <v-tooltip top>
          <template v-slot:activator="{ on }">
            <v-btn small flat color="grey--text" @click="sortBy('title')" v-on="on">
              <v-icon left small>folder</v-icon>
              <span right class="caption text-uppercase">project</span>
            </v-btn>
          </template>
          <span>Sort by project name</span>
        </v-tooltip>
        <v-tooltip top>
          <template v-slot:activator="{ on }">
            <v-btn small flat color="grey--text" @click="sortBy('folder')" v-on="on">
              <v-icon left small>person</v-icon>
              <span right class="caption text-uppercase">person</span>
            </v-btn>
          </template>
          <span>Sort by person name</span>
        </v-tooltip>
        <v-tooltip top>
          <template v-slot:activator="{ on }">
            <v-btn small flat color="grey--text" @click="sortBy('status')" v-on="on">
              <v-icon left small>cached</v-icon>
              <span right class="caption text-uppercase">status</span>
            </v-btn>
          </template>
          <span>Sort by status</span>
        </v-tooltip>

      </v-layout>
      <v-card flat>
        <v-layout row wrap>
          <v-flex xs12 md6>
            <div class="caption grey--text pa-3">Project title</div>
          </v-flex>
          <v-flex xs6 sm4 md2>
            <div class="caption grey--text pa-3">Person</div>
          </v-flex>
          <v-flex xs6 sm4 md2>
            <div class="caption grey--text pa-3">Due by</div>
          </v-flex>
          <v-flex xs6 sm4 md2>
            <div class="caption grey--text pa-3 pr-10" align="right">Status</div>
          </v-flex>
        </v-layout>
      </v-card>

      <v-card flat v-for="project in projects" :key="project.title">
        <v-layout row wrap :class="`pa-3 project ${project.status}`">
          <v-flex xs12 md6>
            <div>{{project.title}}</div>
          </v-flex>

          <v-flex xs6 sm4 md2>
            <div>{{project.person}}</div>
          </v-flex>

          <v-flex xs6 sm4 md2>
            <div>{{project.due}}</div>
          </v-flex>
          <v-flex xs6 sm4 md2>
            <div align="right">
              <v-chip
                small
                :color="`${project.status}`"
                :class="`v-chip--active white--text caption my-2`"
              >{{project.status}}</v-chip>
            </div>
            <!--div><span :class="`status ${project.status}`">{{project.status}}</span></div-->
          </v-flex>
        </v-layout>
        <v-divider></v-divider>
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
          due: "17st Jan 2016",
          status: "in_progress",
          content:
            "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Obcaecati illo, dolorum quia praesentium quam totam quo magni architecto numquam necessitatibus pariatur dolor! Eveniet iure repellendus magni explicabo tempore similique nisi."
        },
        {
          title: "Google",
          person: "Anna",
          due: "10st Jan 2011",
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
          due: "27st Jul 2017",
          status: "complete",
          content:
            "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Obcaecati illo, dolorum quia praesentium quam totam quo magni architecto numquam necessitatibus pariatur dolor! Eveniet iure repellendus magni explicabo tempore similique nisi."
        },
        {
          title: "Google",
          person: "Brian",
          due: "9st Sep  2019",
          status: "pending",
          content:
            "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Obcaecati illo, dolorum quia praesentium quam totam quo magni architecto numquam necessitatibus pariatur dolor! Eveniet iure repellendus magni explicabo tempore similique nisi."
        },
        {
          title: "Scrambler",
          person: "Garry",
          due: "7st Sep  2007",
          status: "failure",
          content:
            "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Obcaecati illo, dolorum quia praesentium quam totam quo magni architecto numquam necessitatibus pariatur dolor! Eveniet iure repellendus magni explicabo tempore similique nisi."
        }
      ]
    };
  },
  methods: {
    sortBy(prop) {
      this.projects.sort((a, b) => (a[prop] < b[prop] ? -1 : 1));
    }
  }
};
</script>
