An office security agency conducted a successful pilot using 100 cameras installed at key locations within the main office. Images from the cameras were uploaded to Amazon S3 and tagged using Amazon Rekognition, and the results were stored in Amazon ES. The agency is now looking to expand the pilot into a full production system using thousands of video cameras in its office locations globally. The goal is to identify activities performed by non-employees in real time  
Which solution should the agency consider?  

A. Use a proxy server at each local office and for each camera, and stream the RTSP feed to a unique Amazon Kinesis Video Streams video stream. On each stream, use Amazon Rekognition Video and create a stream processor to detect faces from a collection of known employees, and alert when non-employees are detected.

B. Use a proxy server at each local office and for each camera, and stream the RTSP feed to a unique Amazon Kinesis Video Streams video stream. On each stream, use Amazon Rekognition Image to detect faces from a collection of known employees and alert when non-employees are detected.

C. Install AWS DeepLens cameras and use the DeepLens_Kinesis_Video module to stream video to Amazon Kinesis Video Streams for each camera. On each stream, use Amazon Rekognition Video and create a stream processor to detect faces from a collection on each stream, and alert when non-employees are detected.

D. Install AWS DeepLens cameras and use the DeepLens_Kinesis_Video module to stream video to Amazon Kinesis Video Streams for each camera. On each stream, run an AWS Lambda function to capture image fragments and then call Amazon Rekognition Image to detect faces from a collection of known employees, and alert when non-employees are detected.

My answer: C

---
## Incorrect Answer

Unfortunately, your answer **C** is incorrect. The correct answer is **A. Use a proxy server at each local office and for each camera, and stream the RTSP feed to a unique Amazon Kinesis Video Streams video stream. On each stream, use Amazon Rekognition Video and create a stream processor to detect faces from a collection of known employees, and alert when non-employees are detected.**

## Explanation

The key requirements in this scenario are:

1. Identify activities performed by non-employees in real-time.
2. Scale to thousands of video cameras across multiple office locations globally.

Option **A** addresses these requirements by leveraging the following components:

- **Proxy server at each local office**: This allows for efficient and secure streaming of video feeds from cameras within the local office network.
- **Amazon Kinesis Video Streams**: A fully managed AWS service for ingesting and processing video streams in real-time.
- **Amazon Rekognition Video**: A computer vision service that can analyze video streams in real-time to detect and recognize faces, objects, activities, and more.
- **Stream processor**: A feature of Amazon Rekognition Video that allows you to process and analyze video streams as they are ingested by Kinesis Video Streams.

By using a unique Kinesis Video Stream for each camera and creating a stream processor with Amazon Rekognition Video, the agency can detect faces from a collection of known employees and alert when non-employees are detected, fulfilling the real-time requirement.

The other options you provided have limitations or do not fully address the requirements:

- **B**: This option uses Amazon Rekognition Image instead of Amazon Rekognition Video, which is not suitable for real-time video analysis.
- **C**: AWS DeepLens cameras are designed for edge-based computer vision and may not be suitable for a large-scale deployment across multiple office locations.
- **D**: This option also uses AWS DeepLens cameras and involves capturing image fragments and calling Amazon Rekognition Image, which is not optimal for real-time video analysis.

#Claude3-sonnet 