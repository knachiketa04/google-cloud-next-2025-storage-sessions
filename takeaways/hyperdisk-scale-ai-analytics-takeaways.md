# Efficiently Scale Storage for AI and analytics workload with Hyperdisk - Key Takeaways & Insights

[YouTube Link](https://youtu.be/hVXCWWa0lyA?si=C8KU31rKc8cH-3om)  
*Session at Google Cloud Next 2025*

## Session Recap
This session detailed Google Cloud's next-generation block storage, Hyperdisk, focusing on its different types, the significant efficiency gains offered by Storage Pools, and how it enables dynamic scaling for demanding AI and analytics workloads. Customer examples from Sentry and Hudson River Trading highlighted practical benefits, and the roadmap showcased future advancements like Exapools for massive scale.

## Key Takeaways
* **Hyperdisk is Google Cloud's Next-Gen Block Storage:** Optimized for diverse workloads (Balanced, Throughput, Extreme, ML) and essential for 4th gen compute. Key features include independent tuning of capacity/performance, instant snapshots/replication, and Hyperdisk ML for accelerated data loading.
* **Storage Pools Drive Efficiency & Cost Savings:** Hyperdisk Pools (up to 5 PB for Balanced, Throughput, Extreme) enable thin provisioning for capacity and performance. This allows provisioning for aggregate workload needs, simplifying management and significantly reducing TCO (customers like HRT reported 50% savings) compared to provisioning individual disks for peak requirements.
* **Shift Towards Dynamic, Pooled Infrastructure:** Large-scale AI/Analytics demands are pushing towards a "Cloud in a Cloud" model. Instead of static per-workload planning, dynamic, orchestrated infrastructure using pooled resources like Hyperdisk is needed to handle variable demands efficiently.
* **Real-World Validation (Sentry & HRT):** Sentry utilizes tiered Hyperdisk (Balanced/Throughput) pools for a unified analytics platform, benefiting from cost savings and performance tuning. Hudson River Trading leverages pools with auto-scaling compute (DWS) for dynamic ML training, reducing queue times drastically and cutting storage costs by 50% compared to standard Hyperdisk.
* **Future is Exabyte-Scale & Faster Loading:** Hyperdisk ML is becoming faster and more integrated (Gen 4 attach preview, GKE volume populators soon). Introducing **Exapools** (Preview Q2) built on Hyperdisk Balanced/Throughput, offering a unified block storage environment for massive scale (up to 2.5 EB capacity, 5 TB/s throughput).

## My Perspective / "Spin"
* The detailed customer case studies from Hudson River Trading (HRT) and Sentry were particularly impactful, showcasing concrete examples of how Hyperdisk pools deliver significant efficiency and cost savings (HRT reported 50% cost reduction using pools).
* It was insightful to see how Hyperdisk isn't used in isolation, but as part of a tiered strategy alongside Local SSD for caching and Cloud Storage for long-term data, demonstrating architectural flexibility.
* The introduction of Exapools, promising multi-exabyte scale (up to 2.5 EB) and massive throughput (5 TB/s) for block storage, is truly astonishing, marking a huge leap from historical storage capacities. While only relevant for the largest workloads today, it signals the future direction.
* These advancements align with the growing trend of customers adopting Hyperdisk alongside Google Cloud's latest compute generations.
* However, adopting concepts like advanced pools, thin provisioning, and managing quotas might require a learning curve for teams new to this model. Thorough evaluation against specific use cases is crucial for success.
* The upcoming integration to automate data hydration from Cloud Storage to Hyperdisk ML via GKE is a practical enhancement that will streamline AI/ML data loading workflows.

## Related Resources
* Hyperdisk [Documentation](https://cloud.google.com/compute/docs/disks/hyperdisks)
* Blog: [Driving enterprise transformation with new compute innovations and offerings](https://cloud.google.com/blog/products/compute/delivering-new-compute-innovations-and-offerings)
* Blog: [Want to save on GKE block storage costs? Hyperdisk Storage Pools can help](https://cloud.google.com/blog/products/storage-data-transfer/hyperdisk-storage-pools-optimizes-gke-block-storage)

---
*Find more [takeaways](https://github.com/knachiketa04/google-cloud-next-2025-storage-sessions/tree/main/takeaways)*