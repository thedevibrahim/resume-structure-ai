# Resume Structure AI

AI-powered resume extraction engine that transforms unstructured CVs
into structured, machine-readable JSON for ATS and talent intelligence
systems.

------------------------------------------------------------------------

## Overview

Resume Structure AI is not just a resume parser. It is a structured data
extraction engine designed to power:

-   Applicant Tracking Systems (ATS)
-   Talent intelligence platforms
-   Candidate search and ranking systems
-   Automated screening pipelines

The system leverages LLM-based extraction combined with deterministic
post-processing to normalize and structure resume data into predictable
JSON output.

------------------------------------------------------------------------

## Core Capabilities

• Extracts structured data from unstructured resumes\
• Identifies key sections (Experience, Education, Skills, etc.)\
• Normalizes roles, dates, and skills\
• Returns clean JSON suitable for downstream systems\
• Built with FastAPI for API-first integration

------------------------------------------------------------------------

## Architecture

The project follows a service-oriented structure:

-   API Layer (FastAPI)
-   Extraction Engine (LLM-driven parsing)
-   Normalization & Post-processing Layer
-   JSON Response Formatter

Designed to be modular so that LLM providers can be swapped without
affecting API consumers.

------------------------------------------------------------------------

## Example Output (Simplified)

``` json
{
  "name": "Jane Doe",
  "email": "jane@example.com",
  "skills": ["Python", "Machine Learning", "SQL"],
  "experience": [
    {
      "company": "TechCorp",
      "role": "Data Scientist",
      "start_date": "2021-01",
      "end_date": "2023-06"
    }
  ]
}
```

------------------------------------------------------------------------

## Running Locally

1.  Create virtual environment\
2.  Install dependencies\
3.  Run FastAPI server

Example:

``` bash
uvicorn main:app --reload
```

------------------------------------------------------------------------

## API Usage

POST resume file or raw text to the parsing endpoint. The service
returns structured JSON response.

------------------------------------------------------------------------

## Design Philosophy

This project is built around three principles:

1.  Structure over raw extraction\
2.  Modularity over tight coupling\
3.  API-first integration

It is designed to serve as a core infrastructure component in AI-driven
hiring systems.

------------------------------------------------------------------------

## Future Extensions

-   Candidate-job matching scoring\
-   Skill ontology integration\
-   Resume embedding search\
-   Multi-language resume support\
-   SaaS deployment model

------------------------------------------------------------------------

## License

MIT License
