

#### ʵս��Ŀ

##### 1. ���ݼ�

SVM�ľ������ݼ������ٰ����

ҽ����Ա�ɼ��˻��������׿龭��ϸ�봩�� (FNA) ������ֻ�ͼ�񣬲��Ҷ���Щ����ͼ�������������ȡ����Щ������������ͼ���е�ϸ���˳��֡�ͨ����Щ�������Խ������ֳ����ԺͶ���

��������һ��569����32���ֶΣ�������һ�¾��������ֶΰ�

![�����׷������ںš�֪��Сһ��](https://raw.githubusercontent.com/double-point/GraphBed/master/machine_learning/svm/data_means.jpg)

����mean��β�Ĵ���ƽ��ֵ��se��β�Ĵ����׼�worst��β�����ֵ���������ָ�������������ֵ��

������ʵ��Ҫ��10�������ֶΣ�һ��id�ֶΣ�һ��Ԥ������ֶ�

`���ǵ�Ŀ����ͨ�������������ֶ���Ԥ�����������Ի��Ƕ���`

׼��������3,2,1 ��ʼ

<br>

##### 2. ����EDA

> EDA:Exploratory Data Analysis̽�������ݷ���

���������ݷֲ����

![�����׷������ںš�֪��Сһ��](https://raw.githubusercontent.com/double-point/GraphBed/master/machine_learning/svm/svm_sz_02.png)

һ��569����32���ֶ�

32���ֶ���1��object���ͣ�һ��int��id��ʣ�µĶ���float ���͡�

`���⣺�����в�����ȱʧֵ`

�󵨲²�һ�£�object���Ϳ�������������ݣ������յ�Ԥ�����ͣ���Ҫ���д����ȼ���

���������������ݵ�ͳ�����ݣ�

![�����׷������ںš�֪��Сһ��](https://raw.githubusercontent.com/double-point/GraphBed/master/machine_learning/svm/svm_sz_03.png)

����Ҳûɶ���⣨��ʵ��Ϊ������ݱ���ȽϹ�����

��ֱ�ӿ�ʼ�������̰�

<br>

##### 3. ��������

���Ⱦ��ǽ��������������

![�����׷������ںš�֪��Сһ��](https://raw.githubusercontent.com/double-point/GraphBed/master/machine_learning/svm/svm_sz_04.png)

�����۲�ÿһ������������ָ�꣺��ֵ����׼������ֵ��

`����ѡ���ֵ���������ָ�ָ�������������`

![�����׷������ںš�֪��Сһ��](https://raw.githubusercontent.com/double-point/GraphBed/master/machine_learning/svm/svm_sz_05.png)

���ڻ���ʮ������������ͨ������ͼ����һ������֮��Ĺ�ϵ

```python
# ����ͼ�鿴����֮��Ĺ�ϵ
sns.heatmap(df_data[df_data_X.columns].corr(), linewidths=0.1, vmax=1.0, square=True,
			cmap=sns.color_palette('RdBu', n_colors=256),
			linecolor='white', annot=True)
plt.title('the feature of corr')
plt.show()
```

����ͼ�������ģ�

![�����׷������ںš�֪��Сһ��](https://raw.githubusercontent.com/double-point/GraphBed/master/machine_learning/svm/svm_heatmap.png)

`���Ƿ���radius_mean��perimeter_mean��area_mean����������ǿ��أ�������ֻ����һ��������`

���ﱣ������ͼ����÷���ߵ�perimeter_mean

���һ��

`��Ϊ��������ֵ����ö�����б�׼��`

��׼��֮��������������ģ�

![�����׷������ںš�֪��Сһ��](https://raw.githubusercontent.com/double-point/GraphBed/master/machine_learning/svm/svm_sz_06.png)

<br>

##### 4. ѵ��ģ��

�����Ѿ��������������̣�����ֱ������ģ�Ϳ���Ч����ô��

��Ϊ����֪���������������Ƿ����Կɷ֣��������Ƕ�����һ�������㷨

��������LinearSVC ��Ч��

![�����׷������ںš�֪��Сһ��](https://raw.githubusercontent.com/double-point/GraphBed/master/machine_learning/svm/svm_sz_07.png)

Ч���ܺã���ֱ�õĲ���

> ���׼ȷ�ʾͲ�Ҫ�����ˣ�����������ʵ�ʰ�����ʱ���پ���׼ȷ�ʰ�

ok������SVC��Ч��

��ΪSVC��Ҫ���ò�����ֱ��ͨ�����������û����Լ��ҵ����Ų���

![�����׷������ںš�֪��Сһ��](https://raw.githubusercontent.com/double-point/GraphBed/master/machine_learning/svm/svm_sz_08.png)

Ч�����ã�Сһ��һʱ��������

���Կ���������ģ�ͻ���ѡ��rbf��˹�˺�������Ȼʵ������

<br>

���ˣ��������Ŀ�͵�����

��Ҫ��ͨ������EDA+����������������ݷ���Ĺ�����Ȼ��ͨ��������֤+��������ȷ��������ģ�ͺ����Ų��� 

<br><br>

#### д�ں���Ļ�

DataWhale����ѧϰ�����һ���㷨����ʵSVM�Լ�֮ǰ�Ϳ�����Ҳд����Ӧ�ıʼǣ������ܽ������ͱȽ��������ࡣ

�������ǰ��ƪ���µ�ͬѧӦ�ûᷢ�������ܽỹ�е��磬��Ϊ����ƪ����һ�������ģ��Ǹ�����ʵ�һ���д��д���˻ἰʱ�������ġ�

����ƪ�����ǹ�����������������ݣ�����ҷ���HMM�Լ������Ǻܶ������ǣ�����ƪ�ͳ���HMM�㷨�ˣ��ȵ�HMMд���һ�������������������һ�ڵġ�

�㷨ѧ����ȷʵ�ܳ���������һ���㷨+һ����Ŀ��ѧ��Ӧ�û�ȵ������㷨����˼Щ��Ҳ���гɾ͸�Щ��

**����Сһ����һ����һ�������½ڼ���**



���ˣ�˼ά��ͼ���ϣ�

![�����׷������ںš�֪��Сһ��](https://raw.githubusercontent.com/double-point/GraphBed/master/machine_learning/SVM/mind.png)

<br>







