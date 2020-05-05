<template>
  <div class="students-show">
    <h2>Resume Info</h2>
    <p>First name: {{ student.first_name }}</p>
    <p>Last Name: {{ student.last_name }}</p>
    <p>Email: {{ student.email }}</p>
    <p>Phone Number: {{ student.phone_number }}</p>
    <p>Short_bio: {{ student.short_bio }}</p>
    <p>Linkedin Url: {{ student.linkedin_url }}</p>
    <p>Twitter Handle: {{ student.twitter_handle }}</p>
    <p>Personal Site Url: {{ student.personal_site_url }}</p>
    <p>Online Resume Url: {{ student.online_resume_url }}</p>
    <p>Github Url: {{ student.github_url }}</p>
    <p>Photo Url: {{ student.photo_url }}</p>
    <p>Online Resume Url: {{ student.online_resume_url }}</p>
    <h2>Capstone</h2>
    <p>Name: {{ student.name }}</p>
    <p>Description:{{ student.description }}</p>
    <p>Url: {{ student.url }}</p>
    <button v-bind:href="`/students/${student.id}/edit`">Edit</button>
    <h2>Experience</h2>
    <p>Start Date:</p>
    <p>End Date:</p>
    <p>Job Title:</p>
    <p>Company Name:</p>
    <p>Details (one long text field)</p>
  </div>
</template>

<script>
// import axios from "axios";

export default {
  data: function() {
    return {
      firstName: "firstName",
      lastName: "lastName",
      email: "email",
      phoneNumber: "phoneNumber",
      shortBio: "shortBio",
      linkedinUrl: "linkedinUrl",
      name: "name",
      description: "description",
      url: "",
      student: {},
    };
  },
  created: function() {
    axios.get("/api/students/ + this.$route.params.id").then(response => {
      console.log(response.data);
      this.student = response.data;
    });
  },
  methods: {},
};
</script>
