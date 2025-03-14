# 📘 Educhain Cookbook Repository

Welcome to the **Educhain Cookbook Repository**! Your one-stop resource for creating quizzes, study guides, and more using AI. Below is a quick-access table to navigate through the categories. 👇

-----

## 🗂️ Quick Navigation

| **Category**            | **Description**                         | **Dropdown**                       |
|--------------------------|-----------------------------------------|-------------------------------------|
| 🔥 **Core Features**    | Advanced features of Educhain.          | [Explore Features](#core-features) |
| 🌐 **Multilingual**      | Quizzes in multiple languages.          | [Explore Multilingual](#multilingual) |
| 🛠️ **Quiz Generators**   | Automatically generate quizzes.         | [Explore Quiz Generators](#quiz-generators) |
| 🌟 **Starters**          | Beginner-friendly guides to get started. | [Explore Starters](#starters)      |
| 🛡️ **Providers**         | AI model integrations.                  | [Explore Providers](#providers)    |
| ⚡ **World’s Fastest Quiz** | Test Educhain’s speed with this notebook. | [Explore World's Fastest Quiz](#worlds-fastest-quiz) |
| 📹 **LiveKit Integration** | Video and audio streaming in classrooms. | [Explore LiveKit Integration](#livekit-integration) |

---

## 🔥 Core Features
Explore Educhain's powerful tools to enhance your learning experience:
- [Generate MCQs from Data (v3)](features/Generate_MCQs_from_Data_Educhain_v3.ipynb)
- [Generate Flashcards (Basics)](features/Generate_flashcards_basics.ipynb)
- [Generate Questions from YouTube](features/Generate_questions_from_youtube.ipynb)
- [Career Connection Quiz Generator](features/educhain_career_connection.ipynb)
- [Generate Lesson Plans](features/educhain_generate_lesson_plan.ipynb)
- [Generate Study Guides](features/educhain_generate_study_guide.ipynb)

---

## 🌐 Multilingual
Break language barriers with Educhain:
- [Generate Quizzes in Indic Languages (v3)](multilingual/educhain_indic_languages_v3.ipynb)

---

## 🛠️ Quiz Generators
Create quizzes from a variety of sources:
- [Convert Any Webpage to a Quiz](quiz_generators/Convert_any_webpage_to_quiz.ipynb)
- [Generate Quizzes from Transcripts](quiz_generators/Generate_quiz_using_transcripts_and_educhain.ipynb)
- [Convert Long PDFs to Quizzes](quiz_generators/Long_PDFs_to_Quiz.ipynb)
- [Quiz on Latest News (v3)](quiz_generators/Quiz_on_Latest_News_v3%20(1).ipynb)

---

## 🌟 Starters
Begin your Educhain journey with ease:
- [Educhain Starter Guide (v3)](starters/Educhain_Starter_Guide_V3.ipynb)
- [Starter Guide for Question Generation](starters/Starter_guide_question_generation.ipynb)
- [Educhain Starter Guide (v3)](starters/educhain_Starter_guide_v3.ipynb)

---

## 🛡️ Providers
Integrate Educhain with cutting-edge AI models:
- [Claude 3.5 Sonnet Integration](providers/educhain_claude3_5_sonnet.ipynb)

---

## ⚡ World’s Fastest Quiz
Experience the speed of Educhain:
- [Educhain World's Fastest Quiz](educhain_worlds_fastest_quiz.ipynb)

---

## 📹 LiveKit Integration
Enhance your classroom experience with video and audio streaming:
- [LiveKit SDK Integration](livekit_integration/livekit_sdk_integration.ipynb)

---

## 🚀 Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/satvik314/educhain
   ```
2. Navigate to the folder:
   ```bash
   cd educhain/cookbook
   ```
3. Open the desired `.ipynb` file in your Jupyter Notebook environment and start creating!

---

## ✨ Features Highlights
- **Comprehensive Quiz Creation**: Generate quizzes from PDFs, web pages, YouTube videos, and transcripts.
- **Multilingual Capability**: Create quizzes in Indic languages.
- **Custom Flashcards and Study Guides**: Tools tailored for personalized learning.
- **Fast and Efficient**: World’s fastest quiz generation engine included.
- **AI Integration**: Seamless integration with Claude 3.5 Sonnet and more.
- **LiveKit Integration**: Video and audio streaming in classrooms.

---

## 📹 LiveKit SDK Integration Example

LiveKit SDK allows for seamless video and audio streaming in classrooms. Here's a brief example of how to use the LiveKit SDK in your classroom application:

```python
from livekit import Room, LocalParticipant, RemoteParticipant

# Initialize LiveKit Room
room = Room(url="your_livekit_server_url", token="your_access_token")

# Join the room
local_participant = room.join()

# Handle remote participants
def on_participant_connected(participant: RemoteParticipant):
    print(f"Participant {participant.identity} connected")

room.on("participantConnected", on_participant_connected)

# Publish local video and audio tracks
local_participant.publish_video_track("path_to_video_file")
local_participant.publish_audio_track("path_to_audio_file")

# Subscribe to remote tracks
def on_track_subscribed(track, publication, participant):
    print(f"Subscribed to {track.kind} track from {participant.identity}")

room.on("trackSubscribed", on_track_subscribed)

# Leave the room
room.leave()
```

### Benefits of Using LiveKit for Live Streaming in Educational Settings

- **Real-time Interaction**: Engage with students in real-time, making the learning experience more interactive and dynamic.
- **High-Quality Streaming**: Ensure high-quality video and audio streaming for a seamless classroom experience.
- **Scalability**: Easily scale your classroom sessions to accommodate a large number of participants.
- **Flexibility**: Integrate LiveKit with various educational tools and platforms to enhance the overall learning experience.

---

Happy learning! 🎉
