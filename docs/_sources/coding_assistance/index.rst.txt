Coding Assistance
=================

PyCharm excels at helping you code in Python and Python frameworks.
`Coding Assistance <https://www.jetbrains.com/pycharm/features/coding_assistance.html>`_
provides autocomplete, error highlighting, and quick fixes.

In this step we add a second Flask route.

Features Shown
--------------

- Autocomplete

- Live Templates

- Warnings

- Quick fixes

- Template language support

- Language injection

Steps
-----

#. Start making the route manually and show autocompletion.

#. Delete that and use the Live Template.

#. Use Quick Preview to show documentation on the route

#. Set PyCharm Preferences to use Jinja2 as template language

#. Make a ``templates`` folder and mark it as a template folder

#. Create the template file at ``src/templates/todos.jinja2``

#. Change route to ``return render_template('todos.jinja2')``

#. Set language injection on the existing string of HTML

#. Edit inline string to link to the new route

#. Reload and view in browser

#. Change to ``@appx`` to show the error

#. Leave out a space at the end to show PEP8 warning

#. Pass in a count of todos using randint, with Alt-Enter to
   generate the import

#. View in the browser