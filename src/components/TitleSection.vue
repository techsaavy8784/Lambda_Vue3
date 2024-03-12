<template>
  <div class="background_image">
    <v-container style="width: 70%">
      <v-row no-gutters>
        <v-col cols="justify-center">
          <p class="title1">
            Lambda is a modular storage network, aiming to provide a Permanent
            DA solution based on EIP-4844 and Web3 storage service.
          </p>
          <p class="title2">
            ✨Lambda DA is a permanent Ethereum DA solution based on
            EIP-4844.<br />

            🚀The great innovation is about to be released.
          </p>
          <div class="d-flex align-center justify-center ga-7 mt-9">
            <v-btn class="button1">Get LAMB</v-btn>
            <v-btn class="button2">Build Now</v-btn>
          </div>
          <div class="mt-10 justify-center d-flex flex-column">
            <p style="font-size: 39px; text-align: center">
              Countdown to Dencun Upgrade
            </p>

            <div class="d-flex justify-center ga-3 mt-7">
              <div>
                <div class="clock">01</div>
                <p style="text-align: center">Days</p>
              </div>
              <div>
                <div class="clock">16</div>
                <p style="text-align: center">Hours</p>
              </div>
              <div>
                <div class="clock">33</div>
                <p style="text-align: center">Minutes</p>
              </div>
              <div>
                <div class="clock">03</div>
                <p style="text-align: center">Seconds</p>
              </div>
            </div>
            <p
              style="font-size: 19px; text-align: center; margin-bottom: 120px"
              class="mt-7"
            >
              Upgrade occurring at Beacon Slot 8626176.
            </p>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script></script>

<style>
.clock {
  font-size: 40px;
  background-color: #222;
  padding-left: 15px !important;
  padding-right: 15px !important;
  border-radius: 0.15em 0.15em;
}
.background_image {
  background-image: url(https://www.lambda.im/img/BG.a63fe479.png);
  background-repeat: no-repeat;
  background-size: cover;
  width: 100vw;
}
.title1 {
  margin-top: 60px;
  font-size: 32px;
  font-weight: 600;
  color: #fff;
  line-height: 42px;
  text-align: center;
}
.title2 {
  margin-top: 30px;
  text-align: center;
  font-size: 18px;
  color: #fff;
  line-height: 22px;
}
.button1 {
  background: transparent !important;
  border: 1px solid #fff !important;
  color: #fff;
  border-radius: 34px !important;
  cursor: pointer;
  text-transform: capitalize !important;
  box-shadow: none !important;
}
.button2 {
  background: #fff !important;
  border: 1px solid #fff !important;
  color: #3f4ae1 !important;
  border-radius: 34px !important;
  cursor: pointer;
  text-transform: capitalize !important;
  box-shadow: none !important;
}
</style>
