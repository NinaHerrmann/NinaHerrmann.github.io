---
layout: page
title: Exploring High- and Low-Level Approaches for GPGPU Processing of Telescope Data.
description: Master thesis
img: assets/img/process.pdf
importance: 1
category: work
related_publications: false
---

<a href="assets/pdf/masterthesis.pdf"><i class="fa-solid fa-file-pdf"></i></a>

Telescope data needs to be processed before it can be used for further analysis.
The focused on a specific polyphase filterbank that applies a FIR-filter and a fast Fourier transformation.
To analyse this data in real time parallel processing is irreplaceable.

The work compared the high-level parallel programming framework Muesli with a low-level implementation.
Tested Settings:

| Setting Number | Data size                        | Channels | Taps | Number of Multiplications for the FIR-filter | Iterations FFT | Number of FFT steps |
|----------------|----------------------------------|----------|------|----------------------------------------------|----------------|---------------------------|
| 1.1      | 134,217,728 | 16       | 32   | 4,294,967,296                                | 4              | 536,870,912               |
| 1.2      | 134,217,728 | 64       | 16   | 2,147,491,584                                | 6              | 805,309,344               |
| 1.3      | 134,217,728 | 2048     | 8    | 1,073,741,824                                | 11             | 1,476,400,464             |
| 1.4     | 134,217,728 | 32768    | 4    | 536,872,896                                  | 15             | 2,013,273,360             |
| 2.1      | 201,326,592 | 16       | 32   | 6,442,450,944                                | 4              | 805,306,368               |
| 2.2      | 201,326,592 | 64       | 16   | 3,221,225,472                                | 6              | 1,207,959,552             |
| 2.3      | 201,326,592 | 2048     | 8    | 1,610,612,736                                | 11             | 221,459,249               |
| 2.4      | 201,326,592 | 32768    | 4    | 805,306,368                                  | 15             | 3,019,898,880             |
| 3.1      | 268,435,456 | 16       | 32   | 8,589,934,592                                | 4              | 1,073,741,824             |
| 3.2      | 268,435,456 | 64       | 16   | 4,294,967,296                                | 6              | 1,610,612,736             |
| 3.3      | 268,435,456| 2048     | 8    | 2,147,483,648                                | 11             | 2,952,790,016             |
| 3.4      | 268,435,456 | 32768    | 4    | 1,073,741,824                                | 15             | 4,026,531,840             |

<img src="assets/img/lowhigh.png" alt="Comparison Low-level High-level" width="500" height="333">
<img src="assets/img/results.png" alt="Comparison All Results" width="500" height="333">
