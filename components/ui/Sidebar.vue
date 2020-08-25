<template>
  <ul
    class="navbar-nav bg-gradient-primary sidebar sidebar-dark accordion"
    id="accordionSidebar"
  >
    <a
      class="sidebar-brand d-flex align-items-center justify-content-center"
      href="index.html"
    >
      <div class="sidebar-brand-icon rotate-n-15">
        <i class="fas fa-laugh-wink"></i>
      </div>
      <div class="sidebar-brand-text mx-3">SB Admin<sup>2</sup></div>
    </a>
    <hr class="sidebar-divider my-0" />
    <li class="nav-item">
      <nuxt-link class="nav-link" to="/admin">
        <i class="fas fa-fw fa-tachometer-alt"></i><span>Dashboard</span>
      </nuxt-link>
    </li>
    <hr class="sidebar-divider" />
    <div class="sidebar-heading">Interface</div>
    <li class="nav-item">
      <a
        class="nav-link collapsed"
        href="#"
        data-toggle="collapse"
        data-target="#collapseTwo"
        aria-expanded="true"
        aria-controls="collapseTwo"
        ><i class="fas fa-fw fa-cog"></i><span>Components</span></a
      >
      <div
        class="collapse"
        id="collapseTwo"
        aria-labelledby="headingTwo"
        data-parent="#accordionSidebar"
      >
        <div class="bg-white py-2 collapse-inner rounded">
          <h6 class="collapse-header">Custom Components:</h6>
          <a class="collapse-item" href="buttons.html">Buttons</a
          ><a class="collapse-item" href="cards.html">Cards</a>
        </div>
      </div>
    </li>
    <hr class="sidebar-divider my-0" />
    <li class="nav-item">
      <nuxt-link class="nav-link" to="/admin/users">
        <i class="fas fa-users"><span>Users</span></i>
      </nuxt-link>
      <!-- <a class="nav-link" href="index.html"
        ><i class="fas fa-users"></i><span>Users</span></a
      > -->
    </li>
    <hr class="sidebar-divider" />
    <div class="text-center d-none d-md-inline">
      <button class="rounded-circle border-0" id="sidebarToggle"></button>
    </div>
  </ul>
</template>
