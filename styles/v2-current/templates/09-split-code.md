# 09 - Split Layout with Code

Display code examples, API documentation, or technical content alongside explanations.

## Use Cases
- API documentation
- Code examples
- Technical tutorials
- Developer features
- Integration guides
- Configuration examples

## Layout Options

### Option A: Explanation + Code Block

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap');
    @import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500&display=swap');

    * { margin: 0; padding: 0; box-sizing: border-box; }

    body {
      font-family: 'Inter', sans-serif;
      -webkit-font-smoothing: antialiased;
    }

    .slide {
      width: 1920px;
      height: 1080px;
      background: #F8F8FC;
      padding: 64px;
      display: flex;
      gap: 48px;
      position: relative;
    }

    .content {
      width: 550px;
      display: flex;
      flex-direction: column;
      justify-content: center;
    }

    .label {
      font-size: 14px;
      font-weight: 500;
      letter-spacing: 0.5px;
      text-transform: uppercase;
      color: #4469fc;
      margin-bottom: 16px;
    }

    .title {
      font-size: 44px;
      font-weight: 600;
      letter-spacing: -0.88px;
      line-height: 1.15;
      color: #1a1c21;
      margin-bottom: 24px;
    }

    .description {
      font-size: 18px;
      font-weight: 400;
      line-height: 1.6;
      color: rgba(26,28,33,0.55);
      margin-bottom: 32px;
    }

    .features {
      display: flex;
      flex-direction: column;
      gap: 16px;
    }

    .feature-item {
      display: flex;
      align-items: center;
      gap: 12px;
    }

    .feature-icon {
      width: 20px;
      height: 20px;
      color: #22c55e;
    }

    .feature-text {
      font-size: 16px;
      font-weight: 500;
      color: #1a1c21;
    }

    .code-container {
      flex: 1;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .code-block {
      background: #1a1c21;
      border-radius: 16px;
      width: 100%;
      max-width: 800px;
      overflow: hidden;
      box-shadow: 0px 8px 40px rgba(0, 0, 0, 0.2);
    }

    .code-header {
      background: rgba(255,255,255,0.05);
      padding: 16px 24px;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .code-dots {
      display: flex;
      gap: 8px;
    }

    .code-dot {
      width: 12px;
      height: 12px;
      border-radius: 50%;
      background: rgba(255,255,255,0.2);
    }

    .code-lang {
      font-size: 13px;
      font-weight: 500;
      color: rgba(255,255,255,0.5);
    }

    .code-content {
      padding: 24px;
      overflow-x: auto;
    }

    pre {
      font-family: 'JetBrains Mono', monospace;
      font-size: 14px;
      line-height: 1.7;
      color: #FFFFFF;
      margin: 0;
    }

    .comment { color: rgba(255,255,255,0.4); }
    .keyword { color: #c792ea; }
    .string { color: #c3e88d; }
    .function { color: #82aaff; }
    .property { color: #f78c6c; }
    .number { color: #f78c6c; }

    .logo {
      position: absolute;
      bottom: 64px;
      left: 64px;
      height: 24px;
      width: auto;
    }
  </style>
</head>
<body>
  <div class="slide">
    <div class="content">
      <div class="label">API Integration</div>
      <h1 class="title">Simple API for Developers</h1>
      <p class="description">Integrate Langdock into your applications with our REST API. Send messages, manage conversations, and access all models programmatically.</p>

      <div class="features">
        <div class="feature-item">
          <svg class="feature-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <polyline points="20 6 9 17 4 12"/>
          </svg>
          <span class="feature-text">RESTful endpoints</span>
        </div>
        <div class="feature-item">
          <svg class="feature-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <polyline points="20 6 9 17 4 12"/>
          </svg>
          <span class="feature-text">Streaming responses</span>
        </div>
        <div class="feature-item">
          <svg class="feature-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <polyline points="20 6 9 17 4 12"/>
          </svg>
          <span class="feature-text">Comprehensive documentation</span>
        </div>
      </div>
    </div>

    <div class="code-container">
      <div class="code-block">
        <div class="code-header">
          <div class="code-dots">
            <div class="code-dot"></div>
            <div class="code-dot"></div>
            <div class="code-dot"></div>
          </div>
          <span class="code-lang">JavaScript</span>
        </div>
        <div class="code-content">
<pre><span class="comment">// Send a message to Langdock API</span>
<span class="keyword">const</span> response = <span class="keyword">await</span> <span class="function">fetch</span>(<span class="string">'https://api.langdock.com/v1/chat'</span>, {
  <span class="property">method</span>: <span class="string">'POST'</span>,
  <span class="property">headers</span>: {
    <span class="string">'Authorization'</span>: <span class="string">`Bearer ${API_KEY}`</span>,
    <span class="string">'Content-Type'</span>: <span class="string">'application/json'</span>
  },
  <span class="property">body</span>: <span class="function">JSON.stringify</span>({
    <span class="property">model</span>: <span class="string">'gpt-4'</span>,
    <span class="property">messages</span>: [
      { <span class="property">role</span>: <span class="string">'user'</span>, <span class="property">content</span>: <span class="string">'Hello!'</span> }
    ]
  })
});

<span class="keyword">const</span> data = <span class="keyword">await</span> response.<span class="function">json</span>();
<span class="function">console.log</span>(data.<span class="property">message</span>);</pre>
        </div>
      </div>
    </div>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
  </div>
</body>
</html>
```

### Option B: Full-Width Code with Title

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap');
    @import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500&display=swap');

    * { margin: 0; padding: 0; box-sizing: border-box; }

    body {
      font-family: 'Inter', sans-serif;
      -webkit-font-smoothing: antialiased;
    }

    .slide {
      width: 1920px;
      height: 1080px;
      background: #F8F8FC;
      padding: 64px;
      display: flex;
      flex-direction: column;
      position: relative;
    }

    .header {
      display: flex;
      align-items: flex-start;
      justify-content: space-between;
      margin-bottom: 40px;
    }

    .header-content {
      max-width: 800px;
    }

    .label {
      font-size: 14px;
      font-weight: 500;
      letter-spacing: 0.5px;
      text-transform: uppercase;
      color: #4469fc;
      margin-bottom: 12px;
    }

    .title {
      font-size: 40px;
      font-weight: 600;
      letter-spacing: -0.8px;
      color: #1a1c21;
    }

    .language-badge {
      background: #ECECF4;
      padding: 8px 16px;
      border-radius: 100px;
      font-size: 14px;
      font-weight: 500;
      color: rgba(26,28,33,0.6);
    }

    .code-block {
      background: #1a1c21;
      border-radius: 16px;
      flex: 1;
      overflow: hidden;
      display: flex;
      flex-direction: column;
    }

    .code-header {
      background: rgba(255,255,255,0.05);
      padding: 16px 24px;
      display: flex;
      align-items: center;
      gap: 16px;
    }

    .code-dots {
      display: flex;
      gap: 8px;
    }

    .code-dot {
      width: 12px;
      height: 12px;
      border-radius: 50%;
      background: rgba(255,255,255,0.2);
    }

    .code-filename {
      font-size: 14px;
      font-weight: 500;
      color: rgba(255,255,255,0.6);
    }

    .code-content {
      padding: 32px;
      overflow: auto;
      flex: 1;
    }

    pre {
      font-family: 'JetBrains Mono', monospace;
      font-size: 15px;
      line-height: 1.8;
      color: #FFFFFF;
      margin: 0;
    }

    .comment { color: rgba(255,255,255,0.4); }
    .keyword { color: #c792ea; }
    .string { color: #c3e88d; }
    .function { color: #82aaff; }
    .property { color: #f78c6c; }

    .logo {
      position: absolute;
      bottom: 64px;
      left: 64px;
      height: 24px;
      width: auto;
    }
  </style>
</head>
<body>
  <div class="slide">
    <div class="header">
      <div class="header-content">
        <div class="label">Configuration</div>
        <h1 class="title">Assistant Configuration Example</h1>
      </div>
      <div class="language-badge">JSON</div>
    </div>

    <div class="code-block">
      <div class="code-header">
        <div class="code-dots">
          <div class="code-dot"></div>
          <div class="code-dot"></div>
          <div class="code-dot"></div>
        </div>
        <span class="code-filename">assistant-config.json</span>
      </div>
      <div class="code-content">
<pre>{
  <span class="property">"name"</span>: <span class="string">"Customer Support Assistant"</span>,
  <span class="property">"model"</span>: <span class="string">"gpt-4"</span>,
  <span class="property">"temperature"</span>: <span class="number">0.7</span>,
  <span class="property">"instructions"</span>: <span class="string">"You are a helpful customer support agent..."</span>,
  <span class="property">"knowledge_sources"</span>: [
    {
      <span class="property">"type"</span>: <span class="string">"confluence"</span>,
      <span class="property">"space"</span>: <span class="string">"SUPPORT"</span>
    },
    {
      <span class="property">"type"</span>: <span class="string">"notion"</span>,
      <span class="property">"database_id"</span>: <span class="string">"abc123"</span>
    }
  ],
  <span class="property">"capabilities"</span>: [<span class="string">"web_search"</span>, <span class="string">"file_upload"</span>]
}</pre>
      </div>
    </div>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
  </div>
</body>
</html>
```

## Syntax Highlighting Colors

```css
/* Dark theme (recommended) */
.comment { color: rgba(255,255,255,0.4); }
.keyword { color: #c792ea; }      /* purple */
.string { color: #c3e88d; }       /* green */
.function { color: #82aaff; }     /* blue */
.property { color: #f78c6c; }     /* orange */
.number { color: #f78c6c; }       /* orange */
.type { color: #ffcb6b; }         /* yellow */
```

## Code Font

Use `JetBrains Mono` for code:
```css
font-family: 'JetBrains Mono', 'Fira Code', 'Monaco', monospace;
font-size: 14-16px;
line-height: 1.7-1.8;
```

## Supported Languages

Common languages to show:
- JavaScript/TypeScript
- Python
- JSON
- cURL
- Bash/Shell
