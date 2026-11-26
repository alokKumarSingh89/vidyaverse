# VidyaVerse — AI Strategy

## 1. Objective

Build a reliable, cost-effective and extensible
educational AI platform.

The initial business shall not depend on permanent
teachers or external sponsors.

AI-generated content shall pass appropriate validation
before publication.

## 2. Technology

- Python 3.13.
- FastAPI.
- Pydantic.
- LangGraph where workflow orchestration is required.
- PostgreSQL.
- pgvector.
- SymPy.
- SQLAlchemy.
- Alembic.
- uv.
- Pytest.

Dependencies shall be introduced incrementally
after compatibility verification.

## 3. AI Capabilities

- Curriculum retrieval.
- Question generation.
- Educational content generation.
- Answer verification.
- Examination blueprint generation.
- Document extraction.
- Translation.
- Visualization configuration generation.
- Answer evaluation.
- Personalized tutoring.
- Model evaluation.
- AI usage accounting.

## 4. Provider Abstraction

AI providers shall be accessed through
provider-independent interfaces.

Business functionality shall not depend directly
on a specific provider SDK.

Provider capabilities may include:

- Text generation.
- Structured generation.
- Image understanding.
- Embedding generation.
- Speech recognition.
- Speech generation.

Provider selection shall consider:

- Required capabilities.
- Educational accuracy.
- Language quality.
- Cost.
- Latency.
- Availability.
- Data protection requirements.

## 5. Workflow Orchestration

AI workflows may combine:

- Deterministic application logic.
- Retrieval operations.
- AI model calls.
- Mathematical computation.
- Schema validation.
- Quality evaluation.
- Conditional processing.

Not every workflow node requires an AI model.

Workflows shall enforce execution limits,
timeouts and bounded retry policies.

## 6. Curriculum-Grounded Generation

Educational generation shall use relevant
curriculum context where available.

Knowledge retrieval shall preserve:

- Source identifiers.
- Curriculum versions.
- Education board.
- Grade.
- Subject.
- Chapter.
- Learning objectives.
- Language.

Only authorized educational material shall be
included in the reusable knowledge base.

## 7. AI Output Management

AI output shall be treated as untrusted data.

Structured output shall pass schema validation.

Generated artifacts shall preserve:

- Model identifier.
- Provider identifier.
- Prompt version.
- Workflow version.
- Source references.
- Generation timestamp.
- Validation results.
- Usage information.

## 8. Reliability

Published educational content shall remain
available during AI provider failures.

Live examinations shall not require real-time AI.

Expensive operations shall support asynchronous
processing where appropriate.

## 9. Cost Management

- Reuse validated generated content.
- Cache common translations.
- Track token and provider usage.
- Enforce per-operation budgets.
- Enforce subscription entitlements.
- Prevent uncontrolled agent execution.
- Select models according to task requirements.

## 10. Future Model Development

Future capabilities may include:

- Proprietary educational datasets.
- Expert-reviewed training examples.
- Supervised fine-tuning.
- Parameter-efficient fine-tuning.
- Specialized multilingual models.
- Self-hosted inference.

Student data shall not be used for training
by default.

Training datasets shall have documented
provenance and appropriate usage rights.

## 11. Safety

AI shall not be presented as infallible.

Age-appropriate educational behaviour,
privacy and child safety shall be enforced.

AI agents shall not receive unrestricted
access to databases, tools or external systems.

## 12. Initial AI Provider and Model Training

The initial AI provider shall be OpenAI,
accessed through the provider abstraction.

AI model selection shall consider educational
quality, latency, cost and data protection.

Custom model training and dedicated GPU
infrastructure shall be deferred until
sufficient datasets, business requirements
and financial resources are available.

The platform shall preserve the ability
to integrate privately fine-tuned models
without redesigning business services.
