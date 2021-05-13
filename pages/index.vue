<template>
  <v-container>
    <v-layout row wrap justify-center align-center>
      <v-flex md6>
        <v-card
          class="debit-card"
          :class="{
            'pa-9': $vuetify.breakpoint.smAndUp,
            'pa-6': $vuetify.breakpoint.xsOnly,
          }"
        >
          <v-row>
            <v-col>
              <img src="../static/assets/logo.svg" alt="" />
            </v-col>
            <v-col class="text-right pa-2">
              <v-btn @click="visible = !visible" icon class="pa-0" small>
                <v-icon size="30" color="#575A65">{{
                  visible ? 'visibility' : 'visibility_off'
                }}</v-icon>
              </v-btn>
            </v-col>
          </v-row>
          <v-row
            :class="{
              'mt-16': $vuetify.breakpoint.smAndUp,
              'mt-9': $vuetify.breakpoint.xsOnly,
            }"
          >
            <v-col>
              <p class="card-pan">{{ visible ? '9273' : '••••' }}</p>
            </v-col>
            <v-col>
              <p class="card-pan">{{ visible ? '6372' : '••••' }}</p>
            </v-col>
            <v-col>
              <p class="card-pan">{{ visible ? '7381' : '••••' }}</p>
            </v-col>
            <v-col>
              <p class="card-pan">9784</p>
            </v-col>
          </v-row>
          <v-row
            :class="{
              'mt-16': $vuetify.breakpoint.smAndUp,
              'mt-7': $vuetify.breakpoint.xsOnly,
            }"
          >
            <v-col md="7" cols="6">
              <p class="card-holder">
                {{ visible ? 'ALABI ADEWUMI D.' : 'Cardholder Name' }}
              </p>
            </v-col>
            <v-col class="text-right">
              <div class="d-flex">
                <p class="small mt-1">VALID<br />THRU</p>
                <p class="date ml-3">10/12</p>
              </div>
            </v-col>
            <v-col class="text-right pr-0">
              <div class="d-flex text-right">
                <p class="small mt-2">CVV</p>
                <p class="date ml-3">{{ visible ? '672' : '•••' }}</p>
              </div>
            </v-col>
          </v-row>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      visible: false,
    }
  },
}
</script>
<style lang="scss" scoped>
.debit-card {
  width: 499px;
  height: 305px;

  background-color: #131313 !important;
  background-image: url('../static/assets/patricia icon.png');
  background-size: 73%;
  border: 1px solid #000000 !important;
  box-sizing: border-box;
  box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25) !important;
  border-radius: 20px !important;
}
p.card-pan {
  filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.25));
  font-style: normal;
  font-weight: normal;
  font-size: 23px;
  line-height: 29px;
  letter-spacing: 0.08em;
  color: #d3dce6;
}
p.card-holder {
  font-style: normal;
  font-weight: normal;
  font-size: 14px;
  line-height: 23px;
  color: #d3dce6;
  text-overflow: ellipsis !important;
  white-space: nowrap;
  word-break: normal;
}
p.small {
  font-style: normal;
  font-weight: normal;
  font-size: 7px;
  line-height: 8px;
  color: #9da8b6;
}
p.date {
  font-style: normal;
  font-weight: normal;
  font-size: 16px;
  line-height: 27px;

  color: #d3dce6;
}
@media only screen and (max-width: 600px) {
  .debit-card {
    height: 220px;
  }
  p.card-pan {
    font-size: 18px;
  }
  p.card-holder,
  p.date {
    font-size: 12px;
  }
}
@media only screen and (max-width: 320px) {
  .debit-card {
    height: 180px;
  }
  p.card-pan {
    font-size: 15px;
  }
  p.card-holder,
  p.date {
    font-size: 12px;
  }
  .mt-9 {
    margin-top: 20px !important;
  }
  .mt-7 {
    margin-top: 10px !important;
  }
  .ml-3 {
    margin-left: 3px !important;
  }
}
</style>
