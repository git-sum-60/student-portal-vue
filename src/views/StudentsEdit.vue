//  edit resume/capstone data
<template>
  <div class="portal-edit">
    <h1>Edit Resume and Capstone Info</h1>
    <hr>
    <h2> Resume Info </h2>
    <p>First Name: <input type="text" v-model="firstName"></p>
    <p>Last Name: <input type="text" v-model="lastName"></p>
    <p>Email: <input type="text" v-model="email"></p>
    <p>Phone Number: <input type="text" v-model="phoneNumber"></p>
    <p>Short Bio: <input type="text" v-model="shortBio"></p>
    <p>LinkedIn URL: <input type="text" v-model="linkedInURL"></p>
    <p>Twitter Handle: <input type="text" v-model="twitterHandle"></p>
    <p>Personal Blog/Website URL: <input type="text" v-model="webUrl"></p>
    <p>Online Resume URL: <input type="text" v-model="onlineResumeUrl"></p>
    <p>Github URL: <input type="text" v-model="gitHubUrl"></p>
    <hr>
    <h2> Capstone Info </h2>
    <p>Name: <input type="text" v-model="name"></p>
    <p>Description: <input type="text" v-model="description"></p>
    <p>URL: <input type="text" v-model="url"></p>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      firstName: "firstName",
      lastName: "lastName",
      email: "email",
      phoneNumber: "phoneNumber",
      shortBio: "shortBio",
      linkedInURL: "linkedInURL",
      twitterHandle: "twitterHandle",
      webUrl: "webUrl",
      onlineResumeUrl: "onlineResumeUrl",
      gitHubUrl: "gitHubUrl",
      name: "name",
      description: "description",
      url: "url"
    }
  }
}
</script>