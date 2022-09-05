# collecting-artifacts

Exploring passing of files over workspaces, before saving all as artifacts in 1 downstream job.

## Explanation

The main workflow will run:

1. create-file-foobar.txt job
2. create-file-fizzbuzz.txt job
3. save-as-artifacts job

(1) and (2) will create files of _foobar.txt_ and _fizzbuzz.txt_ respectively, under the project's working directory.

We then persist the files to the workspace.

(3) will attach the workspace for this workflow, and saves the 2 files as artifacts.
It is **important** to ensure that the 2 files have unique filepaths (i.e., they do not clash or conflict).
