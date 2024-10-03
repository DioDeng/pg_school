<template>
  <section
    class="container-fluid positionSet px-sm-5 pt-sm-4"
    style="z-index: 1040"
  >
    <div class="row">
      <div class="col-12 col-lg-4 py-3 ps-3 p-sm-0" :class="classList.navBar">
        <router-link to="/" class="text-decoration-none">
          <span class="h5 d-none d-sm-block mb-0">打造有效又好笑的課堂<br /></span>
          <span class="h1 d-none d-sm-block">卷民Wrrrrry</span>
          <span class="h4 d-sm-none">卷民Wrrrrry</span>
        </router-link>
      </div>
      <div class="col-4 d-lg-block d-none text-nowrap">
        <ul
          class="list-unstyled d-flex justify-content-center align-items-center h-100"
        >
          <li>
            <router-link to="/" class="text-decoration-none d-flex">
              <div
                class="d-flex align-items-center hvr-icon-float-in text-white"
              >
                <h5 class="me-1">關於卷民</h5>
                <i class="fa-solid fa-circle-arrow-right h4 hvr-icon"></i>
              </div>
            </router-link>
          </li>
          <li class="mx-5">
            <router-link to="/" class="text-decoration-none d-flex">
              <div
                class="d-flex align-items-center hvr-icon-float-in text-white"
              >
                <h5 class="me-1">課程表</h5>
                <i class="fa-solid fa-circle-arrow-right h4 hvr-icon"></i>
              </div>
            </router-link>
          </li>
          <li>
            <router-link to="/" class="text-decoration-none d-flex">
              <div
                class="d-flex align-items-center hvr-icon-float-in text-white"
              >
                <h5 class="me-1">題庫/講義</h5>
                <i class="fa-solid fa-circle-arrow-right h4 hvr-icon"></i>
              </div>
            </router-link>
          </li>
        </ul>
      </div>
      <div class="col-4 d-none d-lg-block">
        <ul
          class="list-unstyled d-flex justify-content-center align-items-center h-100"
        >
          <li>
            <router-link to="/" class="text-decoration-none text-white"
              ><h6>相關問題</h6></router-link
            >
          </li>
          <li class="mx-3">
            <div class="dropdown">
              <button
                class="btn btn-link text-white text-decoration-none"
                type="button"
              >
              <h6>預約聽課</h6>
              </button>
            </div>
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>

<style scoped lang="scss">
.positionSet {
  position: absolute;
}
.navSet a {
  color: #fff;
}
@media (max-width: 576px) {
  .positionSet {
  position: fixed;
}
  .navSet {
    padding: 5.5px;
    a {
      color: #000;
    }
  }
}
// @media (max-width: 576px){
//   .positionSet {
//     background-color: #fff;
//   }
// }
// .dropdownSit::after {
//   content: '';
//   position: absolute;
//   top: -15px;
//   left: 50%;
//   width: 0;
//   height: 0;
//   border-style: solid;
//   border-width: 0 15px 15px 15px;
//   border-color: transparent transparent #343a40 transparent;
//   transform: translateX(-50%);
// }
// .dropdown-menu {
//   transform: translate(-20%, 30%) !important;
// }
</style>

<script>
export default {
  data() {
    return {
      classList: {
        navBar: 'navSet',
      },
    };
  },
  components: {},
  methods: {
    toggleModal() {
      this.dropdown.toggle();
    },
  },
  mounted() {
    window.addEventListener('scroll', () => {
      const windowY = window.scrollY;
      const breakpoint = document.getElementById('breakpoint');
      if (windowY > (breakpoint.offsetTop / 8)) {
        this.classList = {
          navBar: 'navSet bg-white',
        };
      } else {
        this.classList = {
          navBar: 'navSet',
        };
      }
    });
  },
};
</script>
