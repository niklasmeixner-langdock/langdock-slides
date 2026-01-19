# Langdock Knowledge Index

When creating slides about Langdock features, use this index to find relevant documentation. **Fetch pages only when needed** for the specific slide topic.

Base URL: `https://docs.langdock.com`

---

## Chat Features

| Topic | Path | What you'll find |
|-------|------|------------------|
| Chat Basics | `/product/chat/functionalities` | Model selection, basic interaction features |
| Web Search | `/product/chat/web-search` | Real-time internet access, use cases |
| Document Search | `/product/chat/document-search` | Knowledge retrieval from uploaded files |
| Data Analysis | `/product/chat/data-analysis` | CSV, Excel, Sheets processing |
| Image Generation | `/product/chat/image-generation` | Text-to-image capabilities |
| Image Analysis | `/product/chat/image-analysis` | Multimodal visual analysis |
| Deep Research | `/product/chat/deep-research` | Comprehensive cited reports |
| Memory | `/product/chat/memory` | Cross-conversation information retention |
| Actions in Chat | `/product/chat/actions-in-chat` | Using integrations via @ symbol |
| Canvas Writing | `/product/chat/canvas-for-writing` | Document editing alongside chat |
| Canvas Code | `/product/chat/canvas-for-development` | Code editing environment |
| Mermaid Diagrams | `/product/chat/mermaid` | Flowcharts and visualizations |
| Prompt Library | `/product/chat/prompt-library` | Storing, sharing reusable prompts |
| Projects | `/product/chat/projects` | Organizing chats with shared context |

---

## Agents

| Topic | Path | What you'll find |
|-------|------|------------------|
| Agents Overview | `/product/agents/introduction` | What agents are, use cases |
| Agent Configuration | `/product/agents/configuration` | Tools, settings, customization |
| Agent Analytics | `/product/agents/usage-insights` | Usage tracking, feedback |
| Agent Creation Guide | `/resources/agent-creation` | Step-by-step building guide |
| Agent Templates | `/resources/agent-templates` | Pre-built examples |

---

## Workflows (Automation)

| Topic | Path | What you'll find |
|-------|------|------------------|
| Workflows Overview | `/product/workflows/introduction` | AI-driven automation basics |
| Getting Started | `/product/workflows/getting-started` | First workflow tutorial |
| Core Concepts | `/product/workflows/core-concepts` | Nodes, triggers, execution |
| Field Modes | `/product/workflows/field-modes` | Auto, Manual, AI Prompt modes |
| Human in the Loop | `/product/workflows/human-in-the-loop` | Manual approval steps |
| Variables | `/product/workflows/variable-usage` | Accessing data between nodes |
| Cost Management | `/product/workflows/cost-management` | Optimization strategies |

### Workflow Nodes
| Node Type | Path | What you'll find |
|-----------|------|------------------|
| Agent Node | `/product/workflows/nodes/agent-node` | AI analysis and decisions |
| Action Node | `/product/workflows/nodes/action-node` | Execute app actions |
| Web Search | `/product/workflows/nodes/web-search-node` | Internet research |
| File Search | `/product/workflows/nodes/file-search-node` | Knowledge retrieval |
| HTTP Request | `/product/workflows/nodes/http-request-node` | API calls |
| Condition | `/product/workflows/nodes/condition-node` | Branching logic |
| Loop | `/product/workflows/nodes/loop-node` | Array iteration |
| Code | `/product/workflows/nodes/code-node` | JavaScript execution |
| Guardrails | `/product/workflows/nodes/guardrails-node` | Validation checks |
| Delay | `/product/workflows/nodes/delay-node` | Pause execution |
| Notification | `/product/workflows/nodes/notification-node` | Team alerts |

### Workflow Triggers
| Trigger Type | Path | What you'll find |
|--------------|------|------------------|
| Integration | `/product/workflows/nodes/integration-trigger` | Event-based start |
| Scheduled | `/product/workflows/nodes/scheduled-trigger` | Recurring execution |
| Manual | `/product/workflows/nodes/manual-trigger` | On-demand execution |
| Form | `/product/workflows/nodes/form-trigger` | Form submissions |
| Webhook | `/product/workflows/nodes/webhook-trigger` | HTTP POST activation |

---

## Integrations

| Topic | Path | What you'll find |
|-------|------|------------------|
| Integrations Overview | `/product/integrations/introduction` | Native and custom capabilities |
| Connections | `/product/integrations/connections` | Auth and sharing options |
| MCP Directory | `/product/integrations/mcp-directory` | Model Context Protocol servers |
| Integration Permissions | `/administration/integrations-permissions` | Access control setup |
| Integration Details | `/administration/integrations-details` | Technical specifications |

### Popular Integrations (45+ available)
- **Collaboration**: Slack, Teams, Gmail, Outlook
- **Project Management**: Jira, Linear, Asana, Monday.com, Notion
- **Data**: BigQuery, Snowflake, Google Sheets, Airtable
- **Storage**: Google Drive, OneDrive, SharePoint, Confluence
- **CRM**: Salesforce, HubSpot, Zendesk
- **Vector DBs**: Pinecone, Qdrant, Milvus

---

## API Reference

| Topic | Path | What you'll find |
|-------|------|------------------|
| API Overview | `/api-endpoints/api-introduction` | Getting started with APIs |

### Completion API (LLM Access)
| Provider | Path | What you'll find |
|----------|------|------------------|
| OpenAI | `/api-endpoints/completion/openai` | GPT models access |
| Anthropic | `/api-endpoints/completion/anthropic` | Claude models access |
| Google | `/api-endpoints/completion/google` | Gemini models access |
| Mistral | `/api-endpoints/completion/mistral` | Codestral, Mistral models |

### Agent API
| Endpoint | Path | What you'll find |
|----------|------|------------------|
| Guide | `/api-endpoints/agent/agent-api-guide` | Setup and usage |
| Chat | `/api-endpoints/agent/agent` | Send messages to agents |
| Get Agent | `/api-endpoints/agent/agent-get` | Retrieve agent details |
| Create Agent | `/api-endpoints/agent/agent-create` | Build agents via API |
| Update Agent | `/api-endpoints/agent/agent-update` | Modify agents |
| Models List | `/api-endpoints/agent/agent-models` | Available models |
| Attachments | `/api-endpoints/agent/upload-attachments` | File uploads |
| Migration | `/api-endpoints/agent/agent-migration` | Transfer between workspaces |

### Knowledge Folder API
| Endpoint | Path | What you'll find |
|----------|------|------------------|
| Sharing | `/api-endpoints/knowledge-folder/sharing` | Share folders via API |
| Upload | `/api-endpoints/knowledge-folder/upload-file` | Add documents |
| Update | `/api-endpoints/knowledge-folder/update-attachment` | Modify documents |
| Retrieve | `/api-endpoints/knowledge-folder/retrieve-files` | Access files |
| Delete | `/api-endpoints/knowledge-folder/delete-attachment` | Remove documents |
| Search | `/api-endpoints/knowledge-folder/search-knowledge-folder` | Query contents |

### Embedding API
| Endpoint | Path | What you'll find |
|----------|------|------------------|
| OpenAI Embeddings | `/api-endpoints/embedding/openai-embedding` | Text vectorization |

### Usage Export API
| Endpoint | Path | What you'll find |
|----------|------|------------------|
| Overview | `/api-endpoints/usage-export/intro-to-usage-export-api` | Setup and capabilities |
| Users | `/api-endpoints/usage-export/export-users` | User activity data |
| Agents | `/api-endpoints/usage-export/export-agents` | Agent usage metrics |
| Workflows | `/api-endpoints/usage-export/export-workflows` | Workflow execution data |
| Projects | `/api-endpoints/usage-export/export-projects` | Project activity |
| Models | `/api-endpoints/usage-export/export-models` | Model usage stats |

---

## Knowledge Management

| Topic | Path | What you'll find |
|-------|------|------------------|
| Knowledge Basics | `/resources/knowledge/knowledge-basics` | Document processing |
| Vector Databases | `/resources/knowledge/vector-databases-knowledge-folders` | Large collections |
| Knowledge Types | `/resources/knowledge/knowledge-types` | Addition methods |
| Best Practices | `/resources/knowledge/best-practices` | Effective usage |

---

## Prompt Engineering

| Topic | Path | What you'll find |
|-------|------|------------------|
| Prompt Elements | `/resources/prompt-elements` | Building blocks |
| Basics | `/resources/basics` | Foundation concepts |
| Tips & Tricks | `/resources/tricks` | Effective crafting |
| Techniques | `/resources/prompting-techniques` | Zero-shot, few-shot, CoT |
| Instructions | `/resources/instructions` | Clear directive guidelines |
| Structure | `/resources/structure-prompt` | Delimiters, XML tags |
| Output Format | `/resources/output-format` | Controlling responses |
| Chain Prompts | `/resources/chain-prompts` | Breaking complex tasks |
| Context Window | `/resources/context-window` | Token optimization |
| Role Assignment | `/resources/role` | Persona techniques |

---

## Administration & Security

| Topic | Path | What you'll find |
|-------|------|------------------|
| Account Settings | `/settings/account` | User preferences |
| Workspace Settings | `/settings/workspace` | Admin configuration |
| Custom Instructions | `/resources/custom-instructions` | Personalized AI behavior |
| Fair Usage Policy | `/settings/fair-usage-policy` | Rate limits |
| Adding Models | `/settings/models/adding-models` | Custom model integration |
| Static IP | `/settings/security/static-ip-configuration` | Network security |
| SAML (Entra ID) | `/settings/security/entra` | Microsoft SSO |
| SAML (Google) | `/settings/security/google` | Google SSO |
| SCIM Provisioning | `/settings/security/scim/entra` | Auto user provisioning |
| Permissions | `/administration/permissions` | Roles and access |

---

## Billing & Compliance

| Topic | Path | What you'll find |
|-------|------|------------------|
| Pricing | `/administration/pricing` | Plans and costs |
| Subscription | `/administration/subscription` | Plan management |
| Invoices | `/administration/invoices` | Billing history |
| Finding Invoices | `/administration/finding-invoices` | Invoice retrieval |
| Usage Exports | `/administration/usage-exports` | Activity reports |
| API Usage Export | `/administration/api-usage-export` | API analytics |
| Legal Compliance | `/administration/legal-compliance` | Regulatory info |

---

## AI Rollout & Adoption

| Topic | Path | What you'll find |
|-------|------|------------------|
| Rollout Setup | `/administration/rollout-setup` | Initial deployment |
| Rollout Playbook | `/administration/rollout-playbook` | Step-by-step guide |
| Use Case Identification | `/administration/identify-use-cases` | Finding opportunities |
| Workspace Setup | `/administration/workspace-setup` | Technical configuration |
| Slack Channel | `/administration/slack-channel` | Slack integration setup |
| Teams Channel | `/administration/teams-channel` | Teams integration setup |
| MS Admin Approval | `/administration/microsoft-admin-approval` | Microsoft consent |

---

## Learning Resources

| Topic | Path | What you'll find |
|-------|------|------------------|
| Dictionary | `/resources/dictionary` | AI terminology |
| Tricks & Shortcuts | `/resources/tricks-and-shortcuts` | Productivity tips |
| Workshops | `/resources/langdock-workshops` | Training recordings |
| Cheat Sheet | `/resources/cheat-sheet` | Quick reference |
| Further Resources | `/resources/further-resources` | External links |

---

## Usage Instructions

When creating a slide about a Langdock topic:

1. **Identify the topic** from the tables above
2. **Construct the full URL**: `https://docs.langdock.com` + path
3. **Fetch the page** using `WebFetch` tool
4. **Extract only relevant info** for the slide content
5. **Do not fetch multiple pages at once** - only what's needed for the current slide
