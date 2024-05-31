# How to Use AmferModel

## Installation

Install the module using pip:
```bash
pip install AmferModel
```

## Usage

Import the module:
```python
from AmferModel import AMFER_Model
```

### Initialization
```python
model = AMFER_Model(system_setups=True)
```

### Adding a Language
```python
model.include_language("es")
```

### Measuring Text Similarity
```python
similarity_score = model.similarity("Hello", "Hi")
```

### Language Detection
```python
detected_language = model.language_detector("Hello, how are you?")
```

### Tokenization
```python
tokens = model.tokenizer("Hello world.")
```

### Training
```python
training_result = model.train(data="Sample data", language="en", controlled=True, temperature=0.2)
```

### Learning an Image
```python
model.learnimage(file="image.jpg", means="a cat")
```

### Text Completion
```python
generated_text, time_spent = model.completion(data="Once upon a time", temperature=0.2, max_tokens=50)
```

### Observation Detection
```python
observation_result = model.observation_detector(data="Hello world.")
```

### Hierarchical Hidden Markov Model
```python
hhmm_result = model.hhmm(data="Once upon a time", temperature=0.5, max_tokens=50)
```

### Text to Image
```python
image_result, time_spent = model.text_to_image(data="a dog", file="result.jpg", create_temp=0.1, guess_temp=0.5)
```

### Deviation
```python
deviated_text = model.deviate(data="Hello world.", temperature=0.5)
```

### Using Predefined Training Sets
```python
model.amfer_setup(setupname="en-part1", controlled=True, temperature=0.2)
```

### Adding a New Training Set
```python
model.include_setup(setupname="custom-setup", data="New training data", language="en")
```

### Deleting a Training Set
```python
model.delete_setup(setupname="custom-setup")
```

### Saving Brain Data
```python
model.presave()
model.preload()
```

### Saving/Loading Brain Data to/from a File
```python
model.savebrain(file="brain.dat", safe=True)
model.loadbrain(file="brain.dat", safe=True)
```

### Saving/Loading Session to/from a File
```python
model.savesession(file="session.dat", safe=True, session="system")
model.loadsession(file="session.dat", safe=True, session="system")
```
