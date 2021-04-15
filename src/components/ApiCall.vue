<template>
  <div>
    
    <div v-if="loading">Please wait......</div>
    <div v-else>
      <div v-if="users.length === 0">No User exists</div>
      <div v-else>
        <!-- <div v-for="(user, index) of users" :key="index">
          {{ user.name }}
        </div> -->
        <v-simple-table dark>
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
  </v-simple-table>
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