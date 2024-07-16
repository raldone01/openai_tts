# OpenAI Speech Custom Component for Home Assistant

This custom component integrates OpenAI's Text-to-Speech (TTS) and OpenAI's Speech-to-Text (STT) service with Home Assistant, allowing users to convert text into spoken audio.
The service supports various languages and voices, offering customizable options such as voice model.
Custom third party OpenAI compatible endpoints are supported.

## Description

The OpenAI Speech component for Home Assistant makes it possible to use the OpenAI API to generate spoken audio from text and to transcribe audio to text.
This can be used in automations, assistants, scripts, or any other component that supports TTS or STT within Home Assistant.

*For the official OpenAi endpoint an API key is required.*

## Features

- Text-to-Speech conversion using OpenAI's API
- Speech-to-Text conversion using OpenAI's API
- Support for multiple languages and voices
- Customizable speech model (check https://platform.openai.com/docs/guides/text-to-speech for supported voices and models).
  Custom values can be used for third party endpoints.
- Integration with Home Assistant's assistant, automations and scripts

## Sample

[https://www.youtube.com/watch?v=oeeypI_X0qs](https://www.youtube.com/shorts/otTe6-YkQjI)

## Sample Home Assistant service

```
service: tts.speak
target:
  entity_id: tts.openai_nova_engine
data:
  cache: true
  media_player_entity_id: media_player.bedroom_speaker
  message: My speech has improved now!
```

## HACS installation ( *preferred!* )

1. Go to the sidebar HACS menu

2. Click on the 3-dot overflow menu in the upper right and select the "Custom Repositories" item.

3. Copy/paste https://github.com/raldone01/openai_speech into the "Repository" textbox and select "Integration" for the category entry.

4. Click on "Add" to add the custom repository.

5. You can then click on the "OpenAI TTS Speech Services" repository entry and download it. Restart Home Assistant to apply the component.

6. Add the integration via UI, provide API key and select required model and voice. Multiple instances may be configured.

## Manual installation

1. Ensure you have a `custom_components` folder within your Home Assistant configuration directory.

2. Inside the `custom_components` folder, create a new folder named `openai_speech`.

3. Place the repo files inside `openai_speech` folder.

4. Restart Home Assistant

5. Add the integration via UI, provide API key and select required model and voice. Multiple instances may be configured.


## Thanks and Attribution

* [@sfortis](https://github.com/sfortis) for the original project `openai_tts`
* [@qJake](https://github.com/qJake) for the custom endpoint support
* [@davidohne](https://github.com/davidohne) for stt support.
