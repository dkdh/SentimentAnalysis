# SentimentAnalysis

실행방법
---------

1. 깃허브에서 파일을 받아 압축을 풀고, 구글 드라이브에 업로드한다.
2. 용량 문제로 깃허브에 올라오지 않은 ratings_train.txt 파일을 SentimentAnalysis 폴더에 넣는다.
3. 용량 문제로 깃허브에 올라오지 않은 checkpoint-20150 폴더를 SentimentAnalysis 폴더에 output이라는 이름의 폴더를 생성해 그 안에 넣는다.

디렉토리 구조:

    ../SentimentAnalysis /transformers/....
                         /output/checkpoint-20150/...
                         /ratings_train.txt
                         /ratings_test.txt
                         /electra_sa.ipynb

4. electra_sa.ipynb 파일을 열고, 첫 셀을 실행시켜 드라이브 마운트를 진행한다. (구글 계정 로그인 필수)
<pre>
<code>
    from google.colab import drive
    drive.mount('/gdrive')
</code>
</pre>

5. 프로젝트 폴더인 SentimentAnalysis의 경로가 gdrive/My Drive/SentimentAnalysis 인지 확인하고, 다른 경로를 사용할 경우 3번째 셀 15번째 줄을 해당 경로로 수정한다.
<code>
sys.path.append("gdrive/My Drive/SentimentAnalysis/transformers") #필요시 깃허브에서 다운로드받은 transformers 경로로 수정.
</code>

6. 사전 학습된 electra 모델은 https://drive.google.com/drive/folders/1FDUQIzUD9UDnytELTVecMscx_SjW5_vf 에서 얻을 수 있다. train을 진행하기 위해서는 해당 링크의 wordpiece_base 폴더를 다운받아 SentimentAnalysis 폴더에 넣어주고, 마지막 셀의 config 정보의 mode를 train으로 변경해준다. test만 한다면 생략해도 된다.

7. 마지막 셀의 root_dir 또한, 프로젝트 폴더인 SentimentAnalysis가 다른 경로로 설정되어 있다면, 해당 경로로 수정해준다.

8. 특정 txt파일로 모델을 test하려면, 마지막 셀 config의 test_data_path를 해당 txt파일의 경로로 바꿔준다.
