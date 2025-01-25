A simple multfile LaTeX example project. 

Typically each .tex file generates some (enormous) amount of build files. I'd highly recommend configuring whatever latex compiler you are using to _not_ dump these files into the root directory, and instead to dump them in a folder like `/build`.

In VSCode, using [Latex Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop), you can configure the build directory following steps:
- Open settings (`Ctrl + ,`)
- In the search bar type in `@ext:james-yu.latex-workshop` (this _should_ autofill if you have installed Latex Workshop correctly)
- In the search bar add `out dir`. Your final search command should be `@ext:james-yu.latex-workshop out dir`
- In the setting `Latex Workshop > Latex: Out Dir` add `/build`, making the setting `%DIR%/build`

Verify that build files are being stored in a directory called `build`. Keep in mind that LaTeX will not clear old build files that were already made.

Lastly, if you do not want to continiously recompile **all** files, you can open the intermediate `.pdf` from each subfile. Keep in mind that references in this file may not be correct or entirely missing! If you want to verify if these are correct you can _only_ do this in the final generated `.pdf`.
