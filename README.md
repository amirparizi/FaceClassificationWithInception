# FaceClassification

In this project two different data sets were combined and used ( www.thispersondoesnotexist.com & https://www.face-rec.org/databases/). 1000 pictures were labeled and fed into three different NN architecture.

1.simple CNN with 3 Conv layers

2.VGG16 with loaded weights

3.InceptionV3

table=pd.read_csv('/content/drive/My Drive/Fake Faces/table_fakefaces.csv',)
table
Out[64]:
Model	Feature	TP	FP	FN	TN	Precision	Recall	F1-Score	Accuracy
0	Simple CNN	Gender	43	11	30	17	0.796296	0.589041	0.677165	0.594059
1	VGG16	Gender	41	13	9	38	0.759259	0.820000	0.788462	0.782178
2	InceptionV3	Gender	36	18	0	47	0.666667	1.000000	0.800000	0.821782
3	Simple CNN	Expression	38	1	58	4	0.974359	0.395833	0.562963	0.415842
4	VGG16	Expression	20	19	7	55	0.512821	0.740741	0.606061	0.742574
5	InceptionV3	Expression	32	7	18	44	0.820513	0.640000	0.719101	0.752475
In [89]:
plt.plot(table['Model '][0:3],table['Accuracy'][0:3]);
plt.title('Accuracy in terms of Gender');
plt.figure();
plt.plot(table['Model '][3:6],table['Accuracy'][3:6]);
plt.title('Accuracy in terms of Expressions');
plt.figure();
plt.plot(table['Model '][0:3],table['F1-Score'][0:3]);
plt.title('F1-Score in terms of Gender');
plt.figure();
plt.plot(table['Model '][3:6],table['F1-Score'][3:6]);
plt.title('F1-Score in terms of Expressions');
plt.figure();




<Figure size 432x288 with 0 Axes>
We can see that F1-score and accuracy both increase as we move from simple CSS to more sophisticated models like VGG16 and ultimately InceptionV3 model.
