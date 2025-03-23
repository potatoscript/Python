# PotatoPython 

Welcome to the official **PotatoPython** repository! Here, you'll find useful Python Projects and Tutorials to help enhance your development experience. 

## Contents

- [Python Project](#python_project)
- [Tutorials](#python_tutorials)

---

## Python_Project
[menu](#potatopython)

This section highlights our core Python project: the **`potato.py`** library. It provides essential utilities to streamline common tasks like database connectivity, email notifications, and file management.

| **Project**                      | **Description**                                                                                                                                                        |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **[potato.py](https://github.com/potatoscript/potatopython)** | The **potato.py** library offers a collection of utility functions to simplify working with databases, emails, files, and more. This tool is ideal for Python developers looking for efficiency. |

---

## Python_Tutorials
[menu](#potatopython)

The following tutorials cover a wide range of Python topics, from basic syntax to more advanced programming concepts.

| Topic | Description |
| --- | --- |
| [Installation Guide](https://github.com/potatoscript/python/wiki/Installation) | Setup Python and configure your development environment |
| [Hello, World!](https://github.com/potatoscript/python/wiki/Hello-World) | Your first Python program: `print("Hello, World!")` |
| [Variables & Data Types](https://github.com/potatoscript/python/wiki/Variables) | Explore data types like `int`, `float`, `str`, `bool`, and more |
| [String Manipulation](https://github.com/potatoscript/python/wiki/String) | Common string operations: `upper()`, `replace()`, `split()` |
| [User Input](https://github.com/potatoscript/python/wiki/User-Input) | Collecting user input with `input()` |
| [Arithmetic Operations](https://github.com/potatoscript/python/wiki/Arithmetic-Operations) | Basic math operations: `+`, `-`, `*`, `/` and more |
| [Math Functions](https://github.com/potatoscript/python/wiki/Math-Functions) | Using the `math` module for common mathematical operations |
| [Conditionals](https://github.com/potatoscript/python/wiki/If-Statement) | Learn how to use `if`, `elif`, and `else` statements |
| [Loops - While & For](https://github.com/potatoscript/python/wiki/While-Loops) | Control flow with `while` and `for` loops |
| [Lists & Tuples](https://github.com/potatoscript/python/wiki/Lists) | Storing multiple items in `list` and `tuple` containers |
| [Dictionaries & Sets](https://github.com/potatoscript/python/wiki/Dictionaries) | Storing key-value pairs with `dict` and unordered collections with `set` |
| [Functions & Recursion](https://github.com/potatoscript/python/wiki/Functions) | Create reusable functions and explore recursion |
| [Exception Handling](https://github.com/potatoscript/python/wiki/Exceptions) | Gracefully handling errors with `try` and `except` |
| [Object-Oriented Programming](https://github.com/potatoscript/python/wiki/Class) | Work with classes and objects in Python |
| [Modules & Packages](https://github.com/potatoscript/python/wiki/Modules) | Organizing code with modules and packages |
| [Working with Files](https://github.com/potatoscript/python/wiki/Files-Directories) | Read from and write to files using `open()` and `pathlib` |
| [Web Scraping](https://github.com/potatoscript/python/wiki/Web-Scraping) | Scrape data from websites using `BeautifulSoup` |
| [Web Development (Django & Flask)](https://github.com/potatoscript/python/wiki/django) | Build web applications using Django and Flask |
| [Machine Learning](https://github.com/potatoscript/python/wiki/Machine-Learning) | Learn about machine learning with `scikit-learn`, `TensorFlow`, and more |
| [Data Analysis](https://github.com/potatoscript/python/wiki/Data-Analysis) | Explore data analysis with `pandas`, `numpy`, and `matplotlib` |
| [Game Development](https://github.com/potatoscript/python/wiki/Game-Development) | Develop games using the `pygame` library |

---

### Advanced Tutorials
[menu](#potatopython)

If you're looking for more advanced concepts, here are a few additional tutorials:

| Topic | Description |
| --- | --- |
| [Unit Testing](https://github.com/potatoscript/python/wiki/Unit-Testing) | Ensure code quality with the `unittest` framework |
| [Multi-threading](https://github.com/potatoscript/python/wiki/Threading) | Run concurrent tasks with multi-threading in Python |
| [Cybersecurity](https://github.com/potatoscript/python/wiki/Cybersecurity) | Implement hashing and encryption techniques |

---

## Contributing

🥔Potatoscript welcome contributions! If you have a Python project or tutorial that you think would be helpful to the community, feel free to submit a pull request. Here are some ways you can help:

- Suggest new tutorials or content
- Report any issues or bugs
- Improve existing tutorials

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

[menu](#potatopython)

---

## Upload library to PIPY

### **Step 1: Update Version Number**
#### **If using `setup.py`**
Edit `setup.py` and increment the `version` field:
```python
from setuptools import setup, find_packages

setup(
    name="my_library",  
    version="0.1.1",  # Increase the version number
    packages=find_packages(),
)
```
If the previous version was `0.1.0`, change it to `0.1.1`, `0.2.0`, etc.

#### **If using `pyproject.toml` (PEP 517/518)**
Edit `pyproject.toml` and update the version:
```toml
[tool.setuptools]
version = "0.1.1"  # Increment version
```

---

### **Step 2: Delete Old Distribution Files**
Remove old package files from the `dist/` folder:
```bash
rm -rf dist/ build/ *.egg-info
```

---

### **Step 3: Rebuild the Package**
Rebuild the package with the new version:

For `setup.py`:
```bash
python setup.py sdist bdist_wheel
```

For `pyproject.toml` (if using PEP 517/518):
```bash
python -m build
```

---

### **Step 4: Re-upload the New Version**
Now upload again using Twine:
```bash
twine upload dist/*
```

