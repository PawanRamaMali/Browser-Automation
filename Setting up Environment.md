## Setting up Python Virtual Environment

We use a module named virtualenv which is a tool to create isolated Python environments. virtualenv creates a folder which contains all the necessary executables to use the packages that a Python project would need.

Installing virtualenv
```
$ pip install virtualenv
```

Test your installation:
```
$ virtualenv --version
```

Using virtualenv

You can create a virtualenv using the following command:
```
$ virtualenv my_name
```
After running this command, a directory named my_name will be created. This is the directory which contains all the necessary executables to use the packages that a Python project would need. This is where Python packages will be installed.

If you want to specify Python interpreter of your choice, for example Python 3, it can be done using the following command:
```
$ virtualenv -p /usr/bin/python3 virtualenv_name
```

To create a Python 2.7 virtual environment, use the following command:
```
$ virtualenv -p /usr/bin/python2.7 virtualenv_name
```

Now after creating virtual environment, you need to activate it. Remember to activate the relevant virtual environment every time you work on the project. This can be done using the following command:
```
$ source virtualenv_name/bin/activate
```

Once the virtual environment is activated, the name of your virtual environment will appear on left side of terminal. This will let you know that the virtual environment is currently active.

Now you can install dependencies related to the project in this virtual environment. For example if you are using Django 1.9 for a project, you can install it like you install other packages.

```
(virtualenv_name)$ pip install Django==1.9
```

The Django 1.9 package will be placed in virtualenv_name folder and will be isolated from the complete system.
Once you are done with the work, you can deactivate the virtual environment by the following command:

```
(virtualenv_name)$ deactivate
```
