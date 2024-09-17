<!-- tamplete -->
<template>
  <footer className="footer">
    <!-- <h2 className="logo">
      Sabbat<span className="logoLight">Lumpatshia</span>
    </h2> -->
    <div class="flex title flex-shrink-0 items-center title-desktop">
      <span
        ><strong> Sabbat </strong> <span class="myName">Lumpatshia</span></span
      >
    </div>
    <div className="socialLinks">
      <a href="#" aria-label="GitHub profile">
        <img
          src="https://cdn.builder.io/api/v1/image/assets/TEMP/d7630a9f8a9935476612192ef1a23d48c0f7b3c723fa9bbc38040a71beeb5d38?apiKey=05e50562800e46f288f7d79b65b333f2&"
          alt=""
          className="socialIcon"
        />
      </a>
      <a href="#" aria-label="LinkedIn profile">
        <img
          src="https://cdn.builder.io/api/v1/image/assets/TEMP/9c27b90e3164ff915009ef22dfe758438e94156e3f2726a998b23be383474497?apiKey=05e50562800e46f288f7d79b65b333f2&"
          alt=""
          className="socialIcon"
        />
      </a>
      <a href="#" aria-label="Twitter profile">
        <img
          src="https://cdn.builder.io/api/v1/image/assets/TEMP/04d4bc0e77f04c0cc116b217468e792eabf54ab16547bda19f531e181b448d3a?apiKey=05e50562800e46f288f7d79b65b333f2&"
          alt=""
          className="socialIcon"
        />
      </a>
    </div>
  </footer>
</template>

<!-- script -->
<script setup>
import { ref } from "vue";
</script>

<!-- style -->
<style scoped>
.footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 40px 65px;
  margin-top: 45px;
  color: #fff;
}
.title {
  font-size: 1.9em;
}

.myName {
  color: #a6bbcc;
}

.logo {
  font: 700 32px Inter, sans-serif;
}

.logoLight {
  font-weight: 400;
}

.socialLinks {
  display: flex;
  gap: 17px;
}

.socialIcon {
  width: 40px;
  height: 40px;
}

@media (max-width: 991px) {
  .footer {
    flex-direction: column;
    gap: 20px;
    padding: 30px 20px;
  }
}
</style>
