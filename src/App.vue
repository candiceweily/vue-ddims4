<template>
  <div id="app">
    <header>
      <h1>{{ name }}</h1>
      <p>{{ tagline }}</p>
    </header>
    <section>
      <h2>About Me</h2>
      <p>{{ about }}</p>
    </section>
    <section>
      <h2>Hobbies</h2>
      <li v-for="hobby in hobbies" :key="hobby">{{ hobby }}</li>
    </section>
    <section>
      <h2>Contact</h2>
      <p>
        Email: <a :href="'mailto:' + email">{{ email }}</a>
      </p>
    </section>
    <section>
      <h2>My Coding Partner for CS103</h2>
      <img
        src="https://cs-people.bu.edu/weily00/cs103/show&tell/cat1.jpg"
        width="500"
      />
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: 'Candice Wei',
      tagline: 'A cat lover',
      about:
        'A senior student at BU that major in Advertising and learn front-end development in CS 103.',
      hobbies: ['Hiking', 'Photography', 'Drawing'],
      email: 'weily00@bu.edu',
    };
  },
};
</script>

<style>
* {
  box-sizing: border-box;
}

header {
  background-color: #ffc0cb;
  color: black;
  padding: 20px;
}

body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  font-size: 18px;
}

li {
  padding: 5px;
}

section {
  padding: 10px 20px;
}
</style>
