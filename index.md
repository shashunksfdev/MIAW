<html> 
<body>

<script type='text/javascript'>
	function initEmbeddedMessaging() {
		try {
			embeddedservice_bootstrap.settings.language = 'en_US'; // For example, enter 'en' or 'en-US'

			embeddedservice_bootstrap.init(
				'00DE0000000ZmR2',
				'Customer_Support',
				'https://bunn.my.site.com/ESWCustomerSupport1750701273229',
				{
					scrt2URL: 'https://bunn.my.salesforce-scrt.com'
				}
			);
		} catch (err) {
			console.error('Error loading Embedded Messaging: ', err);
		}
	};
</script>
<script type='text/javascript' src='https://bunn.my.site.com/ESWCustomerSupport1750701273229/assets/js/bootstrap.min.js' onload='initEmbeddedMessaging()'></script>
</body>
</body>html> 
