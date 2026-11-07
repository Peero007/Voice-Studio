# Voice Studio

A browser-based voice recorder and enhancer. Record or upload audio, remove background noise, and shape the tone toward a polished studio sound. Everything runs locally in the browser. No audio is uploaded anywhere.

## Features

- Record from the microphone, or upload an audio file
- Spectral noise reduction learned from the quietest parts of the recording
- Gate between words, rumble cut, and 50/60 Hz hum removal
- Tone controls: warmth, mud cut, presence, air, de-ess, compression, output gain
- Presets, live A/B between original and enhanced, waveform view
- Export as WAV, normalized to -1 dB peak

## Tips

Stay silent for about 2 seconds at the start of a recording so the denoiser can learn the room. Record 10 to 15 cm from the mic in a soft, furnished room.

## Run locally

It is a single static file. Serve it over HTTP so the browser allows microphone access:

    npx serve .

## Deploy

Push to GitHub, then import the repo in Vercel with the framework preset set to "Other". No build command is needed. Vercel serves over HTTPS, which microphone access requires.
