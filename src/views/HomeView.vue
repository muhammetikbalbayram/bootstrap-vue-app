<template>
  <b-container>
    <b-row align-v="center">
      <job-card v-for="job in jobs" :key="job.id" :name="job.name"></job-card>
      <!--      <b-col md="3">-->
      <!--        <b-card-->
      <!--          title="This is a card"-->
      <!--          img-src="https://i.picsum.photos/id/1014/6016/4000.jpg?hmac=yMXsznFliL_Y2E2M-qZEsOZE1micNu8TwgNlHj7kzs8"-->
      <!--          img-alt="Job-info"-->
      <!--          img-top-->
      <!--          tag="article"-->
      <!--          style="max-width: 20rem"-->
      <!--          class="mb-2"-->
      <!--        >-->
      <!--          <b-card-text>-->
      <!--            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolor,-->
      <!--            nam.-->
      <!--          </b-card-text>-->
      <!--          <b-button variant="primary">Apply</b-button>-->
      <!--        </b-card>-->
      <!--      </b-col>-->
      <!--      <b-col md="3">-->
      <!--        <b-card-->
      <!--          title="This is a card"-->
      <!--          img-src="https://i.picsum.photos/id/1014/6016/4000.jpg?hmac=yMXsznFliL_Y2E2M-qZEsOZE1micNu8TwgNlHj7kzs8"-->
      <!--          img-alt="Job-info"-->
      <!--          img-top-->
      <!--          tag="article"-->
      <!--          style="max-width: 20rem"-->
      <!--          class="mb-2"-->
      <!--        >-->
      <!--          <b-card-text>-->
      <!--            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolor,-->
      <!--            nam.-->
      <!--          </b-card-text>-->
      <!--          <b-button variant="primary">Apply</b-button>-->
      <!--        </b-card>-->
      <!--      </b-col>-->
      <!--      <b-col md="3">-->
      <!--        <b-card-->
      <!--          title="This is a card"-->
      <!--          img-src="https://i.picsum.photos/id/1014/6016/4000.jpg?hmac=yMXsznFliL_Y2E2M-qZEsOZE1micNu8TwgNlHj7kzs8"-->
      <!--          img-alt="Job-info"-->
      <!--          img-top-->
      <!--          tag="article"-->
      <!--          style="max-width: 20rem"-->
      <!--          class="mb-2"-->
      <!--        >-->
      <!--          <b-card-text>-->
      <!--            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolor,-->
      <!--            nam.-->
      <!--          </b-card-text>-->
      <!--          <b-button variant="primary">Apply</b-button>-->
      <!--        </b-card>-->
      <!--      </b-col>-->
      <!--      <b-col md="3">-->
      <!--        <b-card-->
      <!--          title="This is a card"-->
      <!--          img-src="https://i.picsum.photos/id/1014/6016/4000.jpg?hmac=yMXsznFliL_Y2E2M-qZEsOZE1micNu8TwgNlHj7kzs8"-->
      <!--          img-alt="Job-info"-->
      <!--          img-top-->
      <!--          tag="article"-->
      <!--          style="max-width: 20rem"-->
      <!--          class="mb-2"-->
      <!--        >-->
      <!--          <b-card-text>-->
      <!--            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolor,-->
      <!--            nam.-->
      <!--          </b-card-text>-->
      <!--          <b-button variant="primary">Apply</b-button>-->
      <!--        </b-card>-->
      <!--      </b-col>-->
    </b-row>
  </b-container>
</template>

<script>
// @ is an alias to /src
import jobCard from "@/components/jobCard";
export default {
  name: "HomeView",
  components: {
    jobCard,
  },
  mounted() {
    this.fetchData();
  },
  data() {
    return {
      jobs: [],
    };
  },
  methods: {
    async fetchData() {
      const res = await fetch("jobs.json");
      const val = res.json();
      this.jobs = val;
      console.log(this.jobs);
    },
  },
};
</script>
