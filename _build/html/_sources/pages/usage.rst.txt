Usage
============

Using Chamelon
-----------------

Basic Chamelon usage is:

.. code-block:: shell-session

   $ chamelon -c "[compile command]" -e "[error]" input.ml

 
This will execute the compile command on ``input.ml``, and produce a minimized output ``input_min.ml`` such that the output of the command still contains ``[error]``.

Logs
----------------------

After running this command, Chamelon will display in the standard output the steps it performed:

- ``Starting to minimize [minimized_name].ml`` before each minimization attempt.

- Then, for each atomic heuristic: ``Trying heuristic-name: pos=i, len=j...`` before trying to perform heuristic-name at j program points starting from position i.

- Then, after each atomic heuristics:

   + ``Reduced.`` when the transformation is applied.
   + ``Removes error.`` when the transformation removes the error.
   + ``No more changes.`` when the end of the program is reached.


Options
------------------------------


Chamelon accepts the following options:

.. program:: chamelon

.. option:: -o [file]

   use ``[file]`` as the output instead of the default - that is, suffixing the input file with ``_min``. Inplace minimization can be achieved by setting the output file to the input file.

.. option:: -t [command]

   use ``[command] input.ml`` to produce a ``.cmt`` file from an OCaml file. This is necessary when the given command is not a compilation command and does not produce ``.cmt`` file by itself. This is also useful if you want to minimize a file when the compilation command produces ``.cmt`` files incompatible with the version of OCaml chamelon is compiled with.

.. option:: -m [minimizers]

  run the minimizers from the comma-separated list of minimizers ``[minimizers]`` given as argument instead of the default iteration order.