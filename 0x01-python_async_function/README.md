# 0x01-python_async_function

![4aeaa9c3cb1f316c05c4](https://github.com/Zed-bard/alx-backend-python/assets/132649828/093a7ba2-f3bf-4c71-bc1a-7d3e12e27bb7)

This project contains tasks for learning to use asynchronous code in Python 3. It focuses on understanding the basics of asynchronous programming, executing multiple coroutines concurrently, measuring runtime, and creating tasks with asyncio. The tasks are designed to provide hands-on experience with async programming, helping to understand its concepts and practical applications.

## Tasks To Complete

| Task Number | Task Name | Description | File Link |
|-------------|------------|-------------|-----------|
| 0 | The basics of async | Contains an asynchronous coroutine `wait_random` that waits for a random delay between 0 and `max_delay` seconds and eventually returns it. The `random` module is used. | [0-basic_async_syntax.py](0-basic_async_syntax.py) |
| 1 | Let's execute multiple coroutines at the same time with async | Contains an async routine `wait_n` that spawns `wait_random` n times with the specified `max_delay` and returns the list of delays in ascending order without using `sort()`. | [1-concurrent_coroutines.py](1-concurrent_coroutines.py) |
| 2 | Measure the runtime | Contains a `measure_time` function that measures the total execution time for `wait_n(n, max_delay)` and returns `total_time / n`. The `time` module is used to measure elapsed time. | [2-measure_runtime.py](2-measure_runtime.py) |
| 3 | Tasks | Contains a function `task_wait_random` that takes an integer `max_delay` and returns a `asyncio.Task`. | [3-tasks.py](3-tasks.py) |
| 4 | Tasks | Contains a function `task_wait_n` similar to `wait_n` but calls `task_wait_random`. | [4-tasks.py](4-tasks.py) |

## Details for the Topic of the Project

### Asynchronous Code

| Topic | Description |
|-------|-------------|
| Asynchronous Programming | Asynchronous programming allows for the execution of code in a non-blocking manner. This means that other tasks can continue to run while waiting for long-running operations to complete, improving efficiency and responsiveness. |
| Asyncio Module | The `asyncio` module provides a framework for writing asynchronous code using the `async` and `await` keywords. It is part of the Python standard library and is used to handle asynchronous tasks, manage event loops, and run coroutines concurrently. |
| Coroutines | Coroutines are special functions defined with the `async def` syntax. They can pause their execution using the `await` keyword and resume later, allowing other tasks to run in the meantime. |
| Tasks | In asyncio, a `Task` is a wrapper for a coroutine that allows it to run concurrently with other tasks. Tasks can be created using `asyncio.create_task()` and can be awaited to retrieve their result once they are complete. |
| Event Loop | The event loop is the core of every asyncio application. It runs in a loop and executes tasks, callbacks, and other operations. The event loop can be started with `asyncio.run()`. |

### Project Tasks

| Task Number | Details |
|-------------|---------|
| 0 | **The basics of async**: This task introduces the basic concept of asynchronous coroutines. The `wait_random` coroutine uses the `random` module to wait for a random delay and returns the delay value. This helps understand how coroutines can perform time-consuming operations without blocking the execution of other code. |
| 1 | **Let's execute multiple coroutines at the same time with async**: This task demonstrates how to run multiple coroutines concurrently using asyncio. The `wait_n` function spawns multiple instances of `wait_random` and returns the delays in ascending order. This task highlights the power of async programming in handling multiple tasks simultaneously. |
| 2 | **Measure the runtime**: This task involves measuring the runtime of concurrent coroutines. The `measure_time` function calculates the average time taken for multiple coroutines to complete. This task emphasizes the importance of measuring performance and understanding the efficiency of async code. |
| 3 | **Tasks**: This task covers the creation of asyncio tasks. The `task_wait_random` function returns an `asyncio.Task` that can be awaited. This task demonstrates how to manage and run coroutines as tasks, which is crucial for building complex asynchronous applications. |
| 4 | **Tasks**: This task extends the previous concepts by modifying `wait_n` to use `task_wait_random` instead of directly calling the coroutine. This highlights the flexibility of tasks and their integration into existing async code. |

These tasks provide a comprehensive introduction to asynchronous programming in Python, covering essential concepts and practical applications. By completing these tasks, you will gain a solid understanding of async code and its benefits in improving the performance and responsiveness of your applications.
