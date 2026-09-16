# tts-models

Self-hosted TTS voice packs for [AiVoiceReader](https://github.com/hungcaovu/pdf-reader) (pdf-reader).

The actual model archives (`.tar.bz2`, each 80-340MB) are **not** committed
to this git repo — they're published as [GitHub Release](../../releases)
assets instead (regular git pushes reject files over 100MB, and Release
assets get served off GitHub's CDN with no bandwidth limit).

App-side: `react-native-sherpa-onnx`'s `ensureModel()` fetches these
releases directly (`src/domain/tts/sherpaOnnxTtsEngine.ts` in pdf-reader).

Packaging script (produces the archives + checksum.txt from the source
model folders, run locally before uploading a release):
`pdf-reader/tools/model-packaging/package-models.sh`.
