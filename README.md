# tennis-shot-analysis-ai
  
This is a code for analyzing tennis shots using BlazePose.
  
## Preparation
---
Tennis videos need to be prepared in advance. Here are the requirements:  
1) The video size should not be too large  
In the provided program, when splitting the GIF, all converted GIF frames need to be loaded into memory. Therefore, it is necessary to pre-split very large videos (more than 10 minutes, for example).  
2) Should be only one person in the video  
It is desirable to have only one person in the video whenever possible. If other people appear in the video, there is a possibility that their skeletons might be mistakenly extracted. It should be fine if the opponent is at a considerable distance, but without trying it, it is difficult to ascertain the accuracy.  
3) The video should be in MOV or MP4 format.  
4) Regarding the camera angle  
The program includes a process to correct the camera angle. However, if certain parts are obscured by the body, there is a possibility that the skeleton detection might not accurately determine their positions. Therefore, it is preferable to shoot the video from a consistent angle as much as possible. Additionally, it is desirable for the entire body to be visible in the video.  
5) Regarding the video quality  
There are no specific requirements for image quality or size. The quality similar to the videos you previously provided should be sufficient. Low-quality videos (lower quality than a smartphone's front camera) may affect the accuracy of the results.  
6) Regarding the frame rate  
There is usually no need to be concerned about normal motion, but for movements that cause motion blur (such as high-speed serves), consider recording at a higher frame rate. High-speed cameras or the slow-motion camera on an iPhone are suitable for this purpose.  
Additionally, it is possible to add more video files later on.  
  
## Environments
---
Run the notebook under "codes" folder  on Google Colaboratory.  
  
### About Google Colaboratory  
  
Google Colaboratory is a free-to-use Python execution environment (paid options available). You don't need any special preparations other than a Google account. However, there are separate requirements in the following cases:
  
1) Insufficient Google Drive storage space:
Since Colab cannot directly handle data on your computer, you need to upload it to Google Drive. Therefore, concerns about limited capacity may arise when working with video files in this project. If your Google Drive storage exceeds the free range of 15GB, please consider purchasing additional storage.

2) Insufficient memory leading to a usage limit warning:
When processing extremely large-sized files or a large number of files, there is a possibility of exceeding the specifications of the free-to-use PC. In such cases, please consider performing the processing in smaller batches or exploring other methods.
  