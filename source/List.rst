====
List
====

Pros:

    memory


Cons:

    speed on find, insert


1. unpack the variable in list using explicit unpacking
========================================================

* Don't

.. code-block:: python

    number_list = [1,2,3]

    hello = number_list[0]
    world = number_list[1]
    hey = number_list[2]

* Good

.. code-block:: python

    number_list = [1,2,3]

    hello, world, hey = number_list


2. Using zip() to iterate over a pair of lists.
================================================

* Don't

.. code-block:: python

    numbers = [1, 2, 3]
    letters = ["A", "B", "C"]

    for index in range(len(numbers)):
        print(numbers[index], letters[index])

* Good

.. code-block:: python

    numbers = [1, 2, 3]
    letters = ["A", "B", "C"]

    for numbers_value, letters_value in zip(numbers, letters):
        print(numbers_value, letters_value)

3. Use list comprehension instead of `map()`.
================================================

.. code-block:: python

    values = [1, 2, 3]
    doubles = [x * 2 for x in values]