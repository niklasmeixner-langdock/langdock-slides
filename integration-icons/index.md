# Integration Icons

PNG icons for Langdock integrations. Use these when displaying integration logos on slides.

**Location**: `/integration-icons/{name}-icon.png`

**Usage**: Reference icons via absolute URLs when importing HTML to Figma. For local development, use relative paths.

---

## Icon Categories

### Collaboration & Communication
| Icon | Filename | Integration |
|------|----------|-------------|
| Slack | `slack-icon.png` | Slack messaging |
| Microsoft Teams | `microsoft-teams-icon.png` | Teams messaging |
| Gmail | `gmail-icon.png` | Google email |
| Microsoft Outlook Email | `microsoft-outlook-email-icon.png` | Outlook email |
| Miro | `miro-icon.png` | Visual collaboration |

### Project Management
| Icon | Filename | Integration |
|------|----------|-------------|
| Jira | `jira-icon.png` | Atlassian project tracking |
| Linear | `linear-icon.png` | Issue tracking |
| Asana | `asana-icon.png` | Project management |
| Monday.com | `monday-com-icon.png` | Work OS |
| Microsoft Planner | `microsoft-planner-icon.png` | Task management |
| Microsoft Todo | `microsoft-todo-icon.png` | Personal tasks |
| Wrike | `wrike-icon.png` | Project management |

### Documentation & Storage
| Icon | Filename | Integration |
|------|----------|-------------|
| Confluence | `confluence-icon.png` | Atlassian wiki |
| Notion | `notion-icon.png` | Workspace & docs |
| Google Drive | `google-drive-icon.png` | Cloud storage |
| Google Docs | `google-docs-icon.png` | Documents |
| Google Sheets | `google-sheets-icon.png` | Spreadsheets |
| Google Slides | `google-slides-icon.png` | Presentations |
| Microsoft OneDrive | `microsoft-onedrive-icon.png` | Cloud storage |
| Microsoft SharePoint | `microsoft-sharepoint-icon.png` | Document management |
| Microsoft Excel | `microsoft-excel-icon.png` | Spreadsheets |

### Calendar & Scheduling
| Icon | Filename | Integration |
|------|----------|-------------|
| Google Calendar | `google-calendar-icon.png` | Google calendar |
| Microsoft Outlook Calendar | `microsoft-outlook-calendar-icon.png` | Outlook calendar |
| Google Meet | `google-meet-icon.png` | Video meetings |
| Calendly | `calendly-icon.png` | Scheduling |
| Google Tasks | `google-tasks-icon.png` | Tasks |
| Luma | `luma-icon.png` | Event management |

### CRM & Sales
| Icon | Filename | Integration |
|------|----------|-------------|
| Salesforce | `salesforce-icon.png` | CRM platform |
| HubSpot | `hubspot-icon.png` | Marketing & CRM |
| Zendesk | `zendesk-icon.png` | Customer support |
| Personio | `personio-icon.png` | HR management |
| Pylon | `pylon-icon.png` | Customer operations |
| Ashby | `ashby-icon.png` | Recruiting |

### Data & Analytics
| Icon | Filename | Integration |
|------|----------|-------------|
| BigQuery | `big-query-icon.png` | Google data warehouse |
| Snowflake | `snowflake-icon.png` | Cloud data platform |
| Databricks | `databricks-icon.png` | Data & AI platform |
| Google Analytics | `google-analytics-icon.png` | Web analytics |
| Looker | `looker-icon.png` | BI platform |
| Metabase | `metabase-icon.png` | Open source BI |
| Tableau | `tableau-icon.png` | Data visualization |
| Microsoft PowerBI | `microsoft-powerbi-icon.png` | Business analytics |
| Statista | `statista-icon.png` | Market research |

### Development & DevOps
| Icon | Filename | Integration |
|------|----------|-------------|
| GitHub | `github-icon.png` | Code repository |
| ServiceNow | `service-now-icon.png` | IT service management |
| Stripe | `stripe-icon.png` | Payment processing |

### Vector Databases
| Icon | Filename | Integration |
|------|----------|-------------|
| Pinecone | `pinecone-icon.png` | Vector DB |
| Qdrant | `qdrant-icon.png` | Vector DB |
| Milvus | `milvus-icon.png` | Vector DB |

### AI & Cloud Services
| Icon | Filename | Integration |
|------|----------|-------------|
| AWS Kendra | `aws-kendra-icon.png` | Enterprise search |
| Azure AI Search | `azure-ai-search-icon.png` | AI-powered search |
| Vertex AI Vector Search | `vertex-ai-vector-search-icon.png` | Google vector search |
| DeepL | `deepl-icon.png` | Translation |
| ElevenLabs | `elevenlabs-icon.png` | Voice AI |

### Other
| Icon | Filename | Integration |
|------|----------|-------------|
| Airtable | `airtable-icon.png` | Database/spreadsheet |
| Google Maps | `google-maps-icon.png` | Maps & location |
| Microsoft Entra | `microsoft-entra-icon.png` | Identity management |
| OpenRegister | `openregister-icon.png` | Company data |

---

## HTML Usage

### Single Icon
```html
<img src="integration-icons/slack-icon.png" alt="Slack" style="width: 48px; height: 48px;">
```

### Icon in Circle Container
```html
<div class="integration-icon">
  <img src="integration-icons/slack-icon.png" alt="Slack">
</div>
```

```css
.integration-icon {
  width: 64px;
  height: 64px;
  background: #ffffff;
  border-radius: 12px;
  padding: 12px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
  display: flex;
  align-items: center;
  justify-content: center;
}
.integration-icon img {
  width: 40px;
  height: 40px;
  object-fit: contain;
}
```

### Icon Grid (4x5 layout)
```html
<div class="integration-grid">
  <div class="integration-icon"><img src="integration-icons/slack-icon.png" alt="Slack"></div>
  <div class="integration-icon"><img src="integration-icons/microsoft-teams-icon.png" alt="Teams"></div>
  <!-- ... more icons -->
</div>
```

```css
.integration-grid {
  display: grid;
  grid-template-columns: repeat(4, 64px);
  gap: 16px;
}
```

### Icon with Label
```html
<div class="integration-item">
  <div class="integration-icon">
    <img src="integration-icons/salesforce-icon.png" alt="Salesforce">
  </div>
  <span class="integration-label">Salesforce</span>
</div>
```

```css
.integration-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 8px;
}
.integration-label {
  font-family: 'Inter', sans-serif;
  font-size: 14px;
  font-weight: 500;
  color: #717279;
}
```

---

## Common Groupings for Slides

### Popular Integrations (Top 6)
- `slack-icon.png`
- `microsoft-teams-icon.png`
- `gmail-icon.png`
- `jira-icon.png`
- `notion-icon.png`
- `salesforce-icon.png`

### Google Workspace
- `gmail-icon.png`
- `google-drive-icon.png`
- `google-docs-icon.png`
- `google-sheets-icon.png`
- `google-slides-icon.png`
- `google-calendar-icon.png`
- `google-meet-icon.png`

### Microsoft 365
- `microsoft-teams-icon.png`
- `microsoft-outlook-email-icon.png`
- `microsoft-onedrive-icon.png`
- `microsoft-sharepoint-icon.png`
- `microsoft-excel-icon.png`
- `microsoft-planner-icon.png`

### Data Stack
- `big-query-icon.png`
- `snowflake-icon.png`
- `databricks-icon.png`
- `looker-icon.png`
- `tableau-icon.png`

### Vector Databases
- `pinecone-icon.png`
- `qdrant-icon.png`
- `milvus-icon.png`

---

## Best Practices

1. **Consistent sizing**: Use 40-48px for grid layouts, 32px for inline references
2. **White backgrounds**: Icons look best on white or light surfaces
3. **Adequate spacing**: Use 16-24px gaps between icons
4. **Shadow optional**: Add subtle shadow for cards, remove for inline use
5. **Alt text**: Always include meaningful alt attributes
