
<!DOCTYPE HTML>
<html class="no-js" lang="en">

<head><!-- COMMERCIAL -->
<script>
  // Constants
  const docHead = document.head;
  const environment = "Production";
  // console.log(environment);

  // GET CURRENT URL
  const currentUrl = window.location.href;
  const currentUrlPage = window
    .location
    .href
    .split("/")
    .pop();

  // Tracking scripts
  const trackingScripts = document.createElement("script");
  trackingScripts.innerHTML = `(function(w,d,s,l,i){
    w[l]=w[l]||[];
    w[l].push({'gtm.start':new Date().getTime(),event:'gtm.js'});
    const f=d.getElementsByTagName(s)[0],j=d.createElement(s),dl=l!='dataLayer'?'&l='+l:'';
    j.async=true;
    j.src='https://www.googletagmanager.com/gtm.js?id='+i+dl;
    f.parentNode.insertBefore(j,f);
  })(window,document,'script','dataLayer','GTM-55RHZZX');
  // Facebook Pixel
  !function(f,b,e,v,n,t,s){
    if(f.fbq)return;n=f.fbq=function(){n.callMethod?
    n.callMethod.apply(n,arguments):n.queue.push(arguments)};
    if(!f._fbq)f._fbq=n;n.push=n;n.loaded=!0;n.version='2.0';
    n.queue=[];t=b.createElement(e);t.async=!0;
    t.src=v;s=b.getElementsByTagName(e)[0];
    s.parentNode.insertBefore(t,s)}(window, document,'script',
    'https://connect.facebook.net/en_US/fbevents.js');
    fbq('dataProcessingOptions', ['LDU'], 0, 0);
    fbq('init', '294039261626437');
    fbq('track', 'PageView');
  `;

  // Check for privacy settings
  const gpc = document
    .cookie
    .includes("gpc=1;");
  const doNotSell = document
    .cookie
    .includes("sharing-opt-out=1;");
  const dnt = navigator.globalPrivacyControl || gpc || doNotSell || (window.doNotTrack && window.doNotTrack == "1") || (navigator.doNotTrack && (navigator.doNotTrack == "yes" || navigator.doNotTrack == "1")) || (navigator.msDoNotTrack && navigator.msDoNotTrack == "1") || (window.external && "msTrackingProtectionEnabled" in window.external && window.external.msTrackingProtectionEnabled());
  // create cookieYes script
  const cookieYesScript = document.createElement("script");
  cookieYesScript.src = "https://cdn-cookieyes.com/client_data/1b346b6a2c3ea409ebc9d7b8/script.js";

  // Load scripts based on environment and user privacy settings
  if (environment === "Production" && currentUrlPage !== "patents") {
    // Append CookieYes
    docHead.appendChild(cookieYesScript);

    if (!dnt) {
      // Listen too cookieYes
      // If rejecting non-essential set sharing-opt-out to 1
      document.addEventListener("cookieyes_consent_update", function (eventData) {
        const data = eventData.detail;
        if (data.accepted.length <= 5) {
          // Rejected non-essential cookies
          document.cookie = "sharing-opt-out=1";
        } else {
          // Accepted non-essential cookies
          // Append Tracking Scripts
          docHead.appendChild(trackingScripts);
        }
      });
    }
  }
</script>

<title>BUNN - Commercial Equipment, Service & Digital Solutions</title>
<meta charset="utf-8" />
<meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1" />

<meta name="description" content="BUNN Commercial" />
<meta name="author" content="BUNN Digital" />

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<!-- Fonts and icons -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/magnific-popup.js/1.1.0/magnific-popup.css" integrity="sha256-RdH19s+RN0bEXdaXsajztxnALYs/Z43H/Cdm1U4ar24=" crossorigin="anonymous" />
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/Zebra_datepicker/1.9.12/css/bootstrap/zebra_datepicker.min.css" integrity="sha256-oqpK+r+GDXzm0Pvxj2fd4nGdea1gkAgACEIzyUfJHTo=" crossorigin="anonymous" />
<link rel="stylesheet" href="https://pro.fontawesome.com/releases/v5.9.0/css/all.css" integrity="sha384-vlOMx0hKjUCl4WzuhIhSNZSm2yQCaf0mOU1hEDK/iztH3gU4v5NMmJln9273A6Jz" crossorigin="anonymous">
<script src="https://kit.fontawesome.com/f2c368f8ff.js" integrity="sha384-WAsFbnLEQcpCk8lM1UTWesAf5rGTCvb2Y+8LvyjAAcxK1c3s5c0L+SYOgxvc6PWG" crossorigin="anonymous"></script>

<link rel="shortcut icon" type="image/x-icon" media="all" href="/img/favicon/favicon.ico" />
<link rel="apple-touch-icon" sizes="180x180" href="/img/favicon/apple-touch-icon.png">
<link rel="icon" type="image/png" sizes="32x32" href="/img/favicon/favicon-32x32.png">
<link rel="icon" type="image/png" sizes="16x16" href="/img/favicon/favicon-16x16.png">
<link rel="manifest" href="/img/favicon/manifest.json">
<link rel="mask-icon" href="/img/favicon/safari-pinned-tab.svg" color="#5bbad5">
<meta name="theme-color" content="#ffffff">

<!-- Sandboxing CSS -->


<!-- CSR Mode CSS -->


<!-- <link rel="stylesheet" th:href="@{/css/fonts.css}" /> -->
<!-- <link rel="stylesheet" th:href="@{/css/bunn-commercial.css}" /> -->

<link rel="stylesheet" href="/css/bunn-bundle-976364060.css?themeConfigId=1"/>


<script src="/js/modernizr-custom.js"></script></head>

<style>
    .skip-link {
        position: absolute;
        top: -75px;
        left: 0;
        color: white;
        background: #005EB8;
        padding: 2px 5px 2px 5px;
        z-index: 100;
    }

    .skip-link:hover {
        color: white;
    }

    .skip-link:focus {
        top: 0;
    }

    .hero__image:hover .hero__action {
        text-decoration: underline;
    }
</style>

<body class="locale-en_US">
    <!-- <noscript><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-55RHZZX" height="0" width="0" style="display:none;visibility:hidden"></iframe></noscript> -->
<!-- <noscript><img height="1" width="1" style="display:none" src="https://www.facebook.com/tr?id=294039261626437&ev=PageView&noscript=1" /></noscript> -->
    <a class="skip-link font-sans-medium text-lg-1" href="#main">Skip to main content</a>
    
    
    

    <input id="cartItems" type="hidden" value="0" class="js-cart-cookie" data-site="commercial" />

    <div id="page" class="site-wrapper bg-white">

        
<div class="bg-black px-4 py-3 flex flex-wrap justify-center text-sm-1 md-lg:flex-no-wrap">
	<a href="https://www.bunn.com:443" class="text-white hover:text-white underline no-underline mr-2 sm:mx-2" aria-label="Home">
		<i class="fal fa-home-lg-alt mr-1"></i>
		<span class="hidden sm:inline underline">Home</span>
	</a>
	<div class="md-lg:order-last">
		
		<a href="/bunnserve" class="text-white hover:text-white underline mx-1">
			
			<span class="underline">BUNNserve</span>
		</a><a href="/help" class="text-white hover:text-white underline mx-1">
			
			<span class="underline">Support</span>
		</a><a href="/locations" class="text-white hover:text-white underline mx-1">
			
			<span class="underline">Locations</span>
		</a>
	</div>
	<div class="text-center sm:flex w-full pt-2 justify-center md-lg:w-auto md-lg:flex-grow md-lg:pt-0 md-lg:justify-end md-lg:mx-2">
		
		<div class="block lg:inline-block text-white sm:mx-2">
			<strong class="font-sans-demi">U.S. Orders:</strong>
			<span><a href="tel:+18006262866" class="text-white hover:text-white sm:mx-2">(800) 626-2866</a></span>
		</div>
		<div class="block lg:inline-block text-white sm:mx-2">
			<strong class="font-sans-demi">U.S. Tech Services:</strong>
			<span><a href="tel:+18002866070" class="text-white hover:text-white sm:mx-2">(800) 286-6070</a></span>
		</div>
	</div>
</div>
        <!-- SITE HEADER -->
<div class="js-site-header md:border-b border-gray-200 relative z-shell">

    <!-- NAVBAR -->
    <div class="js-navbar py-2 px-4 flex justify-between items-center md-lg:p-8">

        <!-- BROWSE BUTTON -->
        <div class="md:hidden">
            <button class="js-drawer-trigger uppercase p-2 pl-0" data-drawer="primary-nav-small"><i class="fal fa-bars"></i>&nbsp;Browse</button>
        </div>

        <!-- BRAND / DESKTOP LEFT -->
        <div class="js-navbar-left md-lg:flex md-lg:items-center">
            <a href="/" class="block w-32 h-16 mx-auto md-lg:px-0 md-lg:ml-0 md-lg:mr-4 md-lg:w-48 md-lg:p-0 flex" title="BUNN Commercial Homepage">
                <svg viewBox="0 0 232 45" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" class="block w-full">
	<title>BUNN Logo Horizontal</title>
	<defs>
		<polygon id="path-1" points="0.024 44 231.914 44 231.914 0.0225945946 0.024 0.0225945946"></polygon>
	</defs>
	<g id="Symbols" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
		<g id="BUNN-logo-horizontal">
			<g id="BUNN_Logo_no_slogan">
				<path d="M56.2735589,32.3871617 L82.2467141,32.3871617 C85.2055486,32.3871617 86.6028208,30.9908626 86.6028208,28.0349405 C86.6028208,25.0379863 84.9591133,23.6420895 80.8901118,23.6420895 L56.2735589,23.6420895 L56.2735589,32.3871617 Z M85.534129,15.7594966 C85.534129,12.9266709 84.1779294,11.6128383 81.3423126,11.6128383 L56.2735589,11.6128383 L56.2735589,20.0292512 L80.0682581,20.0292512 C83.9725667,20.0292512 85.534129,18.6333544 85.534129,15.7594966 Z M53.1915067,36 C52.4111282,36 52,35.5892765 52,34.8092638 L52,9.19033389 C52,8.41032125 52.4111282,8 53.1915067,8 L82.6574396,8 C87.4657471,8 89.9313083,10.2990058 89.9313083,15.1025803 C89.9313083,18.5923223 88.3697459,20.7271996 85.1234035,21.671743 L85.1234035,21.753405 C89.1505271,22.5338199 91,24.8738578 91,28.6918568 C91,33.6185277 88.4929636,36 83.5614385,36 L53.1915067,36 L53.1915067,36 Z" id="Fill-1" fill="#0B0C0A"></path>
				<path d="M109.954607,36 C100.746836,36 96,31.2374576 96,22 L96,9.19033389 C96,8.41032125 96.4090026,8 97.1865085,8 L99.027822,8 C99.8466292,8 100.256033,8.41032125 100.256033,9.19033389 L100.256033,22 C100.256033,28.9384518 103.693258,32.3871617 110.568512,32.3871617 L120.553788,32.3871617 C127.429041,32.3871617 130.866668,28.9384518 130.866668,22 L130.866668,9.19033389 C130.866668,8.41032125 131.316972,8 132.094478,8 L133.813091,8 C134.590596,8 135,8.41032125 135,9.19033389 L135,22 C135,31.2374576 130.252763,36 121.045393,36 L109.954607,36" id="Fill-2" fill="#0B0C0A"></path>
				<path d="M175.1001,36 C174.208848,36 173.763222,35.7127751 173.19617,35.2199874 L145.171741,11.6128383 L145.090393,11.6128383 L145.090393,34.8092638 C145.090393,35.5892765 144.685639,36 143.915814,36 L142.215055,36 C141.445229,36 141,35.5892765 141,34.8092638 L141,9.19033389 C141,8.41032125 141.445229,8 142.215055,8 L145.940772,8 C146.831627,8 147.236778,8.28722487 147.844305,8.78001264 L175.828656,32.3871617 L175.909607,32.3871617 L175.909607,9.19033389 C175.909607,8.41032125 176.314758,8 177.084186,8 L178.825818,8 C179.595246,8 180,8.41032125 180,9.19033389 L180,34.8092638 C180,35.5892765 179.595246,36 178.825818,36 L175.1001,36" id="Fill-3" fill="#0B0C0A"></path>
				<path d="M221.099356,36 C220.208907,36 219.762889,35.7127751 219.196239,35.2199874 L191.171698,11.6128383 L191.090748,11.6128383 L191.090748,34.8092638 C191.090748,35.5892765 190.685602,36 189.916181,36 L188.215042,36 C187.445621,36 187,35.5892765 187,34.8092638 L187,9.19033389 C187,8.41032125 187.445621,8 188.215042,8 L191.940722,8 C192.831965,8 193.236714,8.28722487 193.844632,8.78001264 L221.828302,32.3871617 L221.909649,32.3871617 L221.909649,9.19033389 C221.909649,8.41032125 222.314795,8 223.084216,8 L224.825433,8 C225.594854,8 226,8.41032125 226,9.19033389 L226,34.8092638 C226,35.5892765 225.594854,36 224.825433,36 L221.099356,36" id="Fill-4" fill="#0B0C0A"></path>
				<g id="Group-9">
					<mask id="mask-2" fill="white">
						<use xlink:href="#path-1"></use>
					</mask>
					<g id="Clip-6"></g>
					<path d="M229.1932,11.4836036 L229.5428,11.4836036 L229.5428,10.5025225 L229.9188,10.5025225 L230.5432,11.4836036 L230.9188,11.4836036 L230.2572,10.4763604 C230.4304,10.4589189 230.5748,10.4022342 230.6916,10.3059099 C230.8076,10.209982 230.866,10.0585586 230.866,9.85203604 C230.866,9.41877477 230.5976,9.20194595 230.0616,9.20194595 L229.1932,9.20194595 L229.1932,11.4836036 Z M229.5428,9.48536937 L230.0032,9.48536937 C230.0632,9.48536937 230.1232,9.48854054 230.1832,9.49527928 C230.2432,9.50281081 230.298,9.51827027 230.3472,9.54284685 C230.3968,9.56742342 230.4376,9.6030991 230.4692,9.65027027 C230.5008,9.69744144 230.5168,9.75967568 230.5168,9.83657658 C230.5168,9.92774775 230.4988,9.9990991 230.4636,10.0514234 C230.4284,10.1041441 230.3824,10.1425946 230.3264,10.1671712 C230.2696,10.1917477 230.2044,10.2064144 230.1304,10.2115676 C230.056,10.2167207 229.98,10.2194955 229.9028,10.2194955 L229.5428,10.2194955 L229.5428,9.48536937 Z M228.132,11.1216937 C228.236,11.3599279 228.378,11.5648649 228.558,11.7380901 C228.738,11.9113153 228.9472,12.0476757 229.1852,12.1475676 C229.4236,12.2470631 229.6768,12.297009 229.9448,12.297009 C230.2132,12.297009 230.4664,12.2470631 230.7044,12.1475676 C230.9428,12.0476757 231.152,11.9113153 231.332,11.7380901 C231.5116,11.5648649 231.654,11.3599279 231.758,11.1216937 C231.862,10.8838559 231.914,10.625009 231.914,10.3455495 C231.914,10.0692613 231.862,9.81120721 231.758,9.57178378 C231.654,9.33236036 231.5116,9.12583784 231.332,8.95261261 C231.152,8.77978378 230.9428,8.64302703 230.7044,8.54353153 C230.4664,8.44363964 230.2132,8.39369369 229.9448,8.39369369 C229.6768,8.39369369 229.4236,8.44363964 229.1852,8.54353153 C228.9472,8.64302703 228.738,8.77978378 228.558,8.95261261 C228.378,9.12583784 228.236,9.33236036 228.132,9.57178378 C228.028,9.81120721 227.976,10.0692613 227.976,10.3455495 C227.976,10.625009 228.028,10.8838559 228.132,11.1216937 L228.132,11.1216937 Z M228.4524,9.68713514 C228.5368,9.48259459 228.6516,9.3058018 228.7964,9.15715315 C228.9412,9.0085045 229.112,8.89156757 229.31,8.80594595 C229.5076,8.72032432 229.7192,8.67751351 229.9448,8.67751351 C230.1708,8.67751351 230.382,8.72032432 230.5776,8.80594595 C230.7736,8.89156757 230.9444,9.0085045 231.0912,9.15715315 C231.2376,9.3058018 231.3532,9.48259459 231.4376,9.68713514 C231.5224,9.89167568 231.5648,10.1108829 231.5648,10.3455495 C231.5648,10.5833874 231.5224,10.8037838 231.4376,11.0063423 C231.3532,11.2092973 231.2376,11.3849009 231.0912,11.5335495 C230.9444,11.6821982 230.7736,11.7995315 230.5776,11.8851532 C230.382,11.9707748 230.1708,12.0135856 229.9448,12.0135856 C229.7192,12.0135856 229.5076,11.9707748 229.31,11.8851532 C229.112,11.7995315 228.9412,11.6821982 228.7964,11.5335495 C228.6516,11.3849009 228.5368,11.2092973 228.4524,11.0063423 C228.3676,10.8037838 228.3252,10.5833874 228.3252,10.3455495 C228.3252,10.1108829 228.3676,9.89167568 228.4524,9.68713514 L228.4524,9.68713514 Z" id="Fill-5" fill="#0B0C0A" mask="url(#mask-2)"></path>
					<path d="M37.576,37.3116036 C45.462,29.7495495 46.5136,14.5972973 38.0692,6.70781982 C38.0692,6.70781982 37.576,6.2476036 37.0968,6.72209009 C24.7992,21.3047207 25.3096,21.0906667 24.7992,21.5441441 C22.9792,23.161045 20.8036,22.6623784 19.7312,21.5441441 C18.4568,20.2158198 6.7084,6.72209009 6.7084,6.72209009 C6.7084,6.72209009 6.2292,6.2476036 5.734,6.70583784 C-1.5588,13.4580541 -2.4268,28.7335856 6.2292,37.3116036 C14.8856,45.890018 27.928,46.5630991 37.576,37.3116036 Z" id="Fill-7" fill="#0B0C0A" mask="url(#mask-2)"></path>
					<path d="M20.19,17.5175495 C19.656,16.9483243 9.2932,5.39059459 9.2932,5.39059459 C8.962,5.06237838 8.962,4.52526126 9.2932,4.19744144 C9.2932,4.19744144 11.4324,2.36133333 13.912,1.56774775 C18.95,-0.0455855856 22.8176,-0.422558559 26.7176,0.564072072 C31.602,1.79963964 33.9024,3.62544144 34.5248,4.19744144 C34.8556,4.52526126 34.8556,5.06237838 34.5248,5.39059459 C34.5248,5.39059459 24.7884,17.0323604 24.298,17.5175495 C23.2332,18.5711712 21.0608,18.4451171 20.19,17.5175495" id="Fill-8" fill="#265495" mask="url(#mask-2)"></path>
				</g>
			</g>
		</g>
	</g>
</svg>
            </a>
            <!-- insert country selector here for desktop -->
        </div>

        <!-- SEARCH/REGISTER/CART -->
        <div class="js-navbar-right flex md-lg:flex-grow justify-end items-center">
            <!-- insert search here for desktop -->
            <div class="navbar-account relative">
                
                
                    <a href="/login" id="linkLogin" class="text-black p-2 ml-2 block leading-none" aria-label="Login"><i class="fal fa-user"></i>
                        <span class="hidden md-lg:inline-block hover:underline">Sign in / Register</span>
                    </a>
                
                
                
            </div>
            <div class="navbar-cart">
                <a href="/cart" class="text-black block p-2 ml-2 leading-none js-cart-link" title="Go to Cart" aria-label="Cart">
                    <i class="fal fa-shopping-cart"></i>
                    <span class="js-cart-quantity hidden">0</span>
                </a>
            </div>
        </div>

    </div>

    <div class="js-search-bar navbar-search hidden mx-4 mb-2 md-lg:max-w-sm md-lg:mx-8 md-lg:w-full md-lg:flex-grow md-lg:mb-0">

        <div class="rounded-full border border-black bg-white md-lg:border-0 md-lg:px-0">
            <form action="/search" method="GET" class="js-searchForm flex">
                <div class="flex items-center h-10 ml-2 p-2 md-lg:hidden">
                    <i class="fal fa-search"></i>
                </div>
                <label for="searchQuery" class="hidden sr-only">Search</label>
                <input id="searchQuery" type="search" class="js-search flex-grow bg-transparent rounded-r-full h-10 px-2 md-lg:py-1 md-lg:pl-4 md-lg:pr-2 md-lg:border-r-0 md-lg:border md-lg:border-black md-lg:rounded-l-full md-lg:rounded-r-none appearance-none" name="q" autocomplete="off" placeholder="keyword, product #, model name" value="" data-hj-whitelist>

                <button class="py-2 pl-3 rounded-r-full leading-none h-10 md-lg:pr-4 hidden md-lg:inline-block md-lg:bg-black md-lg:hover:bg-brand-primary-light-1 md-lg:text-white" type="submit" aria-label="Submit">
                    <i class="fal fa-search"></i>
                </button>
            </form>
        </div>

        <div class="typeahead z-menu lg:relative" id="typeAhead" style="display:none;">
            <div class="js-typeahead-content flex flex-col absolute z-shell inset-x-0 mt-1 mx-4 bg-white border border-gray-200 rounded-lg shadow-lg transition-all-02s-ease md-lg:flex-row md-lg:items-stretch lg:mx-0 md-lg:p-0 lg:left-auto lg:right-0 lg:w-204">
                <div class="js-typeahead-section js-typeahead-section-keyword px-8 py-4 border-b border-gray-200 md-lg:border-b-0 md-lg:border-r md-lg:pr-12 md-lg:flex-none md-lg:max-w-sm">
                    <div class="uppercase text-sm-2 mb-2 text-gray-700 tracking-wide font-sans-medium">Suggestions</div>
                    <ul class="js-typeahead-keyword mb-0"></ul>
                </div>
                <div class="js-typeahead-section js-typeahead-section-category px-8 py-4 hidden md-lg:block md-lg:border-r md-lg:pr-12 md-lg:flex-grow md-lg:max-w-sm md-lg:border-gray-200">
                    <div class="uppercase text-sm-2 mb-2 text-gray-700 tracking-wide font-sans-medium">Categories</div>
                    <ul class="js-typeahead-category mb-0"></ul>
                </div>
                <div class="js-typeahead-section js-typeahead-section-products px-8 py-4 md-lg:flex-grow md-lg:max-w-sm">
                    <ul class="js-typeahead-product"></ul>
                    <a href="" class="js-view-all-results-link flex items-center font-sans-medium"><span class="mr-2">View all results</span> <i class="fal fa-angle-right"></i></a>
                </div>
            </div>
        </div>

    </div>

</div>
<!-- /site-header -->


<div class="js-region-selector text-center border-b border-gray-300 py-2 lg:border-0 lg:pb-0 lg:pt-1">
    <button class="js-drawer-trigger text-base hover:bg-brand-primary hover:text-white px-4 py-1 rounded-full" data-drawer="regions-menu">
        <i class="fa fa-globe-americas"></i> &nbsp;<strong class="font-sans-demi">Region</strong>: <span class="selected-region underline"><!-- set from cookie --></span>
    </button>
</div>


        <div class="main" id="main" tabindex="-1">

            <div data-czid="Commercial Content Zone Section One" class="content-zone-container">


<div class="row text-center">
    <style>
   #hero-fast-cup {
   background-image: url(https://res.cloudinary.com/bunn-assets/image/upload/v1695851582/landing-pages/Commercial/Main%20Page/Premia_Masthead_Commercial.jpg);
   background-blend-mode: overlay;
   background-size: cover;
   height: 40rem;
   background-position: right center;
   max-width: 2000px;
   margin: 0 auto;
   position: relative;
   }
   .premia_header_text {
   padding-left: 10%;
   }
   @media only screen and (max-width: 1199px) {
   #hero-fast-cup {
   height: 30rem;
   }
   .premia_header_text {
   padding-left: 5%;
   }
   }
   @media only screen and (max-width: 767px) {
   #hero-fast-cup {
   background-image: url(https://res.cloudinary.com/bunn-assets/image/upload/v1695851786/landing-pages/Commercial/Main%20Page/Premia_Masthead_Commercial_mobiel.jpg);
   height: 24rem;
   background-position: center center;
   }
   .hero__branding svg {
   max-width: 50%;
   }
   }
   .banner_sticker {
   position: absolute;
   width: 200px;
   top: 435px;
   left: 85%;
   }
   @media screen and (max-width: 1200px) {
   .banner_sticker {
   top: 330px;
   left: 80%;
   width: 155px;}
   }
   @media screen and (max-width: 767px) {
   .banner_sticker {
   top: 275px;
   left: 70%;
   width: 125px;}
   .w-full {
   width:90%;
   }
   }
</style>
<div class="section--collapsed hero">
   <a href="/premia" title="Premia"></a>
   <div class="hero__image flex items-center justify-left" id="hero-fast-cup">
      <a href="/premia" title="Premia" class="premia_header_text">
         <div class="w-full">
            <div class="hero__content text-white text-left md:w-1/2 lg:w-1/2 px-6 md:px-12 lg:px-16">
               <div class="hero__branding">
                  <svg class="block h-20 mb-2" viewbox="0 0 475.66 54">
                     <title>BUNN Premia</title>
                     <defs>
                        <style>
                          .st0 {
                            fill: #fff;
                          }
                        </style>
                      </defs>
                      <path class="st0" d="M153.8,54c-2.1,0-2.7-.3-3.9-1.6l-15.6-17.6h-38.7l-3.2,16.9c-.3,1.5-1.3,2.3-2.8,2.3h-3.6c-1.5,0-2.1-.8-1.8-2.3L93.7,2.3c.3-1.5,1.3-2.3,2.8-2.3h55.2c8.6,0,14.2,4.4,14.2,12.8,0,13.1-6.3,21.2-20.8,21.2h-1v.2l15.8,16.9c.4.4.5.9.5,1.3,0,1.2-.9,1.7-1.9,1.7h-4.5ZM101,7l-4,20.9h47.3c8.7,0,12.8-5,12.8-13.1s-2.9-7.8-8.6-7.8c0,0-47.4,0-47.4,0Z"/>
                      <path class="st0" d="M184.4,23.2h50.9c1.5,0,2.1.8,1.8,2.3l-.4,2.4c-.3,1.5-1.3,2.3-2.8,2.3h-51l-3.2,16.9h61.3c1.5,0,2.1.8,1.8,2.3l-.5,2.4c-.3,1.5-1.2,2.3-2.7,2.3h-67.2c-1.5,0-2.1-.8-1.8-2.3l9.6-49.4c.3-1.5,1.3-2.3,2.8-2.3h67.1c1.5,0,2.1.8,1.8,2.3l-.4,2.4c-.3,1.5-1.3,2.3-2.8,2.3h-61.3l-3.1,16.2h0Z"/>
                      <path class="st0" d="M340.1,54c-1.5,0-2.2-.8-1.9-2.3l8.7-44.6h-.2l-41.5,45.1c-1,1-1.9,1.7-3.6,1.7h-4.4c-1.7,0-2.4-.7-2.9-1.7l-24-45.1h-.2l-8.6,44.6c-.3,1.5-1.3,2.3-2.8,2.3h-3.3c-1.5,0-2.2-.8-1.9-2.3l9.6-49.4c.3-1.5,1.3-2.3,2.8-2.3h7.5c1.7,0,2.5.7,3,1.7l23.8,44.9h.2L341.7,1.7c1-1,1.8-1.7,3.6-1.7h8.9c1.5,0,2.1.8,1.8,2.3l-9.6,49.4c-.3,1.5-1.2,2.3-2.7,2.3h-3.6Z"/>
                      <path class="st0" d="M363.1,54c-1.5,0-2.1-.8-1.8-2.3l9.6-49.4c.3-1.5,1.3-2.3,2.8-2.3h3.6c1.5,0,2.1.8,1.8,2.3l-9.6,49.4c-.3,1.5-1.3,2.3-2.8,2.3h-3.6Z"/>
                      <path class="st0" d="M66.3,0H12.4c-1.5,0-2.4.8-2.8,2.3l-.9,4.7h54.9c6.2,0,9.2,2.8,9.2,8.4,0,8.6-4.2,14-13.5,14H4.4L0,51.7c-.3,1.5.3,2.3,1.8,2.3h3.6c1.5,0,2.4-.8,2.8-2.3l3-15.4h48c15.4,0,22.3-8.5,22.3-22.6S75.6,0,66.4,0h0Z"/>
                      <path class="st0" d="M457.5,54c-2.1,0-2.6-.5-3.4-1.8l-5.9-10.5h-51.5l-9.9,10.5c-1.4,1.3-2.3,1.8-4.5,1.8h-3.8c-1,0-1.4-.6-1.4-1.3s.2-1,.7-1.4L424.2,1.8c1.3-1.3,1.9-1.8,4-1.8h4c2.2,0,2.5.5,3.3,1.8l27.2,49.4c.2.2.2.5.2.9,0,1-.7,1.9-2,1.9h-3.5ZM445,34.8l-15.7-28h-.2l-26.5,28v.2h42.4v-.2h0Z"/>
                      <path class="st0" d="M459.8,6.4c0-.6.1-1.2.4-1.7.2-.5.6-1,1-1.4.4-.4.9-.7,1.4-1s1.1-.4,1.7-.4,1.2.1,1.7.4,1,.6,1.4,1c.4.4.7.9,1,1.4.2.5.4,1.1.4,1.7s-.1,1.2-.4,1.7c-.2.5-.6,1-1,1.4-.4.4-.9.7-1.4,1s-1.1.4-1.7.4-1.2-.1-1.7-.4-1-.6-1.4-1c-.4-.4-.7-.9-1-1.4-.2-.5-.4-1.1-.4-1.7ZM460.6,6.4c0,.5,0,1,.3,1.4.2.4.5.8.8,1.2s.7.6,1.2.8c.4.2.9.3,1.4.3s1,0,1.4-.3c.4-.2.8-.5,1.2-.8.3-.3.6-.7.8-1.2.2-.4.3-.9.3-1.4s0-1-.3-1.4c-.2-.4-.5-.8-.8-1.2-.3-.3-.7-.6-1.2-.8-.4-.2-.9-.3-1.4-.3s-1,0-1.4.3c-.4.2-.8.5-1.2.8-.3.3-.6.7-.8,1.2-.2.4-.3.9-.3,1.4ZM462.6,3.9h2c.6,0,1.1.1,1.4.4.3.3.4.6.4,1.1s-.1.8-.3,1c-.2.2-.5.4-.9.4l1.3,2.2h-1l-1.3-2.1h-.7v2.1h-.9V3.9ZM463.5,6.1h.7c.1,0,.3,0,.4,0,.1,0,.3,0,.4,0,.1,0,.2-.1.3-.2,0,0,.1-.2.1-.4s0-.3-.1-.4c0,0-.2-.2-.3-.2-.1,0-.2,0-.4,0-.1,0-.3,0-.4,0h-.7v1.4Z"/>
                  </svg>
                  <div class="hero__text text-body md:text-lg-1 lg:text-lg-3 leading-normal pt-1">Coffee Excellence<br> Consumers Crave</div>
                  <div class="hero__action font-sans-medium text-base md:text-lg-1 lg:text-lg-3 leading-normal text-brand-primary pt-4">Learn more</div>
               </div>
            </div>
         </div>
      </a>
      <div class="banner_sticker"><img alt="CSP Best New Product - Retailer Choice - Winner 2024" src="https://res.cloudinary.com/bunn-assets/image/upload/v1730830412/landing-pages/Commercial/Premia/BNPC2024_WINNER_PNG.png"></div>
   </div>
</div>
</div></div>
            <div data-czid="Commercial Content Zone Section Two" class="content-zone-container">


<div class="row text-center">
    <style>
#bunn-portfolio {
    background-image: url(https://res.cloudinary.com/bunn-assets/image/upload/v1770042458/landing-pages/value%20portfolio/BUNN-Advantage-bg.jpg);
    background-size: cover;
    height: 45rem;
    background-position: center;
    max-width: 2000px;
    margin: 0 auto;
}

@media only screen and (max-width: 1199px) {
#bunn-portfolio {
    height: 30rem;
}
}

@media only screen and (max-width: 767px) {
#bunn-portfolio {
    background-image: url(https://res.cloudinary.com/bunn-assets/image/upload/v1770042622/landing-pages/value%20portfolio/BUNN-Advantage-Mobile-bg.jpg);
}
}
</style>
<div class="section--collapsed hero"> <a href="/bunn-advantage" title="BUNN Advantage">
  <div class="hero__image flex items-center justify-center" id="bunn-portfolio">
    <div class="w-full">
      <div class="hero__content text-white px-12 md:px-16 lg:px-40">
        <div class="hero__title font-sans-medium text-lg-2 md:text-lg-3 md:leading-none lg:text-lg-5 uppercase">The BUNN Advantage!</div>
        <div class="hero__text text-body md:text-lg-1 lg:text-lg-3">Learn how BUNN is the partner built to support your business.</div>
      </div>
    </div>
  </div>
  </a></div>
</div></div>
            <div data-czid="Commercial Content Zone Section Three" class="content-zone-container">


<div class="row text-center">
    <style>
  #hero-equipment {
    max-width: 2000px;
    margin: 0 auto;
    background-color: #fcfcfc;
  }
</style>
<div class="section--collapsed hero">
	<a href="/equipment-categories" title="BUNN Equipment">
	<div class="hero__image md:flex items-center justify-center" id="hero-equipment">
		<div class="md:w-1/2 pt-6 pb-2 md:py-0" id="equipment-bg">
			<img src="https://res.cloudinary.com/bunn-assets/image/upload/v1644848772/site-2/development/JPG/comm-lineup-new-mq.jpg" alt="">
		</div>
		<div class="md:w-1/2 flex">
			<div class="hero__content text-black text-left px-6 md:px-12 lg:px-16 pb-12 md:py-32 lg:py-40">
				<div class="hero__title font-sans-medium text-lg-2 md:text-lg-3 md:leading-none lg:text-lg-5 uppercase">Equipment
				</div>
				<div class="hero__text text-body md:text-lg-1 lg:text-lg-3 leading-normal pt-1">BUNN equipment portfolio includes a full line of commercial solutions for every beverage channel and every serving occasion.
				</div>
				<div class="hero__action font-sans-medium text-base md:text-lg-1 lg:text-lg-3 leading-normal text-brand-primary pt-4 font-sans-medium">Explore BUNN Equipment <i class="far fa-angle-right"></i>
				</div>
			</div>
		</div>
	</div>
	</a>
</div>
</div></div>
            <div data-czid="Commercial Content Zone Section Four" class="content-zone-container">


<div class="row text-center">
    <style>
  #hero-bunnserve {
    background-image: url(https://res.cloudinary.com/bunn-assets/image/upload/v1641568231/site-2/development/JPG/bunnserve-banner.jpg), linear-gradient(90deg, rgba(0,0,0,0.85) 27%, rgba(0,0,0,0.5) 50%, rgba(0,0,0,0) 66%);
    background-blend-mode: overlay;
    background-size: cover;
    height: 50rem;
    background-position: center top;
    max-width: 2000px;
    margin: 0 auto;
  }
  @media only screen and (max-width: 1680px) {
    #hero-bunnserve {
      height: 60rem;
    }
  }
  @media only screen and (max-width: 1199px) {
    #hero-bunnserve {
      background-image: url(https://res.cloudinary.com/bunn-assets/image/upload/v1641847213/site-2/development/JPG/bunnserve-banner-ipad.jpg), linear-gradient(90deg, rgba(0,0,0,0.85) 30%, rgba(0,0,0,0.5) 50%, rgba(0,0,0,0) 66%);
      background-blend-mode: overlay;
      background-size: cover;
      height: 38rem;
    }
  }
  @media only screen and (max-width: 767px) {
    #hero-bunnserve {
      background-image: url(https://res.cloudinary.com/bunn-assets/image/upload/v1641826425/site-2/development/JPG/bunnserve-banner-mobile.jpg), linear-gradient(0deg, rgba(0, 0, 0, 0.75), rgba(0, 0, 0, 0.75));
      background-position: center center;
      height: 32rem;
    }
  }</style><div class="section--collapsed hero">
	<a href="/bunnserve" title="BUNNserve"><div class="hero__image flex items-center justify-center" id="hero-bunnserve"><div class="w-full"><div class="hero__content text-white text-left md:w-1/2 lg:w-1/2 px-6 md:px-12 lg:px-16"><div class="hero__title font-sans-medium text-lg-2 md:text-lg-3 md:leading-none lg:text-lg-5">BUNNserve<sup style="font-size: 0.5em;">&reg;</sup></div><div class="hero__text text-body md:text-lg-1 lg:text-lg-3 leading-normal pt-1">Maximize the cost of equipment ownership and ROI through a partnership with BUNNserve, featuring customizable and professionally managed service programs for multi-beverage and multi-vendor platforms. Bundling equipment and service packages from a single-contact supplier simplifies the process for sourcing product specs, equipment installation, comprehensive service and preventive maintenance.</div><div class="hero__action font-sans-medium text-base md:text-lg-1 lg:text-lg-3 leading-normal text-brand-primary pt-4 font-sans-medium">Learn more <i class="far fa-angle-right"></i></div></div></div></div>
	</a></div>
</div></div>
            <div data-czid="Commercial Content Zone Section Five" class="content-zone-container">


<div class="row text-center">
    <style>
  #hero-digital-solutions {
    background-image: url(https://res.cloudinary.com/bunn-assets/image/upload/q_auto:eco/v1644849254/site-2/development/PNG/digital-solutions-bg-mq.png), linear-gradient(270deg, rgba(0,0,0,0.5) 27%, rgba(0,0,0,0.35) 50%, rgba(0,0,0,0) 66%);
    background-blend-mode: overlay;
    background-size: cover;
    height: 45rem;
    background-position: center top;
    max-width: 2000px;
    margin: 0 auto;
  }
  @media only screen and (max-width: 1199px) {
    #hero-digital-solutions {
      height: 32rem;
    }
  }
  @media only screen and (max-width: 767px) {
    #hero-digital-solutions {
      background-image: url(https://res.cloudinary.com/bunn-assets/image/upload/q_auto:eco/v1641827298/site-2/development/JPG/digital-solutions-bg-mobile2.png);
      background-position: center top;
      height: 28rem;
    }
  }</style><div><a href="/bunndigital" title="BUNNdigital"><div class="flex items-center md:justify-end" id="hero-digital-solutions"><div class="text-white text-left md:w-1/2 lg:w-1/2 px-6 md:px-12 lg:px-16"><div class="font-sans-medium text-lg-2 md:text-lg-3 md:leading-none lg:text-lg-5">BUNNdigital<sup style="font-size: 0.5em;">&trade;</sup></div><div class="text-body md:text-lg-1 lg:text-lg-3 leading-normal pt-1">In a high-tech world where touchless commands and machine-to-machine communication are part of the daily norm, BUNN assists our customers by incorporating digital solutions and advanced technology for equipment and service offerings.</div><div class="hero__action font-sans-medium text-base md:text-lg-1 lg:text-lg-3 leading-normal text-brand-primary pt-4 font-sans-medium">Learn more <i class="far fa-angle-right"></i></div></div></div></a></div>
</div></div>
            
            <div data-czid="Commercial Content Zone Section Seven" class="content-zone-container">


<div class="row text-center">
    <style>
  #hero-support {
    background-image: url(https://res.cloudinary.com/bunn-assets/image/upload/v1641569927/site-2/development/JPG/support-bg.jpg), linear-gradient(90deg, rgba(255,255,255,1) 35%, rgba(255,255,255,0.5) 50%, rgba(255,255,255,0) 60%);
    background-blend-mode: overlay;
    background-size: cover;
    height: 45rem;
    background-position: right center;
    max-width: 2000px;
    margin: 0 auto;
  }
  @media only screen and (max-width: 1680px) {
    #hero-support {
      height: 52rem;
    }
  }
  @media only screen and (max-width: 1199px) {
    #hero-support {
      height: 36rem;
    }
  }
  @media only screen and (max-width: 767px) {
    #hero-support {
      background-image: url(https://res.cloudinary.com/bunn-assets/image/upload/v1641569927/site-2/development/JPG/support-bg.jpg), linear-gradient(0deg, rgba(255,255,255,.75), rgba(255,255,255,.75));
      background-position: right center;
      height: 30rem;
    }
  }
</style>
<div class="section--collapsed hero">
	<a href="/help" title="Support">
	<div class="hero__image flex items-center justify-center" id="hero-support">
		<div class="w-full">
			<div class="hero__content text-black text-left md:w-1/2 lg:w-1/2 px-6 md:px-12 lg:px-16">
				<div class="hero__title text-lg-2 md:text-lg-3 md:leading-none lg:text-lg-5">Support
				</div>
				<div class="hero__text text-body md:text-lg-1 lg:text-lg-3 leading-normal pt-1">A comprehensive support center for customers featuring links to product data and materials such as manuals & brochures, care & cleaning videos, warranty information and contact information for various BUNN departments.
				</div>
				<div class="hero__action font-sans-medium text-base md:text-lg-1 lg:text-lg-3 leading-normal text-brand-primary pt-4 font-sans-medium">Learn more <i class="far fa-angle-right"></i>
				</div>
			</div>
		</div>
	</div>
	</a>
</div>
</div></div>

        </div>

        

        <!--Footer menus -->


<footer class="bg-black pt-4 pb-20">
    <div class="container text-center md:text-left">
        <div class="md:flex border-b border-gray-700 py-4 mb-4">
            <div class="md:flex-grow">
                <a href="https://commercial.bunn.com:443" class="block py-2 md:py-0 md:inline-block text-gray-500 hover:text-gray-300 hover:underline md:mr-2">Commercial</a>
                <a href="https://commercial.bunn.com:443/bunnserve" class="block py-2 md:py-0 md:inline-block text-gray-500 hover:text-gray-300 hover:underline md:mr-2">BUNNserve</a>
                <a href="https://retail.bunn.com:443" class="block py-2 md:py-0 md:inline-block text-gray-500 hover:text-gray-300 hover:underline md:mr-2">Home
                    Products</a>
                <a href="https://www.bunn.com:443/company" class="block py-2 md:py-0 md:inline-block text-gray-500 hover:text-gray-300 hover:underline md:mr-2">Company</a>
                <a href="https://www.bunn.com:443/mission-values" class="block py-2 md:py-0 md:inline-block text-gray-500 hover:text-gray-300 hover:underline md:mr-2">Mission
                    &amp; Values</a>
                <a href="https://www.bunn.com:443/careers" class="block py-2 md:py-0 md:inline-block text-gray-500 hover:text-gray-300 hover:underline md:mr-2">Careers</a>
            </div>
            <div class="py-4 md:py-0 md:text-right">
                <a href="https://www.facebook.com/BUNN.Commercial/" aria-label="Facebook" class="inline-block text-gray-500 hover:text-gray-300 hover:underline mx-2">
                    <i class="fab fa-facebook"></i>
                    
                    
                    
                    
                </a><a href="https://twitter.com/bunn" aria-label="Twitter" class="inline-block text-gray-500 hover:text-gray-300 hover:underline mx-2">
                    
                    <i class="fab fa-twitter"></i>
                    
                    
                    
                </a><a href="https://www.instagram.com/bunnquality/" aria-label="Instagram" class="inline-block text-gray-500 hover:text-gray-300 hover:underline mx-2">
                    
                    
                    <i class="fab fa-instagram"></i>
                    
                    
                </a><a href="https://www.linkedin.com/company/bunn-o-matic-corporation" aria-label="LinkedIn" class="inline-block text-gray-500 hover:text-gray-300 hover:underline mx-2">
                    
                    
                    
                    <i class="fab fa-linkedin"></i>
                    
                </a><a href="https://www.youtube.com/bunnbrewers" aria-label="YouTube" class="inline-block text-gray-500 hover:text-gray-300 hover:underline mx-2">
                    
                    
                    
                    
                    <i class="fab fa-youtube"></i>
                </a>
            </div>
        </div>
        <div class="text-sm-1 md:flex text-gray-500 pb-4">
            <div class="mr-3 pb-2 md:pb-0">&copy;<span>2026</span>
                BUNN All rights reserved</div>
            <div>
                <a href="https://www.bunn.com:443/privacy-center"
                    class="text-gray-500 hover:text-gray-500 hover:underline mr-2">Privacy</a>
                <a href="https://www.bunn.com:443/accessibility"
                    class="text-gray-500 hover:text-gray-500 hover:underline mr-2">Accessibility</a>
                <a href="https://www.bunn.com:443/terms-of-use"
                    class="text-gray-500 hover:text-gray-500 hover:underline mr-2">Terms of Use</a>
                <a href="https://www.bunn.com:443/unsubscribe"
                    class="text-gray-500 hover:text-gray-500 hover:underline mr-2">Unsubscribe</a>
                <a href="https://www.bunn.com:443/do-not-sell"
                    class="text-gray-500 hover:text-gray-500 hover:underline">Do Not Sell or Share My Personal Information</a>
            </div>
        </div>
    </div>
</footer>
    </div>
    <!-- /site-wrapper -->

    <!-- marketing modal -->
    <div data-czid="Marketing Modal Zone" class="content-zone-container">


<style>/* marketing modal */
                body.marketing-modal-active {
                  overflow: hidden !important;
                }

                .marketing-modal {
                  visibility: hidden;
                  backdrop-filter: blur(4px);
                  transition: opacity 0.25s ease;
                  z-index: 3000;
                }

                .marketing-modal.marketing-modal-active {
                  visibility: visible;
                }

                .marketing-modal.marketing-modal-active .marketing-modal-overlay {
                  z-index: 3001;
                }

                .marketing-modal.marketing-modal-active .marketing-modal-container {
                  z-index: 3002;
                }

                .marketing-modal .marketing-modal-overlay {
                  opacity: 0.5;
                }

                .marketing-modal .marketing-modal-container {
                  max-height: 82vh;
                  overflow-x: hidden;
                }

                .marketing-modal .marketing-modal-content input[type="text"],
                .marketing-modal .marketing-modal-content input[type="email"] {
                  height: 48px;
                }

                .marketing-modal .marketing-modal-content input[type="email"] {
                  top: 3px;
                }

                .marketing-modal span.marketing-modal-close {
                  top: 10px;
                  right: 10px;
                  padding-top: 3px;
                  opacity: 0.5;
                  background: rgba(0, 0, 0, 0.5);
                }

                .marketing-modal span.marketing-modal-close:hover,
                .marketing-modal span.marketing-modal-close:focus {
                  opacity: 1;
                }
                    .welbilt {
        display: flex;
        justify-content: center;
        align-items: flex-start;
        border-top: 0.3pt solid white;
        padding-top: 13px;
        padding-bottom: 13px;
    }</style><!--Marketing Modals-->

<!--/Marketing Modals--></div>
    <!-- /marketing modal -->

    <!-- Non-U.S. Region Selected -->
<div id="region-checkout" class="mfp-hide bg-white p-8 container max-w-lg shadow-2xl">
    <div class="text-lg-2 font-sans-medium mb-2">Attention</div>
    <p class="text-base">Orders can only be shipped in the United States.  Your selected catalog region indicates that you are outside the U.S.  Please change your region to North America - U.S. if you wish to check out. For international orders please call us at 1 (217) 529 6601</p>
    <div class="flex justify-end">
        <a class="js-popup-dismiss btn btn--primary btn--small" href="#">Dismiss</a>
    </div>
</div>

<!-- Address Verification -->
<div id="address-confirmation" class="mfp-hide bg-white p-8 container max-w-lg shadow-2xl relative">
    <div class="js-verification-title text-lg-2 font-sans-medium mb-2"><!-- Updated in js--></div>
    <p class="js-verification-message text-base mb-1"><!-- Updated in js--></p>
    <p class="text-base font-sans-medium py-3">
        <span class="js-address-line-1 uppercase block"><!-- Updated in js--></span>
        <span class="js-address-line-2 uppercase block hidden"><!-- Updated in js--></span>
        <span class="js-city-state-zip uppercase block"><!-- Updated in js--></span>
    </p>
    <div class="flex flex-col justify-cente items-center mt-2 gap-3">
        <a class="js-pick-address btn btn--outline btn--small w-64 text-center mr-1" data-continue="false" href="#">Pick another saved address</a>
        <a class="js-popup-dismiss btn btn--outline btn--small w-64 text-center mr-1" data-continue="false"  href="#">Edit address</a>
        <a class="js-popup-confirm btn btn--primary mr-1 btn--small w-64 text-center ml-1" data-continue="true" href="#">Use this address</a>
        <a class="js-popup-override btn btn--outline btn--small w-64 text-center ml-1 hidden" href="#">Use entered address</a>
    </div>
</div>

<!-- Cart Modal -->
<div id="cart-modal" class="mfp-hide bg-white p-8 container max-w-lg relative" >
    <div class="js-miniCart px-4">
        <div class="mini-cart-wrapper pt-4">
            


            

            
                <div class="mini-cart-empty">
                    <div class="text-lg-2 text-center">
                        Your cart is empty
                    </div>
                    <div class="flex justify-center mt-2 pt-4 pb-4">
                        <a class="js-popup-dismiss btn btn--outline mr-1 btn--small" data-continue="false" href="#">Continue Shopping</a>
                    </div>
                </div>
            
        </div>
    </div>
</div>
    

<div id="primary-nav-small" class="drawer js-drawer drawer--left z-modal md:py-4" data-hide-at="md" data-modal>

	<div class="fixed bg-white w-full h-16 top-0 z-shell flex justify-between items-center border-b border-gray-200">
		<div class="font-sans-medium leading-none flex-grow pl-6">Browse Equipment</div>
		<button class="js-drawer-close-btn self-stretch h-16 px-6 flex items-center cursor-pointer z-shell text-lg-1" aria-label="Close"><i class="fal fa-times"></i></button>
	</div>

	<div class="js-nav-small absolute inset-0 overflow-y-scroll scrolling-touch pt-16">
		<div class="js-primary-nav text-base md:border-t md:border-gray-200 md:relative md:flex md:justify-center">
			

				
				

				
				
					<div class="dropdown-menu-item js-dropdown-menu-item border-b border-gray-200 md:border-0 group">
						<button class="js-dropdown-menu-trigger cursor-pointer flex items-center py-4 px-6 font-sans-demi leading-none group-active:text-brand-primary">
							<span class="flex-grow md:flex-grow-0">New From BUNN</span>
							<div class="js-dropdown-menu-item-icon text-lg-1 md:ml-2 -my-1" data-active-icon="fa-angle-up" data-inactive-icon="fa-angle-down"><i class="fal fa-angle-down"></i></div>
						</button>
						<div class="dropdown-menu-content js-dropdown-menu-content hidden z-menu pb-2 text-left md:absolute md:py-4 md:max-w-sm md:bg-white md:shadow-md md:mt-px">

							
							<ul class="mb-0">
								
								<li>
									<a href="/platinum-pro" class="block py-2 px-6 text-black hover:text-brand-primary md:pr-8">Platinum Pro</a>
								</li>
								<li>
									<a href="/premia" class="block py-2 px-6 text-black hover:text-brand-primary md:pr-8">Premia</a>
								</li>
								<li>
									<a href="/bunndigital" class="block py-2 px-6 text-black hover:text-brand-primary md:pr-8">BUNNdigital</a>
								</li>
								<li>
									<a href="/new-from-bunn/infusion-series-platinum" class="block py-2 px-6 text-black hover:text-brand-primary md:pr-8">Infusion Series Platinum Edition</a>
								</li>
								<li>
									<a href="/cold-brew" class="block py-2 px-6 text-black hover:text-brand-primary md:pr-8">Cold Brew Mode</a>
								</li>
								<li>
									<a href="/cold-coffee-solutions" class="block py-2 px-6 text-black hover:text-brand-primary md:pr-8">Cold Coffee</a>
								</li>
								<li>
									<a href="/new-from-bunn/ultra-nx" class="block py-2 px-6 text-black hover:text-brand-primary md:pr-8">Ultra NX</a>
								</li>
								<li>
									<a href="/fast-cup" class="block py-2 px-6 text-black hover:text-brand-primary md:pr-8">Fast Cup</a>
								</li>
								<li>
									<a href="/new-from-bunn/infusion-series" class="block py-2 px-6 text-black hover:text-brand-primary md:pr-8">Infusion Series®</a>
								</li>
								<li>
									<a href="/new-from-bunn/nitron" class="block py-2 px-6 text-black hover:text-brand-primary md:pr-8">NITRON®</a>
								</li>
								<li>
									<a href="/new-from-bunn/black-and-white" class="block py-2 px-6 text-black hover:text-brand-primary md:pr-8">Black and White</a>
								</li>
								<li>
									<a href="/jdf" class="block py-2 px-6 text-black hover:text-brand-primary md:pr-8">JDF®</a>
								</li>
								<li>
									<a href="/new-from-bunn/crescendo" class="block py-2 px-6 text-black hover:text-brand-primary md:pr-8">Crescendo®</a>
								</li>
								<li>
									<a href="/new-from-bunn/sure-immersion" class="block py-2 px-6 text-black hover:text-brand-primary md:pr-8">Sure Immersion®</a>
								</li>
								<li>
									<a href="/new-from-bunn/g-series" class="block py-2 px-6 text-black hover:text-brand-primary md:pr-8">G-Series Grinders</a>
								</li>
								<li>
									<a href="/water-quality" class="block py-2 px-6 text-black hover:text-brand-primary md:pr-8">Water Filtration</a>
								</li>
							</ul>
							
						</div>

						
						
						
					</div>
				
				
			

				
				

				
				
					<div class="dropdown-menu-item js-dropdown-menu-item border-b border-gray-200 md:border-0 group">
						<button class="js-dropdown-menu-trigger cursor-pointer flex items-center py-4 px-6 font-sans-demi leading-none group-active:text-brand-primary">
							<span class="flex-grow md:flex-grow-0">Equipment &amp; Accessories</span>
							<div class="js-dropdown-menu-item-icon text-lg-1 md:ml-2 -my-1" data-active-icon="fa-angle-up" data-inactive-icon="fa-angle-down"><i class="fal fa-angle-down"></i></div>
						</button>
						

						
						<div class="dropdown-menu-content js-dropdown-menu-content hidden z-menu text-left md:w-full md:absolute md:inset-x-0 md:bg-white md:shadow-md md:mt-px">

							<div class="max-w-5xl m-auto pb-2 md:py-6 md:flex md:flex-wrap lg:justify-center">
								
									
									<div class="md:w-1/3 lg:w-auto lg:flex-1">
										<div class="hidden md:block font-sans-demi uppercase text-gray-700 text-sm-2 tracking-wide mb-2 px-6 md:pr-8 md:block">Coffee & Tea</div>
										<ul class="mb-0">
											<li>
												<a href="/equipment/coffee" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">Coffee</a>
											</li>
											<li>
												<a href="/equipment/espresso" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">Espresso</a>
											</li>
											<li>
												<a href="/equipment/bean-to-cup" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">Bean to Cup</a>
											</li>
											<li>
												<a href="/equipment/iced-tea" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">Iced Tea</a>
											</li>
											<li>
												<a href="/equipment/coffee-tea-combos" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">Coffee & Tea Combos</a>
											</li>
											<li>
												<a href="/equipment/cold-coffee" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">Cold Coffee</a>
											</li>
										</ul>
									</div>
									
								
									
									<div class="md:w-1/3 lg:w-auto lg:flex-1">
										<div class="hidden md:block font-sans-demi uppercase text-gray-700 text-sm-2 tracking-wide mb-2 px-6 md:pr-8 md:block">Dispensed Beverages</div>
										<ul class="mb-0">
											<li>
												<a href="/equipment/juice" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">Juice</a>
											</li>
											<li>
												<a href="/equipment/frozen-granita-slushy" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">Frozen Granita/Slushy</a>
											</li>
											<li>
												<a href="/equipment/cold-water-still-sparkling" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">Cold Water (still & sparkling)</a>
											</li>
											<li>
												<a href="/equipment/hot-chocolate-cappuccino" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">Hot Chocolate/Cappuccino</a>
											</li>
											<li>
												<a href="/equipment/hot-water" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">Hot Water</a>
											</li>
											<li>
												<a href="/equipment/liquid-coffee" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">Liquid Coffee</a>
											</li>
										</ul>
									</div>
									
								
									
									<div class="md:w-1/3 lg:w-auto lg:flex-1">
										<div class="hidden md:block font-sans-demi uppercase text-gray-700 text-sm-2 tracking-wide mb-2 px-6 md:pr-8 md:block">Grinders, Filters & Accessories</div>
										<ul class="mb-0">
											<li>
												<a href="/equipment/water-filters" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">Water Filters</a>
											</li>
											<li>
												<a href="/equipment/accessories" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">Accessories</a>
											</li>
											<li>
												<a href="/equipment/grinders" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">Grinders</a>
											</li>
											<li>
												<a href="/equipment/serving-holding" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">Serving & Holding</a>
											</li>
											<li>
												<a href="/equipment/paper-filters" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">Paper Filters</a>
											</li>
											<li>
												<a href="/clean-contact-category" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">Clean Contact Solutions</a>
											</li>
											<li>
												<a href="/equipment/supplies" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">Supplies</a>
											</li>
										</ul>
									</div>
									
								
							</div>


							
							


							
							


							
							


							
							<div class="hidden md:block m-auto max-w-5xl mb-8">
								<div class="hidden md:block font-sans-demi uppercase text-gray-700 text-sm-2 tracking-wide mx-6 pt-4 md:block md:mb-2 md:border-t md:border-gray-200">Popular Equipment Families</div>
								<ul class="mb-0 md:flex md:flex-wrap">
									<li class="md:w-1/3 md-lg:w-1/4 lg:w-1/5">
										<a href="/product-families/fast-cup-category" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">Fast Cup®</a>
									</li>
									<li class="md:w-1/3 md-lg:w-1/4 lg:w-1/5">
										<a href="/product-families/sure-immersion" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">Sure Immersion®</a>
									</li>
									<li class="md:w-1/3 md-lg:w-1/4 lg:w-1/5">
										<a href="/product-families/crescendo" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">Crescendo®</a>
									</li>
									<li class="md:w-1/3 md-lg:w-1/4 lg:w-1/5">
										<a href="/product-families/nitron" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">NITRON®</a>
									</li>
									<li class="md:w-1/3 md-lg:w-1/4 lg:w-1/5">
										<a href="/product-families/thermo-fresh" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">ThermoFresh®</a>
									</li>
									<li class="md:w-1/3 md-lg:w-1/4 lg:w-1/5">
										<a href="/product-families/soft-heat" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">Soft Heat®</a>
									</li>
									<li class="md:w-1/3 md-lg:w-1/4 lg:w-1/5">
										<a href="/product-families/gpr-series" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">GPR Series</a>
									</li>
									<li class="md:w-1/3 md-lg:w-1/4 lg:w-1/5">
										<a href="/product-families/vp-series" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">VP Series</a>
									</li>
									<li class="md:w-1/3 md-lg:w-1/4 lg:w-1/5">
										<a href="/product-families/trifecta" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">Trifecta</a>
									</li>
									<li class="md:w-1/3 md-lg:w-1/4 lg:w-1/5">
										<a href="/product-families/axiom" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">Axiom®</a>
									</li>
									<li class="md:w-1/3 md-lg:w-1/4 lg:w-1/5">
										<a href="/product-families/infusion-series" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">Infusion Series®</a>
									</li>
									<li class="md:w-1/3 md-lg:w-1/4 lg:w-1/5">
										<a href="/product-families/black--white" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">Black & White</a>
									</li>
									<li class="md:w-1/3 md-lg:w-1/4 lg:w-1/5">
										<a href="/product-families/imix" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">iMIX®</a>
									</li>
									<li class="md:w-1/3 md-lg:w-1/4 lg:w-1/5">
										<a href="/product-families/bunn-refresh" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">BUNN Refresh</a>
									</li>
									<li class="md:w-1/3 md-lg:w-1/4 lg:w-1/5">
										<a href="/product-families/smart-wave" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">SmartWAVE®</a>
									</li>
									<li class="md:w-1/3 md-lg:w-1/4 lg:w-1/5">
										<a href="/product-families/ultra" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">Ultra® NX</a>
									</li>
									<li class="md:w-1/3 md-lg:w-1/4 lg:w-1/5">
										<a href="/product-families/cw-series" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">CW Series</a>
									</li>
									<li class="md:w-1/3 md-lg:w-1/4 lg:w-1/5">
										<a href="/product-families/titan" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">Titan®</a>
									</li>
									<li class="md:w-1/3 md-lg:w-1/4 lg:w-1/5">
										<a href="/product-families/my-cafe" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">My Café</a>
									</li>
									<li class="md:w-1/3 md-lg:w-1/4 lg:w-1/5">
										<a href="/product-families/jdf-series" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">JDF Series</a>
									</li>
									<li class="md:w-1/3 md-lg:w-1/4 lg:w-1/5">
										<a href="/gvh-grinder" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">GVH Grinder</a>
									</li>
									<li class="md:w-1/3 md-lg:w-1/4 lg:w-1/5">
										<a href="/popular-equipment-families/platinum-pro" class="block py-2 md:py-1 px-6 text-black hover:text-brand-primary md:pr-8">Platinum Pro</a>
									</li>
								</ul>
							</div>

						</div>
						
					</div>
				
				
			

				
				

				
				
					<div class="dropdown-menu-item js-dropdown-menu-item border-b border-gray-200 md:border-0 group">
						<button class="js-dropdown-menu-trigger cursor-pointer flex items-center py-4 px-6 font-sans-demi leading-none group-active:text-brand-primary">
							<span class="flex-grow md:flex-grow-0">Parts</span>
							<div class="js-dropdown-menu-item-icon text-lg-1 md:ml-2 -my-1" data-active-icon="fa-angle-up" data-inactive-icon="fa-angle-down"><i class="fal fa-angle-down"></i></div>
						</button>
						<div class="dropdown-menu-content js-dropdown-menu-content hidden z-menu pb-2 text-left md:absolute md:py-4 md:max-w-sm md:bg-white md:shadow-md md:mt-px">

							
							<ul class="mb-0">
								<li>
									<a href="/parts" class="block py-2 px-6 text-black hover:text-brand-primary md:pr-8">All Parts</a>
								</li>
								<li>
									<a href="/parts/electronic" class="block py-2 px-6 text-black hover:text-brand-primary md:pr-8">Electric/Electronic</a>
								</li>
								<li>
									<a href="/parts/plumbing" class="block py-2 px-6 text-black hover:text-brand-primary md:pr-8">Plumbing</a>
								</li>
								<li>
									<a href="/parts/hardware" class="block py-2 px-6 text-black hover:text-brand-primary md:pr-8">Hardware</a>
								</li>
								<li>
									<a href="/parts/housings" class="block py-2 px-6 text-black hover:text-brand-primary md:pr-8">Housings</a>
								</li>
								<li>
									<a href="/parts/seals-gaskets" class="block py-2 px-6 text-black hover:text-brand-primary md:pr-8">Seals/Gaskets</a>
								</li>
								<li>
									<a href="/parts/decals" class="block py-2 px-6 text-black hover:text-brand-primary md:pr-8">Decals</a>
								</li>
								<li>
									<a href="/parts/hoppers" class="block py-2 px-6 text-black hover:text-brand-primary md:pr-8">Hoppers</a>
								</li>
								<li>
									<a href="/parts/pm-kits" class="block py-2 px-6 text-black hover:text-brand-primary md:pr-8">PM Kits</a>
								</li>
							</ul>
							
						</div>

						
						
						
					</div>
				
				
			

				
				
					<a href="/help" class="block py-3 md:py-4 px-6 font-sans-demi leading-none text-black border-b border-gray-200 md:border-0">Support</a>
				

				
				
				
			

				
				
					<a href="/bunn-advantage" class="block py-3 md:py-4 px-6 font-sans-demi leading-none text-black border-b border-gray-200 md:border-0">The BUNN Advantage</a>
				

				
				
				
			
		</div>
	</div>
</div>
<div id="regions-menu" class="drawer js-drawer drawer--left z-modal lg:py-4" data-modal>

	<div class="fixed bg-white w-full h-16 top-0 z-shell flex justify-between items-center border-b border-gray-200">
		<div class="font-sans-medium leading-none flex-grow pl-6 font-sans-demi">Catalog Region</div>
		<button class="js-drawer-close-btn self-stretch h-16 px-6 flex items-center cursor-pointer z-shell text-lg-1" aria-label="Close"><i class="fal fa-times"></i></button>
	</div>


	<!-- TODO: These country and region values need to be moved into the database. Also, in some cases we are fudging -->
	<!-- country or region to manipulate products for agency. We need to keep the data pristine and figure out a business -->
	<!-- process or additional data elements to sort/filter the products as needed. -->

	<div class="absolute inset-0 overflow-y-scroll scrolling-touch pt-16">
		<div class="js-accordion text-base">
			<div class="js-accordion-item border-b border-gray-200 group">
				<div class="accordion__title js-accordion-title font-sans-demi cursor-pointer flex items-center py-3">
					<div class="flex-grow pl-6 font-sans-demi group-active:text-brand-primary">North America</div>
					<div class="js-accordion-icon text-center flex items-center text-lg-1 mr-6" data-inactive-icon="fa-angle-down" data-active-icon="fa-angle-up"><i class="fal fa-angle-down"></i></div>
				</div>
				<div class="hidden js-accordion-content pb-4">
					<ul class="mb-0">
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="US" data-region="NA" data-selected-region="North America - US">United States</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="CA" data-region="NA" data-selected-region="North America - Canada">Canada</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="MX" data-region="NA" data-selected-region="North America - Mexico">Mexico</a></li>
					</ul>
				</div>
			</div>
			<div class="js-accordion-item border-b border-gray-200 group">
				<div class="accordion__title js-accordion-title font-sans-demi cursor-pointer flex items-center py-3">
					<div class="flex-grow pl-6 font-sans-demi group-active:text-brand-primary">Middle East</div>
					<div class="js-accordion-icon text-center flex items-center text-lg-1 mr-6" data-inactive-icon="fa-angle-down" data-active-icon="fa-angle-up"><i class="fal fa-angle-down"></i></div>
				</div>
				<div class="hidden js-accordion-content pb-4">
					<ul class="mb-0">
						<li><a href="/" class="js-set-region block py-2 px-6 text-sm-2 uppercase tracking-wide font-sans-medium text-gray-600 hover:text-brand-primary" data-country="KW-SA-AE" data-region="CE-ME" data-selected-region="Middle East">Browse All <i class="fal fa-angle-right ml-1"></i></a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="AF" data-region="CE" data-selected-region="Middle East - Afghanistan">Afghanistan</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="BH" data-region="CE-ME" data-selected-region="Middle East - Bahrain">Bahrain</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="CY" data-region="CE" data-selected-region="Middle East - Cyprus">Cyprus</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="EG" data-region="CE-ME" data-selected-region="Middle East - Egypt">Egypt</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="IL" data-region="CE" data-selected-region="Middle East - Israel">Israel</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="IQ" data-region="CE-ME" data-selected-region="Middle East - Iraq">Iraq</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="JO" data-region="CE-ME" data-selected-region="Middle East - Jordan">Jordan</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="KW" data-region="" data-selected-region="Middle East - Kuwait">Kuwait</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="LB" data-region="CE-ME" data-selected-region="Middle East - Lebanon">Lebanon</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="OM" data-region="CE-ME" data-selected-region="Middle East - Oman">Oman</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="QA" data-region="CE-ME" data-selected-region="Middle East - Qatar">Qatar</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="SA" data-region="" data-selected-region="Middle East - Saudi Arabia">Saudi Arabia</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="TR" data-region="CE" data-selected-region="Middle East - Turkey">Turkey</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="AE" data-region="" data-selected-region="Middle East - UAE">United Arab Emirates</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="YE" data-region="CE-ME" data-selected-region="Middle East - Yemen">Yemen</a></li>
					</ul>
				</div>
			</div>
			<div class="js-accordion-item border-b border-gray-200 group">
				<div class="accordion__title js-accordion-title font-sans-demi cursor-pointer flex items-center py-3">
					<div class="flex-grow pl-6 font-sans-demi group-active:text-brand-primary">Central America</div>
					<div class="js-accordion-icon text-center flex items-center text-lg-1 mr-6" data-inactive-icon="fa-angle-down" data-active-icon="fa-angle-up"><i class="fal fa-angle-down"></i></div>
				</div>
				<div class="hidden js-accordion-content pb-4">
					<ul class="mb-0">
						<li><a href="/" class="js-set-region block py-2 px-6 text-sm-2 uppercase tracking-wide font-sans-medium text-gray-600 hover:text-brand-primary" data-country="" data-region="LA12" data-selected-region="Central America">Browse All <i class="fal fa-angle-right ml-1"></i></a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="BZ" data-region="LA12" data-selected-region="Central America - Belize">Belize</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="CR" data-region="LA12" data-selected-region="Central America - Costa Rica">Costa Rica</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="SV" data-region="LA12" data-selected-region="Central America - El Salvador">El Salvador</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="GT" data-region="LA12" data-selected-region="Central America - Guatemala">Guatemala</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="HN" data-region="LA12" data-selected-region="Central America - Honduras">Honduras</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="NI" data-region="LA12" data-selected-region="Central America - Nicaragua">Nicaragua</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="PA" data-region="LA12" data-selected-region="Central America - Panama">Panama</a></li>
					</ul>
				</div>
			</div>
			<div class="js-accordion-item border-b border-gray-200 group">
				<div class="accordion__title js-accordion-title font-sans-demi cursor-pointer flex items-center py-3">
					<div class="flex-grow pl-6 font-sans-demi group-active:text-brand-primary">Caribbean</div>
					<div class="js-accordion-icon text-center flex items-center text-lg-1 mr-6" data-inactive-icon="fa-angle-down" data-active-icon="fa-angle-up"><i class="fal fa-angle-down"></i></div>
				</div>
				<div class="hidden js-accordion-content pb-4">
					<ul class="mb-0">
						<li><a href="/" class="js-set-region block py-2 px-6 text-sm-2 uppercase tracking-wide font-sans-medium text-gray-600 hover:text-brand-primary" data-country="" data-region="LA12-LA23" data-selected-region="Caribbean">Browse All <i class="fal fa-angle-right ml-1"></i></a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="VI" data-region="LA12" data-selected-region="Caribbean - American Virgin Islands">American Virgin Islands</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="AG" data-region="LA23" data-selected-region="Caribbean - Antigua and Barbuda">Antigua and Barbuda</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="AW" data-region="LA12" data-selected-region="Caribbean - Aruba">Aruba</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="BS" data-region="LA12" data-selected-region="Caribbean - Bahamas">Bahamas</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="BB" data-region="LA12" data-selected-region="Caribbean - Barbados">Barbados</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="BM" data-region="LA12" data-selected-region="Caribbean - Bermuda">Bermuda</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="VG" data-region="LA12" data-selected-region="Caribbean - British Virgin Islands">British Virgin Islands</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="KY" data-region="LA12" data-selected-region="Caribbean - Cayman Islands">Cayman Islands</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="CW" data-region="LA12-LA23" data-selected-region="Caribbean - Curacao">Curacao</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="DM" data-region="LA23" data-selected-region="Caribbean - Dominica">Dominica</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="DO" data-region="LA12" data-selected-region="Caribbean - Dominican Republic">Dominican Republic</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="AN" data-region="LA23" data-selected-region="Caribbean - Dutch Antilles">Dutch Antilles</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="GD" data-region="LA23" data-selected-region="Caribbean - Grenada">Grenada</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="GP" data-region="LA23" data-selected-region="Caribbean - Guadeloupe">Guadeloupe</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="HT" data-region="LA12" data-selected-region="Caribbean - Haiti">Haiti</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="JM" data-region="LA12" data-selected-region="Caribbean - Jamaica">Jamaica</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="KN" data-region="LA23" data-selected-region="Caribbean - Saint Kitts and Nevis">Saint Kitts and Nevis</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="LC" data-region="LA23" data-selected-region="Caribbean - St. Lucia">St. Lucia</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="MQ" data-region="LA23" data-selected-region="Caribbean - Martinique">Martinique</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="PR" data-region="LA12" data-selected-region="Caribbean - Puerto Rico">Puerto Rico</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="SX" data-region="LA12-LA23" data-selected-region="Caribbean - Sint Maarten">Sint Maarten</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="TT" data-region="LA12" data-selected-region="Caribbean - Trinidad and Tobago">Trinidad and Tobago</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="TC" data-region="LA12" data-selected-region="Caribbean - Turks and Caicos Islands">Turks and Caicos Islands</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="VC" data-region="LA12-LA23" data-selected-region="Caribbean - St. Vincent and the Grenadines">St. Vincent and the Grenadines</a></li>
					</ul>
				</div>
			</div>
			<div class="js-accordion-item border-b border-gray-200 group">
				<div class="accordion__title js-accordion-title font-sans-demi cursor-pointer flex items-center py-3">
					<div class="flex-grow pl-6 font-sans-demi group-active:text-brand-primary">South America</div>
					<div class="js-accordion-icon text-center flex items-center text-lg-1 mr-6" data-inactive-icon="fa-angle-down" data-active-icon="fa-angle-up"><i class="fal fa-angle-down"></i></div>
				</div>
				<div class="hidden js-accordion-content pb-4">
					<ul class="mb-0">
						<li><a href="/" class="js-set-region block py-2 px-6 text-sm-2 uppercase tracking-wide font-sans-medium text-gray-600 hover:text-brand-primary" data-country="AR-BR" data-region="LA12-LA23" data-selected-region="South America">Browse All <i class="fal fa-angle-right ml-1"></i></a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="AR" data-region="" data-selected-region="South America - Argentina">Argentina</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="BO" data-region="LA23" data-selected-region="South America - Bolivia">Bolivia</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="BR" data-region="" data-selected-region="South America - Brazil">Brazil</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="CL" data-region="LA23" data-selected-region="South America - Chile">Chile</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="CO" data-region="LA12" data-selected-region="South America - Colombia">Colombia</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="EC" data-region="LA12" data-selected-region="South America - Ecuador">Ecuador</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="GF" data-region="LA12" data-selected-region="South America - French Guyana">French Guyana</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="GY" data-region="LA12-LA23" data-selected-region="South America - Guyana">Guyana</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="PY" data-region="LA23" data-selected-region="South America - Paraguay">Paraguay</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="PE" data-region="LA23" data-selected-region="South America - Peru">Peru</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="SR" data-region="LA12-LA23" data-selected-region="South America - Suriname">Suriname</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="UY" data-region="LA23" data-selected-region="South America - Uruguay">Uruguay</a></li>
						<li><a href="/" class="js-set-region block py-1 px-6 text-black hover:text-brand-primary" data-country="VE" data-region="LA12" data-selected-region="South America - Venezuela">Venezuela</a></li>
					</ul>
				</div>
			</div>
			<div class="js-accordion-item border-b border-gray-200 group">
				<div class="accordion__title js-accordion-title font-sans-demi cursor-pointer flex items-center py-3">
					<div class="flex-grow pl-6 font-sans-demi group-active:text-brand-primary">Asia</div>
					<div class="js-accordion-icon text-center flex items-center text-lg-1 mr-6" data-inactive-icon="fa-angle-down" data-active-icon="fa-angle-up"><i class="fal fa-angle-down"></i></div>
				</div>
				<div class="hidden js-accordion-content pb-4">
					<ul class="mb-0">
						<li><a href="/" class="js-set-region block py-2 px-6 text-sm-2 uppercase tracking-wide font-sans-medium text-gray-600 hover:text-brand-primary" data-country="CN-JP-KR-TW" data-region="CE" data-selected-region="Asia">Browse All <i class="fal fa-angle-right ml-1"></i></a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="BD" data-region="CE" data-selected-region="Asia - Bangladesh">Bangladesh</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="BN" data-region="CE" data-selected-region="Asia - Brunei Darussalam">Brunei Darussalam</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="BT" data-region="CE" data-selected-region="Asia - Bhutan">Bhutan</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="CN" data-region="" data-selected-region="Asia - China">China</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="HK" data-region="CE" data-selected-region="Asia - Hong Kong">Hong Kong</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="ID" data-region="CE" data-selected-region="Asia - Indonesia">Indonesia</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="IN" data-region="CE" data-selected-region="Asia - India">India</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="JP" data-region="" data-selected-region="Asia - Japan">Japan</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="KG" data-region="CE" data-selected-region="Asia - Kyrgyzstan">Kyrgyzstan</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="KH" data-region="CE" data-selected-region="Asia - Cambodia">Cambodia</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="KR" data-region="" data-selected-region="Asia - South Korea">South Korea</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="LA" data-region="CE" data-selected-region="Asia - Laos">Laos</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="LK" data-region="CE" data-selected-region="Asia - Sri Lanka">Sri Lanka</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="MN" data-region="CE" data-selected-region="Asia - Mongolia">Mongolia</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="MM" data-region="CE" data-selected-region="Asia - Myanmar">Myanmar</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="MV" data-region="CE" data-selected-region="Asia - Maldives">Maldives</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="MY" data-region="CE" data-selected-region="Asia - Malaysia">Malaysia</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="NP" data-region="CE" data-selected-region="Asia - Nepal">Nepal</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="PH" data-region="CE" data-selected-region="Asia - Philippines">Philippines</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="PK" data-region="CE" data-selected-region="Asia - Pakistan">Pakistan</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="PS" data-region="CE" data-selected-region="Asia - Palestine">Palestine</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="SG" data-region="CE" data-selected-region="Asia - Singapore">Singapore</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="TH" data-region="CE" data-selected-region="Asia - Thailand">Thailand</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="TJ" data-region="CE" data-selected-region="Asia - Tajikistan">Tajikistan</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="TL" data-region="CE" data-selected-region="Asia - East Timor">East Timor</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="TM" data-region="CE" data-selected-region="Asia - Turkmenistan">Turkmenistan</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="TW" data-region="" data-selected-region="Asia - Taiwan">Taiwan</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="UZ" data-region="CE" data-selected-region="Asia - Uzbekistan">Uzbekistan</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="VN" data-region="CE" data-selected-region="Asia - Vietnam">Vietnam</a></li>
					</ul>
				</div>
			</div>
			<div class="js-accordion-item border-b border-gray-200 group">
				<div class="accordion__title js-accordion-title font-sans-demi cursor-pointer flex items-center py-3">
					<div class="flex-grow pl-6 font-sans-demi group-active:text-brand-primary">Africa</div>
					<div class="js-accordion-icon text-center flex items-center text-lg-1 mr-6" data-inactive-icon="fa-angle-down" data-active-icon="fa-angle-up"><i class="fal fa-angle-down"></i></div>
				</div>
				<div class="hidden js-accordion-content pb-4">
					<ul class="mb-0">
						<li><a href="/" class="js-set-region block py-2 px-6 text-sm-2 uppercase tracking-wide font-sans-medium text-gray-600 hover:text-brand-primary" data-country="ZA" data-region="CE" data-selected-region="Africa">Browse All <i class="fal fa-angle-right ml-1"></i></a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="AO" data-region="CE" data-selected-region="Africa - Angola">Angola</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="BF" data-region="CE" data-selected-region="Africa - Burkina Faso">Burkina Faso</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="BI" data-region="CE" data-selected-region="Africa - Burundi">Burundi</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="BJ" data-region="CE" data-selected-region="Africa - Benin">Benin</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="BW" data-region="CE" data-selected-region="Africa - Botswana">Botswana</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="CD" data-region="CE" data-selected-region="Africa - Democratic Republic of the Congo">Democratic Republic of the Congo</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="CF" data-region="CE" data-selected-region="Africa - Central African Republic">Central African Republic</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="CG" data-region="CE" data-selected-region="Africa - Republic of the Congo">Republic of the Congo</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="CI" data-region="CE" data-selected-region="Africa - Cote d'Ivoire">Cote d'Ivoire</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="CM" data-region="CE" data-selected-region="Africa - Cameroon">Cameroon</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="CV" data-region="CE" data-selected-region="Africa - Cape Verde">Cape Verde</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="DJ" data-region="CE" data-selected-region="Africa - Djibouti">Djibouti</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="DZ" data-region="CE" data-selected-region="Africa - Algeria">Algeria</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="ER" data-region="CE" data-selected-region="Africa - Eritrea">Eritrea</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="ET" data-region="CE" data-selected-region="Africa - Ethiopia">Ethiopia</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="GA" data-region="CE" data-selected-region="Africa - Gabon">Gabon</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="GH" data-region="CE" data-selected-region="Africa - Ghana">Ghana</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="GM" data-region="CE" data-selected-region="Africa - Gambia">Gambia</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="GN" data-region="CE" data-selected-region="Africa - Guinea">Guinea</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="GQ" data-region="CE" data-selected-region="Africa - Equatorial Guinea">Equatorial Guinea</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="GW" data-region="CE" data-selected-region="Africa - Guinea-Bissau">Guinea-Bissau</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="KE" data-region="CE" data-selected-region="Africa - Kenya">Kenya</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="KM" data-region="CE" data-selected-region="Africa - Comoros">Comoros</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="LR" data-region="CE" data-selected-region="Africa - Liberia">Liberia</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="LS" data-region="CE" data-selected-region="Africa - Lesotho">Lesotho</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="LY" data-region="CE" data-selected-region="Africa - Libya">Libya</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="MA" data-region="CE" data-selected-region="Africa - Morocco">Morocco</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="ML" data-region="CE" data-selected-region="Africa - Mali">Mali</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="MG" data-region="CE" data-selected-region="Africa - Madagascar">Madagascar</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="MR" data-region="CE" data-selected-region="Africa - Mauretania">Mauretania</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="MU" data-region="CE" data-selected-region="Africa - Mauritius">Mauritius</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="MW" data-region="CE" data-selected-region="Africa - Malawi">Malawi</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="MZ" data-region="CE" data-selected-region="Africa - Mozambique">Mozambique</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="NA" data-region="CE" data-selected-region="Africa - Namibia">Namibia</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="NE" data-region="CE" data-selected-region="Africa - Niger">Niger</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="NG" data-region="CE" data-selected-region="Africa - Nigeria">Nigeria</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="RE" data-region="CE" data-selected-region="Africa - Reunion">Reunion</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="RW" data-region="CE" data-selected-region="Africa - Rwanda">Rwanda</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="SC" data-region="CE" data-selected-region="Africa - Seychelles">Seychelles</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="SL" data-region="CE" data-selected-region="Africa - Sierra Leone">Sierra Leone</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="SN" data-region="CE" data-selected-region="Africa - Senegal">Senegal</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="SO" data-region="CE" data-selected-region="Africa - Somalia">Somalia</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="ST" data-region="CE" data-selected-region="Africa - Sao Tome and Principe">Sao Tome and Principe</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="SZ" data-region="CE" data-selected-region="Africa - Swaziland">Swaziland</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="TD" data-region="CE" data-selected-region="Africa - Chad">Chad</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="TG" data-region="CE" data-selected-region="Africa - Togo">Togo</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="TN" data-region="CE" data-selected-region="Africa - Tunisia">Tunisia</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="TZ" data-region="CE" data-selected-region="Africa - Tanzania">Tanzania</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="UG" data-region="CE" data-selected-region="Africa - Uganda">Uganda</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="YT" data-region="CE" data-selected-region="Africa - Mayotte">Mayotte</a></li>
						<li><a href="/"  class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="ZA" data-region="CE" data-selected-region="Africa - South Africa">South Africa</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="ZM" data-region="CE" data-selected-region="Africa - Zambia">Zambia</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="ZW" data-region="CE" data-selected-region="Africa - Zimbabwe">Zimbabwe</a></li>
					</ul>
				</div>
			</div>
			<div class="js-accordion-item border-b border-gray-200 group">
				<div class="accordion__title js-accordion-title font-sans-demi cursor-pointer flex items-center py-3">
					<div class="flex-grow pl-6 font-sans-demi group-active:text-brand-primary">Europe</div>
					<div class="js-accordion-icon text-center flex items-center text-lg-1 mr-6" data-inactive-icon="fa-angle-down" data-active-icon="fa-angle-up"><i class="fal fa-angle-down"></i></div>
				</div>
				<div class="hidden js-accordion-content pb-4">
					<ul class="mb-0">
						<li><a href="/" class="js-set-region block py-2 px-6 text-sm-2 uppercase tracking-wide font-sans-medium text-gray-600 hover:text-brand-primary" data-country="RU-GB" data-region="CE" data-selected-region="Europe">Browse All <i class="fal fa-angle-right ml-1"></i></a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="AD" data-region="CE" data-selected-region="Europe - Andorra">Andorra</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="AL" data-region="CE" data-selected-region="Europe - Albania">Albania</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="RU" data-region="" data-selected-region="Europe - Armenia">Armenia</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="AT" data-region="CE" data-selected-region="Europe - Austria">Austria</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="AZ" data-region="CE" data-selected-region="Europe - Azerbaijan">Azerbaijan</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="RU" data-region="" data-selected-region="Europe - Belarus">Belarus</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="BE" data-region="CE" data-selected-region="Europe - Belgium">Belgium</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="BA" data-region="CE" data-selected-region="Europe - Bosnia and Herzegovina">Bosnia and Herzegovina</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="BG" data-region="CE" data-selected-region="Europe - Bulgaria">Bulgaria</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="HR" data-region="CE" data-selected-region="Europe - Croatia">Croatia</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="CZ" data-region="CE" data-selected-region="Europe - Czech Republic">Czech Republic</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="DK" data-region="CE" data-selected-region="Europe - Denmark">Denmark</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="EE" data-region="CE" data-selected-region="Europe - Estonia">Estonia</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="FI" data-region="CE" data-selected-region="Europe - Finland">Finland</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="FR" data-region="CE" data-selected-region="Europe - France">France</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="GE" data-region="CE" data-selected-region="Europe - Georgia">Georgia</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="DE" data-region="CE" data-selected-region="Europe - Germany">Germany</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="GR" data-region="CE" data-selected-region="Europe - Greece">Greece</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="HU" data-region="CE" data-selected-region="Europe - Hungary">Hungary</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="IS" data-region="CE" data-selected-region="Europe - Iceland">Iceland</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="IE" data-region="CE" data-selected-region="Europe - Ireland">Ireland</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="IT" data-region="CE" data-selected-region="Europe - Italy">Italy</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="RU" data-region="" data-selected-region="Europe - Kazakhstan">Kazakhstan</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="LV" data-region="CE" data-selected-region="Europe - Latvia">Latvia</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="LI" data-region="CE" data-selected-region="Europe - Liechtenstein">Liechtenstein</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="LT" data-region="CE" data-selected-region="Europe - Lithuania">Lithuania</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="LU" data-region="CE" data-selected-region="Europe - Luxembourg">Luxembourg</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="MC" data-region="CE" data-selected-region="Europe - Monaco">Monaco</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="MD" data-region="CE" data-selected-region="Europe - Moldova">Moldova</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="MK" data-region="CE" data-selected-region="Europe - Macedonia">Macedonia</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="MT" data-region="CE" data-selected-region="Europe - Malta">Malta</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="NL" data-region="CE" data-selected-region="Europe - Netherlands">Netherlands</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="NO" data-region="CE" data-selected-region="Europe - Norway">Norway</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="PL" data-region="CE" data-selected-region="Europe - Poland">Poland</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="PT" data-region="CE" data-selected-region="Europe - Portugal">Portugal</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="RO" data-region="CE" data-selected-region="Europe - Romania">Romania</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="RU" data-region="" data-selected-region="Europe - Russia">Russia</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="SM" data-region="CE" data-selected-region="Europe - San Marino">San Marino</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="RS" data-region="CE" data-selected-region="Europe - Serbia">Serbia</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="SK" data-region="CE" data-selected-region="Europe - Slovakia">Slovakia</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="SI" data-region="CE" data-selected-region="Europe - Slovenia">Slovenia</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="ES" data-region="CE" data-selected-region="Europe - Spain">Spain</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="SE" data-region="CE" data-selected-region="Europe - Sweden">Sweden</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="CH" data-region="CE" data-selected-region="Europe - Switzerland">Switzerland</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="UA" data-region="CE" data-selected-region="Europe - Ukraine">Ukraine</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="GB" data-region="CE" data-selected-region="Europe - United Kingdom">United Kingdom</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="VA" data-region="CE" data-selected-region="Europe - Vatican City">Vatican City</a></li>
					</ul>
				</div>
			</div>
			<div class="js-accordion-item border-b border-gray-200 group">
				<div class="accordion__title js-accordion-title font-sans-demi cursor-pointer flex items-center py-3">
					<div class="flex-grow pl-6 font-sans-demi group-active:text-brand-primary">Pacific</div>
					<div class="js-accordion-icon text-center flex items-center text-lg-1 mr-6" data-inactive-icon="fa-angle-down" data-active-icon="fa-angle-up"><i class="fal fa-angle-down"></i></div>
				</div>
				<div class="hidden js-accordion-content pb-4">
					<ul class="mb-0">
						<li><a href="/" class="js-set-region block py-2 px-6 text-sm-2 uppercase tracking-wide font-sans-medium text-gray-600 hover:text-brand-primary" data-country="AU-US" data-region="CE" data-selected-region="Pacific">Browse All <i class="fal fa-angle-right ml-1"></i></a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="AU" data-region="" data-selected-region="Pacific - Australia">Australia</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="FJ" data-region="CE" data-selected-region="Pacific - Fiji">Fiji</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="US" data-region="" data-selected-region="Pacific - Guam">Guam</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="KI" data-region="CE" data-selected-region="Pacific - Kiribati">Kiribati</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="US" data-region="" data-selected-region="Pacific - Marshall Islands">Marshall Islands</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="US" data-region="" data-selected-region="Pacific - Micronesia">Micronesia</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="NR" data-region="CE" data-selected-region="Pacific - Nauru">Nauru</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="NC" data-region="CE" data-selected-region="Pacific - New Caledonia">New Caledonia</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="AU" data-region="" data-selected-region="Pacific - New Zealand">New Zealand</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="US" data-region="" data-selected-region="Pacific - Palau">Palau</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="PG" data-region="CE" data-selected-region="Pacific - Papua New Guinea">Papua New Guinea</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="US" data-region="" data-selected-region="Pacific - Samoa">Samoa</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="SB" data-region="CE" data-selected-region="Pacific - Solomon Islands">Solomon Islands</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="TO" data-region="CE" data-selected-region="Pacific - Tonga">Tonga</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="TV" data-region="CE" data-selected-region="Pacific - Tuvalu">Tuvalu</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="VU" data-region="CE" data-selected-region="Pacific - Vanuatu">Vanuatu</a></li>
						<li><a href="/" class="js-set-region block py-2 px-6 text-black hover:text-brand-primary" data-country="WF" data-region="CE" data-selected-region="Pacific - Wallis and Futuna Islands">Wallis and Futuna Islands</a></li>
					</ul>
				</div>
			</div>
		</div>
	</div>
</div>


    <div class="modal-overlay js-modal-overlay"></div>

    <!-- <script th:src="@{/js/libs.js}"></script> -->
<!-- <script th:src="@{/js/bunn-design-system.min.js}"></script> -->
<script src="/js/bunn-bundle-562981206.js?themeConfigId=1" type="text/javascript"></script>

<!-- <blc:bundle name="blc-platform.js" -->
<!--             mapping-prefix="/js/" -->
<!--             files="BLC.js, -->
<!--                    blc-dates.js, -->
<!--                    blc-theme.js, -->
<!--                    blc-search.js" /> -->


<!-- <script th:src="@{/js/bunn-commercial.js}"></script> -->

<script src="/widget/js/2?v=123"></script><script src="/widget/js/1351?v=1775002516000"></script>





<script>
  // Environment Variables
  if (environment === "Production") {
    var salesforceChatId = "00DE0000000ZmR2";
    var salesforceName = "Customer_Support";
    var salesforceScript = "https://bunn.my.site.com/ESWCustomerSupport1750701273229";
    var salesforceScrt2URL = "https://bunn.my.salesforce-scrt.com";
  } else {
    var salesforceChatId = "00DTI000004bSHZ";
    var salesforceName = "Chat_Support_QA";
    var salesforceScript = "https://bunn--qa.sandbox.my.site.com/ESWChatSupportQA1752022616707";
    var salesforceScrt2URL = "https://bunn--qa.sandbox.my.salesforce-scrt.com";
  }

  // Salesforce Chat
  function initEmbeddedMessaging() {
    try {
      embeddedservice_bootstrap.settings.language = 'en_US'; // For example, enter 'en' or 'en-US'
      window.addEventListener("onEmbeddedMessagingReady", () => {
        console.log("Inside Prechat API!!");
        embeddedservice_bootstrap.prechatAPI.setHiddenPrechatFields({ "pageUrl": window.location.href });
      });
      embeddedservice_bootstrap.init(
        salesforceChatId,
        salesforceName,
        salesforceScript,
        {
          scrt2URL: salesforceScrt2URL
        }
      );
    } catch (err) {
      console.error('Error loading Embedded Messaging: ', err);
    }
  };
</script>
<script type='text/javascript' src='https://bunn--qa.sandbox.my.site.com/ESWChatSupportQA1752022616707/assets/js/bootstrap.min.js' onload='initEmbeddedMessaging()'></script>

<SCRIPT>
  var params = 
  {"firstName":"","lastName":"","csrfToken":"D79J-EJ7K-SNH9-1D2K-L69G-U72S-7JTP-H9RR","cartItemIdsWithoutOptions":[],"cartItemIdsWithOptions":[],"anonymous":true,"cartItemCount":0,"outOfStockProducts":[],"csrfTokenParameter":"csrfToken","outOfStockSkus":[]};
  updateUncacheableData(params);
</SCRIPT>
</body>

</html>
