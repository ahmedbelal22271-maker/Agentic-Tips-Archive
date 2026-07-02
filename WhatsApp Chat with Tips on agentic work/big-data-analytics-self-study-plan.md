# 300-Hour Big Data Analytics Course → Free Self-Study Replacement Plan

**Target total:** ~300 hours | **Plan total:** ~285–310 hours (variance noted per module)
**Format:** 11 modules → resources → 5 integration projects → week-by-week sequence → gap flags

---

## How to read the tables

- **Free** = no cost at all. **Free-audit** = free if you skip the graded certificate. **Paid** = flagged only when no adequate free substitute exists.
- Hours are realistic *active* study/lab hours, not video runtime.
- Resource order within each module = recommended order, not interchangeable alternatives (unless marked "OR").
- Links were verified at the time this plan was written; course platforms occasionally reorganize URLs, so if a link breaks, search the resource name directly.

---

## Module 1 — Generative AI for Big Data and Analytics (Original: ~20h)

**Topics:** LLM fundamentals, prompt techniques, GenAI platforms (Bedrock, Azure OpenAI, Vertex AI, Gemini), data-use cases (SQL, EDA, docs), limitations and Responsible AI.

**Learning objective:** Write effective prompts for data tasks (SQL generation, EDA summarization, doc Q&A) and explain, for a given use case, which cloud LLM platform fits and why — including its safety/governance limits.

| Resource | Type | Hours | Cost |
|---|---|---|---|
| [Anthropic — Prompt Engineering documentation](https://docs.claude.com/en/docs/build-with-claude/prompt-engineering/overview) | Official docs | 3 | Free |
| [DeepLearning.AI — "ChatGPT Prompt Engineering for Developers"](https://www.deeplearning.ai/short-courses/chatgpt-prompt-engineering-for-developers/) | MOOC | 2 | Free |
| [Google Cloud Skills Boost — "Introduction to Generative AI" learning path](https://www.cloudskillsboost.google/paths/118) | Official vendor course | 4 | Free |
| [AWS — Amazon Bedrock product/getting-started page](https://aws.amazon.com/bedrock/) + [AWS Skill Builder](https://skillbuilder.aws/) free-tier Bedrock labs | Official vendor labs | 5 | Free (AWS free tier) |
| [Microsoft Learn — "Develop Generative AI apps with Azure OpenAI Service"](https://learn.microsoft.com/en-us/training/paths/develop-ai-solutions-azure-openai/) | Official docs/labs | 4 | Free |
| [Google — "Responsible AI Practices"](https://ai.google/responsibility/responsible-ai-practices/) | Official docs | 2 | Free |

**Total: ~20h** (matches original)

---

## Module 2 — Generative AI Systems on Big Data Platforms (Original: ~35h)

**Topics:** RAG architecture, embeddings and vector search, Spark/Kafka integration, HDFS/S3 data lakes, LLMOps, governance guardrails (Ranger-style), end-to-end capstone.

**Learning objective:** Build and deploy a working RAG application — chunk documents, generate embeddings, run vector search, orchestrate retrieval + generation, and evaluate/monitor it.

| Resource | Type | Hours | Cost |
|---|---|---|---|
| [DataTalks.Club — LLM Zoomcamp (GitHub repo + self-paced YouTube playlist)](https://github.com/DataTalksClub/llm-zoomcamp) — covers RAG, embeddings, vector/hybrid search, evaluation, monitoring, agents | Free cohort-based course, self-paced option | 20 | Free |
| [Hugging Face — NLP Course](https://huggingface.co/learn/nlp-course) (embeddings/transformers chapters) | Official free course | 4 | Free |
| [Pinecone Learning Center](https://www.pinecone.io/learn/) — Vector Search & Embeddings guides | Vendor docs/tutorials | 3 | Free |
| [LangChain RAG tutorial](https://python.langchain.com/docs/tutorials/rag/) OR [LlamaIndex documentation](https://docs.llamaindex.ai/en/stable/) (pick one) | Official docs | 3 | Free |
| [Apache Ranger documentation](https://ranger.apache.org/) — policy/governance model overview (read alongside Module 11) | Official docs | 2 | Free |
| **Capstone:** Build a RAG Q&A bot over a public dataset (e.g., Wikipedia subset or your own course notes), store embeddings in a free vector store (Chroma/FAISS, self-hosted), serve via a simple API | Hands-on project | 3 | Free |

**Total: ~35h** (matches original)

---

## Module 3 — Introduction to Big Data (Original: ~10h)

**Topics:** Definition/characteristics of Big Data, evolution of data processing, scalable/fault-tolerant architecture, role of cloud, edge computing & AI.

**Learning objective:** Articulate the 5–6 "Vs" of Big Data with real business examples, and explain why distributed, fault-tolerant architecture is needed instead of a single scaled-up server.

| Resource | Type | Hours | Cost |
|---|---|---|---|
| [Coursera — "Introduction to Big Data" (UCSD, Big Data Specialization, Course 1)](https://www.coursera.org/learn/big-data-introduction) | MOOC, audit mode | 6 | Free-audit |
| [GitHub — AlessandroCorradini/University-of-California-San-Diego-Big-Data-Specialization](https://github.com/AlessandroCorradini/University-of-California-San-Diego-Big-Data-Specialization) — use to cross-check your own work | Repo/reference | 1 | Free |
| [AWS — "What Is Big Data?"](https://aws.amazon.com/what-is/big-data/) explainer page | Official docs | 1 | Free |
| [Google Cloud — "What Is Edge Computing?"](https://cloud.google.com/learn/what-is-edge-computing) overview | Official docs | 1 | Free |
| [Martin Kleppmann's site](https://martin.kleppmann.com/) — free blog posts/talks related to *Designing Data-Intensive Applications* (concepts only, not full reproduction) | Free blog/author site | 1 | Free |

**Total: ~10h** (matches original)

---

## Module 4 — Fundamentals of Big Data (Original: ~20h)

**Topics:** Big Data use cases, intro to public cloud (AWS, Azure), Apache Hadoop & Spark overview, HDFS storage, YARN.

**Learning objective:** Stand up a single-node Hadoop cluster (HDFS + YARN) locally or on a free-tier cloud VM, upload/retrieve files via HDFS commands, and submit a basic YARN-managed job.

| Resource | Type | Hours | Cost |
|---|---|---|---|
| [Coursera — "Big Data Modeling and Management Systems" (UCSD, Course 2)](https://www.coursera.org/learn/big-data-management) | MOOC, audit mode | 8 | Free-audit |
| [Apache Hadoop — official documentation](https://hadoop.apache.org/docs/stable/) — "Single Cluster Setup," HDFS Architecture, YARN Architecture guides | Official docs | 5 | Free |
| [AWS EMR — "Getting Started" guide](https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-gs.html) (small cluster, terminate promptly to stay in free tier) | Official vendor labs | 4 | Free (within limits) |
| [Microsoft Learn — Azure HDInsight "Get Started" tutorial](https://learn.microsoft.com/en-us/azure/hdinsight/hdinsight-hadoop-linux-tutorial-get-started) | Official vendor labs | 3 | Free (within limits) |

**Total: ~20h** (matches original)

---

## Module 5 — Big Data Ingestion (Original: ~30h)

**Topics:** Apache Sqoop, Apache Flume, Spark Streaming, Apache Flink, Apache NiFi pipelines, Apache Kafka, producers/consumers.

**Learning objective:** Build a real-time ingestion pipeline that moves data from a relational source into a streaming system (Kafka), processes it with a streaming engine, and lands it in storage — using NiFi or hand-rolled producers/consumers.

| Resource | Type | Hours | Cost |
|---|---|---|---|
| [Confluent Developer — "Kafka 101" course hub](https://developer.confluent.io/courses/apache-kafka/events/) — the best free, hands-on Kafka curriculum available | Official vendor course | 8 | Free |
| [DataTalks.Club — Data Engineering Zoomcamp (GitHub repo, Module 6: Streaming with Kafka)](https://github.com/DataTalksClub/data-engineering-zoomcamp) | Free course module | 6 | Free |
| [Apache NiFi — documentation hub](https://nifi.apache.org/documentation.html) + in-app templates | Official docs | 4 | Free |
| [Apache Flume — User Guide](https://flume.apache.org/FlumeUserGuide.html) | Official docs | 2 | Free |
| [Apache Sqoop — User Guide](https://sqoop.apache.org/docs/1.4.7/SqoopUserGuide.html) | Official docs | 2 | Free |
| [Apache Flink — official documentation](https://nightlies.apache.org/flink/flink-docs-stable/) (DataStream API / Getting Started) | Official docs | 4 | Free |
| [Spark — Structured Streaming Programming Guide](https://spark.apache.org/docs/latest/structured-streaming-programming-guide.html) (official, also reused in Module 8) | Official docs | 2 | Free |
| **Project checkpoint:** Build a NiFi or Kafka pipeline that ingests a public streaming dataset (e.g., NYC Taxi trip events, simulated) into a topic, then consume and write to local/S3-compatible storage | Hands-on project | 2 | Free |

**Total: ~30h** (matches original)

---

## Module 6 — Big Data Storage (Original: ~30h)

**Topics:** HDFS vs S3, NoSQL fundamentals, Apache HBase, Apache Cassandra, MongoDB.

**Learning objective:** Choose the correct storage system for a given access pattern (wide-column vs document vs object store), and perform basic CRUD + schema design in HBase, Cassandra, and MongoDB.

| Resource | Type | Hours | Cost |
|---|---|---|---|
| [Mahmoud Mohsen — "Big-Data Analytics" YouTube playlist](https://www.youtube.com/playlist?list=PLQhTr3lsMLujYMxra8scZxLTS_0J5PyQI), videos #4–7 (MongoDB vs RDBMS, Operations 1 & 2, MapReduce/Relations) — optional conceptual primer before the hands-on labs below | YouTube series | 2 | Free |
| [MongoDB University — M001 "MongoDB Basics"](https://learn.mongodb.com/) | Official vendor course | 8 | Free |
| [DataStax Academy](https://academy.datastax.com/) + [Apache Cassandra — official documentation](https://cassandra.apache.org/doc/latest/) | Official vendor course + docs | 8 | Free |
| [Apache HBase — Reference Guide](https://hbase.apache.org/book.html) — schema design, region servers | Official docs | 6 | Free |
| [AWS — Amazon S3 documentation](https://aws.amazon.com/s3/) (object storage fundamentals, for comparing against HDFS) | Official docs | 2 | Free |
| **Project checkpoint:** Model the same dataset three ways — as a Cassandra wide-column table, a MongoDB document collection, and an HBase table — and compare query performance/design tradeoffs in a short writeup | Hands-on project | 6 | Free |

**Total: ~32h** (+2h vs. original — optional MongoDB primer added; skip it if you're already comfortable with NoSQL concepts to land back on ~30h)

---

## Module 7 — Big Data Analytics (Original: ~35h)

**Topics:** SQL table creation/querying at scale, Apache Pig, Apache Hive, Impala, Lambda vs Kappa streaming architectures.

**Learning objective:** Write and optimize HiveQL queries against partitioned tables, explain Hive vs Impala tradeoffs, and diagram a Lambda vs a Kappa architecture for the same use case.

| Resource | Type | Hours | Cost |
|---|---|---|---|
| [Mode — free interactive SQL tutorial](https://mode.com/sql-tutorial/) (for refreshing SQL fundamentals before distributed engines) | Free interactive tutorial | 4 | Free |
| [Apache Hive — Language Manual](https://cwiki.apache.org/confluence/display/Hive/LanguageManual) (DDL/DML, partitioning, bucketing) | Official docs | 8 | Free |
| [Apache Impala — official documentation](https://impala.apache.org/impala-docs.html) — SQL reference and architecture | Official docs | 5 | Free |
| [Apache Pig — official documentation](https://pig.apache.org/docs/latest/start.html) ("Getting Started" / Pig Latin Basics) | Official docs | 3 | Free |
| [DataTalks.Club — Data Engineering Zoomcamp (GitHub repo), Data Warehousing & Analytics Engineering modules](https://github.com/DataTalksClub/data-engineering-zoomcamp) — practical SQL-at-scale patterns transferable to Hive/Impala | Free course module | 8 | Free |
| [Jay Kreps — "Questioning the Lambda Architecture" (O'Reilly Radar)](https://www.oreilly.com/radar/questioning-the-lambda-architecture/) + Confluent's Kappa architecture blog posts (read 2–3 articles, summarize in your own notes — don't copy text) | Free articles | 2 | Free |
| **Project checkpoint:** Load a public dataset (e.g., NYC Taxi or NOAA weather data) into Hive-style partitioned tables; write 5 analytical queries; document a Lambda vs Kappa design for the same data | Hands-on project | 5 | Free |

**Total: ~35h** (matches original)

---

## Module 8 — Big Data Processing with Apache Spark (Original: ~45h)

**Topics:** Spark introduction, Core/DataFrame APIs, DStream/Structured Streaming APIs, Spark applications, distributed processing model.

**Learning objective:** Write and submit a Spark application that reads structured data with the DataFrame API, performs transformations/aggregations, and processes a streaming source with Structured Streaming — explaining how Spark partitions and schedules work across a cluster.

| Resource | Type | Hours | Cost |
|---|---|---|---|
| [Apache Spark — official documentation hub](https://spark.apache.org/docs/latest/) — start with the [Quick Start guide](https://spark.apache.org/docs/latest/quick-start.html), then RDD Programming Guide, Spark SQL/DataFrame Guide, and Structured Streaming Guide | Official docs | 12 | Free |
| [UC Berkeley — "Big Data Analysis with Apache Spark" (BerkeleyX CS105x), via Class Central listing](https://www.classcentral.com/course/edx-big-data-analysis-with-apache-spark-3026) — original Spark course from Spark's creators at UC Berkeley/Databricks (course may be archived on edX; check current availability via the link) | University MOOC, audit mode | 15 | Free-audit |
| [Databricks — free training home](https://www.databricks.com/learn/training/home) — self-paced "Apache Spark Programming" introductory modules | Official vendor course | 8 | Free |
| [freeCodeCamp.org — "PySpark Tutorial" (YouTube)](https://www.youtube.com/watch?v=_C8kWso4ne4) | YouTube series | 6 | Free |
| **Project checkpoint:** Re-implement at least 3 of your Module 5–7 pipeline/query exercises using Spark DataFrames instead of Hive/Pig, and add one Structured Streaming job consuming from your Module 5 Kafka topic | Hands-on project | 4 | Free |

**Total: ~45h** (matches original)

---

## Module 9 — Big Data Modeling and AI (Original: ~40h)

**Topics:** ML fundamentals, ML on public cloud, Apache Spark ML/MLlib, pipeline creation, classification/regression, clustering/collaborative filtering.

**Learning objective:** Build a Spark ML pipeline (Transformers + Estimators) that preprocesses a large dataset and trains/evaluates a classification model and a clustering model, and explain how this differs from running scikit-learn locally.

| Resource | Type | Hours | Cost |
|---|---|---|---|
| [Google — Machine Learning Crash Course](https://developers.google.com/machine-learning/crash-course) (official, free) | Official vendor course | 8 | Free |
| [Coursera — "Machine Learning With Big Data" (UCSD, Big Data Specialization, Course 4)](https://www.coursera.org/learn/big-data-machine-learning) | MOOC, audit mode | 10 | Free-audit |
| [Apache Spark — MLlib Programming Guide](https://spark.apache.org/docs/latest/ml-guide.html) — pipelines, classification, regression, clustering, collaborative filtering | Official docs | 10 | Free |
| [Kaggle Learn](https://www.kaggle.com/learn) — "Intro to Machine Learning" + "Intermediate Machine Learning" micro-courses (hands-on notebooks) | Free interactive course | 6 | Free |
| **Project checkpoint:** Use Spark MLlib to build a full pipeline (feature engineering → train/test split → model → evaluation) for a classification task and a clustering task on a public dataset (e.g., a Kaggle dataset such as "Bank Marketing" or "Online Retail") | Hands-on project | 6 | Free |

**Total: ~40h** (matches original)

> Note: the UCSD Big Data Specialization's machine-learning course is officially Course 4 ("# 300-Hour Big Data Analytics Course → Free Self-Study Replacement Plan

**Target total:** ~300 hours | **Plan total:** ~285–310 hours (variance noted per module)
**Format:** 11 modules → resources → 5 integration projects → week-by-week sequence → gap flags

---

## How to read the tables

- **Free** = no cost at all. **Free-audit** = free if you skip the graded certificate. **Paid** = flagged only when no adequate free substitute exists.
- Hours are realistic *active* study/lab hours, not video runtime.
- Resource order within each module = recommended order, not interchangeable alternatives (unless marked "OR").
- Links were verified at the time this plan was written; course platforms occasionally reorganize URLs, so if a link breaks, search the resource name directly.

---

## Module 1 — Generative AI for Big Data and Analytics (Original: ~20h)

**Topics:** LLM fundamentals, prompt techniques, GenAI platforms (Bedrock, Azure OpenAI, Vertex AI, Gemini), data-use cases (SQL, EDA, docs), limitations and Responsible AI.

**Learning objective:** Write effective prompts for data tasks (SQL generation, EDA summarization, doc Q&A) and explain, for a given use case, which cloud LLM platform fits and why — including its safety/governance limits.

| Resource | Type | Hours | Cost |
|---|---|---|---|
| [Anthropic — Prompt Engineering documentation](https://docs.claude.com/en/docs/build-with-claude/prompt-engineering/overview) | Official docs | 3 | Free |
| [DeepLearning.AI — "ChatGPT Prompt Engineering for Developers"](https://www.deeplearning.ai/short-courses/chatgpt-prompt-engineering-for-developers/) | MOOC | 2 | Free |
| [Google Cloud Skills Boost — "Introduction to Generative AI" learning path](https://www.cloudskillsboost.google/paths/118) | Official vendor course | 4 | Free |
| [AWS — Amazon Bedrock product/getting-started page](https://aws.amazon.com/bedrock/) + [AWS Skill Builder](https://skillbuilder.aws/) free-tier Bedrock labs | Official vendor labs | 5 | Free (AWS free tier) |
| [Microsoft Learn — "Develop Generative AI apps with Azure OpenAI Service"](https://learn.microsoft.com/en-us/training/paths/develop-ai-solutions-azure-openai/) | Official docs/labs | 4 | Free |
| [Google — "Responsible AI Practices"](https://ai.google/responsibility/responsible-ai-practices/) | Official docs | 2 | Free |

**Total: ~20h** (matches original)

---

## Module 2 — Generative AI Systems on Big Data Platforms (Original: ~35h)

**Topics:** RAG architecture, embeddings and vector search, Spark/Kafka integration, HDFS/S3 data lakes, LLMOps, governance guardrails (Ranger-style), end-to-end capstone.

**Learning objective:** Build and deploy a working RAG application — chunk documents, generate embeddings, run vector search, orchestrate retrieval + generation, and evaluate/monitor it.

| Resource | Type | Hours | Cost |
|---|---|---|---|
| [DataTalks.Club — LLM Zoomcamp (GitHub repo + self-paced YouTube playlist)](https://github.com/DataTalksClub/llm-zoomcamp) — covers RAG, embeddings, vector/hybrid search, evaluation, monitoring, agents | Free cohort-based course, self-paced option | 20 | Free |
| [Hugging Face — NLP Course](https://huggingface.co/learn/nlp-course) (embeddings/transformers chapters) | Official free course | 4 | Free |
| [Pinecone Learning Center](https://www.pinecone.io/learn/) — Vector Search & Embeddings guides | Vendor docs/tutorials | 3 | Free |
| [LangChain RAG tutorial](https://python.langchain.com/docs/tutorials/rag/) OR [LlamaIndex documentation](https://docs.llamaindex.ai/en/stable/) (pick one) | Official docs | 3 | Free |
| [Apache Ranger documentation](https://ranger.apache.org/) — policy/governance model overview (read alongside Module 11) | Official docs | 2 | Free |
| **Capstone:** Build a RAG Q&A bot over a public dataset (e.g., Wikipedia subset or your own course notes), store embeddings in a free vector store (Chroma/FAISS, self-hosted), serve via a simple API | Hands-on project | 3 | Free |

**Total: ~35h** (matches original)

---

## Module 3 — Introduction to Big Data (Original: ~10h)

**Topics:** Definition/characteristics of Big Data, evolution of data processing, scalable/fault-tolerant architecture, role of cloud, edge computing & AI.

**Learning objective:** Articulate the 5–6 "Vs" of Big Data with real business examples, and explain why distributed, fault-tolerant architecture is needed instead of a single scaled-up server.

| Resource | Type | Hours | Cost |
|---|---|---|---|
| [Coursera — "Introduction to Big Data" (UCSD, Big Data Specialization, Course 1)](https://www.coursera.org/learn/big-data-introduction) | MOOC, audit mode | 6 | Free-audit |
| [GitHub — AlessandroCorradini/University-of-California-San-Diego-Big-Data-Specialization](https://github.com/AlessandroCorradini/University-of-California-San-Diego-Big-Data-Specialization) — use to cross-check your own work | Repo/reference | 1 | Free |
| [AWS — "What Is Big Data?"](https://aws.amazon.com/what-is/big-data/) explainer page | Official docs | 1 | Free |
| [Google Cloud — "What Is Edge Computing?"](https://cloud.google.com/learn/what-is-edge-computing) overview | Official docs | 1 | Free |
| [Martin Kleppmann's site](https://martin.kleppmann.com/) — free blog posts/talks related to *Designing Data-Intensive Applications* (concepts only, not full reproduction) | Free blog/author site | 1 | Free |

**Total: ~10h** (matches original)

---

## Module 4 — Fundamentals of Big Data (Original: ~20h)

**Topics:** Big Data use cases, intro to public cloud (AWS, Azure), Apache Hadoop & Spark overview, HDFS storage, YARN.

**Learning objective:** Stand up a single-node Hadoop cluster (HDFS + YARN) locally or on a free-tier cloud VM, upload/retrieve files via HDFS commands, and submit a basic YARN-managed job.

| Resource | Type | Hours | Cost |
|---|---|---|---|
| [Coursera — "Big Data Modeling and Management Systems" (UCSD, Course 2)](https://www.coursera.org/learn/big-data-management) | MOOC, audit mode | 8 | Free-audit |
| [Apache Hadoop — official documentation](https://hadoop.apache.org/docs/stable/) — "Single Cluster Setup," HDFS Architecture, YARN Architecture guides | Official docs | 5 | Free |
| [AWS EMR — "Getting Started" guide](https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-gs.html) (small cluster, terminate promptly to stay in free tier) | Official vendor labs | 4 | Free (within limits) |
| [Microsoft Learn — Azure HDInsight "Get Started" tutorial](https://learn.microsoft.com/en-us/azure/hdinsight/hdinsight-hadoop-linux-tutorial-get-started) | Official vendor labs | 3 | Free (within limits) |

**Total: ~20h** (matches original)

---

## Module 5 — Big Data Ingestion (Original: ~30h)

**Topics:** Apache Sqoop, Apache Flume, Spark Streaming, Apache Flink, Apache NiFi pipelines, Apache Kafka, producers/consumers.

**Learning objective:** Build a real-time ingestion pipeline that moves data from a relational source into a streaming system (Kafka), processes it with a streaming engine, and lands it in storage — using NiFi or hand-rolled producers/consumers.

| Resource | Type | Hours | Cost |
|---|---|---|---|
| [Confluent Developer — "Kafka 101" course hub](https://developer.confluent.io/courses/apache-kafka/events/) — the best free, hands-on Kafka curriculum available | Official vendor course | 8 | Free |
| [DataTalks.Club — Data Engineering Zoomcamp (GitHub repo, Module 6: Streaming with Kafka)](https://github.com/DataTalksClub/data-engineering-zoomcamp) | Free course module | 6 | Free |
| [Apache NiFi — documentation hub](https://nifi.apache.org/documentation.html) + in-app templates | Official docs | 4 | Free |
| [Apache Flume — User Guide](https://flume.apache.org/FlumeUserGuide.html) | Official docs | 2 | Free |
| [Apache Sqoop — User Guide](https://sqoop.apache.org/docs/1.4.7/SqoopUserGuide.html) | Official docs | 2 | Free |
| [Apache Flink — official documentation](https://nightlies.apache.org/flink/flink-docs-stable/) (DataStream API / Getting Started) | Official docs | 4 | Free |
| [Spark — Structured Streaming Programming Guide](https://spark.apache.org/docs/latest/structured-streaming-programming-guide.html) (official, also reused in Module 8) | Official docs | 2 | Free |
| **Project checkpoint:** Build a NiFi or Kafka pipeline that ingests a public streaming dataset (e.g., NYC Taxi trip events, simulated) into a topic, then consume and write to local/S3-compatible storage | Hands-on project | 2 | Free |

**Total: ~30h** (matches original)

---

## Module 6 — Big Data Storage (Original: ~30h)

**Topics:** HDFS vs S3, NoSQL fundamentals, Apache HBase, Apache Cassandra, MongoDB.

**Learning objective:** Choose the correct storage system for a given access pattern (wide-column vs document vs object store), and perform basic CRUD + schema design in HBase, Cassandra, and MongoDB.

| Resource | Type | Hours | Cost |
|---|---|---|---|
| [Mahmoud Mohsen — "Big-Data Analytics" YouTube playlist](https://www.youtube.com/playlist?list=PLQhTr3lsMLujYMxra8scZxLTS_0J5PyQI), videos #4–7 (MongoDB vs RDBMS, Operations 1 & 2, MapReduce/Relations) — optional conceptual primer before the hands-on labs below | YouTube series | 2 | Free |
| [MongoDB University — M001 "MongoDB Basics"](https://learn.mongodb.com/) | Official vendor course | 8 | Free |
| [DataStax Academy](https://academy.datastax.com/) + [Apache Cassandra — official documentation](https://cassandra.apache.org/doc/latest/) | Official vendor course + docs | 8 | Free |
| [Apache HBase — Reference Guide](https://hbase.apache.org/book.html) — schema design, region servers | Official docs | 6 | Free |
| [AWS — Amazon S3 documentation](https://aws.amazon.com/s3/) (object storage fundamentals, for comparing against HDFS) | Official docs | 2 | Free |
| **Project checkpoint:** Model the same dataset three ways — as a Cassandra wide-column table, a MongoDB document collection, and an HBase table — and compare query performance/design tradeoffs in a short writeup | Hands-on project | 6 | Free |

**Total: ~32h** (+2h vs. original — optional MongoDB primer added; skip it if you're already comfortable with NoSQL concepts to land back on ~30h)

---

## Module 7 — Big Data Analytics (Original: ~35h)

**Topics:** SQL table creation/querying at scale, Apache Pig, Apache Hive, Impala, Lambda vs Kappa streaming architectures.

**Learning objective:** Write and optimize HiveQL queries against partitioned tables, explain Hive vs Impala tradeoffs, and diagram a Lambda vs a Kappa architecture for the same use case.

| Resource | Type | Hours | Cost |
|---|---|---|---|
| [Mode — free interactive SQL tutorial](https://mode.com/sql-tutorial/) (for refreshing SQL fundamentals before distributed engines) | Free interactive tutorial | 4 | Free |
| [Apache Hive — Language Manual](https://cwiki.apache.org/confluence/display/Hive/LanguageManual) (DDL/DML, partitioning, bucketing) | Official docs | 8 | Free |
| [Apache Impala — official documentation](https://impala.apache.org/impala-docs.html) — SQL reference and architecture | Official docs | 5 | Free |
| [Apache Pig — official documentation](https://pig.apache.org/docs/latest/start.html) ("Getting Started" / Pig Latin Basics) | Official docs | 3 | Free |
| [DataTalks.Club — Data Engineering Zoomcamp (GitHub repo), Data Warehousing & Analytics Engineering modules](https://github.com/DataTalksClub/data-engineering-zoomcamp) — practical SQL-at-scale patterns transferable to Hive/Impala | Free course module | 8 | Free |
| [Jay Kreps — "Questioning the Lambda Architecture" (O'Reilly Radar)](https://www.oreilly.com/radar/questioning-the-lambda-architecture/) + Confluent's Kappa architecture blog posts (read 2–3 articles, summarize in your own notes — don't copy text) | Free articles | 2 | Free |
| **Project checkpoint:** Load a public dataset (e.g., NYC Taxi or NOAA weather data) into Hive-style partitioned tables; write 5 analytical queries; document a Lambda vs Kappa design for the same data | Hands-on project | 5 | Free |

**Total: ~35h** (matches original)

---

## Module 8 — Big Data Processing with Apache Spark (Original: ~45h)

**Topics:** Spark introduction, Core/DataFrame APIs, DStream/Structured Streaming APIs, Spark applications, distributed processing model.

**Learning objective:** Write and submit a Spark application that reads structured data with the DataFrame API, performs transformations/aggregations, and processes a streaming source with Structured Streaming — explaining how Spark partitions and schedules work across a cluster.

| Resource | Type | Hours | Cost |
|---|---|---|---|
| [Apache Spark — official documentation hub](https://spark.apache.org/docs/latest/) — start with the [Quick Start guide](https://spark.apache.org/docs/latest/quick-start.html), then RDD Programming Guide, Spark SQL/DataFrame Guide, and Structured Streaming Guide | Official docs | 12 | Free |
| [UC Berkeley — "Big Data Analysis with Apache Spark" (BerkeleyX CS105x), via Class Central listing](https://www.classcentral.com/course/edx-big-data-analysis-with-apache-spark-3026) — original Spark course from Spark's creators at UC Berkeley/Databricks (course may be archived on edX; check current availability via the link) | University MOOC, audit mode | 15 | Free-audit |
| [Databricks — free training home](https://www.databricks.com/learn/training/home) — self-paced "Apache Spark Programming" introductory modules | Official vendor course | 8 | Free |
| [freeCodeCamp.org — "PySpark Tutorial" (YouTube)](https://www.youtube.com/watch?v=_C8kWso4ne4) | YouTube series | 6 | Free |
| **Project checkpoint:** Re-implement at least 3 of your Module 5–7 pipeline/query exercises using Spark DataFrames instead of Hive/Pig, and add one Structured Streaming job consuming from your Module 5 Kafka topic | Hands-on project | 4 | Free |

**Total: ~45h** (matches original)

---

## Module 9 — Big Data Modeling and AI (Original: ~40h)

**Topics:** ML fundamentals, ML on public cloud, Apache Spark ML/MLlib, pipeline creation, classification/regression, clustering/collaborative filtering.

**Learning objective:** Build a Spark ML pipeline (Transformers + Estimators) that preprocesses a large dataset and trains/evaluates a classification model and a clustering model, and explain how this differs from running scikit-learn locally.

| Resource | Type | Hours | Cost |
|---|---|---|---|
| [Google — Machine Learning Crash Course](https://developers.google.com/machine-learning/crash-course) (official, free) | Official vendor course | 8 | Free |
| [Coursera — "Machine Learning With Big Data" (UCSD, Big Data Specialization, Course 4)](https://www.coursera.org/learn/big-data-machine-learning) | MOOC, audit mode | 10 | Free-audit |
| [Apache Spark — MLlib Programming Guide](https://spark.apache.org/docs/latest/ml-guide.html) — pipelines, classification, regression, clustering, collaborative filtering | Official docs | 10 | Free |
| [Kaggle Learn](https://www.kaggle.com/learn) — "Intro to Machine Learning" + "Intermediate Machine Learning" micro-courses (hands-on notebooks) | Free interactive course | 6 | Free |
| **Project checkpoint:** Use Spark MLlib to build a full pipeline (feature engineering → train/test split → model → evaluation) for a classification task and a clustering task on a public dataset (e.g., a Kaggle dataset such as "Bank Marketing" or "Online Retail") | Hands-on project | 6 | Free |

**Total: ~40h** (matches original)

> Note: the UCSD Big Data Specialization's machine-learning course is officially Course 4 ("Machine Learning With Big Data") in the six-course sequence, not Course 3 — corrected from an earlier draft of this plan.

---

## Module 10 — Data Visualization (Original: ~15h)

**Topics:** Visualization fundamentals, Apache Hue, Jupyter notebooks, Power BI.

**Learning objective:** Produce a polished, shareable dashboard/notebook that visualizes results from your Module 7–9 projects, using both a notebook tool and a BI tool.

| Resource | Type | Hours | Cost |
|---|---|---|---|
| [Jupyter — official documentation](https://docs.jupyter.org/en/latest/) | Official docs | 3 | Free |
| [Microsoft Learn — "Get started with Power BI" learning path](https://learn.microsoft.com/en-us/training/powerplatform/power-bi) (uses free Power BI Desktop) | Official vendor course | 6 | Free |
| [Guy in a Cube (YouTube channel)](https://www.youtube.com/@GuyInACube) — Power BI tips/tutorials | YouTube channel | 3 | Free |
| [Apache Hue — official site/live demo](https://gethue.com/) | Official docs/live demo | 2 | Free |
| **Project checkpoint:** Build one Jupyter-notebook visualization report and one Power BI dashboard, both summarizing your Module 9 ML project results | Hands-on project | 1 | Free |

**Total: ~15h** (matches original)

---

## Module 11 — Security and Access Control (Original: ~15h)

**Topics:** Authentication/authorization/encryption basics, Kerberos for cluster access, Apache Ranger/Atlas for ACLs.

**Learning objective:** Explain how Kerberos authenticates services on a cluster, and configure (or trace through documentation) a Ranger policy that restricts a user/group's access to specific Hive tables or HDFS paths.

| Resource | Type | Hours | Cost |
|---|---|---|---|
| [MIT Kerberos — official documentation](https://web.mit.edu/kerberos/) — concepts and protocol overview | Official docs | 4 | Free |
| [Apache Ranger — official documentation](https://ranger.apache.org/) — policy model, plugins, Hive/HDFS integration | Official docs | 5 | Free |
| [Apache Atlas — official documentation](https://atlas.apache.org/) — metadata/governance/data lineage overview | Official docs | 3 | Free |
| [Cloudera documentation hub](https://docs.cloudera.com/) — security architecture concepts (read-only reference) | Free vendor docs | 3 | Free |

**Total: ~15h** (matches original)

---

## Project Milestones (integration checkpoints)

1. **After Modules 3–4:** Stand up a single-node Hadoop cluster on a free-tier VM; load a public dataset into HDFS; run a YARN-submitted word-count or log-analysis job.
2. **After Modules 5–6:** Build an end-to-end ingestion pipeline (Kafka/NiFi → storage) and model the landed data in two different storage systems (e.g., Cassandra + MongoDB), comparing tradeoffs.
3. **After Modules 7–8:** Take the same dataset through Hive/Pig analytics *and* a Spark DataFrame rewrite; benchmark and document the differences.
4. **After Module 9:** Full Spark MLlib pipeline project (classification + clustering) on a public Kaggle dataset, with a written model-evaluation summary.
5. **Capstone (ties Modules 1–2, 9, 10 together):** Build an end-to-end system: ingest a dataset → store it → run Spark ML on it → wrap a RAG/LLM interface around the results (e.g., "ask questions about your analytics output") → visualize everything in a Jupyter or Power BI dashboard. This mirrors the original course's GenAI + Big Data capstone (Chapter 2) and the UCSD Specialization's "Catch the Pink Flamingo" capstone structure ([Coursera — Big Data Capstone Project](https://www.coursera.org/learn/big-data-project)).

---

## Suggested Week-by-Week Sequence (12-week, ~25h/week pace; adjust to your availability)

| Week | Focus | Why this order |
|---|---|---|
| 1 | Module 3 (Intro to Big Data) | Foundational concepts before any tooling |
| 2–3 | Module 4 (Hadoop/Spark/HDFS/YARN fundamentals) | Cluster concepts needed before ingestion/storage work |
| 4 | Module 1 (GenAI fundamentals) | Lightweight, can run in parallel; needed before Module 2 |
| 5–6 | Module 5 (Ingestion: Kafka/NiFi/Flume/Sqoop/Flink) | Requires basic cluster/storage literacy from Module 4 |
| 7 | Module 6 (Storage: HBase/Cassandra/MongoDB) | Needs ingestion output to actually populate |
| 8 | Module 7 (Analytics: Hive/Pig/Impala) | Requires data already sitting in storage |
| 9–10 | Module 8 (Spark processing) | Builds directly on SQL fundamentals + ingestion + storage |
| 11 | Module 9 (ML/MLlib) | Requires Spark DataFrame fluency from Module 8 |
| 12 | Module 10 (Visualization) + Module 11 (Security) + Module 2 (GenAI on Big Data capstone) | Wrap-up modules layered onto a finished pipeline |

If you have less time per week, stretch to 18–20 weeks rather than compressing modules — the dependency chain (cluster basics → ingestion → storage → analytics → Spark → ML) is the part that doesn't compress well.

---

## Gaps: where no adequate free equivalent exists

- **Hands-on multi-node cluster administration** (true distributed Hadoop/Spark cluster ops, not single-node): free-tier cloud quotas won't realistically let you run a multi-node cluster for free without watching costs closely. *Substitute:* use AWS/Azure/GCP free-tier credits for short-lived multi-node clusters (spin up, do the lab, tear down same day), or use Docker Compose multi-container setups locally to simulate multi-node behavior.
- **Vendor-certified GenAI platform depth** (deep Bedrock/Vertex/Azure OpenAI production features like fine-tuning, private networking, enterprise guardrails): official docs and free-tier consoles cover the concepts and basic workflows, but some enterprise features require a paid subscription to fully exercise. *Substitute:* use the free-tier consoles for core workflow practice; treat enterprise-only features as read-only documentation study rather than hands-on.
- **A polished, single end-to-end "GenAI on Big Data" capstone like Chapter 2's** doesn't exist as one free packaged course. *Substitute:* the LLM Zoomcamp capstone + your own combination of Modules 1–2's component pieces (RAG + Spark/Kafka integration) approximates it, but you are assembling it yourself rather than following a pre-built capstone brief.
- **Official certificate of completion equivalent to the paid course's certificate:** Coursera audit mode and most official vendor docs don't issue certificates for free. *Substitute:* DataTalks.Club Zoomcamps (Data Engineering, LLM) do offer free certificates if you join a live cohort and complete peer review — worth timing your plan around their cohort start dates if a certificate matters to you.

---

## Variance Note

This plan totals **~292 hours** of resource time (after the optional MongoDB primer addition) plus the 5 integration projects (~22h embedded in module totals already), landing close to the original 300-hour structure. The biggest swing factor is your existing SQL/Python fluency — if you're already comfortable with SQL and Python, Modules 7 and 9 will likely run faster than estimated; if you're new to both, add 10–15h buffer to those two modules.Machine Learning With Big Data") in the six-course sequence, not Course 3 — corrected from an earlier draft of this plan.

---

## Module 10 — Data Visualization (Original: ~15h)

**Topics:** Visualization fundamentals, Apache Hue, Jupyter notebooks, Power BI.

**Learning objective:** Produce a polished, shareable dashboard/notebook that visualizes results from your Module 7–9 projects, using both a notebook tool and a BI tool.

| Resource | Type | Hours | Cost |
|---|---|---|---|
| [Jupyter — official documentation](https://docs.jupyter.org/en/latest/) | Official docs | 3 | Free |
| [Microsoft Learn — "Get started with Power BI" learning path](https://learn.microsoft.com/en-us/training/powerplatform/power-bi) (uses free Power BI Desktop) | Official vendor course | 6 | Free |
| [Guy in a Cube (YouTube channel)](https://www.youtube.com/@GuyInACube) — Power BI tips/tutorials | YouTube channel | 3 | Free |
| [Apache Hue — official site/live demo](https://gethue.com/) | Official docs/live demo | 2 | Free |
| **Project checkpoint:** Build one Jupyter-notebook visualization report and one Power BI dashboard, both summarizing your Module 9 ML project results | Hands-on project | 1 | Free |

**Total: ~15h** (matches original)

---

## Module 11 — Security and Access Control (Original: ~15h)

**Topics:** Authentication/authorization/encryption basics, Kerberos for cluster access, Apache Ranger/Atlas for ACLs.

**Learning objective:** Explain how Kerberos authenticates services on a cluster, and configure (or trace through documentation) a Ranger policy that restricts a user/group's access to specific Hive tables or HDFS paths.

| Resource | Type | Hours | Cost |
|---|---|---|---|
| [MIT Kerberos — official documentation](https://web.mit.edu/kerberos/) — concepts and protocol overview | Official docs | 4 | Free |
| [Apache Ranger — official documentation](https://ranger.apache.org/) — policy model, plugins, Hive/HDFS integration | Official docs | 5 | Free |
| [Apache Atlas — official documentation](https://atlas.apache.org/) — metadata/governance/data lineage overview | Official docs | 3 | Free |
| [Cloudera documentation hub](https://docs.cloudera.com/) — security architecture concepts (read-only reference) | Free vendor docs | 3 | Free |

**Total: ~15h** (matches original)

---

## Project Milestones (integration checkpoints)

1. **After Modules 3–4:** Stand up a single-node Hadoop cluster on a free-tier VM; load a public dataset into HDFS; run a YARN-submitted word-count or log-analysis job.
2. **After Modules 5–6:** Build an end-to-end ingestion pipeline (Kafka/NiFi → storage) and model the landed data in two different storage systems (e.g., Cassandra + MongoDB), comparing tradeoffs.
3. **After Modules 7–8:** Take the same dataset through Hive/Pig analytics *and* a Spark DataFrame rewrite; benchmark and document the differences.
4. **After Module 9:** Full Spark MLlib pipeline project (classification + clustering) on a public Kaggle dataset, with a written model-evaluation summary.
5. **Capstone (ties Modules 1–2, 9, 10 together):** Build an end-to-end system: ingest a dataset → store it → run Spark ML on it → wrap a RAG/LLM interface around the results (e.g., "ask questions about your analytics output") → visualize everything in a Jupyter or Power BI dashboard. This mirrors the original course's GenAI + Big Data capstone (Chapter 2) and the UCSD Specialization's "Catch the Pink Flamingo" capstone structure ([Coursera — Big Data Capstone Project](https://www.coursera.org/learn/big-data-project)).

---

## Suggested Week-by-Week Sequence (12-week, ~25h/week pace; adjust to your availability)

| Week | Focus | Why this order |
|---|---|---|
| 1 | Module 3 (Intro to Big Data) | Foundational concepts before any tooling |
| 2–3 | Module 4 (Hadoop/Spark/HDFS/YARN fundamentals) | Cluster concepts needed before ingestion/storage work |
| 4 | Module 1 (GenAI fundamentals) | Lightweight, can run in parallel; needed before Module 2 |
| 5–6 | Module 5 (Ingestion: Kafka/NiFi/Flume/Sqoop/Flink) | Requires basic cluster/storage literacy from Module 4 |
| 7 | Module 6 (Storage: HBase/Cassandra/MongoDB) | Needs ingestion output to actually populate |
| 8 | Module 7 (Analytics: Hive/Pig/Impala) | Requires data already sitting in storage |
| 9–10 | Module 8 (Spark processing) | Builds directly on SQL fundamentals + ingestion + storage |
| 11 | Module 9 (ML/MLlib) | Requires Spark DataFrame fluency from Module 8 |
| 12 | Module 10 (Visualization) + Module 11 (Security) + Module 2 (GenAI on Big Data capstone) | Wrap-up modules layered onto a finished pipeline |

If you have less time per week, stretch to 18–20 weeks rather than compressing modules — the dependency chain (cluster basics → ingestion → storage → analytics → Spark → ML) is the part that doesn't compress well.

---

## Gaps: where no adequate free equivalent exists

- **Hands-on multi-node cluster administration** (true distributed Hadoop/Spark cluster ops, not single-node): free-tier cloud quotas won't realistically let you run a multi-node cluster for free without watching costs closely. *Substitute:* use AWS/Azure/GCP free-tier credits for short-lived multi-node clusters (spin up, do the lab, tear down same day), or use Docker Compose multi-container setups locally to simulate multi-node behavior.
- **Vendor-certified GenAI platform depth** (deep Bedrock/Vertex/Azure OpenAI production features like fine-tuning, private networking, enterprise guardrails): official docs and free-tier consoles cover the concepts and basic workflows, but some enterprise features require a paid subscription to fully exercise. *Substitute:* use the free-tier consoles for core workflow practice; treat enterprise-only features as read-only documentation study rather than hands-on.
- **A polished, single end-to-end "GenAI on Big Data" capstone like Chapter 2's** doesn't exist as one free packaged course. *Substitute:* the LLM Zoomcamp capstone + your own combination of Modules 1–2's component pieces (RAG + Spark/Kafka integration) approximates it, but you are assembling it yourself rather than following a pre-built capstone brief.
- **Official certificate of completion equivalent to the paid course's certificate:** Coursera audit mode and most official vendor docs don't issue certificates for free. *Substitute:* DataTalks.Club Zoomcamps (Data Engineering, LLM) do offer free certificates if you join a live cohort and complete peer review — worth timing your plan around their cohort start dates if a certificate matters to you.

---

## Variance Note

This plan totals **~292 hours** of resource time (after the optional MongoDB primer addition) plus the 5 integration projects (~22h embedded in module totals already), landing close to the original 300-hour structure. The biggest swing factor is your existing SQL/Python fluency — if you're already comfortable with SQL and Python, Modules 7 and 9 will likely run faster than estimated; if you're new to both, add 10–15h buffer to those two modules.
