<template>
  <v-container fluid>
    <toolbar-navigation></toolbar-navigation>
    <v-row>
      <v-col cols="12">
        <v-row align="center" justify="center">
          <v-col cols="12" sm="6" lg="3" v-for="item in revenues" :key="item">
            <revenue-card></revenue-card>
          </v-col>
        </v-row>
      </v-col>
      <v-col cols="12" md="12" lg="9">
        <sale-overview></sale-overview>
      </v-col>
      <v-col cols="12" md="12" lg="3">
        <visit-separation></visit-separation>
      </v-col>
      <v-col cols="12" md="12" lg="6">
        <earning-report></earning-report>
      </v-col>
      <v-col cols="12" md="12" lg="6">
        <recent-comments></recent-comments>
      </v-col>
      <v-col cols="12" md="12" lg="4">
        <social-media-card :socialMedia="socialMedia[0]"></social-media-card>
      </v-col>
      <v-col cols="12" md="12" lg="4">
        <social-media-card :socialMedia="socialMedia[1]"></social-media-card>
      </v-col>
      <v-col cols="12" md="12" lg="4">
        <social-media-card :socialMedia="socialMedia[2]"></social-media-card>
      </v-col>
      <v-col cols="12" md="12" lg="6">
        <activity-list></activity-list>
      </v-col>
      <v-col cols="12" md="12" lg="6">
        <profile-card></profile-card>
      </v-col>
      <v-col cols="12" md="12" lg="6">
        <to-do></to-do>
      </v-col>
      <v-col cols="12" md="12" lg="6">
        <master-table></master-table>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import ToolbarNavigation from "@/components/layaout/AppToolbarNavigation";
import RevenueCard from "@/components/ui/RevenueCard";
import SocialMediaCard from "@/components/ui/SocialMediaCard";
import SaleOverview from "@/components/sales/SaleOverview";
import VisitSeparation from "@/components/sales/VisitSeparation";
import EarningReport from "@/components/reports/EarningReport";
import RecentComments from "@/components/activities/RecentComments";
import ActivityList from "@/components/activities/ActivityList";
import ProfileCard from "@/components/activities/ProfileCard";
import ToDoList from "@/components/activities/ToDoList";
import MasterTable from "@/components/activities/MasterTable";
export default {
  components: {
    "toolbar-navigation": ToolbarNavigation,
    "revenue-card": RevenueCard,
    "social-media-card": SocialMediaCard,
    "sale-overview": SaleOverview,
    "visit-separation": VisitSeparation,
    "earning-report": EarningReport,
    "recent-comments": RecentComments,
    "activity-list": ActivityList,
    "profile-card": ProfileCard,
    "to-do": ToDoList,
    "master-table": MasterTable,
  },
  data: () => ({
    revenues: ["1", "2", "3", "4"],
    socialMedia: [
      {
        icon: "mdi-twitter",
        number: "3257+",
        message: "Seguidores en twitter",
        color: "blue",
      },
      {
        icon: "mdi-facebook",
        number: "6509+",
        message: "Me gusta en facebook",
        color: "purple",
      },
      {
        icon: "mdi-email",
        number: "9062+",
        message: "Suscriptores",
        color: "green",
      },
    ],
  }),
};
</script>
