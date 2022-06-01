<template>
  <div id="app">
    <AppHeader />
    <AppMain />
    <AppFooter :listItem="footerMenu" :contactData="contacts" />
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import AppFooter from "./components/AppFooter.vue";

export default {
  name: "App",
  components: {
    AppHeader,
    AppMain,
    AppFooter,
  },
  data: function () {
    return {
      footerMenu: [
        {
          title: "About",
          listMenu: [
            "The Company",
            "Institutional",
            "Social & Events",
            "Innovation",
            "Environment",
            "Technology",
          ],
        },
        {
          title: "Services",
          listMenu: [
            "Audit & Assurance",
            "Financial Advisory",
            "Analytics M&A",
            "Middle Marketing",
            "Legal Consulting",
            "Regulatory Risk",
          ],
        },
        {
          title: "Support",
          listMenu: [
            "Responsibility",
            "Terms of Use",
            "About Cookies",
            "Privacy Policy",
            "Accessibility",
            "Information",
          ],
        },
      ],
      contacts: {
        phoneNumber: "+1 (305) 1234-5678",
        emailAdress: "hello@example.com",
        position: "Main Avenue, 987",
      },
    };
  },
};
</script>

<style lang="scss">
@import "./style/common.scss";

#app {
}
</style>
