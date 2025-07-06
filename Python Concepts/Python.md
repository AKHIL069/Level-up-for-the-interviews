# Basic Python Concepts
---
### 1. What is Python? What are the benefits of using Python?

**Answer**: Python is a programming language with objects, modules, threads, exceptions, and automatic memory management.

**Benefits of Python**:
- Simple and easy to Learn
- Portable
- Extensible
- Built-in data structures
- Open-source

---
### 2. What is PEP 8?
**Answer**: PEP 8 is a coding convention or a set of recommendations on how to write Python code in a more readable and consistent way.

---
### 3. What is pickling and unpickling?
**Answer**: 
* **Pickling**: Converting a Python object into a byte stream using the `pickle` module.
* **Unpickling**: Retrieving the original Python object from the byte stream.

---
### 4. How is Python interpreted?
**Answer**: Python is an interpreted language. The Python interpreter reads and executes the code line by line.

---
### 5. How is memory managed in Python? Explain the concept of reference counting and garbage collection.
**Answer**: Python uses a private heap space for memory management. The allocation is handled by the Python memory manager. It also has a built-in garbage collector to recycle unused memory.

#### Reference counting:
* Python uses reference counting to manage memory.
* Every object has a counter — incremented when referenced, decremented when dereferenced.
* When the count drops to 0 -> memory is released

#### Garbage collection:
* Hanldes cyclic references(e.g.,A->B->A).
* Uses a generational garbage collector to track objects in three generations and clean cyclic garbage periodically.

---
### 6. What are the tools that help to find bugs or perform static analysis?
**Answer**: 
* `PyChecker`: Detects bugs and check style.
* `Pylint`: Checks for coding standard compliance.

---
### 7. What are Python decorators? How can you create a custom one with arguments?
**Answer**: Decorators is a function that takes another function and extend/modifies its behavior without changing its source code.

* Commonly used for logging, access control, memoization.

* With arguments:

```python 
def repeat(n):
    def decorator(func):
        def wrapper(*args, **kwargs):
            for _ in range(n):
                func(*args, **kwargs)
        return wrapper
    return decorator

@repeat(3)
def say_hello():
    print("Hello")
```

---
### 8. What is difference between list and tuple?
**Answer**: 
* A list is a mutable, ordered collection of elements. You can change, add, or remove elements after the list is created.

* A tuple is an immutable, ordered collection of elements. Once created, its content cannot be changed (no add, remove, or update).












