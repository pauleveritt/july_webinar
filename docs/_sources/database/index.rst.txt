Database
========

PyCharm isn't just an IDE for your Python and web development. It also
include DataGrip, our IDE for SQL databases.

Let's change the Flask todo list to get data from a database table.

Features Shown
--------------

- Automatic install and import



Steps
-----

#. Add ``db = SQLAlchemy(app)`` then install and import it

#. Config database

#. Make the ``Todo`` model

#. Use Python Console to import the db and call ``db.create_all()``

#. Drag the ``todos.db`` file onto the Database tool

#. Enter some todos and ``Submit``

#. In Flask view, change the ``todos`` line to use a query

#. Reload browser

#. ``Optimize Imports`` to get rid of the dead import of ``randint``

Code
----

.. code-block:: python

    from random import randint

    from flask import Flask, render_template
    from flask_sqlalchemy import SQLAlchemy

    app = Flask(__name__)
    app.config['SQLALCHEMY_DATABASE_URI'] = 'sqlite:///../todos.db'
    db = SQLAlchemy(app)


    class Todo(db.Model):
        id = db.Column(db.Integer, primary_key=True)
        name = db.Column(db.String(80))


    @app.route("/")
    def hello():
        return '<h1>Hello World!</h1><a href="/todos">Todos</a>'


    @app.route('/todos')
    def todos_list():
        todos = Todo.query.all()
        todo_count = len(todos)
        return render_template("todos_list.jinja2",
                               todo_count=todo_count,
                               todos=todos)


    if __name__ == '__main__':
        app.run(debug=True)
