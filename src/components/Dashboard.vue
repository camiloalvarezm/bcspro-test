<script setup>
import { ref } from "vue";

const listItems = ref([
  {
    company: "Mudleaf Coffee",
    action: "Due Date Reminders Sent",
    date: "Sep 1, 2023",
    person: "Jennifer Bellafonte",
    role: "Account Manager",
  },
  {
    company: "Hooligan's Glass Company",
    action: "Employer Dashboard Visited",
    date: "August 31, 2023",
    person: "Gidget Wiggington",
    role: "Owner",
  },
  {
    company: "Security Services of North D...",
    action: "Employer Note Created",
    date: "August 31, 2023",
    person: "Jennifer Bellafonte",
    role: "Account Manager",
  },
  {
    company: "Acme Brick",
    action: "Analysis Report Downloaded",
    date: "August 31, 2023",
    person: "Gidget Wiggington",
    role: "Owner",
  },
  {
    company: "Mudleaf Coffee",
    action: "Analysis Report Downloaded",
    date: "August 31, 2023",
    person: "Gidget Wiggington",
    role: "Owner",
  },
]);
</script>

<template>
  <div class="dashboard-container mx-auto">
    <h1 class="greeting p-0">Hello, Gidget</h1>

    <div class="d-flex">
      <div class="card my-profile p-0">
        <div
          class="card-header d-flex justify-content-between align-items-center px-4"
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
        <h5 class="card-header d-flex align-items-center title m-0 px-4">
          My Stats
        </h5>
        <div
          class="card-body p-0 d-flex align-items-center justify-content-center"
        >
          <div
            style="width: 175px; margin-right: 19px"
            class="d-flex flex-column align-items-center justify-content-center"
          >
            <span class="number rounded-pill" style="padding: 4px 16px"
              >19</span
            >
            <p class="title text-center">Employers in Progress</p>
            <p class="text-center">
              Lorem ipsum dolor sit amet, consectetur adipiscing.
            </p>
          </div>
          <div
            style="width: 175px; margin-right: 19px"
            class="d-flex flex-column align-items-center justify-content-center"
          >
            <span class="number rounded-pill" style="padding: 4px 12px"
              >32</span
            >
            <p class="title text-center">Total Employers</p>
            <p class="text-center">
              Lorem ipsum dolor sit amet, consectetur adipiscing.
            </p>
          </div>
          <div
            style="width: 251px"
            class="d-flex flex-column align-items-center justify-content-center"
          >
            <span class="number rounded-pill" style="padding: 4px 24px"
              >$10,398,149</span
            >
            <p class="title text-center">Total Compliance Risk Identified</p>
            <p class="text-center" style="width: 175px">
              Lorem ipsum dolor sit amet, consectetur adipiscing.
            </p>
          </div>
        </div>
      </div>
    </div>

    <div class="card latest-activity">
      <div
        class="card-header d-flex justify-content-between align-items-center px-4"
      >
        <h5 class="title m-0">Latest Activity</h5>
        <a class="link m-0 d-flex align-items-center pointer">
          View All Employers
          <img
            class="ms-3"
            src="../assets/right-arrow.svg"
            alt="right-arrow-icon"
          />
        </a>
      </div>
      <ul class="list-group list-group-flush">
        <li class="list-group-item table-header" style="height: 50px">
          <span class="table-title-1">Employer Name</span>
          <span class="table-title-2">Latest Activity</span>
          <span class="table-title-3">Activity Date</span>
          <span class="table-title-4">Team Member</span>
          <span class="table-title-5">Role</span>
          <span class="table-title-6"></span>
        </li>
        <li
          v-for="(item, index) in listItems"
          :key="index"
          class="list-group-item table-row"
        >
          <span class="table-col-1">{{ item.company }}</span>
          <span class="table-col-2">
            <span class="rounded-pill">{{ item.action }}</span>
          </span>
          <span class="table-col-3">{{ item.date }}</span>
          <span class="table-col-4">{{ item.person }}</span>
          <span class="table-col-5">{{ item.role }}</span>
          <button class="btn d-flex align-items-center justify-content-center">
            <img src="../assets/right-arrow-w.svg" alt="right-arrow-icon" />
          </button>
        </li>
      </ul>
    </div>

    <div class="card asked-questions">
      <div
        class="card-header d-flex justify-content-between align-items-center px-4"
      >
        <h5 class="title m-0 my-1">
          Frequently Asked Questions: <span class="label">General</span>
        </h5>
        <a class="link m-0 d-flex align-items-center pointer">
          View All Frequently Asked Questions
          <img
            class="ms-3"
            src="../assets/right-arrow.svg"
            alt="right-arrow-icon"
          />
        </a>
      </div>
      <div class="card-body p-0 d-flex flex-row">
        <div class="section-1">
          <section>
            <header>
              <h4>How do I use BCS Pro?</h4>
            </header>
            <article>
              <p>
                BCS Pro can be used to diagnose, plan, and communicate an
                employer's group health compliance requirements. The
                <span>Calendar</span>
                function serves to identify requirements and send reminders to
                relevant parties, the <span>Planning</span> tool is used by
                benefits operational staff to assist in seasonal review meetings
                with clients, and the <span>Assessment</span> is a tool used to
                identify the gaps and risks in an employer's group health plan.
                To explore each section for an employer, navigate to an
                employer's dashboard to Calendar, Assessment, or Planning.
              </p>
            </article>
          </section>

          <section style="padding-top: 0">
            <header>
              <h4>Who can use BCS pro at my agency?</h4>
            </header>
            <article>
              <p>
                Every user is set up with their own login and password. When
                your agency signed up for BCS pro, all users were given links to
                create their own credentials. If your agency has new employees
                they would like to add that do not currently have login
                credentials, please send an email to
                <span>licenses@bcspro.com</span> with the request.
              </p>
            </article>
          </section>
        </div>

        <div class="section-2">
          <section>
            <header>
              <h4>Is BCS Pro for agencies or employers?</h4>
            </header>
            <article>
              <p>
                BCS Pro is designed for benefits agency employers to assist
                their employer clients with compliance. It generates reminders,
                artifacts, and reports that can be shared with your employers,
                but the tool itself is designed to be used by agency employees.
              </p>
            </article>
          </section>

          <section>
            <header>
              <h4>Does BCS Pro integrate to our agency management system?</h4>
            </header>
            <article>
              <p>
                The current version of BCS Pro does not directly integrate into
                your CMS. We have made it easy to create artifacts like reports
                and to-do-lists that can be easily uploaded to your CMS and tied
                to the employer's account there. We are actively working on
                integrations for future versions of BCS Pro.
              </p>
            </article>
          </section>
        </div>
      </div>
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
  margin-left: 4px;
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

  .card-body {
    .number {
      color: $custom-bg-dark-color;
      font-size: 40px;
      font-weight: $font-weight-title;
      background-color: $custom-text-color-gray;
    }

    p.title {
      font-size: 14px;
      font-weight: $font-weight-title;
      margin: 5px 0 8px 0;
    }

    p {
      font-size: 12px;
      font-weight: 400;
      margin-bottom: 0;
    }
  }
}

.latest-activity {
  height: 312px;
  width: 1176px;
  margin-bottom: 30px;

  li {
    display: flex;
    align-items: center;
    padding: 5px 24px;

    button {
      background-color: $custom-text-color-purple;
      color: $custom-text-color-purple;
      width: 31px;
      height: 31px;
      border-radius: 4px;
    }

    span {
      font-size: 14px;
      font-weight: $font-weight-title;
    }

    @for $i from 1 through 6 {
      span.table-title-#{$i} {
        font-size: 16px;
      }
    }

    .table-row {
      height: 42px;
    }

    .table-col-1,
    .table-col-4 {
      color: $custom-text-color-purple;
    }

    .table-col-2 span {
      background-color: $custom-text-color-gray;
      padding: 4px 8px;
    }

    .table-col-3,
    .table-col-5 {
      font-weight: 400;
    }

    $widths: (276px, 246px, 180px, 184px, 208px);

    @for $i from 1 through length($widths) {
      .table-title-#{$i},
      .table-col-#{$i} {
        width: nth($widths, $i);
      }
    }
  }
}

.asked-questions {
  width: 1176px;
  height: 359px;
  margin-bottom: 40px;

  .section-1 {
    padding: 19px 41px 23px 27px;
  }

  .section-2 {
    padding-top: 19px;
    padding-right: 46px;
  }

  section {
    width: 531px;
    box-sizing: content-box;

    header {
      h4 {
        font-size: 14px;
        font-weight: $font-weight-title;
      }
    }

    article {
      p {
        font-size: 14px;
        font-weight: 230;
        line-height: 18.2px;

        span {
          color: $custom-text-color-purple;
          font-weight: $font-weight-greeting;
          text-decoration: underline;
          cursor: pointer;
        }
      }
    }
  }
}
</style>
