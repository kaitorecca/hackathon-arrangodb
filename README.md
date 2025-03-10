# Disaster Impact Analyzer Agent
## ArangoDB GraphRAG Hackathon Submission

**Author:** Tai Tran
**YouTube Demo:** [Insert URL]  

---

### Project Overview

The **Disaster Impact Analyzer Agent** is an advanced agentic application developed for the ArangoDB GraphRAG Hackathon. It leverages GraphRAG, ArangoDB, NetworkX, and NVIDIA cuGraph to analyze the full GDELT Open Intelligence dataset, focusing on disaster events like violence against civilians. The agent provides insights, predicts disruption impacts, and generates response plans, processing over 65,000 events without sampling limits.

#### Key Features
- **Event Retrieval:** Query historical events (e.g., fatalities in January 1997) using natural language.
- **Impact Prediction:** Assess the cascading effects of event disruptions with GPU-accelerated analytics.
- **Response Planning:** Generate actionable plans for specific locations (e.g., Douaouda).
- **Geo-Visualization:** Interactive map of all event locations using Plotly.
- **User Interface:** Gradio-based dashboard for real-time interaction.

#### Alignment with Judging Criteria
- **Innovation:** Full-dataset analysis with geospatial visualization and impact prediction.
- **Functionality:** Comprehensive query handling across events, actors, and locations.
- **Technical Excellence:** Integrates ArangoDB AQL, `nx_arangodb`, and cuGraph for scalability.
- **Usability:** Intuitive interface for analysts and responders.
- **Documentation:** Detailed notebook and README for reproducibility.

---

### Dataset
- **Source:** GDELT Open Intelligence (`OPEN_INTELLIGENCE`) loaded via `arango-datasets`.
- **Schema:** 
  - Vertex Collections: `Event`, `Actor`, `Location`, `Source`.
  - Edge Collections: `eventActor`, `hasLocation`, `hasSource`.
- **Scale:** 65,534+ events, 116,227 `eventActor` edges, 8,779 locations (based on sample counts).
- **Focus:** Historical violence against civilians (e.g., 1997 Algeria events).

---

### Installation

1. **Prerequisites:**
   - Python 3.10+
   - ArangoDB instance running locally
   - NVIDIA GPU (optional, for cuGraph)

2. **Clone Repository:**
   ```bash
   git clone [Insert GitHub URL]
   cd disaster-impact-analyzer
