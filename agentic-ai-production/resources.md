# Resources

References and further reading drawn from the talk.

## Frameworks & libraries

- **LangGraph** — graph-based orchestration for stateful, multi-agent LLM applications. <https://langchain-ai.github.io/langgraph/>
- **LangChain** — LLM application framework. <https://python.langchain.com/>
- **LangSmith** — tracing, evaluation, and monitoring for LangChain/LangGraph. <https://smith.langchain.com/>
- **Pinecone** — managed vector database used for RAG retrieval. <https://www.pinecone.io/>
- **Microsoft Presidio** — PII detection and anonymization. <https://microsoft.github.io/presidio/>
- **OpenAI Moderation API** — input/output toxicity classification. <https://platform.openai.com/docs/guides/moderation>
- **Gradio** — UI for the demo agent. <https://www.gradio.app/>

## Observability

- **OpenTelemetry** — vendor-neutral tracing and metrics. <https://opentelemetry.io/>
- **Jaeger** — distributed tracing backend used in the demo. <https://www.jaegertracing.io/>
- **Langfuse** — open-source alternative to LangSmith for LLM observability. <https://langfuse.com/>

## RAG evaluation — `ragas`

- **`ragas` documentation** — <https://docs.ragas.io/en/stable/>
- **Faithfulness** — <https://docs.ragas.io/en/stable/concepts/metrics/available_metrics/faithfulness/>
- **Answer relevancy** — <https://docs.ragas.io/en/stable/concepts/metrics/available_metrics/answer_relevance/>
- **LLM context precision (without reference)** — <https://docs.ragas.io/en/stable/concepts/metrics/available_metrics/context_precision/#context-precision-without-reference>
- **NV response groundedness** — <https://docs.ragas.io/en/stable/concepts/metrics/available_metrics/nvidia_metrics/#response-groundedness>
- **NV context relevance** — <https://docs.ragas.io/en/stable/concepts/metrics/available_metrics/nvidia_metrics/#context-relevance>

## Closing framework

- **The Lethal Trifecta** — Simon Willison on private data + external communication + untrusted content as the high-risk overlap for AI agents. <https://simonwillison.net/2025/Jun/16/the-lethal-trifecta/>

## Background concepts

- **Model Context Protocol (MCP)** — standardised tool/data interface for agents. The demo uses an MCP server for order lookups. <https://modelcontextprotocol.io/>
- **ReAct pattern** — reasoning + acting loop that underlies most LangGraph agent nodes. <https://arxiv.org/abs/2210.03629>
- **Human-in-the-Loop with LangGraph interrupts** — <https://langchain-ai.github.io/langgraph/concepts/human_in_the_loop/>
- **LangGraph checkpointers (PostgreSQL, MemorySaver)** — <https://langchain-ai.github.io/langgraph/concepts/persistence/>
