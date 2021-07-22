(Source: https://wikidocs.net/47193)

# Install
`pip install -U pandas-profiling`

# Import
```
import pandas as pd
import pandas_profiling
```

# Profiling
```
pr=data.profile_report() # 프로파일링 결과 리포트를 pr에 저장
# data.profile_report() # 바로 결과 보기
```
데이터프레임에 .profile_report()를 사용하여 데이터를 프로파일링한 리포트를 생성할 수 있습니다. 만약 저장할 변수를 지정하지 않으면 주피터 노트북에서 바로 리포트를 확인할 수 있습니다.

# Save
`pr.to_file('./pr_report.html')` # pr_report.html 파일로 저장

# Result
`pr`

