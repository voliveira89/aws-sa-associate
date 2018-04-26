# EC2 Instance Types

| **Family** | **Specialty** | **Use Case** | **Type** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| H1 | Cheap Storage | Log or data processing applications \(Kafka\) / Big data workload clusters | Storage Optimized |
| D2 | Dense Storage | File Servers / DWH / Hadoop | Storage Optimized |
| R4 | Memory Optimized | Memory Intensive / DBs | Memory Optimized |
| M4, M5 | General Purpose | Application Servers | General Purpose |
| C4, C5 | Compute Optimized | CPU Intensive Apps, DBs | Compute Optimized |
| G2, G3 | Graphics Intensive | Video Encoding / 3D Application Streaming | Accelerated Computing |
| I2, I3 | High speed storage \(IOPS\) | NoSQL DBs, DWH | Storage Optimized |
| F1 | Field Programmable Gate Array | Hardware acceleration of Code | Accelerated Computing |
| T2 | Lowest Cost, General Purpose | Web Servers/ Small DBs | General Purpose |
| P2, P3 | Graphics / General Purpose GPU\[Parallel Processing\] | Machine Learning / Bitcoin Mining | Accelerated Computing |
| X1, X1e | Memory Optimized | SAP HANA / Apache Spark | Memory Optimized |

**DRH MCGIFT PX**

* D – Density
* R – RAM
* H - HDD
* M – Main choice for general purpose apps
* C – Compute
* G – Graphics
* F – FPGA
* T – Cheap general purpose \(T2 micro\)
* P – Graphics \(pics\)
* X – Extreme Memory

**Virtualization Types**

* **Para-virtualization \(PV\)** - Used to be the recommended choice, as it gave you better performance \(with a much closer integration to the virtualization host, through patched specialized kernels/drivers on both the host and the guest\).
* **Hardware-assisted virtualization \(HVM\) **- Uses the benefits provided in modern hardware, and it doesn't require any kind of custom kernel or patches.

**Linux Instances**

* Default Linux EC2 username is ec2-user

**Windows Instances**

* To connect to a Windows Instance, you have to use Remote Desktop that uses the Remote Desktop Protocol \(RDP\)
  * From Windows use the command mstsc
  * From MacOS use Microsoft Remote Desktop
  * From Linux use rdesktop
* Default Windows EC2 username is Administrator

  


