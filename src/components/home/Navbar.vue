<template>
  <nav class="navbar" role="navigation" aria-label="main navigation">
    <div class="navbar-brand">
      <a class="navbar-item logo" href="https://daphne.dev"> daphne </a>

      <a
        role="button"
        class="navbar-burger"
        aria-label="menu"
        aria-expanded="false"
        data-target="navbar"
      >
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
      </a>
    </div>

    <div id="navbar" class="navbar-menu">
      <div class="navbar-start">
        <a href="/" class="navbar-item">Home</a>
        <a href="https://github.com/synthels/daphne/graphs/contributors" class="navbar-item">Developers</a>
        <a href="https://github.com/synthels/daphne/fork" class="navbar-item">Fork on Github</a>
      </div>

      <div class="navbar-end">
        <div class="navbar-item">
          <div class="buttons">
            <a class="button is-primary" style="background-color: #738adb" href="https://discord.gg/Mx8vu6c4U6">
              <strong><span class="fab fa-discord" /> Discord server</strong>
            </a>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: "Navbar",
  // Toggle navbar burger(s)
  mounted() {
    const burgers = Array.prototype.slice.call(
      document.querySelectorAll(".navbar-burger"),
      0
    );

    if (burgers.length > 0) {
      burgers.forEach((el) => {
        el.addEventListener("click", () => {
          const target = document.getElementById(el.dataset.target);
          el.classList.toggle("is-active");
          target.classList.toggle("is-active");
        });
      });
    }
  },
};
</script>

<style scoped>
.navbar,
.navbar-start,
.navbar-menu .navbar-end {
  background-color: var(--dark);
}

.navbar-menu {
  padding: 0;
  box-shadow: none;
}

.navbar-item,
.navbar-link {
  color: var(--text);
}

.navbar-item:hover,
.navbar-link:hover {
  color: var(--brand);
  background-color: transparent;
}

.button {
  background-color: var(--brand);
}

.button:hover {
  background-color: var(--brand);
}

.button:focus {
  background-color: var(--brand);
}

.logo {
  color: white;
  user-select: none;
}

.logo:hover {
  color: white;
}

.logo:focus,
.logo:active {
  color: white;
}
</style>
