## Materials Genome Foundation Workshop

Assets for the Materials Genome Foundation workshop.


## Building the Documentation

The following command will build the workshop docs:

``` python
pip install -r requirements-docs.txt
python setup.py develop
mkdocs build
```

## Developing

Develop new material in either `jupyter-notebook`s or Markdown documents in the `workshop` folder. Any data that needs to be preloaded for use in the notebooks should be kept in the `python_module` or kept locally in the lesson folder if it will be loaded as part of the lesson progress.

Please run `pre-commit run -a` before commiting new material to ensure it is properly formatted and cleaned of any problematic metadata such as kernel name in the Jupyter Notebook.
