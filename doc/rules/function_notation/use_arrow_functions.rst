============================
Rule ``use_arrow_functions``
============================

Anonymous functions with one-liner return statement must use arrow functions.

.. warning:: Using this rule is risky.

   Risky when using ``isset()`` on outside variables that are not imported with
   ``use ()``.

Examples
--------

Example #1
~~~~~~~~~~

.. code-block:: diff

   --- Original
   +++ New
   @@ -1,4 +1,2 @@
    <?php
   -foo(function ($a) use ($b) {
   -    return $a + $b;
   -});
   +foo(fn ($a) => $a + $b);

Rule sets
---------

The rule is part of the following rule set:

@PHP74Migration:risky
  Using the `@PHP74Migration:risky <./../../ruleSets/PHP74MigrationRisky.rst>`_ rule set will enable the ``use_arrow_functions`` rule.
