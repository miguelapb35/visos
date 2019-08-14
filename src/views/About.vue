<template>
  <div class="wrapper">
    <parallax
      class="section page-header header-filter"
      :style="headerStyle"
    ></parallax>
    <div class="main main-raised">
      <div class="section profile-content">
        <div class="container">
          <div class="md-layout">
            <div class="md-layout-item md-size-50 mx-auto">
              <div class="profile">
                <div class="avatar">
                  <img
                    :src="img"
                    alt="Circle Image"
                    class="img-raised rounded-circle img-fluid"
                  />
                </div>
                <div class="name">
                  <h3 class="title">Visos Beauty Salon</h3>
                  <h6>About Us</h6>
                </div>
              </div>
            </div>
          </div>
          <div class="description text-center">
            <p class="text">
              Here at Obsessed Salon we strive to make sure we are well trained in hair, nails, and skin so that way your experience with us is a great one. We believe that a positive environment and positive staff equals happy guests. What makes our salon different from the rest ? We  believe that not only taking care of your hair at the salon, but feel that a good home care regime plays an important as well. So at Obsessed we strive to keep the costs of maintaining your style and integrity of your hair , but not to break the bank. If you are new to our salon please check out our package hair care systems for all hair types. We take pride in keeping our salon clean and well maintained for your health as well as ours. We keep up to date records of all cleaning from our foot baths to our restrooms and have them in areas for you to conveniently look at them. 
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { Tabs } from "@/components";
export default {
  components: {
    Tabs
  },
  bodyClass: "profile-page",
  data() {
    return {
    };
  },
  props: {
    header: {
      type: String,
      default: require("@/assets/img/vue-mk-header.jpg")
    },
    img: {
      type: String,
      default: require("@/assets/img/stylist-grey.jpg")
    }
  },
  computed: {
    headerStyle() {
      return {
        backgroundImage: `url(${this.header})`
      };
    }
  }
};
</script>

<style lang="scss" scoped>
.section {
  padding: 0;
}
.text {
  margin-bottom: 50px;
}
.profile-tabs /deep/ {
  .md-card-tabs .md-list {
    justify-content: center;
  }

  [class*="tab-pane-"] {
    margin-top: 3.213rem;
    padding-bottom: 50px;

    img {
      margin-bottom: 2.142rem;
    }
  }
}
</style>
