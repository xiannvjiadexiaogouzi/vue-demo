<template>
  <div class="mySite">
    <header-component :title="'用户中心'"/>
    <img src="../assets/img/user/bg.png" alt>
    <div class="form border-1px">
      <div class="avatar">
        <div class="avatar-img">
          <img src="../assets/img/user/avatar.png" alt>
        </div>
        <div class="avatar-name">张思涵</div>
      </div>
      <div class="nosite top">您还没有工地？</div>
      <div class="btn">直接预订</div>
    </div>
    <!-- <footer-component/> -->
  </div>
</template>

<script>
import headerComponent from "@/components/HeaderComponent";
// import footerComponent from "@/components/FooterComponent";

export default {
  name: "mySite",
  components: {
    headerComponent
    // footerComponent
  }
};
</script>

<style lang="stylus" scoped>
@import '../assets/stylus/mixin.styl'

.mySite
  background: $bgColor

  &>img
    width: 100%
    position: relative
    top: pr(40)

  .form
    display: flex
    flex-direction: column
    justify-content: center
    align-items: center
    position: relative
    top: pr(25)
    background: white
    padding-top: pr(8)
    margin-bottom: pr(30)
    padding-bottom: pr(30)

    .avatar
      position: absolute
      top: pr(-45)

      .avatar-img
        width: pr(90)
        height: pr(90)

        &>img
          width: 100%

      .avatar-name
        font-size: pr(18)
        font-family: HiraginoSansGB-W3
        font-weight: normal
        color: rgba(95, 95, 95, 1)
        text-align: center
        margin-top: pr(10)

    .option
      width: pr(277)
      height: pr(40)
      margin: pr(7) 0
      padding: pr(13) pr(12)
      display: flex
      justify-content: flex-start
      align-items: center
      border-radius: pr(3)
      border: pr(1) solid rgb(216, 216, 216)
      color: #5F5F5F

      &>span
        font-size: pr(14)
        font-family: FZLTHJW--GB1-0
        font-weight: normal
        line-height: pr(15)
        outline: none
        border: none
        width: 100%

      &>i
        transform: rotate(180deg)

    .top
      margin-top: pr(163)
    .nosite
      font-size:pr(14);
      font-family:HiraginoSansGB-W3;
      font-weight:normal;
      color:rgba(95,95,95,1);
    .btn
      margin-top pr(22)

</style>
