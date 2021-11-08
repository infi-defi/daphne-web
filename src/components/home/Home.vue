<template>
  <Navbar />
  <div class="home">
    <section>
      <Header />
      <Section
        bg="#c91f58"
        inner="
        <h1 class='title'>Our goals</h1>
        <div class='columns'>
          <div class='column'>
            <h1 class='title' style='font-size: larger;'>Transparency</h1>
            <p>We strive to maintain an open source project that is driven by the community, 
               without any corporate interests.</p>
          </div>
          <div class='column'>
            <h1 class='title' style='font-size: larger;'>Being free (as in free beer and as in free speech)</h1>
            <p>Daphne is free and will always remain that way. Meaning that no proprietary software will ever get in the way.
               Every decision will be made by the community.</p>
          </div>
          <div class='column'>
            <h1 class='title' style='font-size: larger;'>Making cool shit</h1>
            <p>And finally, the only reason we're doing this, is to make something cool, even if not particularly useful. 
              The goal is not to create the next Windows, or Linux, but to make something that someone will 
              look at and say 'Hey, that looks really cool!'</p>
          </div>
        </div>
      "
      />
    </section>
  </div>
</template>

<script>
import Navbar from "./Navbar.vue";
import Header from "./Header.vue";
import Section from "./Section.vue";

export default {
  name: "Home",
  components: {
    Navbar,
    Header,
    Section,
  },
};
</script>

<style scoped>
.home {
  display: flex;
  justify-content: center;
}

section {
  position: relative;
  display: flex;
  flex-direction: column;
  min-height: 400px;
  align-items: center;
}

svg {
  background-color: var(--brand);
}
</style>
