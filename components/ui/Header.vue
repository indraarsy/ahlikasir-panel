<template>
  <nav
    class="navbar navbar-expand navbar-light bg-white topbar mb-4 static-top shadow"
  >
    <button
      class="btn btn-link d-md-none rounded-circle mr-3"
      id="sidebarToggleTop"
    >
      <i class="fa fa-bars"></i>
    </button>
    <form
      class="d-none d-sm-inline-block form-inline mr-auto ml-md-3 my-2 my-md-0 mw-100 navbar-search"
    >
      <div class="input-group">
        <input
          class="form-control bg-light border-0 small"
          type="text"
          placeholder="Search for..."
          aria-label="Search"
          aria-describedby="basic-addon2"
        />
        <div class="input-group-append">
          <button class="btn btn-primary" type="button">
            <i class="fas fa-search fa-sm"></i>
          </button>
        </div>
      </div>
    </form>
    <ul class="navbar-nav ml-auto">
      <li class="nav-item dropdown no-arrow d-sm-none">
        <a
          class="nav-link dropdown-toggle"
          id="searchDropdown"
          href="#"
          role="button"
          data-toggle="dropdown"
          aria-haspopup="true"
          aria-expanded="false"
          ><i class="fas fa-search fa-fw"></i
        ></a>
        <div
          class="dropdown-menu dropdown-menu-right p-3 shadow animated--grow-in"
          aria-labelledby="searchDropdown"
        >
          <form class="form-inline mr-auto w-100 navbar-search">
            <div class="input-group">
              <input
                class="form-control bg-light border-0 small"
                type="text"
                placeholder="Search for..."
                aria-label="Search"
                aria-describedby="basic-addon2"
              />
              <div class="input-group-append">
                <button class="btn btn-primary" type="button">
                  <i class="fas fa-search fa-sm"></i>
                </button>
              </div>
            </div>
          </form>
        </div>
      </li>
      <li class="nav-item dropdown no-arrow mx-1">
        <a
          class="nav-link dropdown-toggle"
          id="alertsDropdown"
          href="#"
          role="button"
          data-toggle="dropdown"
          aria-haspopup="true"
          aria-expanded="false"
          ><i class="fas fa-bell fa-fw"></i
          ><span class="badge badge-danger badge-counter">3+</span></a
        >
        <div
          class="dropdown-list dropdown-menu dropdown-menu-right shadow animated--grow-in"
          aria-labelledby="alertsDropdown"
        >
          <h6 class="dropdown-header">Alerts Center</h6>
          <a class="dropdown-item d-flex align-items-center" href="#">
            <div class="mr-3">
              <div class="icon-circle bg-primary">
                <i class="fas fa-file-alt text-white"></i>
              </div>
            </div>
            <div>
              <div class="small text-gray-500">December 12, 2019</div>
              <span class="font-weight-bold"
                >A new monthly report is ready to download!</span
              >
            </div>
          </a>
          <a class="dropdown-item d-flex align-items-center" href="#">
            <div class="mr-3">
              <div class="icon-circle bg-success">
                <i class="fas fa-donate text-white"></i>
              </div>
            </div>
            <div>
              <div class="small text-gray-500">December 7, 2019</div>
              $290.29 has been deposited into your account!
            </div>
          </a>
          <a class="dropdown-item d-flex align-items-center" href="#">
            <div class="mr-3">
              <div class="icon-circle bg-warning">
                <i class="fas fa-exclamation-triangle text-white"></i>
              </div>
            </div>
            <div>
              <div class="small text-gray-500">December 2, 2019</div>
              Spending Alert: We&apos;ve noticed unusually high spending for
              your account.
            </div> </a
          ><a class="dropdown-item text-center small text-gray-500" href="#"
            >Show All Alerts</a
          >
        </div>
      </li>
      <li class="nav-item dropdown no-arrow mx-1">
        <a
          class="nav-link dropdown-toggle"
          id="messagesDropdown"
          href="#"
          role="button"
          data-toggle="dropdown"
          aria-haspopup="true"
          aria-expanded="false"
          ><i class="fas fa-envelope fa-fw"></i
          ><span class="badge badge-danger badge-counter">7</span></a
        >
        <div
          class="dropdown-list dropdown-menu dropdown-menu-right shadow animated--grow-in"
          aria-labelledby="messagesDropdown"
        >
          <h6 class="dropdown-header">Message Center</h6>
          <a class="dropdown-item d-flex align-items-center" href="#">
            <div class="dropdown-list-image mr-3">
              <img
                class="rounded-circle"
                src="https://source.unsplash.com/fn_BT9fwg_E/60x60"
                alt=""
              />
              <div class="status-indicator bg-success"></div>
            </div>
            <div class="font-weight-bold">
              <div class="text-truncate">
                Hi there! I am wondering if you can help me with a problem
                I&apos;ve been having.
              </div>
              <div class="small text-gray-500">Emily Fowler &middot; 58m</div>
            </div>
          </a>
          <a class="dropdown-item d-flex align-items-center" href="#">
            <div class="dropdown-list-image mr-3">
              <img
                class="rounded-circle"
                src="https://source.unsplash.com/AU4VPcFN4LE/60x60"
                alt=""
              />
              <div class="status-indicator"></div>
            </div>
            <div>
              <div class="text-truncate">
                I have the photos that you ordered last month, how would you
                like them sent to you?
              </div>
              <div class="small text-gray-500">Jae Chun &middot; 1d</div>
            </div>
          </a>
          <a class="dropdown-item d-flex align-items-center" href="#">
            <div class="dropdown-list-image mr-3">
              <img
                class="rounded-circle"
                src="https://source.unsplash.com/CS2uCrpNzJY/60x60"
                alt=""
              />
              <div class="status-indicator bg-warning"></div>
            </div>
            <div>
              <div class="text-truncate">
                Last month&apos;s report looks great, I am very happy with the
                progress so far, keep up the good work!
              </div>
              <div class="small text-gray-500">Morgan Alvarez &middot; 2d</div>
            </div>
          </a>
          <a class="dropdown-item d-flex align-items-center" href="#">
            <div class="dropdown-list-image mr-3">
              <img
                class="rounded-circle"
                src="https://source.unsplash.com/Mv9hjnEUHR4/60x60"
                alt=""
              />
              <div class="status-indicator bg-success"></div>
            </div>
            <div>
              <div class="text-truncate">
                Am I a good boy? The reason I ask is because someone told me
                that people say this to all dogs, even if they aren&apos;t
                good...
              </div>
              <div class="small text-gray-500">Chicken the Dog &middot; 2w</div>
            </div> </a
          ><a class="dropdown-item text-center small text-gray-500" href="#"
            >Read More Messages</a
          >
        </div>
      </li>
      <div class="topbar-divider d-none d-sm-block"></div>
      <li class="nav-item dropdown no-arrow">
        <a
          class="nav-link dropdown-toggle"
          id="userDropdown"
          href="#"
          role="button"
          data-toggle="dropdown"
          aria-haspopup="true"
          aria-expanded="false"
          ><span class="mr-2 d-none d-lg-inline text-gray-600 small">{{
            name
          }}</span
          ><img
            class="img-profile rounded-circle"
            src="https://source.unsplash.com/QAB-WJcbgJk/60x60"
        /></a>
        <div
          class="dropdown-menu dropdown-menu-right shadow animated--grow-in"
          aria-labelledby="userDropdown"
        >
          <a class="dropdown-item" href="#"
            ><i class="fas fa-user fa-sm fa-fw mr-2 text-gray-400"></i
            >Profile</a
          ><a class="dropdown-item" href="#"
            ><i class="fas fa-cogs fa-sm fa-fw mr-2 text-gray-400"></i>
            Settings</a
          ><a class="dropdown-item" href="#"
            ><i class="fas fa-list fa-sm fa-fw mr-2 text-gray-400"></i>Activity
            Log</a
          >
          <div class="dropdown-divider"></div>
          <!-- <a @click="logout" class="dropdown-item" data-toggle="modal" data-target="#logoutModal"><i class="fas fa-sign-out-alt fa-sm fa-fw mr-2 text-gray-400"></i>Logout</a> -->
          <a @click="logout" class="dropdown-item logoutBtn"
            ><i class="fas fa-sign-out-alt fa-sm fa-fw mr-2 text-gray-400"></i
            >Logout</a
          >
        </div>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      name: null
    }
  },
  mounted() {
    if (this.$auth.loggedIn) {
      this.name = this.$auth.user.name
    }
  },
  methods: {
    logout() {
      this.$auth.logout()
    }
  }
}
</script>

<style scoped>
.logoutBtn {
  cursor: pointer;
  color: #3a3b45;
}
</style>
