# Master your enterprise workloads with file storage on Google Cloud - Key Takeaways & Insights

*Session at Google Cloud Next 2025*

## Session Recap
This session explored Google Cloud's enterprise file storage solutions, Google Cloud NetApp Volumes and Filestore, detailing new features for migration, performance, cost optimization, and management, including a customer case study from Scotiabank.

## Key Takeaways
* Google Cloud offers robust file storage options: Google Cloud NetApp Volumes for seamless lift-and-shift of ONTAP workloads, and Filestore for high-performance cloud-native NFS based file storage needs.
* **NEW:** Google Cloud NetApp Volumes now features independent scaling ("Flex") allowing separate provisioning of **capacity (1-300 TiB)**, **throughput (64-5,120 MiB/s)**, and **IOPS (1,024-160,000)**, alongside familiar ONTAP management, auto-tiering, and SnapMirror migration support.
* **NEW:** Filestore enhances TCO with customizable performance and capacity scaling (up and down). Users can select capacity from 1 to 100 TiB and independently provision **IOPS performance (from 4K up to 750K IOPS per instance)**, scaling both capacity and performance up or down as needed. This avoids paying for bundled, potentially unused performance, leading to significant TCO reductions
* Filestore also adds a cost-effective 100GB Basic HDD tier and simplifies management with direct GCE integration.
* **NEW:** Filestore improves network efficiency with **Private Service Connect (PSC) support**, reducing the required IP address allocation from a large range to a single IP per instance per VPC.
* Enterprise readiness is highlighted by the Scotiabank case study, demonstrating successful migration and operation of critical file workloads using NetApp Volumes and GCVE.

## My Perspective / "Spin"
* The independent scaling of capacity, throughput, and IOPS in both NetApp Volumes (Flex) and Filestore is incredibly valuable. Based on experience, workloads often need *either* large capacity *or* high performance, but rarely both at maximum levels simultaneously. This decoupling directly addresses real-world needs and prevents overprovisioning, leading to significant TCO improvements. It's a crucial enhancement for tailoring storage precisely to application requirements. End of the day, it helps optimizing overall TCO.
* Next, the native Vertex AI integration with NetApp Volumes is a genuinely exciting development! This could be a massive door-opener for countless customers sitting on vast amounts of unstructured data within their on-premises NetApp systems. It provides a dramatically simplified pathway to bring that data into Google Cloud (via NetApp Volumes) and immediately leverage it for powerful AI use cases – think creating vector embeddings, enabling semantic search, and rapidly building out generative AI pipelines without complex data migrations first. This integration bridges the gap between existing enterprise data and cutting-edge AI capabilities.
* Finally, the Scotiabank reference remains powerful validation for other regulated enterprises considering file storage adoption on Google Cloud.

## Related Resources
*Find more [takeaways](https://github.com/knachiketa04/google-cloud-next-2025-storage-sessions/tree/main/takeaways)*