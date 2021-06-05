<template>
  <div>
    <task-viewer title="My list" :tasks-list="tasksList" />
  </div>
</template>

<script>
import TaskViewer from "./components/TaskViewer.vue";

export default {
  name: "App",
  components: {
    TaskViewer,
  },
  data() {
    return {
      tasksList: [
        {
          id: 1,
          category: 1,
          title: "Client meeting",
          users: [
            {
              name: "Ivan",
              photo:
                "http://s1.iconbird.com/ico/0612/vistabasesoftwareicons/w256h2561339252913User1.png",
            },
            {
              name: "Petro",
              photo:
                "http://s1.iconbird.com/ico/1012/EcommerceBusinessIcons/w256h2561350822895admin256x256.png",
            },
          ],
        },
        {
          id: 2,
          category: 2,
          title: "Plan webinar",
          users: [
            {
              name: "Petro",
              photo:
                "http://s1.iconbird.com/ico/1012/EcommerceBusinessIcons/w256h2561350822895admin256x256.png",
            },
            {
              name: "Sasha",
              photo:
                "http://s1.iconbird.com/ico/0712/iconshockrealvista/w400h4001341689813administrator.png",
            },
            {
              name: "Yana",
              photo:
                "http://s1.iconbird.com/ico/0612/practika/w256h2561339698323user.png",
            },
          ],
        },
      ],
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
