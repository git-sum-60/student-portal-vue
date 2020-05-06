<template>
  <div class="students-show">
    <button v-bind:href="`/students/11/edit`">Edit</button>
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
    <h2>Experience</h2>
    <p>Start Date: {{ student.start_date}}</p>
    <p>End Date: {{ student.end_date }}</p>
    <p>Job Title: {{ student.degree }}</p>
    <p>Company Name: {{ student.university }}</p>
    <p>Details:</p>
  </div>
</template>

<script>
import axios from "axios";

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
    // axios.get("/api/students/ + this.$route.params.id").then(response => {
    //   console.log(response.data);
    //   this.student = response.data;
    // });
  },
  methods: {},
};
</script>
