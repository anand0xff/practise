# practise
sandbox for developing our two-developer workflow created by **developer A**

  - master branch has no files
  - give collab status to **developer D**
  
#### Step 1:

**A** locally makes a dev branch of the master branch for future advances, **adev**, and pushes adev  



  - A creates a file that only A edits, **file_a.py** 
  - A creates a file that both A and D will work on in their respective branches, **fileboth.py**
  - **A does not push local copy of the changed branch adev to the repo**
	 
	 
		  file_both.py in adev contains these lines:
		  x = 1  
		  z = 3.142  
		  boo = True  
		  abcd = 5
    
#### Step 2:

**D** locally makes a dev branch of the master branch for future advances: **ddev**, and pushes ddev  

  - B creates a file that only D edits, **file_d.py**
  - B creates a file that both D and A work on in their respective branches, **file_both.py**, 
  - **file_both.py** is different from A's file of the same name
  - **D does not push local copy of the changed branch ddev to the repo**


	      file_both.py in ddev contains these lines: 
	      x = 1  
	      z = 2.718   
	      log = True  
	      wxyz  = 15  
 
#### Step 3:

**Merging** with [resolving conflicts](https://github.com/cubeton/git101/blob/master/TurtorialInfo/AdditionalGitTechniques.md):

- A pushes adev, D pushed ddev to the repo
- A makes a pull request to B to merge adev with the primary development branch **dev**
- D merges, resolving any conflicts by accepting A's versions
  
#### Step 4:

**Propagate changes of stable development branch to the master**

- A makes a pull request for D to merge dev with master
- They resolve problems using issues?
