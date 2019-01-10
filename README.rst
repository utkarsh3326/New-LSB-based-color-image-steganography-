Cryptosteganography
===================

A python steganography module to store messages or files protected with
AES-256 encryption inside an image.

Steganography is the art of concealing information within different
types of media objects such as images or audio files, in such a way that
no one, apart from the sender and intended recipient, suspects the
existence of the message. By default steganography is a type of security
through obscurity.

Additionally this module also enhance the security of the steganography through data encryption. The data concealed
is encrypted using AES 256 encryption, a popular algorithm used in symmetric key cryptography.

Prerequisites
-------------

`Python 3+ <https://www.python.org/downloads>`_

`pip3 <https://pip.pypa.io/en/stable>`_

(Most Linux systems comes with python 3 installed by default).

Dependencies Installation (Ubuntu)
----------------------------------

.. code:: bash

    $ sudo apt-get install python3-pip


Installation
------------

To install the package just run

.. code:: bash

    $ pip3 install cryptosteganography

Usage
-----

Use as a library in a python program
''''''''''''''''''''''''''''''''''''

**Save message example**

.. code:: bash

    $ cryptosteganography save -i 4824157.png -m "My secret message..." -o output.png
    Enter the key password: 
    Confirm the key password: 
    Output image output.png saved with success

**Retrieve message example**

.. code:: bash

    $ cryptosteganography retrieve -i output.png
    Enter the key password: 
    My secret message...

**Save file example**

.. code:: bash

    $ cryptosteganography save -i input_image_name.jpg -f duck_logo.pem -o output_file.png
    Enter the key password: 
    Confirm the key password: 
    Output image output_file.png saved with success

**Retrieve file example**

.. code:: bash

    $ cryptosteganography retrieve -i output.png -o decrypted_file
    Enter the key password: 
    decrypted_file saved with success


