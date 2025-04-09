# Woovl ComfyUI Replicate Integration Is a fork of the original ComfyUI Replicate Integration
We're aim to make it easier to use Replicate models in ComfyUI, specially if you need to attach a LoRA.

Effortlessly integrate and run cutting-edge [Replicate models](https://replicate.com/explore) within your ComfyUI workflows using this custom node package, proudly brought to you by [Woovl](https://woovl.com).

Explore the power of AI with ease! Check out our [example workflows](https://github.com/replicate/comfyui-replicate/tree/main/example_workflows) and the list of [supported Replicate models](https://github.com/replicate/comfyui-replicate/blob/main/supported_models.json) to get started on your creative journey.

![example-screenshot](https://github.com/replicate/comfyui-replicate/assets/319055/0eedb026-de3e-402a-b8fc-0a14c2fd209e)

## Before You Begin: Setting Your Replicate API Token

To unlock the full potential of this integration, ensure you have your Replicate API token set as an environment variable. You can obtain your API tokens (we recommend creating a new one for this integration) here:

https://replicate.com/account/api-tokens

Here's how to pass your API token when launching ComfyUI:

**On MacOS or Linux:**
```sh
export REPLICATE_API_TOKEN="r8_************"; python main.py
```

**On Windows:**
```sh
set REPLICATE_API_TOKEN="r8_************"; python main.py
```

## Installation with Woovl

Integrate Woovl ComfyUI Replicate into your ComfyUI setup with these simple steps:

```sh
cd ComfyUI/custom-nodes
git clone [https://github.com/replicate/comfyui-replicate](https://github.com/replicate/comfyui-replicate) woovl-comfyui-replicate
cd woovl-comfyui-replicate
pip install -r requirements.txt
```

## Discover Supported Replicate Models

Refer to the `supported_models.json` file to view the list of Replicate models that are included by default with this Woovl integration.

## Keeping Your Models Up-to-Date

Easily update the available Replicate model nodes by running the following command:

```sh
./import_schemas.py
```

This script will fetch the latest model versions automatically.

## Expanding Model Capabilities

Currently, this Woovl integration supports Replicate models that produce straightforward text or image outputs. Models generating audio, video, JSON objects, or mixed outputs may not function as expected at this time.

To incorporate additional compatible models:

- Add the desired model details to the `supported_models.json` file (e.g., `fofr/consistent-character`).
- Execute `./import_schemas.py` to refresh the schemas and import your new model.
- Restart your ComfyUI instance.
- The new model will now be available in your workflows with the title ‘Replicate [model author/model name]’.

## Future Enhancements by Woovl

The Woovl team is actively working on expanding the capabilities of this integration, with future updates potentially including:

- Support for a wider range of Replicate model output types, prioritizing audio and video.
- Displaying real-time logs, prediction status, and progress updates (possibly using `tqdm`).

## Contributing to the Woovl Ecosystem

We encourage community contributions! If you integrate models that you believe would benefit other users, please feel free to submit pull requests. Your contributions help make the Woovl ComfyUI Replicate integration even more powerful.