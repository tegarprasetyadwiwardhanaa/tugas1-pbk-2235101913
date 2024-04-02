<template>
  <div id="app">
    <header>
      <h1>Tegar Prasetya Dwi Wardhana</h1>
      <h2>Web developer</h2>
      <p>Halo! Saya adalah seorang Pengembang Perangkat Lunak (Dev Developer) yang penuh semangat, didorong oleh pesona mengubah baris kode menjadi solusi inovatif. Dengan latar belakang yang kuat di bidang teknologi dan rasa ingin tahu yang mendalam untuk memecahkan masalah, saya berkembang di ranah dinamis pengembangan perangkat lunak.</p>
      <nav>
        <ul>
          <li><a href="#about">About Me</a></li>
          <li><a href="#experience">Experience</a></li>
          <li><a href="#skills">Skills</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </nav>
    </header>

    <main>
      <section id="about">
        <h2>About Me</h2>
        <p>Halo! Saya adalah seorang Pengembang Perangkat Lunak (Dev Developer) yang penuh semangat, didorong oleh pesona mengubah baris kode menjadi solusi inovatif. Dengan latar belakang yang kuat di bidang teknologi dan rasa ingin tahu yang mendalam untuk memecahkan masalah, saya berkembang di ranah dinamis pengembangan perangkat lunak. Perjalanan saya ke dunia pengembangan dimulai dengan ketertarikan yang mendalam terhadap bagaimana teknologi membentuk kehidupan sehari-hari kita. Saya memulai langkah ini dengan pondasi yang kokoh dalam bahasa pemrograman seperti Python, Java, JavaScript, dan lainnya. Seiring waktu, saya mengasah keterampilan saya melalui proyek-proyek langsung dan pembelajaran berkelanjutan, menelusuri berbagai kerangka kerja dan metodologi untuk memperluas kotak alat saya.</p>
      </section>

      <section id="experience">
        <h2>Experience</h2>
        <ul>
          <li v-for="experience in experiences" :key="experience.company">
            <h3>{{ experience.title }}</h3>
            <h4>{{ experience.company }} - {{ experience.startDate }} to {{ experience.endDate }}</h4>
            <ul>
              <li v-for="responsibility in experience.responsibilities" :key="responsibility">{{ responsibility }}</li>
              <li v-for="achievement in experience.achievements" :key="achievement">{{ achievement }}</li>
            </ul>
          </li>
        </ul>
      </section>

      <section id="skills">
        <h2>Skills</h2>
        <ul>
          <li v-for="skill in skills" :key="skill.name">
            {{ skill.name }} (Proficiency Level: {{ skill.level }})
          </li>
        </ul>
      </section>


      <section id="contact">
        <h2>Contact</h2>
        <ul>
          <li><a href="mailto:[Your Email Address]">tegar1240@gmail.com</a></li>
        </ul>
      </section>
    </main>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      experiences: [
        /* Add your experience details here */
        
      ],
      skills: [
        /* Add your skills and proficiency levels here */
        { name: 'html', level: 'Intermediate' },
        { name: 'css', level: 'Intermediate' },
        { name: 'javascript', level: 'Intermediate' },
      ],
    };
  },
};
</script>

<style scoped>
/* Reset default browser styles */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* Body styles */
body {
  font-family: Arial, sans-serif;
  line-height: 1.6;
  background-color: #f4f4f4;
  color: #333;
}

/* Header styles */
header {
  background-color: #333;
  color: #fff;
  padding: 20px;
  text-align: center;
}

header h1 {
  font-size: 2.5rem;
}

header h2 {
  font-size: 1.5rem;
}

/* Navigation styles */
nav ul {
  list-style: none;
  padding: 0;
}

nav ul li {
  display: inline;
  margin-right: 20px;
}

nav ul li a {
  color: #fff;
  text-decoration: none;
}

/* Main content styles */
main {
  padding: 20px;
}

/* Section styles */
section {
  margin-bottom: 40px;
}

section h2 {
  font-size: 2rem;
  margin-bottom: 20px;
}

section p {
  margin-bottom: 20px;
}

/* Footer styles */
footer {
  background-color: #333;
  color: #fff;
  padding: 20px;
  text-align: center;
}

/* Remove bullet points from list items */
ul {
  list-style-type: none;
}

/* Change color on hover */
nav ul li a:hover {
  color: #ffd700; /* Ubah ke warna kuning saat dihover */
}
</style>
