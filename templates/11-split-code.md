# Split Layout with Code

Left side content/info, right side code example. For developer-focused slides.

## When to Use
- API documentation
- Code examples
- Technical tutorials
- Developer onboarding

## Layout Pattern
- Title at top (128px)
- Left: endpoint info, auth details, key points
- Right: syntax-highlighted code block
- Full height utilization

## Full Template

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=1920, height=1080">
  <title>API Example - Langdock</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
  <link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@tabler/icons-webfont@latest/tabler-icons.min.css">
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      font-family: 'Inter', sans-serif;
      background: #f8f8f9;
      width: 1920px;
      height: 1080px;
      position: relative;
      overflow: hidden;
    }
    .header {
      position: absolute;
      top: 40px;
      left: 64px;
      right: 64px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .breadcrumbs { display: flex; align-items: center; gap: 12px; }
    .footnote { font-size: 18px; font-weight: 500; color: #717279; letter-spacing: -0.36px; }
    .slide-number { font-size: 18px; font-weight: 500; color: #717279; }
    .main-title {
      position: absolute;
      top: 128px;
      left: 64px;
      font-size: 64px;
      font-weight: 600;
      color: #121420;
      letter-spacing: -3.2px;
      line-height: 1.1;
    }
    .split-layout {
      position: absolute;
      top: 260px;
      left: 64px;
      right: 64px;
      bottom: 64px;
      display: grid;
      grid-template-columns: 1fr 1.2fr;
      gap: 48px;
    }
    .left-panel {
      display: flex;
      flex-direction: column;
      gap: 24px;
    }
    .info-section {
      background: #ffffff;
      border-radius: 16px;
      padding: 28px;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.04);
    }
    .info-label {
      font-size: 14px;
      font-weight: 600;
      color: #717279;
      text-transform: uppercase;
      letter-spacing: 0.5px;
      margin-bottom: 8px;
    }
    .info-value {
      font-size: 20px;
      font-weight: 500;
      color: #121420;
      font-family: 'JetBrains Mono', monospace;
    }
    .info-list {
      display: flex;
      flex-direction: column;
      gap: 16px;
    }
    .info-item {
      display: flex;
      align-items: center;
      gap: 12px;
    }
    .info-item-text {
      font-size: 18px;
      color: #121420;
    }
    .right-panel {
      display: flex;
      flex-direction: column;
    }
    .code-block {
      background: #1e1e2e;
      border-radius: 16px;
      overflow: hidden;
      flex: 1;
      display: flex;
      flex-direction: column;
    }
    .code-header {
      background: #2a2a3e;
      padding: 12px 20px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-bottom: 1px solid #3a3a4e;
    }
    .code-language {
      font-family: 'JetBrains Mono', monospace;
      font-size: 13px;
      color: #717279;
      text-transform: uppercase;
    }
    .code-content {
      padding: 24px;
      margin: 0;
      overflow: auto;
      flex: 1;
    }
    .code-content code {
      font-family: 'JetBrains Mono', monospace;
      font-size: 15px;
      color: #e0e0e0;
      line-height: 1.7;
      white-space: pre;
    }
    /* Syntax highlighting */
    .keyword { color: #c678dd; }
    .string { color: #98c379; }
    .comment { color: #5c6370; }
    .function { color: #61afef; }
    .number { color: #d19a66; }
  </style>
</head>
<body>
  <div class="header">
    <div class="breadcrumbs">
      <i class="ti ti-chevron-right" style="font-size: 18px; color: #717279;"></i>
      <span class="footnote">Assistants API</span>
    </div>
    <span class="slide-number">15</span>
  </div>

  <h1 class="main-title">Assistants API - How to Use</h1>

  <div class="split-layout">
    <div class="left-panel">
      <div class="info-section">
        <p class="info-label">Endpoint</p>
        <p class="info-value">POST /v1/assistants/{id}/chat</p>
      </div>
      <div class="info-section">
        <p class="info-label">Authentication</p>
        <div class="info-list">
          <div class="info-item">
            <i class="ti ti-key" style="font-size: 20px; color: #456AFC;"></i>
            <span class="info-item-text">Bearer token required</span>
          </div>
          <div class="info-item">
            <i class="ti ti-shield-check" style="font-size: 20px; color: #456AFC;"></i>
            <span class="info-item-text">API key from Settings</span>
          </div>
        </div>
      </div>
      <div class="info-section">
        <p class="info-label">Key Parameters</p>
        <div class="info-list">
          <div class="info-item">
            <i class="ti ti-check" style="font-size: 20px; color: #456AFC;"></i>
            <span class="info-item-text">message (required)</span>
          </div>
          <div class="info-item">
            <i class="ti ti-check" style="font-size: 20px; color: #456AFC;"></i>
            <span class="info-item-text">conversation_id (optional)</span>
          </div>
          <div class="info-item">
            <i class="ti ti-check" style="font-size: 20px; color: #456AFC;"></i>
            <span class="info-item-text">stream (optional, default: false)</span>
          </div>
        </div>
      </div>
    </div>

    <div class="right-panel">
      <div class="code-block">
        <div class="code-header">
          <span class="code-language">Python</span>
        </div>
        <pre class="code-content"><code><span class="keyword">import</span> requests

<span class="comment"># Initialize the client</span>
API_KEY = <span class="string">"your-api-key"</span>
ASSISTANT_ID = <span class="string">"ast_123456"</span>

<span class="comment"># Send a message</span>
response = requests.<span class="function">post</span>(
    <span class="string">f"https://api.langdock.com/v1/assistants/{ASSISTANT_ID}/chat"</span>,
    headers={
        <span class="string">"Authorization"</span>: <span class="string">f"Bearer {API_KEY}"</span>,
        <span class="string">"Content-Type"</span>: <span class="string">"application/json"</span>
    },
    json={
        <span class="string">"message"</span>: <span class="string">"Summarize our Q4 report"</span>,
        <span class="string">"stream"</span>: <span class="keyword">False</span>
    }
)

<span class="function">print</span>(response.json())</code></pre>
      </div>
    </div>
  </div>
</body>
</html>
```

## Variations

### Different Languages
Change `.code-language` text and adjust syntax highlighting as needed.

### Shorter Code
Reduce code block height and add more info sections on the left.

### With Response Example
Add a second code block below showing the expected response.

### Terminal Style
```css
.code-block {
  background: #000000;
}
.code-header {
  background: #1a1a1a;
}
.code-content code {
  color: #00ff00;
}
```
