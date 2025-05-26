<template>
  <div :class="['driver-radio', className]">
    <div class="overlap-group">
      <TeamLogo
        class="team-instance"
        :mercedes="teamMercedes"
        team="mercedes"
      />
      <div class="last-name">HAMILTON</div>
      <div class="text-wrapper">RADIO</div>
    </div>
    <div class="line" />
    <!-- 音频波形竖条 -->
    <div class="audio-bars">
      <div class="bar bar-1"></div>
      <div class="bar bar-2"></div>
      <div class="bar bar-3"></div>
      <div class="bar bar-4"></div>
      <div class="bar bar-5"></div>
      <div class="bar bar-6"></div>
      <div class="bar bar-7"></div>
      <div class="bar bar-8"></div>
      <div class="bar bar-9"></div>
      <div class="bar bar-10"></div>
      <div class="bar bar-11"></div>
      <div class="bar bar-12"></div>
      <div class="bar bar-13"></div>
      <div class="bar bar-14"></div>
      <div class="bar bar-15"></div>
      <div class="bar bar-16"></div>
      <div class="bar bar-17"></div>
      <div class="bar bar-18"></div>
      <div class="bar bar-19"></div>
      <div class="bar bar-20"></div>
    </div>
    <div class="transcription">
      <p class="div">
        &quot;F1 SEASON IS FINISHED, SO ALL I HAVE LEFT IS MAKING IT IN FIGMA.&quot;
      </p>
    </div>
  </div>
</template>

<script>
import TeamLogo from './TeamLogo.vue';

export default {
  name: 'DriverRadio',
  components: {
    TeamLogo
  },
  props: {
    className: {
      type: String,
      default: ''
    },
    teamMercedes: {
      type: String,
      default: 'mercedes.png'
    }
  }
};
</script>

<style>
.driver-radio {
  background: linear-gradient(
    180deg,
    rgba(23, 22, 32, 1) 0%,
    rgba(48, 49, 59, 1) 0%,
    rgba(23, 22, 30, 1) 30%,
    rgba(23, 22, 30, 1) 100%
  );
  height: 255px;
  position: relative;
  width: 200px; /* 固定宽度 */
  max-width: 200px; /* 确保不会超出 */
  margin: 0 auto; /* 居中对齐 */
}

.driver-radio .overlap-group {
  height: 58px;
  left: 10px;
  right: 10px;
  position: absolute;
  top: 11px;
  display: flex;
  flex-direction: column;
  align-items: flex-end; /* 保持右对齐 */
}

.driver-radio .team-instance {
  right: 95px !important; /* 贴着RADIO文字的左边 */
  position: absolute !important;
  top: 32px !important;
}

.driver-radio .last-name {
  color: #65dccf;
  font-family: "Formula1-Display-Bold", Helvetica;
  font-size: 26.1px;
  font-weight: 700;
  right: 0;
  letter-spacing: -1.56px;
  line-height: normal;
  position: absolute;
  top: 0;
  white-space: nowrap;
  text-align: right; /* 确保右对齐 */
}

.driver-radio .text-wrapper {
  color: #ffffff;
  font-family: "Formula1-Display-Bold", Helvetica;
  font-size: 26.1px;
  font-weight: 700;
  right: 0; /* 改为右对齐 */
  letter-spacing: -1.56px;
  line-height: normal;
  position: absolute;
  top: 27px;
  white-space: nowrap;
  text-align: right; /* 确保右对齐 */
}

.driver-radio .line {
  background-color: #65dccf;
  height: 2px;
  left: 0;
  position: absolute;
  top: 114px;
  width: 200px; /* 与容器宽度一致 */
}

/* 音频波形竖条样式 */
.driver-radio .audio-bars {
  position: absolute;
  top: 75px;
  left: 5px;
  width: 190px;
  height: 30px;
  display: flex;
  align-items: flex-end;
  justify-content: space-between;
  gap: 1px;
}

.driver-radio .bar {
  background: linear-gradient(
    to top,
    #65dccf 0%,
    #65dccf 60%,
    rgba(101, 220, 207, 0.8) 80%,
    rgba(101, 220, 207, 0.4) 90%,
    rgba(101, 220, 207, 0.1) 100%
  );
  width: 7px;
  border-radius: 3px 3px 0 0;
}

/* 不同高度的竖条 */
.driver-radio .bar-1 { height: 8px; }
.driver-radio .bar-2 { height: 16px; }
.driver-radio .bar-3 { height: 12px; }
.driver-radio .bar-4 { height: 20px; }
.driver-radio .bar-5 { height: 18px; }
.driver-radio .bar-6 { height: 14px; }
.driver-radio .bar-7 { height: 22px; }
.driver-radio .bar-8 { height: 10px; }
.driver-radio .bar-9 { height: 25px; }
.driver-radio .bar-10 { height: 15px; }
.driver-radio .bar-11 { height: 28px; }
.driver-radio .bar-12 { height: 13px; }
.driver-radio .bar-13 { height: 19px; }
.driver-radio .bar-14 { height: 24px; }
.driver-radio .bar-15 { height: 11px; }
.driver-radio .bar-16 { height: 17px; }
.driver-radio .bar-17 { height: 21px; }
.driver-radio .bar-18 { height: 9px; }
.driver-radio .bar-19 { height: 13px; }
.driver-radio .bar-20 { height: 7px; }

.driver-radio .transcription {
  align-items: center;
  background: linear-gradient(
    180deg,
    rgba(34, 36, 43, 1) 0%,
    rgba(17, 19, 25, 1) 100%
  );
  border-color: #30333c;
  border-top-style: solid;
  border-top-width: 1px;
  display: flex;
  gap: 8px;
  justify-content: flex-end;
  left: 0;
  padding: 15px;
  position: absolute;
  top: 125px;
  width: 200px; /* 与容器宽度一致 */
  box-sizing: border-box; /* 确保padding不会增加总宽度 */
}

.driver-radio .div {
  color: #65dccf;
  font-family: "Formula1-Display-Regular", Helvetica;
  font-size: 16.4px;
  font-weight: 400;
  letter-spacing: -0.99px;
  line-height: normal;
  margin-top: -1.00px;
  position: relative;
  text-align: right; /* 右对齐 */
  width: 100%; /* 占满可用宽度 */
  max-width: 170px; /* 考虑padding后的最大宽度 */
}
</style>