{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "title": "Transcription Metadata",
  "description": "Metadata for audio/video transcription files.",
  "type": "object",
  "properties": {
    "source": {
      "type": "string",
      "description": "Name or identifier of the original audio/video source."
    },
    "language": {
      "type": "string",
      "description": "Language of the transcription."
    },
    "duration": {
      "type": "string",
      "description": "Duration of the source recording in HH:MM:SS format.",
      "examples": ["01:25:30"]
    },
    "model": {
      "type": "string",
      "enum": [
        "whisper-small",
        "whisper-large-v3"
      ],
      "description": "Whisper model used for transcription."
    },
    "diarization": {
      "type": "boolean",
      "description": "Indicates whether speaker diarization was performed."
    },
    "url": {
      "type": "string",
      "format": "uri",
      "description": "URL of the original audio/video source."
    }
  },
  "required": [
    "source",
    "language",
    "duration",
    "model",
    "diarization",
    "url"
  ],
  "additionalProperties": false
}