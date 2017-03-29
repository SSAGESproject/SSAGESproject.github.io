#SSAGES and COPPS Website

To work on the website, work only out of the `project` directory.  Files at the top level will be autogenerated later.

When ready to deploy, either locally or on the GitHub pages, take the following steps:

1. Install the website requirements: `pip install -r requirements.txt`
2. Execute `python freeze.py`.  This will generate a static version of the website.

To run locally:

1. Execute `python run.py`.  
2. Point your browser of choice to localhost:5000.  Success!

To deploy on GitHub Pages:

1. Commit your changes to the `gh-pages` branch.  
2. Navigate to https://whitmergroup.github.io/SSAGES-site/.  Success!

To update the documentation:

1. From a SSAGES repository, build the documentation (follow instructions there).
2. Copy the results of building the API documentation into the api folder at the top level of this repository (for the hosted website) and in the project/templates/api directory (for running locally).  
3. Do the same for the results of building the Sphinx manual.

The included pythons script copydocs.py will automatically run this process (simply edit the file to give it a path to a current SSAGES install)

Unfortunately at the moment there is an unresolved bug in testing the API referance and manual for local testing; the CSS and JS will not be picked up by the flask app and thus the pages will not render properly.  However, since there is no need to test the content of these automatically generated pages, this is not considered critical; once you update the api and manual folders appropriately, the content will be served just fine on the hosted website.
