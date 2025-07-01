<html>
<body>
<script type='text/javascript'>
	function initEmbeddedMessaging() {
		try {
			embeddedservice_bootstrap.settings.language = 'en_US'; // For example, enter 'en' or 'en-US'

			embeddedservice_bootstrap.init(
				'00DE0000000ZmR2',
				'Customer_Chat_Support_Hub',
				'https://bunn.my.site.com/ESWCustomerChatSupport1751329774880',
				{
					scrt2URL: 'https://bunn.my.salesforce-scrt.com'
				}
			);
		} catch (err) {
			console.error('Error loading Embedded Messaging: ', err);
		}
	};
</script>
<script type='text/javascript' src='https://bunn.my.site.com/ESWCustomerChatSupport1751329774880/assets/js/bootstrap.min.js' onload='initEmbeddedMessaging()'></script>
</body>
</html>
