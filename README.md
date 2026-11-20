# Mtraineemodels

Modelos de IA que o app **MusicTrainee** para celular baixa quando a pessoa usa a função pela primeira vez. Depois de baixados, funcionam sem internet, dentro do aparelho.

Este repositório guarda **só os modelos e os avisos de licença**. O código do app não está aqui.

## Arquivos (versão `modelos-v1`)

| Arquivo | Tamanho | Uso no app | Origem |
|---|---|---|---|
| `htdemucs.web.onnx` | 90 MB | Separar instrumentos (bateria, baixo, voz, outros) | htdemucs (Demucs v4, Meta), convertido para ONNX com os mesmos pesos (meia precisão) |
| `spleeter4.onnx` | 79 MB | Separação rápida em 4 faixas (voz, bateria, baixo e outros) | Spleeter 4stems (Deezer), convertido para ONNX com os mesmos pesos (meia precisão) |
| `whisper-small-encoder.onnx` | 92 MB | Letra automática | Whisper small (OpenAI), versão ONNX int8 de [onnx-community/whisper-small_timestamped](https://huggingface.co/onnx-community/whisper-small_timestamped) |
| `whisper-small-decoder.onnx` | 157 MB | Letra automática | Idem |
| `whisper-small-vocab.txt` | 0,5 MB | Vocabulário do Whisper | Extraído do `tokenizer.json` do modelo |
| `whisper-small.cfg` | 1 KB | Ajustes do Whisper (alinhamento das palavras, tokens suprimidos, idiomas) | Extraído do `generation_config.json` do modelo |

As assinaturas SHA-256 estão em [`SHA256SUMS`](SHA256SUMS). O app tem essas assinaturas gravadas e recusa qualquer arquivo diferente.

## Licenças

Os modelos são distribuídos pelos autores sob a licença **MIT**; os textos estão em [`LICENSE`](LICENSE).

- **Demucs / htdemucs** — Alexandre Défossez, Meta AI. "Hybrid Transformers for Music Source Separation" (Rouard, Massa, Défossez, 2023). https://github.com/facebookresearch/demucs
- **Spleeter** — Deezer Research. "Spleeter: a fast and efficient music source separation tool with pre-trained models" (Hennequin, Khlif, Voituret, Moussallam, 2020). https://github.com/deezer/spleeter
- **Whisper** — OpenAI. "Robust Speech Recognition via Large-Scale Weak Supervision" (Radford et al., 2022). https://github.com/openai/whisper
