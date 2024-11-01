# Titu Speech To Text Development
[![Hugging Face](https://img.shields.io/badge/🤗%20Hugging%20Face-TituLM-blue)](https://huggingface.co/hishab)

Titu STT (Speech-to-Text) is an open-source project developed by Hishab, aimed at advancing speech recognition capabilities with a focus on the Bangla language. As part of the broader TituLM initiative, TituSTT pushes the boundaries of automatic speech recognition (ASR) technology for product development.

At Hishab, we are dedicated to improving speech-to-text conversion through a comprehensive pipeline of pretraining and fine-tuning models on diverse speech recognition tasks. While TituSTT primarily emphasizes Bangla, its underlying technology is not limited to a single language, allowing for potential expansion to other languages in the future.

Our goal is to create robust and accurate speech recognition models that can be integrated into various applications, enhancing accessibility and user experience across different domains.

## Models

| STT Model                                                                           | Description   | MegaBNSpeech-YT |
|-------------------------------------------------------------------------------------|---------------|-----------------|
| [TituSTT-BN-FastConformer](https://huggingface.co/hishab/titu_stt_bn_fastconformer) | Trained with YT news,talkshow data| 6.4/3.399       |


## Usage
### Inference Using Nemo

```python
# pip install -q 'nemo_toolkit[asr]'

import nemo.collections.asr as nemo_asr
asr_model = nemo_asr.models.ASRModel.from_pretrained("hishab/titu_stt_bn_fastconformer")

auido_file = "test_bn_fastconformer.wav"
transcriptions = asr_model.transcribe([auido_file])
print(transcriptions)
# ['আজ সরকারি ছুটির দিন দেশের সব শিক্ষা প্রতিষ্ঠান সহ সরকারি আধা সরকারি স্বায়ত্তশাসিত প্রতিষ্ঠান ও ভবনে জাতীয় পতাকা অর্ধনমিত ও কালো পতাকা উত্তোলন করা হয়েছে']
```

## Fine-Tuning


## Benchmark
