
### Transcription Metadata JSON Schema

```json
{
  "type": "object",
  "properties": {
    "source": {
      "type": "string"
    },
    "language": {
      "type": "string"
    },
    "duration": {
      "type": "string",
      "format": "hours-min-sec"
    },
    "model": {
      "enum": [
        "whisper-small",
        "whisper-large-v3"
      ]
    },
    "diarization": {
      "type": "boolean"
    },
    "url": {
      "type": "string"
    }, 
    "verified": {
      "type": "boolean"
    }
  }
}
```