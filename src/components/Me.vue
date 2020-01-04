<template>
  <div class="me">
    <section class="profile">
      <div class="img">
        <img class="img-me" src="../assets/images/eliyahu.jpg" alt />
      </div>
      <h3 class="name">Eliyahu Hillel</h3>
      <h4 class="profesion">Web developer</h4>
      <ul class="links">
        <a
          target="_blank"
          rel="noopener noreferrer"
          href="https://www.linkedin.com/in/eliyahu-hillel-394b84144/"
        >
          <li class="circle">
            <i class="fab fa-linkedin-in"></i>
          </li>
        </a>
        <a
          target="_blank"
          rel="noopener noreferrer"
          href="https://www.facebook.com/profile.php?id=100009026220513"
        >
          <li class="circle">
            <i class="fab fa-facebook-f"></i>
          </li>
        </a>
        <a target="_blank" rel="noopener noreferrer" href="https://github.com/HIELIYA2">
          <li class="circle">
            <i class="fab fa-github"></i>
          </li>
        </a>
      </ul>
    </section>

    <section class="Self-detail">
      <p>
        Over Eight months experience as a web application developer. A team player is eager to find
        the next opportunity and notice the details. Currently working as a freelancer, Developing
        an application that helps to memories patterns
      </p>
    </section>
  </div>
</template>

<script>
export default {
  name: "Me"
};
</script>

<style scoped lang="scss">
.me {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 75vh;
  padding: 0 70px 0 200px;
  .profile {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    .img {
      width: 200px;
      height: 200px;
      overflow: hidden;
      margin-bottom: 20px;
      border-radius: 50%;
      .img-me {
        object-fit: cover;
        margin: -10% -35%;
        width: 160%;
        height: 160%;
      }
    }
    .name {
      margin-bottom: 6px;
      font-weight: bold;
      font-size: 22px;
    }
    .profesion {
      font-size: 17px;
      margin-bottom: 16px;
    }
    .links {
      display: flex;
      justify-content: space-evenly;
      .circle {
        cursor: pointer;
        margin: 10px;
        background-color: #4d4d4d;
        border-radius: 50%;
        width: 35px;
        height: 35px;
        display: flex;
        justify-content: center;
        align-items: center;
        margin-bottom: 20px;
        transition: 0.3s;
        .fab {
          font-size: 20px;
          color: white;
        }
      }
      .circle:hover {
        background-color: #fed136;
      }
    }
  }
  .Self-detail {
    padding: 100px;
    p {
      line-height: 1.6;
    }
  }
}

@media (max-width: 893px) {
  .me {
    display: flex;
    flex-direction: column;
    height: auto;
    padding: 4px;

    .profile {
      .img {
        width: 140px;
        height: 140px;
        overflow: hidden;
        margin-bottom: 20px;
        border-radius: 50%;
        .img-me {
          object-fit: cover;
          margin: -10% -35%;
          width: 160%;
          height: 160%;
        }
      }
    }
    .Self-detail {
      padding: 14px;
    }
  }
}
</style>
