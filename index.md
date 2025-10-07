<html> 
<body>

<script type='text/javascript'>
	function initEmbeddedMessaging() {
		try {
			embeddedservice_bootstrap.settings.language = 'en_US'; // For example, enter 'en' or 'en-US'
window.addEventListener("onEmbeddedMessagingReady", () => { 
	console.log( "Inside Prechat API!!" ); 
	 embeddedservice_bootstrap.prechatAPI.setHiddenPrechatFields( { "pageUrl" : window.location.href } ); 
	
	});
			embeddedservice_bootstrap.init(
				'00DTI000004bSHZ',
				'Chat_Support_QA',
				'https://bunn--qa.sandbox.my.site.com/ESWChatSupportQA1752022616707',
				{
					scrt2URL: 'https://bunn--qa.sandbox.my.salesforce-scrt.com'
				}
			);
		} catch (err) {
			console.error('Error loading Embedded Messaging: ', err);
		}
	};
</script>
<script type='text/javascript' src='https://bunn--qa.sandbox.my.site.com/ESWChatSupportQA1752022616707/assets/js/bootstrap.min.js' onload='initEmbeddedMessaging()'></script>

</body>
</html>
