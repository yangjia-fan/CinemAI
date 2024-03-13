The **GOAL** of this project is to predictively analyze new input film dialogues/action lines and associate them with distinguished genre types (horror, sci-fi, action, etc.) It is a piece of the puzzle, a first step in automating virtual film production (ALl files open via JupyterNotebook)

**_genre.generator.ipynb_** contains code for a supervised learning NLP model that uses Python’s _pandas_, _nltk_, _sk-learn_, and various libraries to perform ML tasks on film dialogues

Methods used to facilitate the machine learning procedures include tokenization, dimensionality reduction, TFIDF, cross-validation, grid search, and decision tree classifiers

The data is modeled on 100,000 lines of film dialogues with associated genres from Cornell's Movie Dialogue Corpus, contained in the file **_dialogue.db_**

**_Save_OptimalModel.ipynb_** branches from the main _genre.generator.ipynb_ code. It serializes an optimal model using the identified set of hyper-parameters from the main code in a file named **_CinemAiModel.joblib_** using the joblib library

**_Load_OptimalModel.ipynb_** branches from the main _genre.generator.ipynb_ code. It deserializes the optimal model by reading _CinemAiModel.joblib_ to predict user inputs. The environment must be set with the same libraries and custom functions to ensure its environment mirrors the training environment _CinemAiModel.joblib_  was serialized on

You can view an interactive demo to see the code in action on higgingface! - https://huggingface.co/spaces/yangjia-fan/CinemAi
