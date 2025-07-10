# dMel Tokenization

### Example usage of dMel, a recently announced audio tokenization technique that requires no prior training to generate tokens.
This repository demonstrates how to perform audio tokenization and detokenization using the `speechbrain/tts-hifigan-libritts-16kHz` vocoder. 

It uses LLM-compatible token representations of the form `<c{channel_id}b{bin_id}>`, where:
- channel_id is one of the 80 mel filterbank channels.
-	bin_id is one of the 16 magnitude bins 

### Configuration

The default settings are:

- Code Dimension or Mel Channels: 80

- Cookbook Size or Magnitude Bins: 16 (4-bits) 

- Sampling rate: 16 kHz

- Frame rate: 40 Hz (hop length = 400 samples)

- Token throughput: 3200 tokens/sec

You can adjust the quantization bit depth, sampling rate, and frame rate to better match your vocoder’s characteristics. Changing the frame rate will directly affect token throughput.

### References
- [dMel: Speech Tokenization Made Simple](https://machinelearning.apple.com/research/speech-tokenization-made-simple)
- [GitHub: apple/dMel](https://github.com/apple/dmel)
