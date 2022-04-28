<template>
  <div class="container-fluid">
    <div class="container">
      <div class="row p-1">
        <div class="col-5">
          <p>Starts TOMORROW! Our biggest event of the year...</p>
        </div>
        <div class="col-1"><i class="fa-solid fa-clock"></i></div>
        <div class="col-1 p-0 text-center">
          <p>{{ displayDays }}:</p>
        </div>
        <div class="col-1 p-0 text-center">
          <p>{{ displayHours }}:</p>
        </div>
        <div class="col-1 p-0 text-center">
          <p>{{ displayMinutes }}:</p>
        </div>
        <div class="col-1 p-0 text-center">
          <p>{{ displaySeconds }}</p>
        </div>
        <div class="col-2"><button class="">Get started today</button></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CountdownComponent",
  props: ["year", "month", "date", "hour", "minute", "second", "millisecond"],
  data: () => ({
    displayDays: 0,
    displayHours: 0,
    displayMinutes: 0,
    displaySeconds: 0,
  }),
  computed: {
    _seconds: () => 1000,
    _minutes() {
      return this._seconds * 60;
    },
    _hours() {
      return this._minutes * 60;
    },
    _days() {
      return this._hours * 24;
    },
  },
  mounted() {
    this.showRemaining();
  },
  methods: {
    showRemaining() {
      const timer = setInterval(() => {
        const now = new Date();
        const end = new Date(2022, 4, 22, 10, 10, 10, 10);
        const distance = end.getTime() - now.getTime();

        if (distance < 0) {
          clearInterval(timer);
          return;
        }

        const days = Math.floor(distance / this._days);
        const hours = Math.floor((distance % this._days) / this._hours);
        const minutes = Math.floor((distance % this._hours) / this._minutes);
        const seconds = Math.floor((distance % this._minutes) / this._seconds);
        this.displayMinutes = minutes < 10 ? "0" + minutes : minutes;
        this.displaySeconds = seconds < 10 ? "0" + seconds : seconds;
        this.displayHours = hours < 10 ? "0" + hours : hours;
        this.displayDays = days < 10 ? "0" + days : days;
      }, 1000);
    },
  },
};
</script>

<style lang="scss" scoped>
@import "@/style/general";
@import "@/style/component-style";
.container-fluid {
  background-color: rgb(233, 233, 233);

  button {
    padding: 5px;
    border: none;
    background-color: $main-orange;
    color: #fff;
    font-weight: bold;
    border-radius: 10px;
  }
  p {
    font-weight: bold;
  }
}
</style>
