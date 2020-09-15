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

