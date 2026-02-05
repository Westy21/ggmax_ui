AI Liquid is a real-time audio visualizer that renders a fluid, organic blob animation driven by audio input streamed over WebSocket.

Core Features

•  WebSocket PCM16 Audio Streaming: Connects to a backend server (default ws://localhost:8765) to receive raw 16-bit PCM mono audio data at 16kHz
•  Ultra-Low Latency Playback: Uses AudioWorklet (with ScriptProcessor fallback) for minimal audio latency
•  Frequency-Reactive Visualization: A soft-body liquid simulation responds to bass, mid, and treble frequency bands—bass causes radial pulsing, treble adds tangential motion
•  Interactive Canvas: Users can click and drag the blob to deform it; this gesture also resumes the AudioContext (required by browsers)

Technical Highlights

•  Soft-body physics: 64 control points with Verlet integration, distance constraints, and area preservation
•  Visual effects: Radial gradients, specular highlights, blurred shadows, and a glassmorphism frame
•  Configurable parameters: Responsiveness, damping, viscosity, bass/treble sensitivity via UI sliders
•  Dual audio path: Prefers AudioWorklet for performance; gracefully degrades to ScriptProcessorNode

Use Case

Ideal for AI voice assistant interfaces, music visualizers, or any application needing a visually appealing, audio-reactive UI element.
<img width="2970" height="1674" alt="image" src="https://github.com/user-attachments/assets/875400c4-0b30-4205-8cee-9ff860484d35" />
