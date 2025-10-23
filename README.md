# adagen

Automatic image dataset generation and labeling with CV segmentation and LLMs.

## Pipeline

```mermaid
flowchart LR
  I([Images]) --> S[Segmentation]
  S --> L[LLM labels each segment]
  L --> D{Separated or combined?}
  D -- Separated --> E[Convert segments to standardized format]
  D -- Combined --> F[Convert annotated image to standardized format]
  E --> STD([Standardized dataset])
  F --> STD
```

## Tech Stack

- C++ with OpenCV for segmentation and final dataset generation
- Python with OpenAI SDK for labeling
