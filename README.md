# Thriambak Giriprakash

**Software, Cloud, and AI Engineer**

[Live portfolio](https://thriambakg.github.io) · [Resume](Thriambak_Giriprakash_Resume.pdf) · [Email](mailto:Thriambak.g@gmail.com) · [LinkedIn](https://www.linkedin.com/in/thriambakg/) · [GitHub](https://github.com/thriambakg) · [Medium](https://medium.com/@thriambak.g) · (309) 750-6190

AWS-certified software engineer and founder with 4+ years of enterprise experience and two active ventures. I bridge cloud infrastructure and AI integrations with an MBA-level view of the product. I build scalable systems, from enterprise data pipelines to consumer-facing AI platforms.

Open to **software engineering, cloud, and AI engineering** roles.

The page recruiters should open is [thriambakg.github.io](https://thriambakg.github.io). This repository is that site. GitHub Pages serves the static `index.html` from the root of `main`. There is no Node or Python server behind it.

## Now

| | |
|---|---|
| Software Engineer, State Farm | Jul 2024 – Present |

## Experience

### State Farm — Software Engineer

Jul 2024 – Present · Full-time

- Built a RAG chatbot on Amazon Q that keeps knowledge in sync across five GitLab repositories, and integrated it into an enterprise Vue/TypeScript application.
- Architected Python/Lambda/Glue/SQS pipelines that process thousands of XML policy files each month, with faster ETL and 88% test coverage.
- Eliminated cross-region infrastructure drift with Terraform and GitLab CI/CD (OIDC), keeping production, staging, and development in parity.
- Integrated Bedrock with OpenSearch Serverless for RAG knowledge retrieval, cutting manual QA by 50%.

### State Farm — Software Engineer Intern

May 2022 – Aug 2023 · Part-time

- Built and embedded personalized Amazon QuickSight dashboards on the department React page for 20+ users. Public sample: [EmbeddedDash](https://github.com/thriambakg/EmbeddedDash).
- Deployed a Datadog resource-tracking dashboard to monitor AWS spend and usage.
- Created reusable Terraform modules for repeated infrastructure, which shortened turnover for other developers.

## Selected work

### FinGov — research workspace for following the money

**Live:** [fingov.ai](https://fingov.ai) · **Code:** [Cosine2.0](https://github.com/thriambakg/Cosine2.0) · [Cosine-Base-Infra](https://github.com/thriambakg/Cosine-Base-Infra) · **Write-up:** [product design case study](https://github.com/thriambakg/Cosine2.0/blob/prod/docs/FinGov-Product-Design-Case-Study.md)

Government-to-citizen SaaS I designed and shipped alone. It puts SEC filings, USAspending contracts, Congress, FEC contributions, lobbying disclosures, and congressional trades in one workspace. A campaign manager uses it to shape candidate strategy.

The assistant is a tool-using agent on Amazon Bedrock (Claude through Strands). It searches attached evidence, reads documents, and can produce charts or files. Session context is stored in DynamoDB and S3 so the model stays under the token budget and inside what the user attached. An earlier planner/orchestrator split (the model planned, a deterministic runner executed tools) was simplified to a Strands tool-calling agent on Lambda for reliability.

The interface is a dashboard for composing a research surface, full search pages where tiles were too cramped, a Files area for durable evidence, and chat that only sees dragged-in or attached context. Easy Mode came out of demos with people in local politics: common fields first, advanced filters still there.

Infrastructure is serverless AWS — Lambda, SQS/SNS, Step Functions, OpenSearch, Cognito, CloudFront — with Glue for scheduled large data flows. Terraform modules and GitHub Actions are shared with the base-infrastructure repo so the next service is reuse, not a fork.

### RDI — Remote Drone Interfaces

**In progress:** [rdistaging.com](https://rdistaging.com) · **Code:** [RDI-1.0](https://github.com/thriambakg/RDI-1.0) · [RDI-Base-Infra](https://github.com/thriambakg/RDI-Base-Infra) · [RDI-Pipelines](https://github.com/thriambakg/RDI-Pipelines)

Low-latency global drone operation from a browser. The control plane is API Gateway, Lambda, DynamoDB, Cognito, and CloudFront. The data plane is WebRTC between the pilot’s browser and a Raspberry Pi CM4 relay in the field. Amazon Kinesis Video Streams carries signaling only. Commands, telemetry, and video stay on the peer connection after the session is up.

Relays are backhauled with Starlink. That was chosen over AWS Wavelength so a session does not depend on a carrier edge zone through local weather or a disrupted link. Field software is Rust and Python speaking MAVLink to PX4 and ArduPilot-class autopilots, with an optional radio hop past the relay. The AWS side reused Terraform modules and CI/CD I already ran, which removed months of platform work.

## Skills

| Area | |
|---|---|
| Languages | Terraform (HCL), Python, Java, TypeScript, React, C. Familiar with Rust, Kotlin, C++, HTML/CSS. |
| Cloud | AWS (Lambda, API Gateway, Glue, SQS/SNS, Step Functions, DynamoDB, S3, OpenSearch, Cognito, CloudFront, Bedrock, Kinesis Video Streams, QuickSight). Familiar with Azure. |
| AI | Amazon Bedrock, Amazon Q, Strands, OpenAI API, TensorFlow, Keras. RAG over code, docs, and selected records. |
| Data | Glue, Spark, Hadoop, Pandas, Matplotlib, SQL, NoSQL. |
| Delivery | GitHub Actions, GitLab CI, OIDC to AWS, reusable Terraform modules, containers, single-push full-stack deploys. |
| Systems | Linux/Unix, Windows, embedded relays, WebRTC, PX4, ArduPilot, MAVLink. Web front ends on serverless APIs. |

## Education

**Iowa State University**, Ames, IA — graduated May 2024

- Master of Business Administration
- Bachelor of Software Engineering

**Certifications**

- AWS Certified Cloud Practitioner
- AWS Certified Developer – Associate
- AWS Certified Solutions Architect – Associate

## This site

Static files only, which is what GitHub Pages can host.

| File | Role |
|---|---|
| `index.html` | Portfolio page |
| `styles.css` | Layout and type |
| `Thriambak_Giriprakash_Resume.pdf` | Resume download |
| `favicon.svg` | Tab icon |

`.nojekyll` is present so Pages publishes these files as-is. Pushing `main` updates [thriambakg.github.io](https://thriambakg.github.io).
