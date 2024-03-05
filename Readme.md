Twitch Integration Layer for AI-TTS

Using https://elevenlabs.io/ services

```
let config = {
    "channel": "..", // Twitch channel name
    "apiKey": "...", // elevenlabs API Key
    "voice": {
        "bits": {
            "min": 1,           // min amount for cheer TTS
            "default": {        // use this AI voice as fallback
                "id": "....",
                "similiarity": 0.8,
                "stability": 0.7,
                "style": 0.3
            },   
            "151": { ... },          // use this AI voice for 151 bit
            "152": { ... },          // use this AI voice for 152 bit
        }
    }
}

btoa(JSON.stringify(config)) // use this as query parameter c for configuration
```