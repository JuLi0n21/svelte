<script>
    let githubUsername = 'juli0n21';
    let linkedinProfile = 'https://www.linkedin.com/in/yourusername/';
  </script>
  
  <style>
    .container {
      max-width: 800px;
      margin: 0 auto;
      padding: 20px;
    }
  
    .intro h1 {
      font-size: 24px;
      margin-bottom: 5px;
    }
  
    .intro p {
      font-size: 18px;
      margin: 5px 0;
    }
  
    .study {
      font-style: italic;
    }
  
    .skills h2 {
      font-size: 20px;
      margin-bottom: 10px;
    }
  
    .badge-table {
      /* Define your badge table styling here */
    }
  
    .badge-table img {
      margin: 5px;
    }
  
    .connect h2,
    .github-stats h2,
    .projects summary {
      font-size: 20px;
      margin-bottom: 10px;
      cursor: pointer;
    }
  
    .connect a img {
      width: 120px;
    }
  
    .github-stats img,
    .projects details {
      margin-top: 10px;
    }
  </style>
  
  <div class="container">
    <section class="intro">
      <h1>Hello! I'm JuLi0n</h1>
      <p>Computer Science Student</p>
      <p>Aspiring Software Engineer</p>
      <p class="study">Studying Computer Science at Westfälische Hochschule</p>
    </section>
  
    <section class="skills">
      <h2>Languages and Tools</h2>
      <div class="badge-table">
        <!-- Your badge table content here -->
      </div>
      <img src={`https://github-readme-stats.vercel.app/api/top-langs/?username=${githubUsername}&layout=compact`} alt="Top Languages" />
    </section>
  
    <section class="connect">
      <h2>Connect with Me</h2>
      <a href={linkedinProfile} target="_blank" rel="noopener noreferrer">
        <img src="https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin" alt="LinkedIn" />
      </a>
    </section>
  
    <section class="github-stats">
      <h2>GitHub Stats</h2>
      <img src={`https://github-readme-stats.vercel.app/api?username=${githubUsername}&show_icons=true&theme=dark`} alt="GitHub Stats" />
    </section>
  
    <section class="projects">
      <details>
        <summary>Projects</summary>
        <!-- Your projects details here -->
      </details>
    </section>
  </div>
  