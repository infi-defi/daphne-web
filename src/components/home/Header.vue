<template>
  <div class="header">
    <div class="row">
      <div class="column" id="img-col">
        <img width="350" src="../../assets/phone.png" />
      </div>
      <div class="column">
        <h1 class="title">daphne</h1>
        <p>
          Daphne is a hobby operating system built from scratch, with the goal
          of eventually running on ARM devices.
        </p>
        <a class="button" href="https://github.com/synthels/daphne/releases"
          >Download latest</a
        >
        <a
          class="button"
          id="button-github"
          target="_blank"
          rel="noopener noreferrer"
          href="https://github.com/synthels/daphne"
          ><strong
            ><span class="fab fa-github" /> Check out on Github</strong
          ></a
        >
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style scoped>
.header {
  margin-top: 80px;
}

.title {
  color: white;
  margin-top: 70px; /* stupid hack */
}

img {
  user-select: none;
}

.row {
  display: flex;
}

.title {
  font-size: 30;
  font-weight: bold;
}

#button-github {
  margin-left: 20px;
}

p {
  color: var(--par);
}

/* Create three equal columns that sits next to each other */
.column {
  flex: 1;
  padding: 0;
}

.button {
  background-color: var(--brand);
  margin-top: 20px;
}

.button:focus {
  background-color: var(--brand);
}

.button:hover {
  background-color: var(--brand);
}

#img-col {
  margin-right: -140px;
}

@media screen and (max-width: 1080px) {
  #img-col {
    display: none;
  }
}

@media screen and (max-width: 1080px) {
  .header {
    margin-top: -15px;
  }

  .column {
    padding: 1rem;
  }
}

@media screen and (max-width: 380px) {
  #button-github {
    margin-left: 0;
  }
}
</style>
