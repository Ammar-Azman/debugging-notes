# Issue: Resource limitation in Streamlit
* Problem hypothesis:
  * The size of the documents is too big, exceeding the memory limit on Streamlit Cloud
* Streamlit has limitation on its RAM memory. 
* This has caused some of the computation process crashed. 
## Description
* Date: 9/5/2023 <br>
* Time: 10:55 <br>
* Error: Crashing while uploading PDF <br>
* Project: Invoice Parser
* Details: - <br>
* Folder tree (during error): - 
## Solution
* Solution idea from Haffiz:
  * Manipulating the instance in Streamlit Cloud by `mkdir data`; a new directory to keep the PDF file.
  * After the `data/` is created, the document uploaded into Streamlit will be stored within `data` directory.
  * Hence, we are not require to convert the PDF to `bytes` (bytes is stored in RAM), and directly taking the document from `data` path. 

* The real solution:
  * (not found yet)


## Status 
- [ ] **Solved**
