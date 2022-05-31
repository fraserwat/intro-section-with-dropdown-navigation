<template>
  <header>
    <img src="/images/logo.svg" alt="Snap" class="logo" tabindex="0">
    <button aria-label="Menu" class="[ hamburger ] [ menu dropdown ]" @click="menuToggle"></button>
    <nav class="[ menu__nav ] [ font-grey ]">
      <ul>
        <div class="list-container">
          <li class="[ dropdown ]" @click="menuToggle" @keypress="menuToggle" ref="submenuOne" tabindex="0">Features</li>
          <ul>
            <li><a href=""><i><img src="/icons/icon-todo.svg" alt=""></i>Todo List</a></li>
            <li><a href=""><i><img src="/icons/icon-calendar.svg" alt=""></i>Calendar</a></li>
            <li><a href=""><i><img src="/icons/icon-reminders.svg" alt=""></i>Reminders</a></li>
            <li><a href=""><i><img src="/icons/icon-planning.svg" alt=""></i>Planning</a></li>
          </ul>
        </div>
        <div class="list-container">
          <li class="[ dropdown ]" @click="menuToggle" @keypress="menuToggle" ref="submenuTwo" tabindex="0">Company</li>
          <ul>
            <li><a href="">History</a></li>
            <li><a href="">Our Team</a></li>
            <li><a href="">Blog</a></li>
          </ul>
        </div>
        <li><a href="">Careers</a></li>
        <li><a href="">About</a></li>
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
