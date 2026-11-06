
# ADR-001: Continuous Speech Translation Engine

Status: Accepted - Pending Technical Validation

## Objective
Build a continuous real-time speech-to-speech
translation system for smart glasses.

## Primary Model
Meta SeamlessStreaming (2.5B parameters)

## Foundation Model
SeamlessM4T v2

## Reason
- Supports simultaneous speech translation.
- Generates translations before the speaker finishes.
- Supports speech-to-speech and speech-to-text.
- Uses Efficient Monotonic Multihead Attention (EMMA).
- Designed for low-latency translation.

## Initial Language Pairs
- English -> Vietnamese
- Vietnamese -> English

## Architecture
Continuous Audio Capture
-> Audio Buffering
-> SeamlessStreaming Inference
-> Incremental Translation Output
-> Audio Playback

## Technical Risks
- High computational requirements.
- Streaming speech-output language coverage.
- Latency and audio synchronization.
- Model licensing.
- Hardware compatibility.

## Validation
- Test Vietnamese speech output.
- Benchmark both translation directions.
- Measure end-to-end latency.
- Test 10-minute continuous sessions.

## Future Consideration
Evaluate the unified Seamless model.
