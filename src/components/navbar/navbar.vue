<template>
  <nav class="navbar top-navbar col-lg-12 col-12 p-0">
    <div class="container">
      <div class="navbar-menu-wrapper d-flex align-items-center">
        <ul class="navbar-nav navbar-nav-right">
          <Messages />
          <Notifications />
          <Userinfo />
        </ul>
        
        <button
          class="navbar-toggler navbar-toggler-right d-lg-none align-self-center"
          type="button"
          data-toggle="horizontal-menu-toggle"
        >
          <span class="mdi mdi-menu"></span>
        </button>
      </div>
    </div>
  </nav>
</template>

<script>
import Messages from "./messages";
import Notifications from './notifications';
import Userinfo from './userinfo';

export default {
  name: "Navbar",
  components: {
    Messages,
    Notifications,
    Userinfo
  }
};
</script>

<style>
</style>