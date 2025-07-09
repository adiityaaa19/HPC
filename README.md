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









# Firecrawl Tools

---

| Function                  | Description                                         |
|--------------------------|-----------------------------------------------------|
| `firecrawl_scrape`       | Single page content → returns markdown/html         |
| `firecrawl_batch_scrape` | Multiple known URLs → returns markdown/html[]       |
| `firecrawl_map`          | Discovering URLs on a site → returns URL[]          |
| `firecrawl_crawl`        | Multi-page extraction (with limits) → returns markdown/html[] |
| `firecrawl_search`       | Web search for info → returns results[]             |
| `firecrawl_extract`      | Structured data from pages → returns JSON           |
| `firecrawl_deep_research`| In-depth, multi-source research → returns summary, sources |
| `firecrawl_generate_llmstxt` | Generate LLMs.txt for a domain → returns text      |
| `firecrawl_check_batch_status` | Check the status of a batch operation → returns text |
| `firecrawl_check_crawl_status` | Check the status of a crawl job → status of the crawl job |

---

