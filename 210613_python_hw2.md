# 특정 컬럼에서 특정 문자값 찾기
 - df['embark_lower'].str.contains('south') ## 처음 풀때는 이 코드로 작동했는데 갑자기 작동하지 않음
 - 오류 코드
 
         ---------------------------------------------------------------------------
      KeyError                                  Traceback (most recent call last)
      ~\anaconda3\lib\site-packages\pandas\core\indexes\base.py in get_loc(self, key, method, tolerance)
         3079             try:
      -> 3080                 return self._engine.get_loc(casted_key)
         3081             except KeyError as err:

      pandas\_libs\index.pyx in pandas._libs.index.IndexEngine.get_loc()

      pandas\_libs\index.pyx in pandas._libs.index.IndexEngine.get_loc()

      pandas\_libs\hashtable_class_helper.pxi in pandas._libs.hashtable.PyObjectHashTable.get_item()

      pandas\_libs\hashtable_class_helper.pxi in pandas._libs.hashtable.PyObjectHashTable.get_item()

      KeyError: 'embark_lower'

      The above exception was the direct cause of the following exception:

      KeyError                                  Traceback (most recent call last)
      <ipython-input-8-357a42894f2f> in <module>
      ----> 1 df['embark_lower'].str.contains('south')

      ~\anaconda3\lib\site-packages\pandas\core\frame.py in __getitem__(self, key)
         3022             if self.columns.nlevels > 1:
         3023                 return self._getitem_multilevel(key)
      -> 3024             indexer = self.columns.get_loc(key)
         3025             if is_integer(indexer):
         3026                 indexer = [indexer]

      ~\anaconda3\lib\site-packages\pandas\core\indexes\base.py in get_loc(self, key, method, tolerance)
         3080                 return self._engine.get_loc(casted_key)
         3081             except KeyError as err:
      -> 3082                 raise KeyError(key) from err
         3083 
         3084         if tolerance is not None:

      KeyError: 'embark_lower'
         ---------------------------------------------------------------------------

  # 두 가지 조건이 필터된(Series 2개) 데이터프레임 만들기
   - 1차: df.sort_values(by = ["embarked_c", "pclass_3"]) << 에러남
   - 2차: df[(df['embarked'] == 'C') & (df['pclass'] == 3)].shape << 성공
  
  # Boolean indexing이 뭔지 다시 공부해볼 것
  
  # (Question) fare 가 500보다 큰 값을 출력합니다
   - df[df["fare"] > 500]['fare'] #['fare의 의미는?']
  
  
  
  
  
