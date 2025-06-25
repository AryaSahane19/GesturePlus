🚀 GesturePlus
GesturePlus bridges the gap between gesture-based and traditional input methods, promoting broader adoption of multimodal interaction systems.

✨ Overview
GesturePlus: A Hands-Free Revolution in Human-Computer Interaction
GesturePlus is a pioneering system that transforms how users interact with computers by leveraging advanced machine learning and computer vision technologies. It provides a hands-free, intuitive interface through gesture control, voice commands, and a chatbot module.

Designed for environments where sterility or accessibility is critical, GesturePlus ensures real-time responsiveness and user-friendly experiences across major operating systems: Windows, Linux, and macOS.

🧠 Core Algorithms
1️⃣ Gesture Recognition Algorithm
Captures video frames using OpenCV.

Preprocesses frames (e.g., horizontal flip, color-space normalization).

Uses MediaPipe to detect up to 2 hands and extract 21 landmarks per hand.

Calculates spatial distances/ratios using NumPy and math to determine finger states.

Applies bitwise encoding to match gestures like FIST, PALM, V_GEST, etc.

Implements temporal smoothing to ensure accuracy.

Executes actions (e.g., mouse movement, scroll, click) via pyautogui.

Uses OS-specific libraries for system controls like:

osascript for macOS

alsaaudio, xrandr for Linux

pycaw, screen_brightness_control for Windows

2️⃣ Voice Command Processing Algorithm
Captures real-time audio using a custom SpeechThread (QThread).

Adapts to ambient noise and streams audio to SpeechRecognition using Google’s API.

Recognized text is parsed in the VoiceAssistant class to detect keywords and intents.

Supports commands like "search", "open", "time", etc.

Triggers system actions and gesture module activation.

Uses pyttsx3 for text-to-speech feedback.

Includes noise resilience and context-awareness using thresholding and directory stack logic.

3️⃣ Parallel Processing
Uses Python’s multiprocessing to run gesture and voice modules on separate CPU cores.

Prevents latency and resource bottlenecks.

Improves performance, responsiveness, and maintainability.

Managed via run_parallel.py.

4️⃣ Resource Monitoring
Implements real-time system performance tracking using psutil.

Monitors CPU, memory, and I/O at 1-second intervals.

Calculates throughput from delta differences in I/O counters.

Visualizes data using Plotly interactive charts.

Ensures system stability and optimization under heavy loads.

📄 Research Paper
🔗 DOI: 10.47191/ijcsrr/V8-i5-57

🔍 Index Copernicus
