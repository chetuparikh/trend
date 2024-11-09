
<html lang="en"><head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
  
  <title>CodePen - Clever Signal</title>
  <link rel="stylesheet" href="./CodePen - Clever Signal_files/style.css">

<style><br>          @import url('https://fonts.googleapis.com/css2?family=Outfit:wght@100;200;300;400&display=swap');<br>  <br>          #whatsapp-chat-widget{<br>              display: block<br>          }<br>          .wa-chat-box-content-send-btn-text{<br>              font-family: 'Outfit', sans-serif !important;<br>              font-weight: 500;<br>              font-size: 16px;<br>              line-height: 20px;<br>              color: #FFFFFF !important;<br>          }<br>          .wa-chat-box-content-send-btn{<br>              background-color: #1D1D1B !important;<br>              box-shadow: 4px 4px 0px #00e785;<br>              border-radius: 8px;<br>              text-decoration: none;<br>              cursor: pointer;<br>              position: relative;<br>              display: flex;<br>              align-items: center;<br>              gap: 14px;<br>              padding: 16px 20px;<br><br>              border-width: initial;<br>              border-style: none;<br>              border-color: initial;<br>              border-image: initial;<br>              overflow: hidden;<br>              opacity: 1 !important;<br>          }<br>          .wa-chat-box-content-chat-welcome{        <br>              font-family: 'Outfit', sans-serif !important;<br>              font-size: 20px;<br>              line-height: 150%;<br>              color: #000000;<br>          }<br>          .wa-chat-box-brand{<br>              width: 52px;<br>              height: 52px;<br>              border: 1px solid #363636;<br>              box-shadow: 0px 2px 240px rgba(0, 0, 0, 0.04);<br>              border-radius: 100px;<br>              background-color: #00e785;<br>          }<br>          .wa-chat-box{<br>              background-color: white;<br>              z-index: 16000160 !important;<br>              margin-bottom: 106px;<br>              margin-bottom: 92px;<br>              min-width: 320px;<br>              position: fixed !important;<br>              bottom: 20px !important;<br>              right : 20px;<br>              border-radius: 32px;<br>              border: 2px solid #363636;<br>              box-shadow: 4px 6px 0px #00e785;<br>              padding: 32px 32px 16px;<br>              min-height: 279px;<br>              display: flex;<br>              flex-direction: column;<br>              justify-content: space-between;<br>              gap: 12px;<br><br>              pointer-events: none;<br>              opacity: 0;<br>              scale: 0;<br>              transform-origin: right bottom;<br>              <br>          }<br>          .wa-chat-box-visible{<br>              pointer-events: auto;<br>              opacity: 1;<br>              scale: 1;<br>          }<br>          .wa-chat-box-transition {<br>              transition: scale 150ms ease-in, opacity 250ms ease-in;<br>          }<br>          .wa-widget-send-button {<br>              margin: 0 0 20px 0 !important;      <br>              position: fixed !important;<br>              z-index: 16000160 !important;<br>              bottom: 0 !important;<br>              text-align: center !important;<br>              height: 52px;<br>              min-width: 52px;<br>              border: 0 solid #363636;<br>              border-radius: 100px;<br>              visibility: visible;<br>              transition: none !important;<br>              background-color: #00e785;<br>              box-shadow: 4px 5px 10px rgba(0, 0, 0, 0.4);<br>              right : 20px;<br>              cursor: pointer;<br>              display: flex;<br>              align-items: center;<br>              justify-content: center;<br>          }<br>          .wa-widget-send-button-clicked {<br>            border: 1px solid #363636;<br>          }<br>          .wa-chat-box-poweredby{<br>              margin-left: auto;<br>              margin-right: auto;<br>              display: flex;<br>              justify-content: center;<br>              align-items: center;<br>              gap: 3px;<br>              font-family: 'Outfit', sans-serif !important;<br>              font-size: 12px;<br>              line-height: 18px;<br>              color: #999999;<br>          }<br>          .wa-chat-box-poweredby-link{<br>              font-weight: 600;<br>              color: #666666 !important;<br>              text-decoration: none !important;<br>          }<br>          .wa-chat-box-poweredby-link::hover{<br>              color: #666666 !important;<br>              text-decoration: none !important;<br>          }<br>  <br>          .wa-chat-bubble{<br>              display: flex;<br>              align-items: center;<br>              gap: 8px;<br>              z-index: 16000160 !important;<br>              position: fixed !important;<br>              margin-bottom: 63px;<br>              bottom: 20px !important;<br>              right : 20px;<br>          }<br>          .wa-chat-bubble-closed{<br>            display: none;<br>          }<br>          .wa-chat-bubble-close-button{<br>              height: 20px;<br>              min-width: 20px;<br>              background: #000000;<br>              border-radius: 24px;<br>              cursor: pointer;<br>              display: flex;<br>              align-items: center;<br>              justify-content: center;<br>              order: 1;<br>          }<br>          .wa-chat-bubble-text{<br>             font-family: 'Outfit', sans-serif !important;<br>             background: #FFFFFF;<br>             border: 1px solid #363636;<br>             box-shadow: 2px 3px 0px #00e785;<br>             border-radius: 24px;<br>             padding: 8px 16px;<br>  <br>             font-weight: 500;<br>             font-size: 14px;<br>             line-height: 150%;<br>             color: #202020;<br>             cursor: pointer;<br>          }<br>          .wa-chat-box::before {<br>             content: '';<br>             position: absolute;<br>             top: 100%;<br>             right: 29px;<br>             width: 0;<br>             height: 0;<br>             border-width: 0 0px 30px 30px;<br>             border-color: transparent transparent white transparent;<br>             border-style: solid;<br>             transform: rotate(270deg);<br>             z-index: 1;<br>          }<br>          .wa-chat-box::after {<br>             content: '';<br>             position: absolute;<br>             top: 100%;<br>             right: 27px;<br>             width: 0;<br>             height: 0;<br>             border-width: 0px 0px 34px 34px;<br>             border-color: transparent transparent black transparent;<br>             border-style: solid;<br>             border-radius: 2px;<br>             filter: drop-shadow(-2px 5px 0px #00e785);<br>             transform: rotate(270deg);<br>          }<br>  <br>          @media only screen and (max-width: 600px) {<br>              .wa-chat-box<br>              {<br>                  box-sizing: border-box;<br>                  min-width: 0%;<br>                  position: fixed !important;<br>                  right: 20px!important;<br>                  left: 20px!important;<br>              }<br>          }<br>      </style><script src="./CodePen - Clever Signal_files/color.js.download"></script><style id="svelte-ohbfj8-style">.razorpay-payment-button.svelte-ohbfj8,.razorpay-payment-button.svelte-ohbfj8 *,.razorpay-payment-button.svelte-ohbfj8 *::before,.razorpay-payment-button.svelte-ohbfj8 *::after{box-sizing:border-box}.razorpay-payment-button.svelte-ohbfj8{position:relative;display:inline-block;-webkit-font-smoothing:antialiased;-moz-osx-font-smoothing:grayscale}</style><style id="svelte-7tbrl8-style">.razorpay-payment-form-container.svelte-7tbrl8{z-index:1000000000;position:fixed;top:0;display:block;left:0;height:100%;width:100%;backface-visibility:hidden;overflow-y:visible}.razorpay-payment-form-frame.svelte-7tbrl8{opacity:1;min-height:100% !important;position:fixed;top:0;background:none;display:block;border:0 none transparent;margin:0;padding:0;z-index:2;width:100% !important}.razorpay-backdrop.svelte-7tbrl8{min-height:100%;transition:all .3s ease-out 0s;position:fixed;top:0;left:0;width:100%;height:100%;background:rgba(0,0,0,0.6);opacity:0}.test-mode-badge.svelte-7tbrl8{text-decoration:none;background:#d64444;border:1px dashed #fff;padding:3px;opacity:0;transform:rotate(45deg);transition:opacity .3s ease-in 0s;font-family:lato,ubuntu,helvetica,sans-serif;color:#fff;position:absolute;width:200px;text-align:center;right:-50px;top:50px}</style><style id="svelte-q4m8xw-style">.razorpay-loader.svelte-q4m8xw{position:relative;height:50px;width:50px;border-radius:50%;top:30%;margin:0 auto;border:1px solid rgba(255,255,255,0.2);border-top-color:rgba(255,255,255,0.7);animation:svelte-q4m8xw-rzp-rot 1s infinite linear;transition:.2s;opacity:0}@-moz-keyframes svelte-q4m8xw-rzp-rot{100%{transform:rotate(360deg)}}@-webkit-keyframes svelte-q4m8xw-rzp-rot{100%{transform:rotate(360deg)}}@-o-keyframes svelte-q4m8xw-rzp-rot{100%{transform:rotate(360deg)}}@keyframes svelte-q4m8xw-rzp-rot{100%{transform:rotate(360deg)}}</style><script src="./CodePen - Clever Signal_files/bundle.min.js.download"></script><script src="./CodePen - Clever Signal_files/bundle.js.download"></script><style id="svelte-ekc7fv-style">@import url("https://fonts.googleapis.com/css2?family=Muli:wght@700;800&display=swap");.PaymentButton.svelte-ekc7fv.svelte-ekc7fv{position:relative;display:inline-block;min-width:160px;height:40px;padding:0;border-radius:3px;text-align:center;font-style:italic;font-family:Muli,helvetica,sans-serif;font-display:swap;overflow:hidden;border:1px solid transparent;outline:none;cursor:pointer;-webkit-tap-highlight-color:transparent;text-decoration:none}.PaymentButton--customSecuredByLogo.svelte-ekc7fv.svelte-ekc7fv{height:48px}.PaymentButton--light.svelte-ekc7fv.svelte-ekc7fv{color:#072654}.PaymentButton--dark.svelte-ekc7fv.svelte-ekc7fv{color:#fff}.PaymentButton--rzpTheme.svelte-ekc7fv.svelte-ekc7fv::before{content:'';position:absolute;left:-6px;top:0;width:46px;height:100%;background:#1e40a0;border-radius:2px 0 0 2px;transform:skew(-15deg,0)}.PaymentButton--rzp-dark-standard.svelte-ekc7fv.svelte-ekc7fv{background:#072654;border-color:#072654}.PaymentButton--rzp-outline-standard.svelte-ekc7fv.svelte-ekc7fv{background:#eaf2fe;border-color:#1e40a0}.PaymentButton--rzp-outline-standard.svelte-ekc7fv.svelte-ekc7fv::before{box-shadow:2px 0 4px rgba(0,0,0,0.15)}.PaymentButton--rzp-light-standard.svelte-ekc7fv.svelte-ekc7fv{background:#fff;border-color:#fff}.PaymentButton--rzp-light-standard.svelte-ekc7fv.svelte-ekc7fv::before{box-shadow:2px 0 4px rgba(0,0,0,0.15)}svg.svelte-ekc7fv.svelte-ekc7fv{position:absolute;top:0;left:0;margin:9px 11px}svg.svelte-ekc7fv svg path.svelte-ekc7fv{fill:#fff}.PaymentButton--rzpTheme.svelte-ekc7fv svg path.svelte-ekc7fv{fill:#fff}.PaymentButton--light.svelte-ekc7fv:not(.PaymentButton--rzpTheme) svg path.svelte-ekc7fv{fill:#072654}.PaymentButton.svelte-ekc7fv.svelte-ekc7fv:not(.PaymentButton--rzpTheme):not(.PaymentButton--noRzpLogo)::before{content:'';position:absolute;bottom:0;left:0;top:0;right:0;background:linear-gradient(121deg,rgba(255,255,255,0) 40%,rgba(255,255,255,0.2) 100%)}.PaymentButton-contents.svelte-ekc7fv.svelte-ekc7fv{padding:4px 28px 4px 44px;margin:1px 0}.PaymentButton--noRzpLogo.svelte-ekc7fv .PaymentButton-contents.svelte-ekc7fv{padding-left:28px !important}.PaymentButton--rzpTheme.svelte-ekc7fv .PaymentButton-contents.svelte-ekc7fv{padding-left:60px}.PaymentButton-text.svelte-ekc7fv.svelte-ekc7fv{display:block;min-height:18px;line-height:18px;font-size:14px;font-weight:800;opacity:1;text-transform:initial}.PaymentButton-securedBy.svelte-ekc7fv.svelte-ekc7fv{font-size:8px;line-height:10px;text-transform:initial;margin-top:0;opacity:.6}.PaymentButton--customSecuredByLogo.svelte-ekc7fv .PaymentButton-securedBy.svelte-ekc7fv{opacity:1;margin-top:1px}.secured-by-logo.svelte-ekc7fv.svelte-ekc7fv{vertical-align:middle}</style></head>
<body>
<!-- partial:index.partial.html -->



  
  <title>CodePen - Clever Signal</title>
  <link rel="stylesheet" href="./CodePen - Clever Signal_files/style.css">



<!-- partial:index.partial.html -->



  
  <title>CodePen - Clever Signal</title>
  <link rel="stylesheet" href="./CodePen - Clever Signal_files/style.css">



<!-- partial:index.partial.html -->



  
  <title>CodePen - Clever Signal</title>
  <link rel="stylesheet" href="./CodePen - Clever Signal_files/style.css">



<!-- partial:index.partial.html -->



  
  <title>CodePen - Clever Signal</title>
  <link rel="stylesheet" href="./CodePen - Clever Signal_files/style.css">



<!-- partial:index.partial.html -->



  
  <title>CodePen - Clever Signal</title>
  <link rel="stylesheet" href="./CodePen - Clever Signal_files/style.css">



<!-- partial:index.partial.html -->



    
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Live Options Signal</title>
    <link rel="stylesheet" href="./CodePen - Clever Signal_files/styles.css">
    <link rel="stylesheet" href="./CodePen - Clever Signal_files/all.min.css">


      <!-- Meta Pixel Code -->
    <script type="text/javascript" async="" src="./CodePen - Clever Signal_files/watiWidget.js.download"></script><script async="" src="./CodePen - Clever Signal_files/fbevents.js.download"></script><script>
    !function(f,b,e,v,n,t,s)
    {if(f.fbq)return;n=f.fbq=function(){n.callMethod?
    n.callMethod.apply(n,arguments):n.queue.push(arguments)};
    if(!f._fbq)f._fbq=n;n.push=n;n.loaded=!0;n.version='2.0';
    n.queue=[];t=b.createElement(e);t.async=!0;
    t.src=v;s=b.getElementsByTagName(e)[0];
    s.parentNode.insertBefore(t,s)}(window, document,'script',
    'https://connect.facebook.net/en_US/fbevents.js');
    fbq('init', '756352619988724');
    fbq('track', 'PageView');
    </script>
    <noscript><img height="1" width="1" style="display:none"
    src="https://www.facebook.com/tr?id=756352619988724&ev=PageView&noscript=1"
    /></noscript>
    <!-- End Meta Pixel Code -->
    <header class="header">
        <div class="container">
            <h1><i class="fas fa-signal"></i> Clever Exam - Clever Signal</h1>
            <h2>Live Option Signal <i class="fas fa-chart-line"></i></h2>
            <p>Real-time market data with advanced Algo indicator <i class="fas fa-sync-alt"></i></p>
        </div>
    </header>
    <div class="toolbar" id="offer-section">
        <div class="container">
            <span class="offer-text"><i class="fas fa-gift"></i> Unlock exclusive features with our premium offer for just 100 rupees! <i class="fas fa-arrow-right"></i> Lifetime validity!</span>
            <button id="get-offer-btn"><i class="fas fa-tag"></i> Get Offer</button>
        </div>
    </div>
    <nav class="nav">
        <div class="container">
            <button id="nifty-btn" class="active"><i class="fas fa-chart-bar"></i> NIFTY 50</button>
            <button id="banknifty-btn"><i class="fas fa-chart-bar"></i> BANKNIFTY</button>
            <button id="finifty-btn"><i class="fas fa-chart-bar"></i> FINNIFTY</button>
            <button id="midcapnifty-btn"><i class="fas fa-chart-bar"></i> MIDCAP NIFTY</button>
            <button id="stock-btn"><i class="fas fa-chart-bar"></i> STOCK</button>
        </div>
    </nav>
    <main class="main">
        <div class="container">
            <section class="access-code-section">
                <input type="text" id="access-code" placeholder="Enter Access Code">
                <button id="access-code-submit"><i class="fas fa-sign-in-alt"></i> Login</button>
                <p id="access-code-error" style="color: red; display: none;"><i class="fas fa-exclamation-circle"></i> Invalid Access Code</p>
            </section>
            <section class="headline-section">
                <h2 id="current-data-title">Viewing NIFTY 50 Data <i class="fas fa-chart-bar"></i></h2>
            </section>
            <section class="data-table">
                <div id="loading" class="loading" style="display: none;">
                    <div class="spinner"></div>
                    <p><i class="fas fa-spinner fa-spin"></i> Loading data, please wait...</p>
                </div>
                <div id="table-container" style="display: block;">Error fetching data.</div>
                <div id="pagination">
                    <button id="prev-btn" disabled=""><i class="fas fa-chevron-left"></i> Previous</button>
                    <span id="page-info">Page 1 of 4</span>
                    <button id="next-btn">Next <i class="fas fa-chevron-right"></i></button>
                                 </div>
            </section>
            <section class="video-section">
                <h2>Watch the Tutorial <i class="fas fa-video"></i></h2>
                <div class="video-container">
                    <iframe width="560" height="315" src="./CodePen - Clever Signal_files/3qM-qtBTQ-c.html" title="YouTube video player" frameborder="0" allowfullscreen=""></iframe>
                </div>
            </section>
                </div>
            
            <section class="pcr-indicator">
                <h2>Algo Indicator <i class="fas fa-chart-pie"></i></h2>
                <div class="pcr-content">
                    <div class="pcr-description">
                        <p>Our advanced Algo Indicator provides exact buy and sell signals to help you enter the market at the right time. Here’s why it stands out:</p>
                        <ul>
                            <li><i class="fas fa-check-circle"></i> Generates Real Time signals</li>
                            <li><i class="fas fa-check-circle"></i> High accuracy rate of 90%</li>
                            <li><i class="fas fa-check-circle"></i> Easy to use interface</li>
                            <li><i class="fas fa-check-circle"></i> Comprehensive coverage</li>
                            <li><i class="fas fa-check-circle"></i> Affordable one-time payment</li>
                        </ul>
                        <button class="get-indicator-btn"><i class="fas fa-tag"></i> Get Indicator</button>
                    </div>
                    <div class="pcr-image">
                        <img src="./CodePen - Clever Signal_files/Untitled-design.png" alt="Algo Indicator">
                    </div>
                </div>
            </section>
            <section class="features">
                <h2>Features <i class="fas fa-star"></i></h2>
                <p>The Put-Call Ratio (PCR) is a popular indicator used by traders to gauge the market sentiment. With our real-time PCR Signal, you get:</p>
                <div class="feature-list">
                    <div class="feature-item">
                        <i class="fas fa-clock feature-icon"></i>
                        <div class="feature-content">
                            <h3>Real-time Data Updates <i class="fas fa-sync"></i></h3>
                            <p>Stay ahead with the latest market movements.</p>
                        </div>
                    </div>
                    <div class="feature-item">
                        <i class="fas fa-chart-line feature-icon"></i>
                        <div class="feature-content">
                            <h3>Algo Indicator <i class="fas fa-bullseye"></i></h3>
                            <p>Know the best times to enter the market with our highly accurate tool.</p>
                        </div>
                    </div>
                    <div class="feature-item">
                        <i class="fas fa-bullseye feature-icon"></i>
                        <div class="feature-content">
                            <h3>High Accuracy <i class="fas fa-check"></i></h3>
                            <p>Our PCR indicator tool boasts an accuracy of 90%, ensuring you make informed decisions.</p>
                        </div>
                    </div>
                    <div class="feature-item">
                        <i class="fas fa-tags feature-icon"></i>
                        <div class="feature-content">
                            <h3>Affordable Pricing <i class="fas fa-rupee-sign"></i></h3>
                            <p>Get lifetime access for just 100 rupees with a one-time payment.</p>
                        </div>
                    </div>
                    <div class="feature-item">
                        <i class="fas fa-user-friends feature-icon"></i>
                        <div class="feature-content">
                            <h3>User-friendly Interface <i class="fas fa-users"></i></h3>
                            <p>Our platform is easy to navigate, making it accessible for both beginners and experienced traders.</p>
                        </div>
                    </div>
                    <div class="feature-item">
                        <i class="fas fa-globe feature-icon"></i>
                        <div class="feature-content">
                            <h3>Comprehensive Market Coverage <i class="fas fa-globe"></i></h3>
                            <p>Access data for NIFTY 50, BANKNIFTY, FINIFTY, and MIDCAP NIFTY all in one place.</p>
                        </div>
                    </div>
                    <div class="feature-item">
                        <i class="fas fa-headset feature-icon"></i>
                        <div class="feature-content">
                            <h3>Expert Support <i class="fas fa-life-ring"></i></h3>
                            <p>Receive 24/7 support from our team.</p>
                        </div>
                    </div>
                </div>
            </section>
            <section class="testimonials">
                <h2>Testimonials <i class="fas fa-comments"></i></h2>
                <div class="testimonial">
                    <div class="testimonial-content">
                        <i class="fas fa-quote-left"></i>
                        <p>The Algo Indicator tool has significantly improved my trading strategy. Highly recommend!</p>
                        <i class="fas fa-quote-right"></i>
                    </div>
                    <div class="testimonial-author">
                        <p>Ravi Kumar</p>
                    </div>
                </div>
                <div class="testimonial">
                    <div class="testimonial-content">
                        <i class="fas fa-quote-left"></i>
                        <p>Accurate signals and real-time data updates have been a game-changer for my trading.</p>
                        <i class="fas fa-quote-right"></i>
                    </div>
                    <div class="testimonial-author">
                        <p>Anjali Sharma</p>
                    </div>
                </div>
                <div class="testimonial">
                    <div class="testimonial-content">
                        <i class="fas fa-quote-left"></i>
                        <p>Easy to use and very effective. Great value for the price!</p>
                        <i class="fas fa-quote-right"></i>
                    </div>
                    <div class="testimonial-author">
                        <p>Amit Patel</p>
                    </div>
                </div>
            </section>
        
    </main>
    <footer class="footer">
        <div class="container">
            <p>© 2024 Clever Exam - Clever Signal. All rights reserved.</p>
        </div>
    </footer>


  
