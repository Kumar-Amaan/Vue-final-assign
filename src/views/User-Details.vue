<template>
  <div>
        <div v-if="loading">Please wait......</div>
    <div v-else>
      <div v-if="users.length === 0">No User exists</div>
      <div v-else>
        <div v-for="(user, index) of users" :key="index">
          <strong class="st"> {{ user.id }} </strong>
          <div v-for="(user, index) of users" :key="index"></div>
          <strong class="st1">
            Name: {{ user.name }}<br />
            UserName: {{ user.username }}<br />
            EmailId: {{ user.email }}<br />
            PhoneNo: {{ user.phone }}<br />
          </strong>
          <hr />
        </div>
        <!-- <v-simple-table dark>
    <template v-slot:default>
      <thead>
        <tr>
          <th class="text-left">
            id
          </th>
          <th class="text-left">
            Name
          </th>
          <th class="text-left">
            username
          </th>
          <th class="text-left">
            email
          </th>
          <th class="text-left">
            phone
          </th>
          <th class="text-left">
            website
          </th>
        </tr>
      </thead>
      <tbody>
        <tr
          v-for="user in users"
          :key="user.name"
        >
          <td>{{ user.id }}</td>
          <td>{{ user.name }}</td>
          <td>{{ user.username }}</td>
          <td>{{ user.email }}</td>
          <td>{{ user.phone }}</td>
          <td>{{ user.website }}</td>
        </tr>
      </tbody>
    </template>
  </v-simple-table> -->
      </div>
    </div>
  </div>
</template>



<script>
import axios from "axios";
export default {
  name: "Api Call",
  data() {
    return {
      loading: false,
      users: {},
    };
  },
  mounted() {
    this.getData();
  },
  methods: {
    async getData() {
      this.loading = true;
      try {
        const response = await axios.get(
          "https://jsonplaceholder.typicode.com/users"
        );
        this.users = response.data;
        this.loading = false;
      } catch (error) {
        window.console.log(error);
        this.loading = false;
      }
    },
  },
};
</script>




<style>
body{
    margin: 0;
    padding: 0;
   /* background-image: url('img.jpg'); */
   background-color: rgba(139, 162, 212, 0.199);
    box-sizing: border-box;
}
.st1 ,.st{
color: rgb(71, 80, 55);
 animation-name: st1;
  animation-duration: 15s;
}
@keyframes st1 {
  0% {
    background-color: red;
  }
  /* 15%{background-color: rgb(14, 10, 10);} */
  25% {
    background-color: yellow;
  }
  50% {
    background-color: blue;
  }
  100% {
    background-color: green;
  }
}


</style>









