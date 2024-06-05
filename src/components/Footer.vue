<script setup></script>
<template>
  <footer class="d-flex flex-column">
    <div class="footer-wrapper d-flex flex-row mx-auto justify-content-between">
      <div class="d-flex flex-row">
        <ul class="list-inline mb-0" style="margin-right: 88px">
          <li>Home</li>
          <li>Help</li>
          <li>Search</li>
          <li>Contact</li>
        </ul>

        <ul class="list-inline mb-0" style="margin-right: 91px">
          <li>Frequently Asked Questions</li>
          <li>All Employer Dashboard</li>
          <li>Help & Resources</li>
          <li>Profile</li>
        </ul>

        <ul class="list-inline mb-0">
          <li>Privacy Policy</li>
          <li>Terms & Conditions</li>
          <li>Legal</li>
        </ul>
      </div>
      <div class="icons-wrapper">
        <img src="../assets/linkedin.svg" alt="linkedin-icon" />
        <img src="../assets/facebook.svg" alt="facebook-icon" />
        <img src="../assets/instagram.svg" alt="instagram-icon" />
        <img src="../assets/youtube.svg" alt="youtube-icon" />
      </div>
    </div>
    <div class="footer-wrapper mx-auto">
      <p class="mb-0">
        © 2024 Benefits Compliance Solutions. All rights reserved.
      </p>
    </div>
  </footer>
</template>

<style scoped lang="scss">
@import "../style.scss";

footer {
  background-color: $custom-text-color-gray;
  height: 219px;
  color: $custom-text-color-purple;
  font-size: 14px;
  font-weight: $font-weight-label;
  padding: 30px 0;

  .footer-wrapper {
    width: 1176px;

    ul li:not(:last-child) {
      margin-bottom: 8px;
    }

    ul li {
      cursor: pointer;
    }

    p {
      margin: 32px 0 0 0;
      font-size: 12px;
      color: $custom-text-color-black;
    }

    .icons-wrapper {
      img {
        margin-left: 15px;
        cursor: pointer;
      }
    }
  }
}
</style>
