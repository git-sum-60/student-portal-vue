<template>
  <div class="portal-edit">
    <h1>Edit Resume and Capstone Data</h1>
    <hr>
    <h4> Edit Personal Info </h4>
    <button v-on:click="togglePersonalInfo()"> Show/Hide </button>
      <div v-if="personal_info === true">
        <p>First Name: <input type="text" v-model="student.first_name"></p>
        <p>Last Name: <input type="text" v-model="student.last_name"></p>
        <p>Email: <input type="text" v-model="student.email"></p>
        <p>Phone Number: <input type="text" v-model="student.phone_number"></p>
        <p>Short Bio: <input type="text" v-model="student.short_bio"></p>
        <p>LinkedIn URL: <input type="text" v-model="student.linkedin_url"></p>
        <p>Twitter Handle: <input type="text" v-model="student.twitter_handle"></p>
        <p>Personal Blog/Website URL: <input type="text" v-model="student.personal_site_url"></p>
        <p>Online Resume URL: <input type="text" v-model="student.online_resume_url"></p>
        <p>Github URL: <input type="text" v-model="student.github_url"></p>
        <p>Photo URL: <input type="text" v-model="student.photo_url"></p>
        <button>Submit</button>
      </div>
    <hr>
    <h4> Add Experience </h4>
    <button v-on:click="togglePersonalExperience()"> Show/Hide </button>
      <div v-if="personal_experience === true">
        <p>Start Date: <input type="text" v-model="startDate"></p>
        <p>End Date: <input type="text" v-model="endDate"></p>
        <p>Job Title: <input type="text" v-model="jobTitle"></p>
        <p>Company Name:<input type="text" v-model="companyName"></p>
        <p>Details: <input type="text" v-model="details"></p>
        <button>Submit</button>        
      </div>
    <hr>
    <h4> Add Education </h4>
    <button v-on:click="togglePersonalEducation()"> Show/Hide </button>
      <div v-if="personal_education === true">
        <p>start_date: <input type="text" v-model="educationStartDate"></p>
        <p>end_date: <input type="text" v-model="educationEndDate"></p>
        <p>degree: <input type="text" v-model="degree"></p> 
        <p>university: <input type="text" v-model="university"></p>
        <p>details: <input type="text" v-model="educationDetails"></p>
        <button>Submit</button>      
      </div>
    <hr>
    <h4> Add Skill </h4>
    <button v-on:click="togglePersonalSkill()"> Show/Hide </button>
      <div v-if="personal_skill === true">
        <p>skill: <input type="text" v-model="skill"></p>
        <button>Submit</button>
      </div>
    <hr>
    <h4> Add Capstone </h4>
    <button v-on:click="togglePersonalCapstone()"> Show/Hide </button>
      <div v-if="personal_capstone === true">
        <p>name: <input type="text" v-model="capstoneName"></p>
        <p>description: <input type="text" v-model="capstoneDescription"></p>
        <p>url: <input type="text" v-model="capstoneUrl"></p>
        <p>screenshot_url: <input type="text" v-model="capstoneScreenShotUrl"></p>
        <p>student_id: <input type="text" v-model="capstoneStudentId"></p>
        <button>Submit</button>
      </div>
    <hr>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  data: function() {
    return {
      student: {},
      personal_info: false,
      personal_experience: false,
      personal_education: false,
      personal_skill: false,
      personal_capstone: false,
      startDate: "",
      endDate: "",
      jobTitle: "",
      companyName: "",
      details: "",
      educationStartDate: "",
      educationEndDate: "",
      degree: "",
      university: "",
      educationDetails: "",
      skill: "",
      capstoneName: "",
      capstoneDescription: "",
      capstoneUrl: "",
      capstoneScreenShotUrl: "",
      capstoneStudentId: ""
    };
  },

  created: function() {
    console.log('in the created function on edit page');
    // uncomment this to grab data from backend
    // axios.get(`/api/students/${this.$route.params.id}`).then(response => {
    //   console.log(response.data);
    //   this.student = response.data
    // });
  },

  methods: {
    togglePersonalInfo: function() {
      this.personal_info = !this.personal_info;
      console.log("Show personal info:" + this.personal_info)
    },
    togglePersonalExperience: function() {
      this.personal_experience = !this.personal_experience;
      console.log("Show personal experience: " + this.personal_experience)
    },
    togglePersonalEducation: function() {
      this.personal_education = !this.personal_education;
      console.log("Show personal education: " + this.personal_education)
    },
    togglePersonalSkill: function() {
      this.personal_skill = !this.personal_skill;
      console.log("Show personal education: " + this.personal_skill)
    },
    togglePersonalCapstone: function() {
      this.personal_capstone = !this.personal_capstone;
      console.log("Show personal education: " + this.personal_capstone)
    },
    submit: function() {
      var params = {
        first_name: this.student.first_name,
        last_name: this.student.last_name,
        email: this.student.email,
        phone_number: this.student.phone_number,
        short_bio: this.student.short_bio,
        linkedin_url: this.student.linkedin_url,
        twitter_handle: this.student.twitter_handle,
        personal_site_url: this.student.personal_site_url,
        online_resume_url: this.student.online_resume_url,
        github_url: this.student.github_url,
        photo_url: this.student.photo_url
      };
      console.log('submit function')
      // console.log('params are below');
      // console.log(params);
      // axios.patch(`/api/students/${this.student.id}`, params).then(response => {
      //   this.$router.push(`/students/${this.student.id}`);
      // })
      //   .catch(error => {
      //     this.errors = error.response.data.errors;
      //     console.log(this.errors)
      //   });
    },
  }
};
</script>


    t.string "name"
    t.string "description"
    t.string "url"
    t.string "screenshot_url"
    t.integer "student_id"


      