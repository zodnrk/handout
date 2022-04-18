# Handout
Our handout for the SWOS-Module at BFH.

The topic of our handout is Maven / git.

[Download the handout](https://github.com/zodnrk/handout/releases/download/1.0.0/handout.pdf)

## How to use LaTeX-Templates:
```{.sh}
# check them out
git submodule update --init --recursive

# apply the patch for correct styling
cd .latex
git apply ../document_format.patch
cd ..

# actually build the document
# (requires pandoc and LaTeX)
./.latex/build.sh handout.md
```
