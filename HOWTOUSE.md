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
generated_text, time_spent = model.completion(data="Once upon a time", temperature=0.2, max_tokens=50, transformdata=False)
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
model.savebrain(file="brain.amfer", safe=True)
model.loadbrain(file="brain.amfer", safe=True)
```

### Saving/Loading Session to/from a File
```python
model.savesession(file="session.amfers", safe=True, session="system")
model.loadsession(file="session.amfers", safe=True, session="system")
```
Anlaşıldı, işte her bir fonksiyonun olası çıktılarına ek olarak, dönüş değeri olarak kullanılabilen örnek değerler:

### Core Functions
- **`include_language(language)`**
  - **Example Return Value**: None (No return value).

- **`similarity(text1, text2)`**
  - **Example Return Value**: A similarity score between 0 and 100.

- **`language_detector(data)`**
  - **Example Return Value**: The detected language code (e.g., "en" for English).

- **`tokenizer(data)`**
  - **Example Return Value**: A list of tokens (words) extracted from the provided data.

### Text Generation
- **`completion(data, temperature=0.2, max_tokens=150, count=1, session="system", recall=False, keepinmind=False, wordreply=True, wordreplycount=5, transformdata=False)`**
  - **Example Return Value**: ["Generated Text", TimeSpent]

### Observation
- **`observation_detector(data, language="system")`**
  - **Example Return Value**: A list of indices representing the positions of words in the vocabulary of the specified language. (e.g. [0, 5, 17, 4])

### Hierarchical Hidden Markov Model (HHMM)
- **`hhmm(data, temperature=0.5, max_tokens=150, count=1, session="system", recall=False, keepinmind=False)`**
  - **Example Return Value**: ["GeneratedText", TimeSpent]

### Text to Image
- **`text_to_image(data, file="result.jpg", create_temp=0.1, guess_temp=0.5)`**
  - **Example Return Value**: None

### Deviation
- **`deviate(data, temperature=0.5, language="system")`**
  - **Example Return Value**: The modified text after applying deviation.

### Predefined Training Sets
- **`amfer_setup(setupname, controlled=True, temperature=0.2)`**
  - **Example Return Value**: None (No return value).

- **`include_setup(setupname, data, language="system")`**
  - **Example Return Value**: None (No return value).

- **`delete_setup(setupname)`**
  - **Example Return Value**: None (No return value).

### Brain and Session Management
- **`presave()`**
  - **Example Return Value**: None (No return value).

- **`preload()`**
  - **Example Return Value**: None (No return value).

- **`savebrain(file, safe=True)`**
  - **Example Return Value**: None (No return value).

- **`loadbrain(file, safe=True)`**
  - **Example Return Value**: None (No return value).

- **`savesession(file, safe=True, session="system")`**
  - **Example Return Value**: None (No return value).

- **`loadsession(file, safe=True, session="system")`**
  - **Example Return Value**: None (No return value).
