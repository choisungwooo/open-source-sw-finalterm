# Brain Tumor Classification
[![MIT License](http://img.shields.io/badge/license-MIT-blue.svg?style=flat)](LICENSE)


## Goal of this project
In this project, we want to find the best model to fit the training data points by using Scikit Learn


## Training dataset
- Brain Tumors are classified as : glioma, meningioma, pituitary, no tumor
- There are four folders that contains MRI data
- Each folder have MRIs of respective tumor classes


## Install

```bash
pip install jupyter
```

### Requirements

You need a machine learning packages and plotting library.

- Install the scikit-learn

  ~~~shell
  pip install scikit-learn scikit-image
  ~~~

- Install the matplotlib

  ~~~shell
  pip install matplotlib
  ~~~

## Classification Model & Tuning

Voting Classifiers

: machine learning model that trains on an ensemble of numerous models and predicts an output based on their highest probability of chosen class as the output.

In this project, I'll use Voting Classifiers by combining the three classifiers.
   ~~~shell
   estimators = [('svc',svc), ('knn', knn), ('etc', etc)]
   voc = VotingClassifier(estimators, voting='soft',n_jobs=-1)
   ~~~

1. Support Vector Machine

   ~~~shell
   svc = SVC(C=10, gamma=0.01, probability=True)
   ~~~

2. K Nearest Neighbors

   ~~~shell
   knn = KNeighborsClassifier(n_neighbors=1, p=4)
   ~~~
   
3. Extra Tree

   ~~~shell
   etc = ExtraTreesClassifier(random_state=100)
   ~~~



## 👋 Contact


<table>
    <tr height="160px">
        <td align="center" width="150px">
            <a href="https://github.com/choisungwooo"><img height="120px" width="120px" src="https://avatars.githubusercontent.com/u/104629605?v=4"/></a>
            <br />
            <strong>choisungwooo</strong>
    </tr>
    <tr height="50px">
        <td align="center">
            <a href="https://github.com/choisungwooo">:octocat: GitHub</a>
        </td>
    </tr>
</table>

- email : andy0354@cau.ac.kr
