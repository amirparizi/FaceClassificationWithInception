# FaceClassification

In this project two different data sets were combined and used ( www.thispersondoesnotexist.com & https://www.face-rec.org/databases/). 1000 pictures were labeled and fed into three different NN architecture.

1.simple CNN with 3 Conv layers

2.VGG16 with loaded weights

3.InceptionV3

Here you can find the summary of the results from these three models. Also you can try your own pictures or capture pictures using your webcam (InceptionV3 used as a model)

| Model         | Feature       |   TP  | FP | FN | TN | Precision | Recall | F1-Score | Accuracy|
| ------------- |:-------------:| -----:|:--:|:--:|:--:|:---------:|:------:|:--------:|:-------:|
| Simple CNN    | Gender.       | 43    |11  |30  |17  | 0.797     | 0.589  |0.677     | 0.594   |
| VGG16    | Gender      |   41 |13 |9  |38  |0.759  | 0.820     | 0.788 |0.782    |
| zebra stripes | are neat      |    $1 |

We can see that F1-score and accuracy both increase as we move from simple CSS to more sophisticated models like VGG16 and ultimately InceptionV3 model.
VGG16	Gender	41	13	9	38	0.759259	0.820000	0.788462	0.782178
