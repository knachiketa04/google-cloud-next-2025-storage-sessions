# AI Hypercomputer: Master your storage infrastructure - Key Takeaways & Insights

[YouTube Link](https://youtu.be/CXwFLE4Eelg?si=NNy_uWDJxqX_Hr3z)

*Session at Google Cloud Next 2025*

## Session Recap
This session covered Google Cloud's storage solutions optimized for AI/ML workloads. It defined the AI Hypercomputer concept, highlighted the critical role of storage, typical requirements, high-performance options (like the new Rapid Storage and GA'd Anywhere Cache), parallel file systems (including the new Managed Lustre and Parallelstore), and featured compelling customer successes from Snap Inc., Anthropic, AssemblyAI, and TII.

## Key Takeaways
* **AI Hypercomputer Defined:** Google defines AI Hypercomputer as an end-to-end, integrated system combining optimized hardware (GPUs, TPUs, networking), software (JAX, PyTorch, GKE), and flexible consumption models, specifically designed for AI workloads.
* **Storage is Critical for AI:** Storage is a crucial piece of the AI data pipeline, and I/O bottlenecks can severely impact GPU/TPU utilization.
* **Typical AI/ML Storage Needs:** Workloads often demand capacity for Terabytes to Exabytes, Terabytes per second throughput, millions of requests per second, low millisecond latency, and handling spiky traffic patterns.
* **Optimized Google Cloud Storage Solutions:**
    * **Anywhere Cache (GA):** Now Generally Available, it allows data stored once (e.g., in a multi-region bucket) to be cached and co-located with compute across an entire continent. It delivers up to 2.5TB/s additional throughput, up to 70% lower read latency, and potentially offers cost savings for up to 70% of multi-region bucket users.
    * **Rapid Storage (Private Preview):** A new high-performance storage class (in Private Preview) built on Colossus, offering ultra-low latency (<1ms random reads/appends after open via gRPC) and high throughput (up to 6TB/s) within a zone. It's ~5x faster than similar competitor products, 10-20x faster than Cloud Storage Standard, with 8x higher initial QPS limits.
    * **Cloud Storage FUSE:** Enables mounting buckets like file systems, integrating with features like Anywhere Cache.
* **High-Performance Parallel File System (PFS) Options:**
    * **Managed Lustre (Allowlist GA):** A new, fully managed, persistent PFS offering based on DDN ExaScaler (Allowlist GA). It delivers up to 1TB/s throughput, <1ms latency, full POSIX compliance, full duplex capabilities (e.g., checkpointing during training), and high per-VM throughput (saturating >20GB/s links).
    * **Parallelstore:** Another PFS option available, often suited for scratch storage needs. Google Cloud offers both to cater to different persistence and workload requirements.
* **Customer Success Examples:**
    * **Snap:** Operates at massive scale on GCP, ingesting 20-30 *trillion* events weekly, processing Exabytes daily, and handling 30PB for A/B tests within hours[cite: 1]. They built a central Lakehouse on GCS and see 100% YoY AI/ML use case growth. Their peak ingestion (75M TPS) highlights the need for high-QPS storage like Rapid Storage.
    * **Anthropic:** Uses Anywhere Cache for resilience and co-locating data with TPUs, achieving up to 2.5TB/s read throughput.
    * **AssemblyAI:** Saw a 10x throughput increase and 15x training performance improvement using high-performance Cloud Storage.
    * **Technology Innovation Institute (TII):** Uses *both* Parallelstore (for 75% of training) and Cloud Storage FUSE (for 25%), demonstrating the value of choosing the right storage per need. They accelerated FalconLLM training using Parallelstore, significantly reducing checkpoint times and improving TCO.

## My Perspective / "Spin"
* **Storage Criticality:** It's common to see initial AI projects prioritize GPUs, only realizing later how suboptimal storage choices bottleneck the entire pipeline and prevent maximizing accelerator utilization. It's encouraging that Google Cloud explicitly addresses storage's critical role and provides clear guidance, translating complex AI workload needs into tangible storage requirements like throughput and latency.
* **Object Storage Performance:** This focus translates into powerful features for those leveraging object storage APIs but demanding higher performance. Innovations like Rapid Storage, Anywhere Cache, GCSFuse enhancements (including the PyTorch connector), and direct gRPC API access deliver significant speed and efficiency gains.
* **Parallel File System Integration:** Simultaneously, Google recognizes that many AI/HPC infrastructures rely heavily on Parallel File Systems (PFS). Managed Lustre is a strategic addition, offering a seamless on-ramp for organizations already invested in Lustre or requiring a traditional distributed file system experience, facilitating easier migration and faster adoption for HPC use cases.

## Related Resources
* Cloud Architecture Center: [Design storage for AI and ML workloads in Google Cloud](https://cloud.google.com/architecture/ai-ml/storage-for-ai-ml)
* Blog [High performance storage innovations for your AI workloads](https://cloud.google.com/blog/products/storage-data-transfer/high-performance-storage-innovations-for-ai-hpc)
* Blog: [Colossus: the secret ingredient in Rapid Storage’s high performance](https://cloud.google.com/blog/products/storage-data-transfer/how-the-colossus-stateful-protocol-benefits-rapid-storage)
* [Anywhere Cache Overview](https://cloud.google.com/storage/docs/anywhere-cache)
* High performance parallel file system [Google Cloud Managed Lustre](https://cloud.google.com/products/managed-lustre?hl=en)
* Cloud Architecture Center: [Optimize AI and ML workloads with Cloud Storage FUSE](https://cloud.google.com/architecture/optimize-ai-ml-workloads-cloud-storage-fuse)

---
*Find more [takeaways](https://github.com/knachiketa04/google-cloud-next-2025-storage-sessions/tree/main/takeaways)*