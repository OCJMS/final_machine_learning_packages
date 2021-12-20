# final_machine_learning_packages

1. What I do in this project
    사이킷런 라이브러리에 존재하는 데이터인 Olivetti faces를 사용하여 지도학습 중 하나인 분류 문제를 Support Vector Machine을 이용해서 훈련시켰다.
2. What is the training dataset in this project
    사이킷런 라이브러리에 존재하는 Olivetti faces 데이터이다. 이것은 400개의 sample들로 이루어져 있으며 각각의 sample들에는 대응되는 class가 있다. 이 class는 총 40가지이다.
    data의 shape는 (400,4096)이며 target의 shape는 (400,)이다. 다시 말해 (data,target)의 쌍은 400개이고 각 한 쌍당 data는 4096개의 데이터가 존재하고, target에는 1개의 데이터가 존재한다.
    그리고 이 1개의 데이터는 0~39중 하나이다. 즉, 분류 문제라는 것을 알 수 있다. 
    여기서 (data,target)을 train 데이터(직접 훈련시키는 데이터)와 test데이터(훈련시켜 만든 것을 검증하는 데이터)로 나눈다.
3. What is the algorithm I choose
    Support Vecor Machine을 사용하여서 훈련을 진행시켰다.
4. What is hyper-parameter of the function
    kernel이라는 hyper-parameter는 알고리즘에 사용할 커널 유형을 지정한다. 필자는 여기서 'poly'를 선택하였다.
    또한 kernel을 'poly'로 하면, 또 다른 hyper-parameter인 degree를 지정할 수 있게 된다. 여기서 default값인 3이 아닌 것들을 넣어보면 모두 default일 때보다 더 좋지 않은 accuracy를 
    내는 것을 알 수 있으므로 dgree는 default값인 3으로 유지시킨다.
5. Explanation of code
   svc객체를 만든다(kernel = 'poly') -> fit을 이용하여 훈련시킨다 -> predict를 이용해서 새로운 데이터를 넣어본다 -> 이 predict와 y_test를 이용하여 accuracy를 측정한다.
