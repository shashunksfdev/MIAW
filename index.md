<html> 
<body>

<script type='text/javascript'>
	function initEmbeddedMessaging() {
		try {
			embeddedservice_bootstrap.settings.language = 'en_US'; // For example, enter 'en' or 'en-US'

			embeddedservice_bootstrap.init(
				'00DVD00000E9E5J',
				'Chat_Support_QA',
				'https://bunn--qa.sandbox.my.site.com/ESWChatSupportQA178093760822',
				{
					scrt2URL: 'https://bunn--qa.sandbox.my.salesforce-scrt.com'
				}
			);
		} catch (err) {
			console.error('Error loading Embedded Messaging: ', err);
		}
	};
</script>
<script type='text/javascript' src='https://bunn--qa.sandbox.my.site.com/ESWChatSupportQA1780937608226/assets/js/bootstrap.min.js' onload='initEmbeddedMessaging()'></script>
</body>
</html>
