# Foreign-Whispers

## Sections

- [About](#about)
- [Example Outputs](#example)
- [How to Use](#usage)
- [Hugging Face Space](#space)

## About <a id="about"></a>

Takes a video as input and outputs the same video with both spoken and written subtitles in Spanish, replicating each individual voice. Utilizes OpenAI Whisper, Opus NLP, Pyannote and xTTS models.

### Approaches

- Audio stetching/shrinking

To match the video length, the script speeds up the audio in specific sections. This approach ensures that the translated speech fits within the given timestamps for each speaker's segment.

- Frame adding/deleting

To allow the voice playback to play naturally, the script determines time interval differences and triggers markers for additional frames that need to be inserted or removed.

## Examples <a id="example"></a>

### Audio Speed Manipulation

https://github.com/user-attachments/assets/98b8c054-b45d-4fc3-95a3-005702de68f9

### Audio Speed + Frame Manipulation

https://github.com/user-attachments/assets/a4e57fcd-b4d1-4b4c-af32-236445a444ca

<a href="https://github.com/user-attachments/assets/a4e57fcd-b4d1-4b4c-af32-236445a444ca" target="_blank">
  <img src="https://github.com/user-attachments/assets/3f5cb49a-cb3a-428f-b1cb-6dd0de5992d8" alt="Video Thumbnail" style="width:300px;height:200px;">
</a>


## How to use: <a id="usage"></a>

Before running the script, ensure you have Python installed on your machine. You can download Python from the [official website](https://www.python.org/downloads/). 

1. Clone the repository to your local machine

```
git clone https://github.com/RobCaamano/foreign-whispers.git
```

2. Navigate to the project directory and download 'requirements.txt'. It is recommended to do this in a virtual environment. For information about creating and using conda environments, visit their [site](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html).

```
cd '[path to dir]'
pip install -r requirements.txt
```

3. This script is best used with a GPU for acceleration. To do this, you need to have a GPU with CUDA support and the appropriate CUDA toolkit installed. Follow the [CUDA installation guide](https://docs.nvidia.com/cuda/cuda-installation-guide-microsoft-windows/index.html) for details.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Note:** The time required for the script to complete depends on the computational power of your GPU.

6. Run the script in your virtual environment, providing the url through command line argument

```
python ./main.py "[url]"
```

## Huggingface Space <a id="space"></a>

[link](https://huggingface.co/spaces/Samin-Rob/FOREIGN-WHISPERS)
