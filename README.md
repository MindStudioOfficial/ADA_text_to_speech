# ADA - Satisfactory Artificial Directory and Assistant Voice Generator for python

A python notebook that generates text-to-speech audio files from a given text input in [ADA](https://satisfactory.wiki.gg/wiki/ADA)'s voice.

https://satisfactory.guru/articles/read/index/id/47/name/ADA+Voice

## Setup

This project uses conda to manage the environment. To create the environment, run the following command:

```bash
conda env create -f environment.yml
```

To activate the environment, run the following command:

```bash
conda activate ADA_audio
```

The original ADA voice is generated using Google Cloud Text-to-Speech API. To use the API, you need to set up a Google Cloud account and enable the Text-to-Speech API. 

You can then simply create an API-key and set it as an environment variable in a `.env` file in the root directory of the project:

```bash	
ADA_API_KEY="my_api_key"
```

## Usage

To generate an audio file from a text input execute the cells in the [ADA.ipynb](ADA.ipynb) notebook. 

Simply provide your text input in the `input` variable in the second cell and run the notebook. The audio file will be saved as `output.wav` in the root directory of the project.

The last cell adds some post-processing to the audio file to make it sound more like ADA using [audioFX](https://pypi.org/project/audioFX/). A documentation for the library can be found [here](https://pypi.org/project/audioFX/).

The processed audio file will be saved as `output_fx.wav` in the root directory of the project.