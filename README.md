# Translation Memory Tools

---

| Function                | Description                               |
|------------------------|-------------------------------------------|
| `list_memories`       | List saved translation memories           |
| `create_memory`       | Create a new translation memory           |
| `update_memory`       | Update a memory’s name                    |
| `delete_memory`       | Delete a translation memory               |
| `add_translation`     | Add a translation unit to a memory        |
| `delete_translation`  | Remove a translation unit from a memory   |
| `import_tmx`          | Import a TMX file into a memory           |
| `check_import_status` | Check TMX import status                   |

---













# Brave Search Tools

---

| Function              | Description                                                                                       |
|-----------------------|---------------------------------------------------------------------------------------------------|
| `brave_web_search`    | Execute web searches with pagination and filtering.Inputs: `query` (string), `count` (number, optional, max 20), `offset` (number, optional, max 9) | 
| `brave_local_search`  | Search for local businesses and services. Falls back to web search if no local results found.Inputs: `query` (string), `count` (number, optional, max 20) | 

---









flowchart LR
  A[Start – Intro: About our Company/Asss] --> B{Qualified?}
  B -->|✅ Yes| C[Ask for contact number & code]
  B -->|✅ Yes| D[Ask for specific time]
  D --> E[API hook ➜ Salesforce CRM]
  C --> E
  B -->|❌ No| F[Book appointment calendar]
  F --> E
  
  E --> G[Data‑batch RPA]
  E --> H[Digital brochures]
  E --> I[Sales force]
  E --> J[MSP Support]

  subgraph Global Note
    K[Call Transfer]
  end

