<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Bunn — Chat Test Page</title>
  <link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet"/>
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
    :root {
      --bg: #0f1117; --surface: #181c27; --border: #262c3e;
      --accent: #4f8ef7; --accent-dim: rgba(79,142,247,0.12);
      --green: #3ecf8e; --green-dim: rgba(62,207,142,0.12);
      --red: #f56565; --yellow: #f5a623;
      --text-primary: #e8ecf4; --text-secondary: #8891a8; --text-muted: #4a5166;
      --font: 'DM Sans', sans-serif; --mono: 'DM Mono', monospace;
    }
    body { font-family: var(--font); background: var(--bg); color: var(--text-primary); min-height: 100vh; display: flex; flex-direction: column; }
    header { border-bottom: 1px solid var(--border); padding: 0 2rem; height: 60px; display: flex; align-items: center; justify-content: space-between; position: sticky; top: 0; background: rgba(15,17,23,0.92); backdrop-filter: blur(10px); z-index: 100; }
    .logo { font-size: 1rem; font-weight: 600; letter-spacing: 0.08em; text-transform: uppercase; }
    .env-badge { font-family: var(--mono); font-size: 0.7rem; padding: 3px 10px; border-radius: 4px; font-weight: 500; letter-spacing: 0.04em; text-transform: uppercase; background: var(--green-dim); color: var(--green); border: 1px solid rgba(62,207,142,0.25); }
    main { flex: 1; max-width: 860px; width: 100%; margin: 0 auto; padding: 3rem 2rem; }
    h1 { font-size: 1.6rem; font-weight: 600; margin-bottom: 0.4rem; }
    .subtitle { color: var(--text-secondary); font-size: 0.9rem; margin-bottom: 2.5rem; }
    .card { background: var(--surface); border: 1px solid var(--border); border-radius: 10px; padding: 1.5rem; margin-bottom: 1.25rem; }
    .card-title { font-size: 0.75rem; font-weight: 600; letter-spacing: 0.08em; text-transform: uppercase; color: var(--text-muted); margin-bottom: 1rem; }
    .config-grid { display: grid; gap: 0.6rem; }
    .config-row { display: grid; grid-template-columns: 160px 1fr; gap: 1rem; align-items: start; }
    .config-key { color: var(--text-secondary); font-family: var(--mono); font-size: 0.78rem; padding-top: 2px; }
    .config-val { font-family: var(--mono); font-size: 0.78rem; color: var(--accent); word-break: break-all; background: var(--accent-dim); padding: 3px 8px; border-radius: 4px; border: 1px solid rgba(79,142,247,0.15); }
    .status-row { display: flex; align-items: center; gap: 0.6rem; font-size: 0.85rem; margin-bottom: 0.6rem; }
    .dot { width: 8px; height: 8px; border-radius: 50%; flex-shrink: 0; }
    .dot.green  { background: var(--green);  box-shadow: 0 0 6px var(--green);  animation: pulse 2s infinite; }
    .dot.red    { background: var(--red);    box-shadow: 0 0 6px var(--red); }
    .dot.yellow { background: var(--yellow); box-shadow: 0 0 6px var(--yellow); animation: pulse 2s infinite; }
    @keyframes pulse { 0%,100%{opacity:1} 50%{opacity:0.4} }
    .status-label { color: var(--text-secondary); }
    .status-value { color: var(--text-primary); font-weight: 500; }
    .console { background: #0a0c11; border: 1px solid var(--border); border-radius: 8px; padding: 1rem; font-family: var(--mono); font-size: 0.75rem; min-height: 140px; max-height: 260px; overflow-y: auto; line-height: 1.7; }
    .log-line { display: flex; gap: 0.75rem; }
    .log-time { color: var(--text-muted); flex-shrink: 0; }
    .log-info    { color: var(--accent); }
    .log-success { color: var(--green); }
    .log-warn    { color: var(--yellow); }
    .log-error   { color: var(--red); }
    footer { border-top: 1px solid var(--border); padding: 1.25rem 2rem; text-align: center; font-size: 0.75rem; color: var(--text-muted); }
  </style>
</head>
<body>

<header>
  <span class="logo">Bunn</span>
  <span class="env-badge">Production</span>
</header>

<main>
  <h1>Salesforce Chat — Test Page</h1>
  <p class="subtitle">Production environment. Verifying chat widget loads and initialises correctly.</p>

  <!-- Active config -->
  <div class="card">
    <div class="card-title">Active Configuration</div>
    <div class="config-grid">
      <div class="config-row">
        <span class="config-key">environment</span>
        <span class="config-val">Production</span>
      </div>
      <div class="config-row">
        <span class="config-key">salesforceChatId</span>
        <span class="config-val">00DE0000000ZmR2</span>
      </div>
      <div class="config-row">
        <span class="config-key">salesforceName</span>
        <span class="config-val">Customer_Support</span>
      </div>
      <div class="config-row">
        <span class="config-key">salesforceScript</span>
        <span class="config-val">https://bunn.my.site.com/ESWCustomerSupport1750701273229</span>
      </div>
      <div class="config-row">
        <span class="config-key">salesforceScrt2URL</span>
        <span class="config-val">https://bunn.my.salesforce-scrt.com</span>
      </div>
    </div>
  </div>

  <!-- Status -->
  <div class="card">
    <div class="card-title">Bootstrap Script Status</div>
    <div class="status-row">
      <div class="dot yellow" id="scriptDot"></div>
      <span class="status-label">bootstrap.min.js</span>
      <span class="status-value" id="scriptStatus">Loading…</span>
    </div>
    <div class="status-row">
      <div class="dot yellow" id="initDot"></div>
      <span class="status-label">embeddedservice_bootstrap.init()</span>
      <span class="status-value" id="initStatus">Waiting…</span>
    </div>
  </div>

  <!-- Console -->
  <div class="card">
    <div class="card-title">Console Output</div>
    <div class="console" id="consoleLog"></div>
  </div>
</main>

<footer>Salesforce Embedded Messaging — Production Debug Page</footer>

<!-- Production credentials (hardcoded) -->
<script>
  var environment       = "Production";
  var salesforceChatId  = "00DE0000000ZmR2";
  var salesforceName    = "Customer_Support";
  var salesforceScript  = "https://bunn.my.site.com/ESWCustomerSupport1750701273229";
  var salesforceScrt2URL = "https://bunn.my.salesforce-scrt.com";
</script>

<!-- Your original init function, unchanged -->
<script>
  function initEmbeddedMessaging() {
    try {
      embeddedservice_bootstrap.settings.language = 'en_US';
      window.addEventListener("onEmbeddedMessagingReady", () => {
        log("Inside Prechat API — widget ready ✓", "success");
        embeddedservice_bootstrap.prechatAPI.setHiddenPrechatFields({ "pageUrl": window.location.href });
      });
      embeddedservice_bootstrap.init(
        salesforceChatId,
        salesforceName,
        salesforceScript,
        { scrt2URL: salesforceScrt2URL }
      );
      markStatus("initDot", "initStatus", "green", "init() called successfully");
      log("embeddedservice_bootstrap.init() called ✓", "success");
    } catch (err) {
      markStatus("initDot", "initStatus", "red", "Error — " + err.message);
      log("Error in initEmbeddedMessaging(): " + err.message, "error");
      console.error('Error loading Embedded Messaging: ', err);
    }
  }
</script>

<!-- Dynamically load bootstrap.min.js from production script URL -->
<script>
  (function () {
    var src = salesforceScript + "/assets/js/bootstrap.min.js";
    log("Loading bootstrap.min.js from:", "info");
    log(src, "info");
    var s = document.createElement("script");
    s.setAttribute("type", "text/javascript");
    s.setAttribute("src", src);
    s.onload = function () {
      markStatus("scriptDot", "scriptStatus", "green", "Loaded ✓");
      log("bootstrap.min.js loaded successfully ✓", "success");
      initEmbeddedMessaging();
    };
    s.onerror = function () {
      markStatus("scriptDot", "scriptStatus", "red", "Failed to load — 404 or blocked");
      log("FAILED to load bootstrap.min.js", "error");
      log("→ Verify the Experience Site is Active in Setup → Embedded Service Deployments", "warn");
      log("→ Check guest user profile permissions on the Experience Site", "warn");
    };
    document.head.appendChild(s);
  })();
</script>

<!-- UI helpers -->
<script>
  function log(msg, type) {
    var box  = document.getElementById("consoleLog");
    var line = document.createElement("div");
    line.className = "log-line";
    line.innerHTML = '<span class="log-time">' + new Date().toLocaleTimeString() + '</span>'
                   + '<span class="log-' + (type || "info") + '">' + msg + '</span>';
    box.appendChild(line);
    box.scrollTop = box.scrollHeight;
  }
  function markStatus(dotId, labelId, color, text) {
    document.getElementById(dotId).className = "dot " + color;
    document.getElementById(labelId).textContent = text;
  }
  log("Page loaded — environment: Production", "info");
</script>

</body>
</html>
