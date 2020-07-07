# 예제 1-5
#### POSCAR 파일을 읽어 INCAR 파일 수정하기
- POSCAR 정보를 읽어 INCAR 파일에 설정되지 않은 MAGMOM, LDAUL, LDAUU, LDAUJ 값 수정
#### 조건
- POSCAR 의 각 element 갯수를 기록하는 코드가 포함되어야 함
- 각 element 이름을 key 로 저장한 Dictionary 를 활용 (ex. <code>MAGMOM_dict = {"Li":0, "Ni": 3.5 ...}</code>)
#### 값 정보
<pre>
          Li      Ni     Mn      Co     O
-----------------------------------------
MAGMOM     0     3.5    4.5       5     0
LDAUL      0       2      2       2     0
LDAUU      0    5.84   6.14    7.37     0
LDAUJ      0       1      1       1     0
</pre>
