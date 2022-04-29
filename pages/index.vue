<template>
  <div>
  <div class="main_section">
      <div class="main-bg pc-mob"></div>
      <div class="container">
          <div class="d-flex main_block">
            <div class="wrap main_block1">
              <div class="main_block_row">
                <h1>The First DEX on BNB Chain with <br> a three-type referral system</h1>
                <span>Enjoy profitable yield farming and exchanging with the lowest fees <br>  in DeFi space!</span>
              </div>
              <a class="a-gr" href="">
               <div class="btn-green">
                  <SvgImport name="vuesax/bold/dollar-circle"/>
                  <span>Trade Now</span>
              </div>
              </a>
              <div class="main_section_plus">
                  <div class="main_section_plus_item">
                    <SvgImport name="discount-shape"/>
                    <div class="row">
                      <span>The Lowest Trade Fee in <br>the DeFi Space</span>
                      <p>0.1%</p>
                    </div>
                  </div>
                <div class="main_section_plus_item main_section_plus_item--style-red">
                  <SvgImport name="empty-wallet-change"/>
                  <div class="row">
                    <span>Exchange Fee <br>Reimbursement</span>
                    <p>up to 90%</p>
                  </div>
                </div>
              </div>
            </div>
            <div class="wrap main_block2">
                <div class="trading_values">
                      <div class="d-flex">
                          <div class="item">
                            <SvgImport name="binance"/>
                            <div class="wrap">
                                <span>Total value locked</span>
                                <p>$574 721 205</p>
                            </div>
                          </div>
                        <div class="item">
                          <div class="wrap">
                            <span>Total trading Volume</span>
                            <p>$38 179 465 697</p>
                          </div>
                        </div>
                      </div>
                </div>
            </div>
          </div>
          <div class="currency_lists">
            <div class="currency_item">
                <img src="/images/coins/fil.svg" alt="">
                <div class="wrap">
                      <div class="currency_name">
                          Fil
                          <span class="green">+3.43</span>
                      </div>
                      <div class="currency_price">
                        $19.05
                      </div>
                </div>
              </div>
            <div class="currency_item">
              <img src="/images/coins/btcb.svg" alt="">
              <div class="wrap">
                <div class="currency_name">
                  BTCB
                  <span class="red">-1.99%</span>
                </div>
                <div class="currency_price">
                  $42.044.63
                </div>
              </div>
            </div>
            <div class="currency_item">
              <img src="/images/coins/ada.svg" alt="">
              <div class="wrap">
                <div class="currency_name">
                  ADA
                  <span class="red">+6.66%</span>
                </div>
                <div class="currency_price">
                  $1.04
                </div>
              </div>
            </div>
            <div class="currency_item">
              <img src="/images/coins/doge.svg" alt="">
              <div class="wrap">
                <div class="currency_name">
                  DOGE
                  <span class="red">-1.19%</span>
                </div>
                <div class="currency_price">
                  $0.12
                </div>
              </div>
            </div>
            <div class="currency_item">
              <img src="/images/coins/trx.svg" alt="">
              <div class="wrap">
                <div class="currency_name">
                  TRX
                  <span class="red">+3.56%</span>
                </div>
                <div class="currency_price">
                  $0.06
                </div>
              </div>
            </div>
            <div class="currency_all pc-mob">
              <a href="">
                <span>All Markets</span>
                <img src="/images/right.png" alt="">
              </a>
            </div>
          </div>
      </div>
  </div>
  <div class="container">
    <div class="slider_lets-go pc-mob ">
        <div class="slider_wrap">
          <carousel v-if="!loading" :perPage="3" :paginationPadding="paggPadding" :navigationEnabled="true">
            <slide>
              <div class="slider_item si1">
                <div class="wrap">
                  <p>Use CyberDex <br> on mobile phone</p>
                  <span>Search for nft right in <br> your phone</span>
                  <a href="">
                    <div class="btn-lets-go">
                      Let’s go!
                    </div>
                  </a>
                </div>
                <img class="slider_img" src="/images/nft_1.png" alt="">
              </div>
            </slide>
            <slide>
              <div class="slider_item si2">
                <div class="wrap">
                  <p>NFT prizes for new <br> users</p>
                  <span>Discover new NFTs at <br>the CyberDex project</span>
                  <a href="">
                    <div class="btn-lets-go">
                      Let’s go!
                    </div>
                  </a>
                </div>
                <img class="slider_img" src="/images/nft_2.png" alt="">
              </div>
            </slide>
            <slide>
              <div class="slider_item si3">
                <div class="wrap">
                  <p>Buy NFT and enter the <br>top buyers</p>
                  <span>Our platform is designed for <br>this condition</span>
                  <a href="">
                    <div class="btn-lets-go">
                      Let’s go!
                    </div>
                  </a>
                </div>
              </div>
            </slide>
            <slide>
              <div class="slider_item si1">
                <div class="wrap">
                  <p>Use CyberDex <br> on mobile phone</p>
                  <span>Search for nft right in <br> your phone</span>
                  <a href="">
                    <div class="btn-lets-go">
                      Let’s go!
                    </div>
                  </a>
                </div>
                <img class="slider_img" src="/images/nft_1.png" alt="">
              </div>
            </slide>
            <slide>
              <div class="slider_item si2">
                <div class="wrap">
                  <p>NFT prizes for new <br> users</p>
                  <span>Discover new NFTs at <br>the CyberDex project</span>
                  <a href="">
                    <div class="btn-lets-go">
                      Let’s go!
                    </div>
                  </a>
                </div>
                <img class="slider_img" src="/images/nft_2.png" alt="">
              </div>
            </slide>
            <slide>
              <div class="slider_item si3">
                <div class="wrap">
                  <p>Buy NFT and enter the <br>top buyers</p>
                  <span>Our platform is designed for <br>this condition</span>
                  <a href="">
                    <div class="btn-lets-go">
                      Let’s go!
                    </div>
                  </a>
                </div>
              </div>
            </slide>
          </carousel>
        </div>
    </div>
    <div class="slider_lets-go mob">
      <div class="slider_wrap">
        <carousel v-if="!loading" :perPage="1" :paginationPadding="paggPadding" :navigationEnabled="true">
          <slide>
            <div class="slider_item si1">
              <div class="wrap">
                <p>Use CyberDex <br> on mobile phone</p>
                <span>Search for nft right in <br> your phone</span>
                <a href="">
                  <div class="btn-lets-go">
                    Let’s go!
                  </div>
                </a>
              </div>
              <img class="slider_img" src="/images/nft_1.png" alt="">
            </div>
          </slide>
          <slide>
            <div class="slider_item si2">
              <div class="wrap">
                <p>NFT prizes for new <br> users</p>
                <span>Discover new NFTs at <br>the CyberDex project</span>
                <a href="">
                  <div class="btn-lets-go">
                    Let’s go!
                  </div>
                </a>
              </div>
              <img class="slider_img" src="/images/nft_2.png" alt="">
            </div>
          </slide>
          <slide>
            <div class="slider_item si3">
              <div class="wrap">
                <p>Buy NFT and enter the <br>top buyers</p>
                <span>Our platform is designed for <br>this condition</span>
                <a href="">
                  <div class="btn-lets-go">
                    Let’s go!
                  </div>
                </a>
              </div>
            </div>
          </slide>
          <slide>
            <div class="slider_item si1">
              <div class="wrap">
                <p>Use CyberDex <br> on mobile phone</p>
                <span>Search for nft right in <br> your phone</span>
                <a href="">
                  <div class="btn-lets-go">
                    Let’s go!
                  </div>
                </a>
              </div>
              <img class="slider_img" src="/images/nft_1.png" alt="">
            </div>
          </slide>
          <slide>
            <div class="slider_item si2">
              <div class="wrap">
                <p>NFT prizes for new <br> users</p>
                <span>Discover new NFTs at <br>the CyberDex project</span>
                <a href="">
                  <div class="btn-lets-go">
                    Let’s go!
                  </div>
                </a>
              </div>
              <img class="slider_img" src="/images/nft_2.png" alt="">
            </div>
          </slide>
          <slide>
            <div class="slider_item si3">
              <div class="wrap">
                <p>Buy NFT and enter the <br>top buyers</p>
                <span>Our platform is designed for <br>this condition</span>
                <a href="">
                  <div class="btn-lets-go">
                    Let’s go!
                  </div>
                </a>
              </div>
            </div>
          </slide>
        </carousel>
      </div>
    </div>
    <div class="earn_launchpools">
        <div class="d_flex">
            <div class="title_w">
                <span>Earn CYD + Fees in Farms</span>
              <a href="">
                <img src="/icons/arrow-right.svg" alt="">
              </a>
            </div>
            <div class="content_w">
              <div class="cyd_item">
                    <div class="cyd_item_w">
                        <div class="cyd_item_icons">
                            <img src="/images/coins/usdt.svg" alt="">
                            <img src="/images/coins/bsw.svg" alt="">
                        </div>
                        <div class="cyd_item_name">
                          USD - CYD
                        </div>
                    </div>
                  <div class="cyd_item_w">
                      <div class="row">
                         <span>APY</span>
                        <SvgImport name="computing"/>
                      </div>
                      <div class="row">
                        <span class="interest">121.30%</span>
                        <Helper typeImg="2" nameImg="icon" />
                      </div>
                  </div>
                  <div class="cyd_item_w">
                    <a href="">
                      <div class="cyd_item_btn">
                        Start Farm
                      </div>
                    </a>
                  </div>
                </div>
              <div class="cyd_item">
                <div class="cyd_item_w">
                  <div class="cyd_item_icons">
                    <img src="/images/coins/bnb.svg" alt="">
                    <img src="/images/coins/bsw.svg" alt="">
                  </div>
                  <div class="cyd_item_name">
                    BNB - BSW
                  </div>
                </div>
                <div class="cyd_item_w">
                  <div class="row">
                    <span>APY</span>
                    <SvgImport name="computing"/>
                  </div>
                  <div class="row">
                    <span class="interest">148.96%</span>
                    <Helper typeImg="2" nameImg="icon" />
                  </div>
                </div>
                <div class="cyd_item_w">
                  <a href="">
                  <div class="cyd_item_btn">
                    Start Farm
                  </div>
                  </a>
                </div>
              </div>
              <div class="cyd_item">
                <div class="cyd_item_w">
                  <div class="cyd_item_icons">
                    <img src="/images/coins/bfg.svg" alt="">
                    <img src="/images/coins/bsw.svg" alt="">
                  </div>
                  <div class="cyd_item_name">
                    BFG - BSW
                  </div>
                </div>
                <div class="cyd_item_w">
                  <div class="row">
                    <span>APY</span>
                    <SvgImport name="computing"/>
                  </div>
                  <div class="row">
                    <span class="interest">163.53%</span>
                    <Helper typeImg="2" nameImg="icon" />
                  </div>
                </div>
                <div class="cyd_item_w">
                  <a href="">
                  <div class="cyd_item_btn">
                    Start Farm
                  </div>
                  </a>
                </div>
              </div>
              <div class="cyd_item">
                <div class="cyd_item_w">
                  <div class="cyd_item_icons">
                    <img src="/images/coins/luna.svg" alt="">
                    <img src="/images/coins/busd.svg" alt="">
                  </div>
                  <div class="cyd_item_name">
                    LUNA-BUSD
                  </div>
                </div>
                <div class="cyd_item_w">
                  <div class="row">
                    <span>APY</span>
                    <SvgImport name="computing"/>
                  </div>
                  <div class="row">
                    <span class="interest">33.62%</span>
                    <Helper typeImg="2" nameImg="icon" />
                  </div>
                </div>
                <div class="cyd_item_w">
                  <a href="">
                  <div class="cyd_item_btn">
                    Start Farm
                  </div>
                  </a>
                </div>
              </div>
              <div class="cyd_item">
                <div class="cyd_item_w">
                  <div class="cyd_item_icons">
                    <img src="/images/coins/doge.svg" alt="">
                    <img src="/images/coins/bnb.svg" alt="">
                  </div>
                  <div class="cyd_item_name">
                    DOGE-BNB
                  </div>
                </div>
                <div class="cyd_item_w">
                  <div class="row">
                    <span>APY</span>
                    <SvgImport name="computing"/>
                  </div>
                  <div class="row">
                    <span class="interest">12.78%</span>
                    <Helper typeImg="2" nameImg="icon" />
                  </div>
                </div>
                <div class="cyd_item_w">
                  <a href="">
                  <div class="cyd_item_btn">
                    Start Farm
                  </div>
                  </a>
                </div>
              </div>
            </div>

        </div>
      <div class="d_flex">
        <div class="title_w">
          <span>Launchpools</span>
          <a href="">
          <img src="/icons/arrow-right.svg" alt="">
          </a>
        </div>
        <div class="content_w content_w--style-2">
          <div class="cyd_item">
            <div class="cyd_item_w">
              <div class="cyd_item_icons">
                <img src="/images/coins/bsw.svg" alt="">
                <img src="/images/coins/bsw.svg" alt="">
              </div>
              <div class="cyd_item_name_w">
                <p>Holder Pool</p>
                <span>Stake BSW - Earn BSW</span>
              </div>
            </div>
            <div class="cyd_item_w">
              <div class="row">
                <span>APY</span>
                <SvgImport name="computing"/>
              </div>
              <div class="row">
                <span class="interest">71.30%</span>
                <Helper typeImg="2" nameImg="icon" />
              </div>
            </div>
            <div class="cyd_item_w">
              <a href="">
              <div class="cyd_item_btn">
                Start Farm
              </div>
              </a>
            </div>
          </div>
          <div class="cyd_item">
            <div class="cyd_item_w">
              <div class="cyd_item_icons">
                <img src="/images/coins/bsw.svg" alt="">
                <img src="/images/coins/bsw.svg" alt="">
              </div>
              <div class="cyd_item_name_w">
                <p>Auto Compound</p>
                <span>Stake BSW - Earn BSW</span>
              </div>
            </div>
            <div class="cyd_item_w">
              <div class="row">
                <span>APY</span>
                <SvgImport name="computing"/>
              </div>
              <div class="row">
                <span class="interest">71.21%</span>
                <Helper typeImg="2" nameImg="icon" />
              </div>
            </div>
            <div class="cyd_item_w">
              <a href="">
              <div class="cyd_item_btn">
                Start Farm
              </div>
              </a>
            </div>
          </div>
          <div class="cyd_item">
            <div class="cyd_item_w">
              <div class="cyd_item_icons">
                <img src="/images/coins/bsw.svg" alt="">
                <img src="/images/coins/bsw.svg" alt="">
              </div>
              <div class="cyd_item_name_w">
                <p>Earn BSW</p>
                <span>Stake BSW</span>
              </div>
            </div>
            <div class="cyd_item_w">
              <div class="row">
                <span>APY</span>
                <SvgImport name="computing"/>
              </div>
              <div class="row">
                <span class="interest">53.77%</span>
                <Helper typeImg="2" nameImg="icon" />
              </div>
            </div>
            <div class="cyd_item_w">
              <a href="">
              <div class="cyd_item_btn">
                Start Farm
              </div>
              </a>
            </div>
          </div>
          <div class="cyd_item">
            <div class="cyd_item_w">
              <div class="cyd_item_icons">
                <img src="/images/coins/eth.svg" alt="">
                <img src="/images/coins/bsw.svg" alt="">
              </div>
              <div class="cyd_item_name_w">
                <p>Earn ETH</p>
                <span>Stake BSW</span>
              </div>
            </div>
            <div class="cyd_item_w">
              <div class="row">
                <span>APY</span>
                <SvgImport name="computing"/>
              </div>
              <div class="row">
                <span class="interest">77.93%</span>
                <Helper typeImg="2" nameImg="icon" />
              </div>
            </div>
            <div class="cyd_item_w">
              <a href="">
              <div class="cyd_item_btn">
                Start Farm
              </div>
              </a>
            </div>
          </div>
        </div>

      </div>
    </div>
    <div class="benefits">
        <div class="title">Our Benefits</div>
        <div class="slider_benefits mob">
          <div class="slider_wrap">
            <carousel v-if="!loading" :perPage="1" :paginationPadding="paggPadding" :navigationEnabled="true">
              <slide>
                <div class="slider_item">
                    <img src="/images/benefits1.svg" alt="">
                    <span>3-type Referral System</span>
                    <p>Invite your friends and earn a <br> certain commision reverd every
                      time they make a swap on Biswap <br> and 5% from their Income in Farms <br> & Launchpools.</p>
                </div>
              </slide>
              <slide>
                <div class="slider_item">
                  <img src="/images/benefits2.svg" alt="">
                  <span>The Lowest Exchange Fee</span>
                  <p>Safely buy and sell your <br> cryptocurrency with the lowest <br> exchange fee in the DeFi space</p>
                </div>
              </slide>
              <slide>
                <div class="slider_item">
                  <img src="/images/benefits3.svg" alt="">
                  <span>Trade Fee Reimbursement</span>
                  <p>Make a swap on a Biswap at no cost. <br> Up to 90% of the trading fee <br>
                    returned in BSW tokens.</p>
                </div>
              </slide>
              <slide>
                <div class="slider_item">
                  <img src="/images/benefits4.svg" alt="">
                  <span>Competitions</span>
                  <p>Participate in the regular Beswap <br>
                    trading competitions and win <br>
                    exclusive prizes.</p>
                </div>
              </slide>
            </carousel>
          </div>
        </div>
        <div class="wrap pc-mob">
            <div class="item">
              <img src="/images/benefits1.svg" alt="">
              <span>3-type Referral System</span>
              <p>Invite your friends and earn a <br> certain commision reverd every
                time they make a swap on Biswap <br> and 5% from their Income in Farms <br> & Launchpools.</p>
            </div>
          <div class="item">
            <img src="/images/benefits2.svg" alt="">
            <span>The Lowest Exchange Fee</span>
            <p>Safely buy and sell your <br> cryptocurrency with the lowest <br> exchange fee in the DeFi space</p>
          </div>
          <div class="item">
            <img src="/images/benefits3.svg" alt="">
            <span>Trade Fee Reimbursement</span>
            <p>Make a swap on a Biswap at no cost. <br> Up to 90% of the trading fee <br>
              returned in BSW tokens.</p>
          </div>
          <div class="item">
            <img src="/images/benefits4.svg" alt="">
            <span>Competitions</span>
            <p>Participate in the regular Beswap <br>
              trading competitions and win <br>
              exclusive prizes.</p>
          </div>
        </div>
    </div>

    <div class="stats">
        <div class="item">
          <img src="/images/stats1.png" alt="">
          <span>Total Volume</span>
          <p>$39.14B</p>
        </div>
      <div class="item">
        <img src="/images/stats2.png" alt="">
        <span>24H Volume</span>
        <p>$95.53B</p>
      </div>
      <div class="item">
        <img src="/images/stats3.png" alt="">
        <span>Active users</span>
        <p>414.14K</p>
      </div>
      <div class="item">
        <img src="/images/stats4.png" alt="">
        <div class="wrap">
          <span>Trade Fee Saved</span>
          <Helper typeImg="2" nameImg="icon" />
        </div>
        <p>$93.75M</p>
      </div>
      <div class="item">
        <img src="/images/stats5.png" alt="">
        <div class="wrap">
          <span>LP Earned</span>
          <Helper typeImg="2" nameImg="icon" />
        </div>
        <p>$19.71M</p>
      </div>
    </div>
  </div>

  <div class="wrap_for_bg">
      <div class="bg-green"></div>
      <div class="bg-red"></div>
      <div class="bg-star bg-star-red"></div>
      <div class="container">

          <div class="reviews">
              <div class="about">
                 <h2>Reviews From Reputable <br>Crypto Resources</h2>
                 <h3>Read more about the accomplishments of Biswap <br>on the most reputable crypto resources.</h3>
                  <div class="arrows">

                  </div>
              </div>

            <div class="slider pc-mob">
                  <div class="slider_bg"></div>
                <div class="slider_wrap">
                    <carousel v-if="!loading" :perPage="3" :paginationEnabled="false" :navigationEnabled="false">
                      <slide>
                        <div class="slider_item">
                          <img src="/images/review-slide1.svg" alt="">
                          <span>Biswap passes the 1 billion <br> transactions millestone and is listed <br>
                              amongst the top Des and BSC in a <br> more few months after its launch</span>
                          <div class="read">
                            <a href="">Read more</a>
                            <SvgImport name="arrow-right-read"/>
                          </div>
                          <div class="bg"></div>
                        </div>
                      </slide>
                      <slide>
                        <div class="slider_item">
                          <img src="/images/review-slide2.svg" alt="">
                          <span>Biswap is among the top 10 Most <br> Valuable Builders on the BSC <br>  network.</span>
                          <div class="read">
                            <a href="">Read more</a>
                            <SvgImport name="arrow-right-read"/>
                          </div>
                          <div class="bg"></div>
                        </div>
                      </slide>
                      <slide>
                        <div class="slider_item">
                          <img src="/images/review-slide3.svg" alt="">
                          <span>Biswap is among the top 10 Most <br> Valuable Builders on the BSC <br> network.</span>
                          <div class="read">
                            <a href="">Read more</a>
                            <SvgImport name="arrow-right-read"/>
                          </div>
                          <div class="bg"></div>
                        </div>
                      </slide>
                      <slide>
                        <div class="slider_item">
                          <img src="/images/review-slide1.svg" alt="">
                          <span>Biswap passes the 1 billion <br> transactions millestone and is listed <br>
                              amongst the top Des and BSC in a <br> more few months after its launch</span>
                          <div class="read">
                            <a href="">Read more</a>
                            <SvgImport name="arrow-right-read"/>
                          </div>
                          <div class="bg"></div>
                        </div>
                      </slide>
                      <slide>
                        <div class="slider_item">
                          <img src="/images/review-slide2.svg" alt="">
                          <span>Biswap is among the top 10 Most <br> Valuable Builders on the BSC <br>  network.</span>
                          <div class="read">
                            <a href="">Read more</a>
                            <SvgImport name="arrow-right-read"/>
                          </div>
                          <div class="bg"></div>
                        </div>
                      </slide>
                      <slide>
                        <div class="slider_item">
                          <img src="/images/review-slide3.svg" alt="">
                          <span>Biswap is among the top 10 Most <br> Valuable Builders on the BSC <br> network.</span>
                          <div class="read">
                            <a href="">Read more</a>
                            <SvgImport name="arrow-right-read"/>
                          </div>
                          <div class="bg"></div>
                        </div>
                      </slide>
                     </carousel>
                  </div>
              </div>
            <div class="slider mob">
              <div class="slider_bg"></div>
              <div class="slider_wrap">
                <carousel v-if="!loading" :perPage="1" :paginationEnabled="false" :navigationEnabled="false" :loop="true" :autoplay="true">
                  <slide>
                    <div class="slider_item">
                      <img src="/images/review-slide1.svg" alt="">
                      <span>Biswap passes the 1 billion <br> transactions millestone and is listed <br>
                              amongst the top Des and BSC in a <br> more few months after its launch</span>
                      <div class="read">
                        <a href="">Read more</a>
                        <SvgImport name="arrow-right-read"/>
                      </div>
                      <div class="bg"></div>
                    </div>
                  </slide>
                  <slide>
                    <div class="slider_item">
                      <img src="/images/review-slide2.svg" alt="">
                      <span>Biswap is among the top 10 Most <br> Valuable Builders on the BSC <br>  network.</span>
                      <div class="read">
                        <a href="">Read more</a>
                        <SvgImport name="arrow-right-read"/>
                      </div>
                      <div class="bg"></div>
                    </div>
                  </slide>
                  <slide>
                    <div class="slider_item">
                      <img src="/images/review-slide3.svg" alt="">
                      <span>Biswap is among the top 10 Most <br> Valuable Builders on the BSC <br> network.</span>
                      <div class="read">
                        <a href="">Read more</a>
                        <SvgImport name="arrow-right-read"/>
                      </div>
                      <div class="bg"></div>
                    </div>
                  </slide>
                  <slide>
                    <div class="slider_item">
                      <img src="/images/review-slide1.svg" alt="">
                      <span>Biswap passes the 1 billion <br> transactions millestone and is listed <br>
                              amongst the top Des and BSC in a <br> more few months after its launch</span>
                      <div class="read">
                        <a href="">Read more</a>
                        <SvgImport name="arrow-right-read"/>
                      </div>
                      <div class="bg"></div>
                    </div>
                  </slide>
                  <slide>
                    <div class="slider_item">
                      <img src="/images/review-slide2.svg" alt="">
                      <span>Biswap is among the top 10 Most <br> Valuable Builders on the BSC <br>  network.</span>
                      <div class="read">
                        <a href="">Read more</a>
                        <SvgImport name="arrow-right-read"/>
                      </div>
                      <div class="bg"></div>
                    </div>
                  </slide>
                  <slide>
                    <div class="slider_item">
                      <img src="/images/review-slide3.svg" alt="">
                      <span>Biswap is among the top 10 Most <br> Valuable Builders on the BSC <br> network.</span>
                      <div class="read">
                        <a href="">Read more</a>
                        <SvgImport name="arrow-right-read"/>
                      </div>
                      <div class="bg"></div>
                    </div>
                  </slide>
                </carousel>
              </div>
            </div>
          </div>
          <div class="w">
            <div class="investor">
                <div class="info">
                    <h2>Our Strategic Investor</h2>
                    <h3>Binance Labs, the venture capital and incubator of Binance, announced strategic investment in Biswap. The synergy from two companies working together in tandem will bring new high-quality products & services, technology enhancement, and further worldwide expansion.</h3>
                  <a href="">
                      <div class="btn">
                          <SvgImport name="flash-circle"/>
                          <span>Details</span>
                      </div>
                    </a>
                </div>
              <div class="img">
                  <img src="/images/binanceLabs.svg" alt="">
              </div>
            </div>
            <div class="bg"></div>
          </div>
          <div class="partners">
              <div class="title">
                  <h2>Biswap Partners</h2>
              </div>
              <div class="wrap">
                  <div class="item">
                    <img src="/images/partners/1.svg" alt="">
                  </div>
                <div class="item">
                  <img src="/images/partners/2.svg" alt="">
                </div>
                <div class="item">
                  <img src="/images/partners/3.svg" alt="">
                </div>
                <div class="item">
                  <img src="/images/partners/4.svg" alt="">
                </div>
                <div class="item">
                  <img src="/images/partners/5.svg" alt="">
                </div>
                <div class="item">
                  <img src="/images/partners/6.svg" alt="">
                </div>
                <div class="item gate">
                  <img src="/images/partners/7.svg" alt="">
                </div>
                <div class="item">
                  <img src="/images/partners/8.svg" alt="">
                </div>
                <div class="item">
                  <img src="/images/partners/9.svg" alt="">
                </div>
                <div class="item">
                  <img src="/images/partners/10.svg" alt="">
                </div>
                <div class="item">
                  <img src="/images/partners/11.svg" alt="">
                </div>
                <div class="item">
                  <img src="/images/partners/12.svg" alt="">
                </div>
                <div class="item">
                  <img src="/images/partners/13.svg" alt="">
                </div>
                <div class="item">
                  <img src="/images/partners/14.svg" alt="">
                </div>
                <div class="item">
                  <img src="/images/partners/15.svg" alt="">
                </div>
                <div class="item">
                  <img src="/images/partners/16.svg" alt="">
                </div>
                <div class="item">
                  <img src="/images/partners/17.svg" alt="">
                </div>
                <div class="item">
                  <img src="/images/partners/18.svg" alt="">
                </div>
                <div class="item">
                  <img src="/images/partners/19.svg" alt="">
                </div>
                <div class="item">
                  <img src="/images/partners/20.svg" alt="">
                </div>
                <div class="item">
                  <img src="/images/partners/21.svg" alt="">
                </div>
                <div class="item">
                  <img src="/images/partners/22.svg" alt="">
                </div>
                <div class="item">
                  <img src="/images/partners/23.svg" alt="">
                </div>
                <div class="item">
                  <img src="/images/partners/24.svg" alt="">
                </div>
                <div class="item">
                  <img src="/images/partners/25.svg" alt="">
                </div>
                <div class="item">
                  <img src="/images/partners/26.svg" alt="">
                </div>
                <div class="item">
                  <img src="/images/partners/27.svg" alt="">
                </div>
                <div class="item">
                  <img src="/images/partners/28.svg" alt="">
                </div>
                <div class="item">
                  <img src="/images/partners/29.svg" alt="">
                </div>
                <div class="item">
                  <img src="/images/partners/30.svg" alt="">
                </div>
                <div class="item">
                  <img src="/images/partners/31.svg" alt="">
                </div>
                <div class="item">
                  <img src="/images/partners/32.svg" alt="">
                </div>
              </div>
          </div>
      </div>



  </div>
    <SelectToken />
  </div>
</template>

<script>
import SvgImport from '~/components/layout/SvgImport';
import Helper from '~/components/Helper';
import SelectToken from '~/components/modals/SelectToken';


export default {
  data: () => ({
    loading: true,
    paggPadding: 5,
    flickityOptions: {
      initialIndex: 3,
      pageDots: true,
      wrapAround: true
    }
  }),
  mounted() {
    this.$nuxt.$emit('active-page', 1);
  },
  created() {
    this.$nextTick(function() {
      this.loading = false
    })
  },
  components:{
    SvgImport,
    Helper,
    SelectToken,
  }
}
</script>
