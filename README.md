<h1 align="center">
  <br>
  <img height="300" src="https://github.com/go-skynet/model-gallery/assets/2420543/7a6a8183-6d0a-4dc4-8e1d-f2672fab354e"> <br>
  <a href="https://github.com/go-skynet/LocalAI">LocalAI</a> model gallery
<br>
</h1>

The model gallery is a curated collection of models created by the community and tested with [LocalAI](https://github.com/go-skynet/LocalAI).

We encourage contributions to the gallery! However, please note that if you are submitting a pull request (PR), we cannot accept PRs that include URLs to models based on LLaMA or models with licenses that do not allow redistribution. Nevertheless, you can submit a PR with the configuration file without including the downloadable URL.


## Helper tool

To load a model from main onto localhost

```shell
bash ./load.sh wizard
```

## More 
For how to use the files in this repository, see the [Documentation](https://localai.io/models/)


# Draft spec of the model definition yaml file

## Main Configuration

- `name`: Name of the model
- `parameters`: Prediction parameters
  - `top_p`: Top P value
  - `top_k`: Top K value
  - `maxtokens`: Maximum tokens
  - `temperature`: Temperature
  - `model`: Model file
- `f16`: Use F16 format (true/false)
- `threads`: Number of threads
- `debug`: Debug mode (true/false)
- `roles`: Map of roles
- `embeddings`: Use embeddings (true/false)
- `backend`: Backend name

## Template Configuration

- `template`
  - `chat`: Chat template
  - `chat_message`: Chat message template
  - `completion`: Completion template
  - `edit`: Edit template
  - `function`: Function template

## Function Configuration

- `function`
  - `disable_no_action`: Disable no action (true/false)
  - `no_action_function_name`: No action function name
  - `no_action_description_name`: No action description name

## Feature Flags

- `feature_flags`: Map of feature flags

## LLM Configuration

- `llm`
  - `system_prompt`: System prompt
  - `tensor_split`: Tensor split
  - `main_gpu`: Main GPU
  - `rms_norm_eps`: RMS Norm Epsilon
  - `ngqa`: NGQA
  - `prompt_cache_path`: Prompt cache path
  - `prompt_cache_all`: Prompt cache all (true/false)
  - `prompt_cache_ro`: Prompt cache read-only (true/false)
  - `mirostat_eta`: Mirostat ETA
  - `mirostat_tau`: Mirostat TAU
  - `mirostat`: Mirostat
  - `gpu_layers`: GPU layers
  - `mmap`: Use MMAP (true/false)
  - `mmlock`: Use MMLock (true/false)
  - `low_vram`: Low VRAM mode (true/false)
  - `grammar`: Grammar
  - `stopwords`: List of stopwords
  - `cutstrings`: List of cutstrings
  - `trimspace`: List of trimspace
  - `context_size`: Context size
  - `numa`: Use NUMA (true/false)
  - `lora_adapter`: Lora adapter
  - `lora_base`: Lora base
  - `no_mulmatq`: No MulMatQ (true/false)
  - `draft_model`: Draft model
  - `n_draft`: N Draft
  - `quantization`: Quantization

## AutoGPTQ Configuration

- `autogptq`
  - `model_base_name`: Model base name
  - `device`: Device
  - `triton`: Use Triton (true/false)
  - `use_fast_tokenizer`: Use fast tokenizer (true/false)

## Diffusers Configuration

- `diffusers`
  - `pipeline_type`: Pipeline type
  - `scheduler_type`: Scheduler type
  - `cuda`: Use CUDA (true/false)
  - `enable_parameters`: Enable parameters
  - `cfg_scale`: CFG Scale
  - `img2img`: Image to Image Diffuser (true/false)
  - `clip_skip`: Clip skip
  - `clip_model`: Clip model
  - `clip_subfolder`: Clip subfolder

## GRPC Configuration

- `grpc`
  - `attempts`: Attempts
  - `attempts_sleep_time`: Attempts sleep time

## Vall-E Configuration

- `vall-e`
  - `audio_path`: Audio path
