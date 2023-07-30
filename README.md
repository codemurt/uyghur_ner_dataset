# Uyghur NER dataset

## Description

This dataset is in [WikiAnn](https://huggingface.co/datasets/wikiann) format. The dataset is assembled from named entities parsed from Wikipedia, Wiktionary and Dbpedia. For some words, new case forms have been created using [Apertium-uig](https://github.com/apertium/apertium-uig). Some locations have been translated using the Google Translate API.

The dataset is divided into two parts: `train` and `extra`. `Train` has full sentences, `extra` has only named entities.

Tags: `O (0), B-PER (1), I-PER (2), B-ORG (3), I-ORG (4), B-LOC (5), I-LOC (6)`

## Data example

```
{
	'tokens': ['قاراماي', 'شەھىرى', '«مەملىكەت', 'بويىچە', 'مىللەتل…'],
 	'ner_tags': [5, 0, 0, 0, 0],
 	'langs': ['ug', 'ug', 'ug', 'ug', 'ug'],
 	'spans': ['LOC: قاراماي']
}
```

## Usage with `datasets` library

```py
from datasets import load_dataset

dataset = load_dataset("codemurt/uyghur_ner_dataset") 
```