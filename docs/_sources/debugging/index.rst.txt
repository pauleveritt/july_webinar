Debugging
=========

PyCharm's visual debugger is its highest-valued feature. Let's show it
in action while changing the todo listing to use a sequence of fake data
in dictionaries.

Features Shown
--------------

- Visual debugging, both in Python and Django/Jinja2 templates

Steps
-----

#. Stop the run, and run instead under the debugger, reload browser

#. Edit the todo_list route to have, locally, a list of todos passed
   into the template

#. Edit the template to iterate over a sequence of todos in a ``<ul>``,
   but *with an error*

#. Reload browser, see the error

#. Put a breakpoint in the Flask view, data looks good

#. Put a breakpoint in the template, see the error
