# Row, Column의 갯수 구하기
 - df.shape

# (Question) 결측치를 센다는 것이 무슨 의미인지?
 - 해결: df.isna().sum()
 - 구글 키워드: python count number of nan in dataframe column

# 특정 컬럼을 그룹화해서 세기
 - df.groupby(['컬럼명']).size()
 - 예시와 정확히 같게 나오지는 않았음
 - 구글 키워드 : python dataframe count by group
 - https://stackoverflow.com/questions/19384532/get-statistics-for-each-group-such-as-count-mean-etc-using-pandas-groupby

# 특정 컬럼의 요약값 구하기
 - 처음에는 df.describe(['컬럼명'])으로 넣어서 오류 발생
 - 컬럼명이 df로 들어가야 했음 > df.['컬럼명'].describe
 - https://stackoverflow.com/questions/50165953/python-dataframes-describing-a-single-column
 - 결과: count, mean, std, min, 4분위수 출력

# object 요약값 구하기
 - count, unique, top, freq를 출력함
 - df.describe(include='object')
 - 배운 점: object 맨앞을 대문자로만 써도 인식을 못함 ㅠ_ㅠ
