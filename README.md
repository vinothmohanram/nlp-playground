# NLP Code Examples
A repo for storing code for NLP worked examples, for use in exploring and explaining possible NLP approaches for projects.

----

## Using the example notebooks

The purpose of this repo is to provide a number of worked examples of NLP techniques, to aid understanding of what's possible and how to get started.

Examples are stored in the **examples** folder, with one notebook per approach or example. These are titled with the technique they're using, and are designed to be run as stand-alone notebooks, with the data used accessible to all users of the AP.

Examples currently include:
- Analysis of key themes in consultations: topic modelling, phrase collocation and TF-IDF
- Analysis of sentiment in consultation responses
- Basic demo of sentiment analysis
- Basic demo of summarisation
- Basic demo of text classification
- Basic demo of topic modelling: LDA and BERTopic

There is also a demo of BERTopic for use with Google colab (see the 'colab' folder). This example is designed to be run on Google colab, enabling access to GPU.

  ----

## Other folders

The 'code-dev' folder includes notebooks used by the team in researching and developing the code used for the example notebooks. These are retained for future reference, and are not designed to be used as examples for the techniques they relate to.

----

## Setting up packages

- Clone the repo
- Set up a virtual environment 
  ```
  cd ./nlp-code-examples # Change to correct directory
  python -m venv <env-name> # Create venv - only needs to be done first time
  source <env-name>/bin/activate # Activate venv
  ```
  
- Load the correct packages into the virtual environment from the requirements.txt file. Note that you'll need to [install torch](https://pytorch.org/get-started/locally/) and scikit-learn separately first.
    ```
  pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cpu #install torch first
  pip install -r requirements.txt # Install packages - only needs to be done first time
  ```
  
- Set up your venv as a Jupyter kernel
   ```
   python -m ipykernel install --user --name="venv_PROJECTNAMEHERE" --display-name="My project name"
   ```
   Once this has been set up (you might need to refresh the page), you can select this kernel when using running the Jupyter notebooks.
   
 >Developer note: If you update the requirements.txt file, you'll need to manually remove any lines related to torch, torchvision and torchaudio; these will cause errors in installing pacakges if left in requirements.txt.

----

## Updates and feedback

This repo is a living resource, and will continue to be updated and expanded by the Data Science Capability team over time. If you have any comments or feedback on the content, please contact the team at datasciencecapability@justice.gov.uk

If you think that something is missing or not quite right you should either:
1. [Contribute directly](https://moj-analytical-services.github.io/our-coding-standards/collaborate.html#versioncontrol)
2. [Raise an issue](https://github.com/moj-analytical-services/nlp-code-examples/issues)

