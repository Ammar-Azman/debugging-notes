# Description
Date: 8/5/2023 <br>
Time: 3:29 pm <br>
Issues: `ModuleNotFoundError` <br>
Specific: Script that I have created is not found by the Streamlit Cloud 
Folder tree (during error):
```
form_recognizer
    |- main_project
        |- __init__.py
        |- form_recog.py
        |- utils.py
    |- streamlitui
        |- __init__.py
        |- main_ui.py
        |- fr_ui.py
        |- utils,py
```
* Top-script for Streamlit Cloud: `main_ui.py`

# Solution
* Move the `main_ui.py` into `form_recognizer` directory (outside of `streamlitui` dir)
```
form_recognizer
    |- main_project
        |- __init__.py
        |- form_recog.py
        |- utils.py
    |- streamlitui
        |- __init__.py
        |- fr_ui.py
        |- utils.py
    |- main_ui.py
```
* Problem hypothesis:
  * Top-script cannot have the same level as module 
  * If it happens, the problem might occur during import the module

# Status 
* **Solved**✅
