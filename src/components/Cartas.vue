<template>
  <div class="container mt-4">
    <div class="row">
      <div class="col-md-4" v-for="(item, index) in chuck" :key="index">
        <div class="card mb-4 shadow-sm">
          <img
            src="./chuck.jpg"
            class="card-img-top"
          />
          <div class="card-body">
            <div class="icon-container">
              <i :class="item.icon"></i>
            </div>
            <p class="card-text">{{ item.value }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ChuckCardList",
  data() {
    return {
      chuck: [
        { value: "Chuck Norris can skydive into outer space.", icon: "bi bi-airplane" },
        { value: "The chief export of Chuck Norris is pain.", icon: "bi bi-box-seam" },
        { value: "Chuck Norris doesn't read books. He stares them down until he gets the information he wants.", icon: "bi bi-book" },
        { value: "Time waits for no man. Unless that man is Chuck Norris.", icon: "bi bi-clock-history" },
        { value: "If you spell Chuck Norris in Scrabble, you win. Forever.", icon: "bi bi-award" },
      ],
    };
  },
};
</script>

<style scoped>
.card {
  border-radius: 10px;
  overflow: hidden;
}

.icon-container {
  text-align: center;
  margin-bottom: 10px;
}

.icon-container i {
  font-size: 2rem;
  color: #007bff;
}

.card-title {
  font-weight: bold;
  color: #007bff;
}

.card-text {
  font-size: 0.95rem;
  color: #333;
}

.card-img-top {
  height: 150px;
  object-fit: cover;
}

.shadow-sm {
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}
</style>