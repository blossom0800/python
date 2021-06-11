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

# 컬럼값을 소문자로 바꾸기
 - 역시 한번에 되지 않았음
 - df['컬럼명'] 뒤에 lower()를 써야 하는 것은 알고 있었지만
 - 중간에 str이 들어가야 했음
 - 즉, df.['컬럼명'].str.lower()로 입력해야 정상 출력됨

# 특정 컬럼에서 특정 문자가 들어가는지 여부 확인(T/F), sum 구하기
 - 게속 오류가 난다 -- Do we have a boolean indexer?
 - df[df["컬럼명"].str.contains("찾고자하는 문자")]
 - 사실 위의 구조가 정확히 이해되지는 않음
 - 다시 해보기 > df["컬럼명"].str.contains("찾으려는 문자") --> T/F로 나왔음!
 - 총 갯수 구하기 --> 뒤에 .sum() 만 붙여주면 됨.

# 새 컬럼을 만들고 그 컬럼의 groupby를 하기
 - https://pandas.pydata.org/pandas-docs/stable/user_guide/groupby.html
 - 
