Sign Language Generator:- AI-powered system that converts YouTube video audio → ASL Gloss → Pose-Animated Sign Language Video
Project Overview:
Sign Language Generator is an AI-driven web application that converts spoken content from any YouTube video into an American Sign Language (ASL) pose-animated video.
The system extracts audio, transcribes speech using Whisper, converts English sentences into ASL gloss using Gemini AI, and finally maps each gloss token to a pre-generated pose-based sign language video generated using MediaPipe + OpenCV.
This project supports:
1.ASL Alphabet (Fingerspelling) generation
2.WLASL 2000+ word-level dataset processing
3.Smooth pose rendering using MediaPipe
4.Automatic gloss generation
5.Token-to-video stitching
6.Full caption & transcript display
7.Streamlit UI

Key Features
 1. Speech-to-Text (Whisper Model)
 2. Extracts clean audio using yt-dlp
 3. Transcribes using Whisper (base model)
 4. ASL Gloss Generation (Google Gemini API)
 5. Converts English → ASL gloss following:
      TIME–TOPIC–COMMENT grammar
      Uppercase gloss format
      FS- prefix for fingerspelling
      Returns JSON structure for clean parsing
6. Pose-Based Sign Video Generation
7. Using MediaPipe Pose, the system:
      Processes WLASL videos
      Extracts body landmarks
      Draws colored skeletons on a black canvas
      Saves each word as a separate MP4 clip
      Also converts GIFs and images for fingerspelling set

8. Gloss Token Processing Splits gloss into individual tokens
9. Handles pauses. Supports fingerspelling (FS-A, FS-B, …).Generates fallback pause clip for missing words
10. Final Video Rendering
      Combines all sign clips
      Adds captions
      Exports final ASL video to /output_videos/

11. User Interface (Streamlit)
     YouTube URL input
     Gemini API key
     Live transcript + gloss visualization
     Progress indicators
     Download final video
