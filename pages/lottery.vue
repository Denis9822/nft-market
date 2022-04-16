<template>
  <div class="lottery">
      <div class="main">
          <div class="bg-ellipse-red"></div>
          <div class="bg-ellipse-green"></div>
          <div class="container">
            <div class="column">
                <h1>The Biswap Lottery</h1>
                <h2>
                  $23 215
                </h2>
                <p>In Prizes</p>
                <div @click="showModalWallet" class="wallet">
                  <SvgImport name="wallet-white" />
                  <span>Connect Wallet</span>
                </div>
            </div>
            <div class="column2">
                <div class="bg-ticket"></div>
                <div class="ticked_time">
                    <p>GET YOUR TICKETS NOW</p>
                    <div class="time">
                          <div class="item">
                              <div class="data">
                                {{theTime.hours }}
                              </div>
                              <span>Hours</span>
                        </div>
                      <div class="item txt">:</div>
                      <div class="item">
                        <div class="data">
                          {{theTime.minutes }}
                        </div>
                        <span>Minutes</span>
                      </div>
                      <div class="item txt">:</div>
                      <div class="item">
                        <div class="data">
                          {{theTime.seconds }}
                        </div>
                        <span>Seconds</span>
                      </div>
                    </div>
                </div>
                <div class="buy">
                    <div class="price">
                        <span>$1</span>
                        <p>In BSW per ticket</p>
                    </div>
                    <div class="buy">
                       Buy tickets
                    </div>
                </div>
            </div>
          </div>
      </div>
      <div class="bg_w">
        <div class="container">
            <div class="stats_lottery">
                <div class="item">
                  <img src="/images/balance.png" alt="">
                   <div class="column">
                        <span>Lottery balance</span>
                        <p>-</p>
                   </div>

                  <div class="btn">
                      Withdraw
                  </div>
                </div>
              <div class="item">
                <img src="/images/referral.png" alt="">
                <div class="column">
                  <span>Referral</span>
                  <p>-</p>
                </div>
                <div class="btn">
                  Withdraw
                </div>
              </div>
            </div>
            <div class="draw">
              <div class="draw_w">
                <div class="title">
                  <h2>Next draw</h2>
                  <span>#403 l Draw: 29 mar. 2022y. 05:01</span>
                </div>
                <div class="wrap">
                  <div class="d_flex">
                    <div class="column">
                        <div class="bg_draw"></div>
                      <div class="bg-ellipse-green"></div>
                        <div class="group">
                            <span>Prize Pot</span>
                            <p>$23 215</p>
                            <div class="time">
                            <div class="item">
                              <div class="data">
                                {{theTime.hours }}
                              </div>
                              <span>Hours</span>
                            </div>
                            <div class="item txt">:</div>
                            <div class="item">
                              <div class="data">
                                {{theTime.minutes }}
                              </div>
                              <span>Minutes</span>
                            </div>
                            <div class="item txt">:</div>
                            <div class="item">
                              <div class="data">
                                {{theTime.seconds }}
                              </div>
                              <span>Seconds</span>
                            </div>
                          </div>
                        </div>
                    </div>
                    <div class="column">
                        <div class="ticket">
                            <div class="col">
                              <span>Your tickets</span>
                              <p>You have 0 tickets this round</p>
                            </div>
                            <div class="btn">
                              Buy tickets
                            </div>
                        </div>
                    </div>
                  </div>
                  <div v-if="dravActive==false" @click="dravActive=true" class="more">
                      <span>More</span>
                      <img src="/images/down2.png" alt="">
                  </div>
                </div>
              </div>
              <div class="draw_hidden" :class="{active:dravActive}">
                  <div class="title">
                    Match the winning number in the same order to share prizes. Current prizes up for grabs:
                  </div>
                  <div class="items">
                      <div class="item">
                          <p>Match first</p>
                          <span>940.77 BSW</span>
                          <h5>$642.02</h5>
                          <h6>3.81 BSW each</h6>
                          <h7>247 Winners</h7>
                      </div>
                    <div class="item">
                      <p>Match first2</p>
                      <span>940.77 BSW</span>
                      <h5>$642.02</h5>
                      <h6>3.81 BSW each</h6>
                      <h7>247 Winners</h7>
                    </div>
                    <div class="item">
                      <p>Match first</p>
                      <span>940.77 BSW</span>
                      <h5>$642.02</h5>
                      <h6>3.81 BSW each</h6>
                      <h7>247 Winners</h7>
                    </div>
                    <div class="item">
                      <p>Match first2</p>
                      <span>940.77 BSW</span>
                      <h5>$642.02</h5>
                      <h6>3.81 BSW each</h6>
                      <h7>247 Winners</h7>
                    </div>
                    <div class="item">
                      <p>Match first</p>
                      <span>940.77 BSW</span>
                      <h5>$642.02</h5>
                      <h6>3.81 BSW each</h6>
                      <h7>247 Winners</h7>
                    </div>
                  </div>
                <div @click="dravActive=false" class="more">
                  <span>More</span>
                  <img src="/images/down2.png" alt="">
                </div>
              </div>
            </div>
            <div class="finished_rounds">
                <div class="title">
                  <h2>Finished rounds</h2>
                  <div class="btns">
                      <div class="btn" @click="typeActive = 'all'" :class="{active:typeActive == 'all'}" >
                        All history
                      </div>
                      <div class="btn" @click="typeActive = 'your'" :class="{active:typeActive == 'your'}">
                        Your history
                      </div>
                  </div>
                </div>
                <div class="rounds">
                    <div class="menu">
                        <div class="left">
                            <span>Round</span>
                            <div class="count">
                              402
                            </div>
                            <p>Drown 28 mar 2022y. 17:00</p>
                        </div>
                        <div class="right">
                          <div class="left">
                            <img src="images/left.png" alt="">
                          </div>
                          <div class="right">
                            <img src="images/right2.png" alt="">
                          </div>
                          <div class="all_right">
                            <img src="images/right-all.png" alt="">
                          </div>
                        </div>
                    </div>
                    <div class="content">
                        <div class="bg-rounds"></div>
                          <div class="price">
                                <div class="prices">
                                  <span>Prize Pot</span>
                                  <p>$25 766</p>
                                </div>
                                <div class="stat">
                                  <span>32 640.46 BSW</span>
                                  <p>Total tickets this round: 2 985</p>
                                </div>
                                <div class="ticket">
                                  <span>Your tickets</span>
                                  <p>You had 0 tickets this round</p>
                                </div>
                          </div>
                          <div class="winning">
                              <span>Winning number</span>
                              <div class="wrap">
                                <img src="images/num4.png" alt="">
                                <img src="images/num3.png" alt="">
                                <img src="images/num3.png" alt="">
                                <img src="images/num4.png" alt="">
                                <img src="images/num9.png" alt="">
                                <img src="images/num8.png" alt="">
                              </div>
                          </div>
                     </div>
                </div>
            </div>
            <div class="lottery_competition">
                <div class="bg_lottery_competition"></div>
                <div class="row">
                    <div class="column">
                      <h2>Lottery Competition</h2>
                      <h3>Buy lottery tickets and take part in the <br>contest with exclusive prizes.</h3>
                    </div>
                  <div class="column">
                     <span>Lottery Competition</span>
                    <p>$22</p>
                  </div>
                </div>
                <div class="row bottom">
                    <div class="ends">
                        <div class="in">Ends in</div>
                        <div class="time">6D:20:18:16</div>
                    </div>
                    <div class="rewards">
                        <div class="img">
                          <img src="/images/rewards.png" alt="">
                        </div>
                        <div class="count">
                            <div class="row">
                              <span>Your reward</span>

                              <Helper typeImg="1" nameImg="reward-info.png" />
                            </div>
                            <h4>$0</h4>
                        </div>
                    </div>
                    <div class="ranking">
                      <div class="img">
                        <img src="/images/ranking.png" alt="">
                      </div>
                      <div class="count">
                        <div class="row">
                          <span>Your ranking</span>
                          <Helper typeImg="1" nameImg="reward-info.png" />
                        </div>
                        <h4>0</h4>
                      </div>
                    </div>

                    <div class="btn">
                      More Details
                    </div>
                </div>
            </div>
            <div class="invite_friends">
              <div class="img">
                <img src="/images/invite-friends.png" alt="">
              </div>
              <div class="column">
                <h2>Invite your friends <br> Earn cryptocurrency together</h2>
                <h3>Get 2% from your friends’ total ticket lottery purchase amount immediately <br>   to your referral balance.</h3>
                <a href="">
                <div class="btn">
                  Go to Referral
                </div>
                </a>
              </div>
            </div>
            <div class="how_to">
            <h2>How To Play</h2>
            <h3>If the digits on your tickets match the winning numbers in the correct order, you win a portion of the prize pool. Simple!</h3>
            <div class="wrap">
              <div class="item">
                <div class="count count1">
                  1
                </div>
                <img src="/images/how-to-4.png" alt="">
                <h4>Buy Tickets</h4>
                <span>
                  Prices are set when the round starts, <br>equal to $1 in BSW per ticket.
                </span>
              </div>
              <div class="item">
                <div class="count count2">
                  2
                </div>
                <img src="/images/how-to-5.png" alt="">
                <h4>Waith for the draw</h4>
                <span>
                  There are two draws every day: <br>one every 12 hours.
                </span>
              </div>
              <div class="item">
                <div class="count count3">
                  3
                </div>
                <img src="/images/how-to-6.png" alt="">
                <h4>Check for prizes</h4>
                <span>Once the round’s over, come back to <br>the page and check the results</span>
              </div>

            </div>
          </div>
            <div class="winning_criteria">
                <div class="column">
                    <h2>Winning Criteria</h2>
                     <h3>The digits on your ticket must match in the correct order to win.</h3>
                  <h4>Here’s an example of a lottery draw, with two tickets,  A and B</h4>
                    <span class="list">Ticket A: The first 3 digits and the last 2 digits match, but the 4th digit is wrong, <br>so this ticket only wins a Match first 3 prize.</span>
                    <span class="list" >
                      Ticket B: Even though the last 5 digits match, the first digit is wrong, so this ticket <br>doesn’t win a prize
                    </span>
                    <span>
                      Prize brackets don’t stack: If you match the first 3 digits in order, you’ll only win prizes from the “Match 3” bracket, and not from “Match 1” and “Match 2”.
                    </span>
                </div>
              <img src="/images/winning-criteria.png" alt="">
            </div>
            <div class="price_funds">
              <img src="/images/price-funds.png" alt="">
              <div class="column">
                <h2>Prize Funds</h2>
                <span>
                  The prizes for each lottery round come from two sources:
                </span>
                <h3>Ticket Purchases</h3>
                  <span>
                    80% of the BSW paid by people buying tickets that round goes back into the prize <br>pools.
                  </span>
                <h3>Rollover Prizes</h3>
                <span>After every round, if nobody wins in one of the prize brackets, the unclaimed BSW <br> tokens for that bracket, will roll over into the next round and will be redistribued <br>among the prize pools.</span>
              </div>
          </div>
            <div class="still_question">
            <div class="img">
              <img src="/images/still-question.png" alt="">
            </div>
            <div class="column">
              <h2>Still got questions?</h2>
              <h3>
                In case you’ve got any questions about the lottery, we invite you to go over our <br>detailed explanation in the docs section.
              </h3>
              <a href="">
              <div class="btn">
                More details
              </div>
              </a>
            </div>
          </div>
        </div>
      </div>
  </div>
</template>

<script>
import SvgImport from '~/components/layout/SvgImport'
import Exchange from '~/components/Exchange'
import Helper from '~/components/Helper';
export default {
  data() {
    return{
      dravActive:false,
      typeActive:'all',
      deadline: 'Oct 5, 2023 20:45:00',
      days: 'HI',
      hours: 'TH',
      minutes: 'ER',
      seconds: 'E!',
      expired: false
    };
  },
  computed: {
    theTime() {
      var ctx = this;

// Цикл обратного отсчета
      var x = setInterval(function () {

//Разница между двумя датами
        var countDownDate = new Date(ctx.deadline).getTime(),
          now = new Date().getTime(),
          diff = countDownDate - now,

// Преобразование времени в дни, часы, минуты и секунды
          tdays = Math.floor(diff / (1000 * 60 * 60 * 24)),
          thours = Math.floor((diff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60)),
          tminutes = Math.floor((diff % (1000 * 60 * 60)) / (1000 * 60)),
          tseconds = Math.floor((diff % (1000 * 60)) / 1000);

// Отображать две цифры
        ctx.days = (tdays < 10) ? '0' + tdays : tdays;
        ctx.hours = (thours < 10) ? '0' + thours : thours;
        ctx.minutes = (tminutes < 10) ? '0' + tminutes : tminutes;
        ctx.seconds = (tseconds < 10) ? '0' + tseconds : tseconds;

// Проверка истечения времени
        if (diff < 0) {
          clearInterval(x);
          ctx.expired = true;
        }
      }, 1000);

// Возвращение данных

      return {
        days: ctx.days,
        hours: ctx.hours,
        minutes: ctx.minutes,
        seconds: ctx.seconds
      };
    }
  },
  mounted() {
    this.$nuxt.$emit('active-page', 8);
  },
  methods: {
    showModalWallet(){
      this.$nuxt.$emit('showModalConnectWallet');
    }
  },
  components:{
    SvgImport,
    Exchange,
    Helper,
  }
}
</script>
