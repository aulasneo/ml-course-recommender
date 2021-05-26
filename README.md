# Course recommender for Open edX
This is a Jupyter Notebook file to run a machine learning demo that implements the Implicit BPR algorithm
to recommend courses for Open edX platform.
## Requirements
- Jupyter Notebook from https://jupyter.org/install.html.
It will run on Linux (not tested) or MacOS (not on Windows).
- AWS CLI from https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-install.html

## How to install
Clone the repository to the local computer and run the Jupyter Notebook.
At the beginning you will find instructions of how to subscribe to the algorithm in Sagemaker's marketplace.
Create a S3 bucket to store all the files.
You will also need to create an IAM role with access to Sagemaker and S3.
## How to run
Update the first cell with actual values of the IAM role and the algorithm ARNs, and the name of the bucket created.
Here you can also set the size of the test set.

We have included a dummy file `student_courseenrollment.csv` that you can use to test, 
but will not produce any interesting result.

Replace the `student_courseenrollment.csv` file in the current directory with actual data. 
There is a script in the second cell of the notebook that can be run on an LMS to extract actual data from MySQL.

You can run repeatedly the first cell of the _Benchmarking_ section to check randomly with other users.

This notebook will accumulate the results in the `scores.csv` and `top10counts.csv` and will show the results
of these multiple runs in the graphs of the _Benchmarking_ section. Each run will change randomly the testing set.
Make several runs with actual data and see the statistical graphs.

# LICENSE
Created by [Aulasneo](https://www.aulasneo.com).

This is distributed under Apache GPL license.

# How to contribute
For additional questions please contact me at [andres@aulasneo.com](mailto:andres@aulasneo.com) or
find our contact information at our [web page](https://www.aulasneo.com).