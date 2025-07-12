# UpAndDown-SpatialAudio

A spatial audio and immersive 360° video project exploring audio localization for virtual and augmented reality experiences. This was developed as a research and creative media collaboration between Colby Weiser and Isaac Munoz at San Diego State University.

---

## 🎵 Project Summary

This project demonstrates spatialized music recording using a 360° Ricoh Theta camera and Sennheiser Ambeo VR mic. It features the song **"Up and Down"** performed live and mixed in Reaper for ambisonic playback.

**Contributors:**
- 🎸 Colby Weiser – Guitarist, audio mixing, Unity integration
- 🎤 William Andrea – Vocalist
- 🎓 Isaac Munoz – Research supervisor (SDSU)

---

## 📂 Folder Structure

UpAndDown-SpatialAudio/
├── stems/ # Raw multi-track audio (Take #8)
├── mixes/ # Mastered & binaural audio
├── binural/ # Binaural syncs for 360 video export
├── docs/ # Papers, instructions, session notes
├── README.md # Project overview and documentation
├── LICENSE # Usage license
└── .gitignore


---

## 📺 Watch the 360° YouTube Video

[![Watch on YouTube](https://img.youtube.com/vi/6qshsljUsrQ/0.jpg)](https://www.youtube.com/watch?v=6qshsljUsrQ)

> 🔗 https://www.youtube.com/watch?v=6qshsljUsrQ  
> 🎧 Best experienced with headphones to hear the full spatial audio effect.

---

## 🛠 Tools Used

- 🎚️ [Reaper DAW](https://www.reaper.fm/)
- 🎧 [Sennheiser Ambeo A-B Converter](https://en-us.sennheiser.com/ambeo-abconverter)
- 🧠 [IEM Binaural Decoder](https://plugins.iem.at/)
- 📽️ [FFmpeg](https://ffmpeg.org/download.html)
- 🛠️ [Google Spatial Media Metadata Injector](https://github.com/google/spatial-media/releases/tag/v2.1)
- 🕹️ [Unity + Oculus Spatializer Plugin](https://developer.oculus.com/documentation/unity/audio-osp-unity-req-setup/)

---

## 📦 Export Instructions

### 1️⃣ Merge 360 Video with Ambisonic Audio

```bash
ffmpeg -i Take8_R0010410_er.MP4 -i AmbiX.wav -map 0:v -map 1:a -c:v copy -c:a copy output_360.mov

2️⃣ Inject Metadata for Spatial Audio (YouTube Compatible)
Download Google’s Spatial Media Metadata Injector, then:

bash
Copy
Edit
python spatialmedia -i --stereo=none --spatial_audio output_360.mov final_output_with_metadata.mov
This ensures YouTube recognizes the video as 360° with spatial audio.

📜 Attribution & License
This project may be used for non-commercial research, education, and demo purposes.

Supervised by Isaac Munoz
Attribution for media:

Guitar: Colby Weiser

Vocals: William Andrea

🚧 Future Work
Unity scene integration (VR headset support)

Experiment with real-time spatial mixing

Deployment on Oculus or other immersive platforms

yaml
Copy
Edit

---

### 📥 How to Use:

In Terminal:

```bash
nano README.md
