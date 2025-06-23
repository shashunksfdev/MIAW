<html>
  <body>
<script type='text/javascript'>
	function initEmbeddedMessaging() {
		try {
			embeddedservice_bootstrap.settings.language = 'en_US'; // For example, enter 'en' or 'en-US'
			// ✅ Listen for 'embeddedMessagingReady' message
          window.addEventListener("message", function (event) {
            if (event.data && event.data.type === "embeddedMessagingReady") {
              console.log("Inside Prechat API!!");

              // Set the hidden pre-chat field
              embeddedservice_bootstrap.prechatAPI.setHiddenPrechatFields({
                pageUrl: window.location.href
              });
            }
          });

   				embeddedservice_bootstrap.init(
				'00DVE000000QejN',
				'GitHub_Chat_Support',
				'https://bunn--qa.sandbox.my.site.com/ESWGitHubChatSupport1750717571736',
				{
					scrt2URL: 'https://bunn--qa.sandbox.my.salesforce-scrt.com'
				}
			);
		} catch (err) {
			console.error('Error loading Embedded Messaging: ', err);
		}
	};
</script>
<script type='text/javascript' src='https://bunn--qa.sandbox.my.site.com/ESWGitHubChatSupport1750717571736/assets/js/bootstrap.min.js' onload='initEmbeddedMessaging()'></script>
</body>
</html>
