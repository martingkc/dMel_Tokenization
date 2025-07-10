# dMel Tokenization

### Example usage of dMel, a recently announced audio tokenization technique that requires no prior training to generate tokens.
This repository demonstrates how to perform audio tokenization and detokenization using the `speechbrain/tts-hifigan-libritts-16kHz` vocoder. 

It uses LLM-compatible token representations of the form `<c{channel_id}b{bin_id}>`, where:
- channel_id is one of the 80 mel filterbank channels.
-	bin_id is one of the 16 magnitude bins (for 4-bit quantization).

You can use this example to generate and reconstruct audio datasets with dMel tokens for training or inference. 
