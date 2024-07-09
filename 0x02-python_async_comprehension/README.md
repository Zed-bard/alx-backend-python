# 0x02-python_async_comprehension

## Async Comprehension

This project contains tasks for learning to use asynchronous comprehensions in Python 3.

## Tasks To Complete

+ [x] 0. **Async Generator**<br/>[0-async_generator.py](0-async_generator.py) contains an asynchronous coroutine called `async_generator` that takes no arguments and meets the following requirements:
  + The coroutine will loop 10 times, each time asynchronously wait 1 second, then yield a random number between 0 and 10.
  + Use the `random` module.

+ [x] 1. **Async Comprehensions**<br/>[1-async_comprehension.py](1-async_comprehension.py) contains a script that meets the following requirements:
  + Import `async_generator` from the previous task and then write a coroutine called `async_comprehension` that takes no arguments.
  + The coroutine will collect 10 random numbers using an async comprehensing over `async_generator`, then return the 10 random numbers.

+ [x] 2. **Run time for four parallel comprehensions**<br/>[2-measure_runtime.py](2-measure_runtime.py) contains a script that meets the following requirements:
  + Import `async_comprehension` from the previous file and write a `measure_runtime` coroutine that will execute `async_comprehension` four times in parallel using `asyncio.gather`.
  + `measure_runtime` should measure the total runtime and return it.

## Requirements

### General

- Allowed editors: vi, vim, emacs
- All your files will be interpreted/compiled on Ubuntu 18.04 LTS using python3 (version 3.7)
- All your files should end with a new line
- The first line of all your files should be exactly `#!/usr/bin/env python3`
- A README.md file, at the root of the folder of the project, is mandatory
- Your code should use the pycodestyle style (version 2.5.x)
- The length of your files will be tested using `wc`
- All your modules should have documentation (e.g., `python3 -c 'print(__import__("my_module").__doc__)'`)
- All your functions should have documentation (e.g., `python3 -c 'print(__import__("my_module").my_function.__doc__)'`)
- A documentation is not a simple word, it’s a real sentence explaining what’s the purpose of the module, class, or method (the length of it will be verified)
- All your functions and coroutines must be type-annotated.

## How to Run

1. Clone the repository:
    ```sh
    git clone https://github.com/your-username/async-comprehension.git
    cd async-comprehension
    ```

2. Create a virtual environment and activate it:
    ```sh
    python3 -m venv venv
    source venv/bin/activate
    ```

3. Install dependencies:
    ```sh
    pip install -r requirements.txt
    ```

4. Run the scripts:
    - To run the async generator script:
      ```sh
      python3 0-async_generator.py
      ```
    - To run the async comprehension script:
      ```sh
      python3 1-async_comprehension.py
      ```
    - To measure runtime for four parallel comprehensions:
      ```sh
      python3 2-measure_runtime.py
      ```

## Project Structure

```
async-comprehension/
│
├── 0-async_generator.py
├── 1-async_comprehension.py
├── 2-measure_runtime.py
├── requirements.txt
└── README.md
```

