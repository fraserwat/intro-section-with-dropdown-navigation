<template>
  <header>
    <img src="/images/logo.svg" alt="Snap" class="logo">
    <button aria-label="Menu" class="[ hamburger ] [ menu dropdown ]" @click="menuToggle"></button>
    <nav class="[ menu__nav ] [ font-grey ]">
      <ul>
        <li class="[ dropdown ]" @click="menuToggle" ref="submenuOne">Features</li>
        <ul>
          <li><i><img src="/icons/icon-todo.svg" alt=""></i>Todo List</li>
          <li><i><img src="/icons/icon-calendar.svg" alt=""></i>Calendar</li>
          <li><i><img src="/icons/icon-reminders.svg" alt=""></i>Reminders</li>
          <li><i><img src="/icons/icon-planning.svg" alt=""></i>Planning</li>
        </ul>
        <li class="[ dropdown ]" @click="menuToggle" ref="submenuTwo">Company</li>
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
      if (event.target.classList.contains('menu') && event.target.classList.contains('active')) {
        event.target.classList.add('slide-out');
        setTimeout(function () {
          event.target.classList.remove('slide-out');
          event.target.classList.remove('active');
        }, 250);
        this.$refs.submenuOne.classList.remove('active');
        this.$refs.submenuTwo.classList.remove('active');
      } else {
        event.target.classList.toggle('active')
      }
    }
  },
}
</script>
