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
| InceptionV3    | Gender      |   36 |18 |0  |47  |0.666 | 1.000     | 0.8 |0.821    |
| Simple CNN    | Expression      |   38 |1 |58  |4  |0.974 | 0.395     | 0.563 |0.415    |
| VGG16    | Expression      |   20 |19 |7  |55  |0.512 | 0.740     | 0.606 |0.742    |
| InceptionV3    | Expression      |   32 |7 |18  |44  |0.82 | 0.64     | 0.720 |0.752    |

We can see that F1-score and accuracy both increase as we move from simple CSS to more sophisticated models like VGG16 and ultimately InceptionV3 model.


