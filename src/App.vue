<template>
  <div class="container-scroller">
    <div class="horizontal-menu">
      <Navbar />
    </div>
    <div class="container-fluid page-body-wrapper">
      <div class="main-panel">
        <div class="content-wrapper">
          <div class="row">
            <Welcomeback />
          </div>
          <div class="row">
            <div class="col-xl-6 grid-margin">
              <div class="row">
                <Totalusers />
                <Totalprojects />
              </div>
              <div class="row">
                <div class="col-md-12 stretch-card">
                  <Downloads />
                </div>
              </div>
            </div>
            <div class="col-xl-6 grid-margin stretch-card">
              <Totalsaleschart />
            </div>
          </div>
          <div class="row">
            <Tinytotalsales />
            <Tinytotalpurchases />
            <Tinytotalorders />
            <Tinytotalgrowth />
          </div>
          <div class="row">
            <div class="col-xl-8 grid-margin stretch-card">
                <Tickets />
            </div>
            <div class="col-xl-4 grid-margin stretch-card">
              <Updates />
            </div>
          </div>
          <div class="row">
            <div class="col-xl-3 grid-margin stretch-card">
              <Distribution />
            </div>
            <div class="col-xl-9 grid-margin stretch-card">
              <Salesreport />
            </div>
          </div>
          <div class="row">
            <div class="col-md-12">
              <Openinvoices />
            </div>
          </div>
        </div>
        <Footer />
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from "./components/navbar/navbar";
import Welcomeback from "./components/welcomeback";
import Totalusers from "./components/totals/totalusers";
import Totalprojects from "./components/totals/totalprojects";
import Downloads from "./components/totals/downloads";
import Totalsaleschart from "./components/totals/totalsaleschart";
import Tinytotalsales from "./components/totals/tiny/Tinytotalsales";
import Tinytotalpurchases from "./components/totals/tiny/Tinytotalpurchases";
import Tinytotalorders from "./components/totals/tiny/Tinytotalorders";
import Tinytotalgrowth from "./components/totals/tiny/Tinytotalgrowth";
import Tickets from "./components/tickets/tickets";
import Updates from "./components/updates/updates";
import Distribution from "./components/distribution";
import Salesreport from "./components/salesreport/salesreport";
import Openinvoices from "./components/openinvoices/openinvoices";
import Footer from "./components/footer";

export default {
  name: "app",
  components: {
    Navbar,
    Welcomeback,
    Totalusers,
    Totalprojects,
    Downloads,
    Totalsaleschart,
    Tinytotalsales,
    Tinytotalpurchases,
    Tinytotalorders,
    Tinytotalgrowth,
    Tickets,
    Updates,
    Distribution,
    Salesreport,
    Openinvoices,
    Footer
  }
};
</script>

<style>
</style>
