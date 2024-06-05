<script setup></script>

<template>
  <nav class="custom-navbar">
    <div class="d-flex flex-row justify-content-between w-100">
      <div class="d-flex flex-row align-items-center">
        <img class="logo" src="../assets/logo.svg" alt="logo-img" />
        <ul class="d-none d-md-flex m-0 p-0 h-100 d-flex align-items-center text-white">
          <li class="list-inline-item d-flex align-items-center active">
            Home
          </li>
          <li class="list-inline-item">Employers</li>
          <li class="list-inline-item">Help & Resources</li>
        </ul>
      </div>
      <div class="text-white d-flex align-items-center">
        <img class="search-icon" src="../assets/search.svg" alt="search-img" />
        <img class="user-icon" src="../assets/user.svg" alt="user-img" />
      </div>
    </div>
  </nav>
</template>

<style scoped lang="scss">
@import "../style.scss";
.custom-navbar {
  height: 61px;
  background-color: $custom-bg-dark-color;
}

img.logo {
  width: 135px;
  margin: 0 66px 0 28px;
  width: auto;
}

ul {
  font-size: 14px;
  li {
    padding: 0 20px;
    cursor: pointer;
  }

  .active {
    background-color: $custom-bg-medium-color;
    height: 61px;
  }
}

img.user-icon,
img.search-icon {
  width: 20px;
}

img.user-icon {
  margin: 0 26px 0 20px;
}

img.search-icon {
  margin-left: 20px;
}
</style>
