=====
Dict
=====

Pros:

    speed on find, insert

Cons:

    memory



1. Use defaultdict() to initialize dict keys
=============================================

* Dont't

.. code-block:: python

    dt = {}

    if "k" not in dt:
        dt["k"] = 6

    dt["k"] += 1

    print(dt["k"])

* Good

.. code-block:: python

    from collections import defaultdict

    dt = defaultdict(lambda : 6)

    dt["k"] += 1

    print(dt["k"])  # 7

2. using `dict.get` to get the key value in Dict.
==================================================

Which is better to show `KeyError`.

* Don't

.. code-block:: python


    dict = {"test": "value"}

    data = ""

    if "test" in dict:
        print(dict["test"])

    print(dict["test"])

* Good

.. code-block::

    dict = {"test": "value"}

    data = dict.get("test", "Not Fount")

    print(dict["test"])

2. using setdefault() to initialize a dictionary
=================================================

It it common that initializing a dictionary before check the existence of a key,
then create if it doesn't.

* Don't

.. code-block:: python

    dict = {}

    if "key" not in dict:
        dict["key"] = []

    dict["key"]append("123")

* Good

.. code-block:: python

    dict = {}

    dictionary.setdefault("list", []).append("123")

3. speed up your `in` query in dict.
====================================

dict.keys will make dict into list, which is slower than dictionary.

* Don't

.. code-block:: python

    if "some_thing" not in dict.keys():
        print("not found")

* Good

.. code-block:: python

    if "some_thing" not in dict:
        print("not found")

4. using dict keys when formatting strings.
==========================================


.. code-block:: python

    person = {
        'first':'Tobin',
        'last': 'Brown',
        'age':20
    }
    print('{first} {last} is {age} years old'.format(**person))

5.  initialization on Dict.
============================

* Dont't

dict() function call is slower than call {} directly.

.. code-block:: python

    a = dict()

* Good

.. code-block:: python

    a = {}