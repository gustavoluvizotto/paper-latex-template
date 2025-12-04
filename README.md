# Latex source code for the paper "TITLE"

## SW Requirements  

- make  
- latexmk  
- bibtex  
- git-latexdiff  

It has been tested on MacOS, but it should work as well on any Linux distribution with the above SW installed.  

## Usage  

To generate the paper's pdf, simply run:  
```
make
```

The build artifacts will be created and placed into the ``build`` directory.  

If you want to generate a ``diff`` between two pdfs, run the following:  
```
make diff from=COMMIT1 to=COMMIT2
```

Where ``COMMIT1`` and ``COMMIT2`` are commit hash, tag or git reference (e.g., HEAD).  

To clean the build artifacts and start a fresh build (due to any strange Latex error), run the following:  
```
make clean
```

## Set up webpage

Copy to your repository the .github/workflows/build_yml file. Go to Settings -> Pages and select the following options:

Source: Deploy from branch  
Branch: gh-pages (it may take a while to this branch appear; it depends on Github workflow process one time after you insert the .github/workflows/build_pdf.yml)  
/ (root)  

Hit "Save". Go back to your repository page. Then click on the engine icon next to the "About" (top right of the page). Then, check the following boxes:  

- Use your GitHub Pages website  
- Releases
- Packages
- Deployments 

