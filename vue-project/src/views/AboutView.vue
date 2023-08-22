<script>
export default {
    data() {
      return {
        name: 'KARAN BALHOTRA',
        intro: 'Hello,everyone I am a first year university student and a passionate web-developer. Till now I have learned about the these things:',
        skills: ['HTML', 'CSS', 'JavaScript', 'Vue.js', 'Responsive Design'],
        projects: [
          {
            title: 'Project 1',
            description: 'In this task I have made a To-do app. Through this application person can add as well as delete his/her daily tasks.This app will help the person to be on track with the all daily activities.',
            link: 'https://github.com/Karan-Balhotra/SIT-120-Responsive-web-apps.git'
          },
          {
            title: 'Project 2',
            description: 'In this task I have developed a Quiz application for the students. Through this app the students can take quiz for multiple subjects.This application is a prototype of a bigger application.',
            link:'https://github.com/Karan-Balhotra/credit-task-2.git'
          },
          {
            title:'Project 3',
            description: 'This was the first website that I had ever built in my life. Altough I have come a long way ahead of this...😁😁😁😊😊',
            link: 'https://github.com/Karan-Balhotra/SIT-120-Introduction-to-Responsive-Web-Apps.git'
          },
          {
            title:'Project 4',
            description: 'Through this task I was asked to demonstrate my javascript skills.',
            link: 'https://github.com/Karan-Balhotra/web-development-task-1.2p.git'
          }
        ],
        email: 'KaranBalhotra@Gmail.com',
        Instagram: 'KaranBalhotra@56',
        phone : '+61-3434xxxxx'
      };
    }
}
</script>

<template>

  <link rel="icon" href="../favicon-32x32.png">
 <div>
        <div class="header">
          <h1>My Resume</h1>
        </div>
        <div class="container">
          <div class="intro">
            <h2>{{ name }}</h2>
            <p>{{ intro }}</p>
          </div>
          <div class="skills">
            <div class="skill" v-for="skill in skills">{{ skill }}</div>
          </div>
          <div v-for="project in projects" class="project">
            <h2>{{ project.title }}</h2>
            <p>{{ project.description }}</p>
           <button> <a :href="project.link">click here</a></button>
          </div>
          <div class="contact">
            <p>Contact me at:</p>
            <p>Email: {{ email }}</p>
            <p>Instagram:{{ Instagram }}</p>
            <p>Phone:{{ phone }}</p>
          </div>
        </div>
      </div>
</template>

<style>
body{
  background-color: yellowgreen;
}

.header{
  text-align: center;
  font-family: 'Tilt Prism', cursive;
}

.intro h2{
  font-family: 'Pacifico', cursive;
}


.intro {
    padding: 20px;
    text-align: center;
    background-color:cornflowerblue;
    border-radius: 5px;
  }
  
  .skills {
    margin-top: 20px;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
  }
  
  .skill {
    background-color:rebeccapurple;
    color:rgb(152, 211, 152);
    padding: 5px 10px;
    margin: 5px;
    border-radius: 3px;
  }
  
  .project {
    border: 1px solid papayawhip;
    padding: 20px;
    margin: 10px;
    background-color:cornflowerblue;
    border-radius: 5px;
  }
  
  .project h2 {
    margin-top: 0;
    color: #333;
    font-family: 'Pacifico', cursive;
  }
  
  .contact {
    margin-top: 20px;
    text-align: center;
    background-color:cornflowerblue;
    border-radius: 5px;
    padding: 20px;
  }
  
  .contact p {
    margin: 10px 0;
  }
  
  .contact a {
    color: #333;
    text-decoration: none;
  }
  
  .contact a:hover {
    color: #007bff;
  }
  
  .container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 20px;
    box-sizing: border-box;
  }

  .project button {
    background-color:lightgreen;
    color: black;
    border: none;
    padding: 5px 10px;
    cursor: pointer;
    margin-top: 10px;
    border-radius: 12px;
    transition-duration: 0.4s;
  }

  .project button:hover{
    background-color: #4CAF50; 
    color: white;
  }

  @media (max-width: 768px) {
    .project {
      padding: 10px;
      margin: 5px;
    }
  }
</style>