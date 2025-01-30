Political Speech Classifier

Overview

This machine learning model is designed to classify audio speech into two categories: Political and Non-Political. Unlike traditional models that strictly define political content as related to governance or policy, this classifier takes a broader approach. It identifies speech that aims to change opinions on political or cultural topics, even if it does not explicitly reference policy matters.

Purpose

The goal of this model is to help users discern when speech presents social issues in a particular light to favor a specific point of view. This could include discussions on governance, activism, economics, or social movements. By highlighting political undertones in speech, the model can be a valuable tool for researchers, content analysts, and educators looking to understand the nuances of spoken content.

How It Works

The model was trained using Apple's Create ML with a dataset containing diverse examples of both political and non-political speech.

It classifies speech clips based on tone, context, and implicit or explicit attempts to persuade listeners on political or social issues.

Examples of political speech include discussions on:

Gender pay gap

"Made in America" policies

Economic incentives tied to political figures (e.g., tax policies linked to specific administrations)

Social justice movements

Non-political speech includes general conversations, entertainment discussions, and factual reporting without persuasive intent.

Usage

macOS/iOS Integration

Download the PoliticalSpeechClassifier.mlmodel file.

Add it to your Xcode project.

Use the following Swift code to load and use the model:

import CoreML
let model = try? PoliticalSpeechClassifier()
let prediction = try? model.prediction(audio: yourAudioData)
print(prediction?.label)

Running as a Web Demo (Optional)

The model can be deployed as a Hugging Face Space using Gradio or Streamlit.

This allows users to upload an audio clip and receive real-time classifications.

Future Improvements

Expand Dataset: Incorporate more diverse voices and styles of speech.

Fine-Tune Accuracy: Adjust parameters to better capture subtle political framing.

Multi-Language Support: Extend classification capabilities beyond English.

Contributing

Contributions are welcome! If you'd like to improve the dataset or refine the classification, feel free to submit a pull request.

License

This project is open-source under the MIT License.
