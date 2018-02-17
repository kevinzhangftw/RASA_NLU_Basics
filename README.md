# VoiceOS
Voice Operating System

### change directory in config_spacy.json:
{
  "pipeline": "spacy_sklearn",
  "path" : "./projects",
  "data" : "./data/kittensRasaData.json"
}

### train server:
python3 -m rasa_nlu.train -c config_spacy.json

### run server:
python3 -m rasa_nlu.server

### make a request:
curl -XPOST localhost:5000/parse -d '{"q":"find me a cat"}'
