<template>
  <div class="col-md-6 grid-margin stretch-card">
    <div class="card">
      <div class="card-body">
        <p class="card-title">Users</p>
        <div class="d-flex flex-wrap align-items-baseline">
          <h2 class="mr-3">{{results.users}}</h2>

          <!-- results innehåller allt jag behöver, så jag hämtar det jag behöver
          med hjäp av de dubbla måsvingarna. På det sättet vet vue vad den ska göra
          och letar efter en variabel som heter det som står mellan måsvingarna.
          
          Det är inte svårare än så.
             -->
          <i class="mdi mdi-arrow-up mr-1 text-danger"></i>
          <span>
            <p class="mb-0 text-danger font-weight-medium">{{results.growth}}%</p>
          </span>
        </div>
        <p class="mb-0 text-muted">Total users world wide</p>
      </div>
      <canvas id="users-chart"></canvas>
    </div>
  </div>
</template>

<script>

// Jag behöver lite data från API:et och det hämtar jag så här:
export default {
  name: "Totalusers",
  data() {
    return {
      results: {} // Et objekt som heter results. Via return, så kommer jag åt det
      // i min HTML i template.
    }
  },

  // Här hämtar jag datat från API:et.
  created() {
    fetch('https://inlupp-fa.azurewebsites.net/api/total-users')
    .then(res => res.json()) // Görs om till ett JSON-objekt
    .then(data => {
      this.results = data; // Lagras i min variabel results.
    })
  }
};
</script>

<style>
</style>