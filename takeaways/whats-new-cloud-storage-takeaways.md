# What's new in Cloud Storage - Key Takeaways & Insights
[YouTube Link](https://youtu.be/owvXIIl8LdU?si=LPvnlp3pxAnPtnL4)  

*Session at Google Cloud Next 2025*

## Session Recap 
This session covered seven key areas of innovation across Google Cloud Storage, driven heavily by the demands of AI and analytics, while also focusing on simplifying cloud migration and data protection. Key announcements included Rapid Storage, Managed Lustre, the GA of Storage Intelligence and Anywhere Cache, and updates to NetApp Volumes and Filestore.

## Key Takeaways
* **Rapid Storage Announced:** A new zonal GCS bucket type offering extremely low latency (<1ms reads), high throughput (up to 6 TB/s), and high QPS by providing direct API access to Google's underlying Colossus file system, optimized for demanding AI/ML workloads (5x better performance than competitors claimed).
* **Managed Lustre Launched (via DDN Partnership):** Google Cloud now offers Lustre, the gold-standard parallel file system for HPC and AI, as a first-party managed service, simplifying deployment and management for high-throughput, low-latency file access.
* **Storage Intelligence is GA - with Agentic AI Vision:** This service provides an enterprise-wide view of storage (cost, usage, security insights) and enables easy actions like single-click bucket moves. **Crucially, the future vision demonstrated powerful agentic AI capabilities, using Gemini to understand natural language requests (e.g., "find all factory images with safety hazards and ensure they are protected") and orchestrate multi-step, content-aware actions like filtering, moving data, and applying security settings automatically.** A 30-day free trial for current GA features is available. [Link](https://cloud.google.com/storage/docs/storage-intelligence/overview)
* **Anywhere Cache is GA:** Acts like a "turbo button" for GCS, providing a fully managed, SSD-backed local read cache. It significantly reduces read latency (up to 70% for regional, 96% for multi-regional buckets demonstrated) and can lower egress costs, improving compute efficiency for data lake and analytics workloads. Includes observability and a recommendation engine.
* **Migration & Modernization Boosted:**
    * *Google Cloud NetApp Volumes:* Now supports SnapMirror for easier migration from on-prem NetApp, and features a new Vertex AI connector to leverage AI services directly on migrated file data.
    * *Filestore:* Offers independent scaling of capacity (1-100 TiB) and performance (4k-750k IOPS) for better cost optimization.
    * *Google Cloud Backup:* Provides centralized backup management across workloads (GCE, GCVE, Databases+) with ransomware protection via immutable Backup Vaults and an integrated GCE experience.

## My Perspective / "Spin"
* From experience with large customers, AI workloads (especially training) are pushing storage boundaries, demanding performance at massive scale (PiB+) with diverse datasets (mixed large/small files). The significant enhancements targeting high read throughput and low latency – **Rapid Storage, Anywhere Cache, and GCS Fuse updates** – directly address these critical needs.
* Many customers rely on existing POSIX-based applications or lack time for refactoring. The launch of **Managed Lustre** as a first-party service provides a timely, high-performance parallel file system option for these scenarios.
* The **Agentic AI capability envisioned for Storage Intelligence** is particularly exciting. For organizations managing billions or trillions of objects, the ability to easily analyze and automate complex, content-aware tasks (like optimizing data locality near compute resources) using natural language is a game-changer.
* Unlocking the potential of vast unstructured data still residing on-premises is crucial. The pathway provided by **Google Cloud NetApp Volumes (with SnapMirror migration) integrating directly with Vertex AI** offers a powerful solution for migrating *and* modernizing.
* **Filestore's** introduction of independent capacity and performance scaling is a welcome and timely update, providing much-needed flexibility for dynamic workloads, especially common within GKE environments.
* Finally, the simplicity and enhanced security within **Google Cloud Backup** are highly valuable. Features like easy policy setup, integrated GCE experience, immutable Backup Vaults, and the protection summary dashboard significantly improve data protection posture for GCP customers.

## Related Resources
* Blog [High performance storage innovations for your AI workloads](https://cloud.google.com/blog/products/storage-data-transfer/high-performance-storage-innovations-for-ai-hpc)
* Blog: [Colossus: the secret ingredient in Rapid Storage’s high performance](https://cloud.google.com/blog/products/storage-data-transfer/how-the-colossus-stateful-protocol-benefits-rapid-storage)
* [Anywhere Cache Overview](https://cloud.google.com/storage/docs/anywhere-cache)
* High performance parallel file system [Google Cloud Managed Lustre](https://cloud.google.com/products/managed-lustre?hl=en)
* [Storage Intelligence Overview](https://cloud.google.com/storage/docs/storage-intelligence/overview)
* NetApp Press Release: [NetApp Partners With Google Cloud to Simplify Scaling High-Performance Workloads in the Cloud](https://www.netapp.com/newsroom/press-releases/news-rel-20250409-420785/)
* [Google Cloud NetApp Volumes Documentation](https://cloud.google.com/netapp/volumes/docs/discover/overview)
* [Filestore Custom Performance](https://cloud.google.com/filestore/docs/custom-performance)
* [Backup vault for immutable and indelible backups](https://cloud.google.com/backup-disaster-recovery/docs/concepts/backup-vault)

---
*Find more [takeaways](https://github.com/knachiketa04/google-cloud-next-2025-storage-sessions/tree/main/takeaways)*