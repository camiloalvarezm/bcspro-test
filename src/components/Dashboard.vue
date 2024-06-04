<script setup></script>

<template>
  <div class="dashboard-container mx-auto">
    <h1 class="greeting p-0">Hello, Gidget</h1>
    <div class="d-flex">
      <div class="card my-profile p-0">
        <div
          class="card-header d-flex justify-content-between align-items-center"
        >
          <h5 class="title m-0">My profile</h5>
          <a class="link m-0 d-flex align-items-center pointer">
            View Full Profile
            <img
              class="ms-3"
              src="../assets/right-arrow.svg"
              alt="right-arrow-icon"
            />
          </a>
        </div>
        <div class="card-body p-0 d-flex align-items-center">
          <img src="../assets/company.png" alt="company-img" />
          <div class="ms-4">
            <p>Name</p>
            <p>Company</p>
            <p>Email</p>
            <p>Phone</p>
            <p>Seats</p>
          </div>
          <div class="d-flex flex-column ms-3">
            <span>Gidget Wiggington</span>
            <span>Compliance-R-Us</span>
            <span>gwigs@compliancerus.com</span>
            <span>(703) 256-1234</span>
            <span>4 Teammates</span>
          </div>
        </div>
      </div>

      <div class="card my-stats p-0">
        <h5 class="card-header d-flex align-items-center title m-0">
          My Stats
        </h5>
        <div class="card-body"></div>
      </div>
    </div>

    <div class="card latest-activity">
      <h5 class="card-header title m-0 d-flex align-items-center">
        Latest Activity
      </h5>
      <div class="card-body"></div>
    </div>

    <div class="card asked-questions">
      <h5 class="card-header title d-flex align-items-center">
        Frequently Asked Questions: <span class="label">General</span>
      </h5>
      <div class="card-body"></div>
    </div>
  </div>
</template>

<style scoped lang="scss">
@import "../style.scss";

.dashboard-container {
  width: 1176px;
}

h1.greeting {
  font-weight: $font-weight-greeting;
  font-size: $font-size-greeting;
  margin: 17px 0 27px 0;
}

h5.title {
  font-weight: $font-weight-title;
  font-size: $font-size-title;
}

span.label {
  font-size: $font-size-label;
  font-weight: $font-weight-label;
  margin-left: 8px;
}

.card-header {
  height: 51px;

  a.link {
    @include link-styles;
  }
}

.my-profile,
.my-stats {
  height: 238px;
  margin-bottom: 30px;
}

.my-profile {
  width: 456px;

  .card-body {
    img {
      width: 118px;
      margin-left: 27px;
    }

    p {
        margin: 0 0 6px 0;
        font-weight: $font-weight-title;
        font-size: 14px;
    }

    span {
        font-size: 14px;
        margin: 0 0 6px 0;
    }
  }
}

.my-stats {
  width: 698px;
  margin-left: 23px;
}

.latest-activity {
  height: 312px;
  width: 1176px;
  margin-bottom: 30px;
}

.asked-questions {
  width: 1176px;
  height: 359px;
  margin-bottom: 40px;
}
</style>
