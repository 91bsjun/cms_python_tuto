# 예제 1-4
#### INCAR 파일에서 해당 옵션으로 수정 후 저장. 원본은 INCAR.ori 로 백업
- ISIF=3
- ISPIN=1
- LCHARG=False
- EDIFF=1E-05
- PREC=Normal
#### 조건    
- INCAR 옵션 전체를 dictionary 타입으로 저장 (ex. <code>{"NWRITE": 2, "ISTART": 0, "LWAVE": ".FALSE."  ... }</code>
