# llama.ggmlv3.cpp

forked from [ggerganov/llama.cpp](https://github.com/ggerganov/llama.cpp) commit ffb06a3

Since the commit 2d5db48 on May 19, as shown in [pull request 1508](https://github.com/ggerganov/llama.cpp/pull/1508), the quantization format in llama.cpp has changed from using 32-bit floats to 16-bit floats.

## Build:
```shell
git clone https://github.com/star-bits/llama.ggmlv3.cpp
cd llama.ggmlv3.cpp

make
```

## Models:
```shell
ls ../../weights/llama.ggmlv3.cpp/models 
wizard-vicuna-13B-GGML
```
- [<code>wizard-vicuna-13B-GGML/wizard-vicuna-13B.ggmlv3.q4_0.bin</code>](https://huggingface.co/TheBloke/wizard-vicuna-13B-GGML)
- [<code>wizard-vicuna-13B-GGML/wizard-vicuna-13B.ggmlv3.q4_1.bin</code>](https://huggingface.co/TheBloke/wizard-vicuna-13B-GGML)
- [<code>wizard-vicuna-13B-GGML/wizard-vicuna-13B.ggmlv3.q5_0.bin</code>](https://huggingface.co/TheBloke/wizard-vicuna-13B-GGML)
- [<code>wizard-vicuna-13B-GGML/wizard-vicuna-13B.ggmlv3.q5_1.bin</code>](https://huggingface.co/TheBloke/wizard-vicuna-13B-GGML)

## Help:
```shell
./main -h
```

## System prompt:
`./prompts/context-setting.txt`
```
A conversation with an AI that provides helpful, polite, and concise answers.

User: Hey, you there?
AI: At your service, sir.
User:
```

## Run:
```shell
./main -m ../../weights/llama.ggmlv3.cpp/models/wizard-vicuna-13B-GGML/wizard-vicuna-13B.ggmlv3.q4_1.bin -n -1 --repeat_penalty 1.0 --color -i -f prompts/context-setting.txt -r "User:"
```
