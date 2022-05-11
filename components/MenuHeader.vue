<template>
  <header>
    <img src="/images/logo.svg" alt="Snap" class="logo">
    <button aria-label="Menu" class="[ menu dropdown ]" @click="menuToggle"></button>
    <nav class="menu__nav">
      <ul>
        <li class="[ dropdown ]" @click="menuToggle">Features</li>
        <ul>
          <li><i class="icon-todo"></i>Todo List</li>
          <li><i class="icon-calendar"></i>Calendar</li>
          <li><i class="icon-reminders"></i>Reminders</li>
          <li><i class="icon-planning"></i>Planning</li>
        </ul>
        <li class="[ dropdown ]" @click="menuToggle">Company</li>
        <ul>
          <li>History</li>
          <li>Our Team</li>
          <li>Blog</li>
        </ul>
        <li>Careers</li>
        <li>About</li>
        <button>Login</button>
        <button>Register</button>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  methods: {
    menuToggle: function (event) {
      event.target.classList.toggle('active')
      if (event.target.classList.contains('menu') && !event.target.classList.contains('active')) {
        [...this.$el.querySelectorAll('.dropdown')].forEach(function (ddm) {
          ddm.classList.remove('active');
        })
      }
    }
  },
}
</script>
