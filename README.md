# Website Scraping into Neo4j (Airtable + Smartsheet)

We scraped data from Airtable and Smartsheet using Firecrawl and stored structured content in Neo4j as pages and sections.

- Each site is a Page node with linked Section and Tag nodes using HAS_SECTION and HAS_TAG relationships.

- Database: firecrawl-db | Username: neo4j | Password: test123

- Example 1: (:Page {title: "Smartsheet"})-[:HAS_SECTION]->(:Section {name: "Creative Operations"})

- Example 2: (:Page {title: "Airtable"})-[:HAS_TAG]->(:Tag {name: "AI"})
 
- Example 3: MATCH (p:Page)-[:HAS_SECTION]->(s:Section) RETURN p, s

## Tools & Technologies Used

Firecrawl for structured web scraping

Neo4j Desktop for local graph database setup

Cypher Query Language for graph modeling

Markdown + JSON parsing for extracting clean content

Visual inspection through Neo4j Browser UI
