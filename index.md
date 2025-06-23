<html>
  <body>
<script type='text/javascript'>
	function initEmbeddedMessaging() {
		try {
			embeddedservice_bootstrap.settings.language = 'en_US'; // For example, enter 'en' or 'en-US'

			embeddedservice_bootstrap.init(
				'00DVE000000QejN',
				'Customer_Support',
				'https://bunn--qa.sandbox.my.site.com/ESWCustomerSupport1740757143988',
				{
					scrt2URL: 'https://bunn--qa.sandbox.my.salesforce-scrt.com'
				}
			);
		} catch (err) {
			console.error('Error loading Embedded Messaging: ', err);
		}
	};
</script>
<script type='text/javascript' src='https://bunn--qa.sandbox.my.site.com/ESWCustomerSupport1740757143988/assets/js/bootstrap.min.js' onload='initEmbeddedMessaging()'></script>
</body>
</html>
