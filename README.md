# Python Tutorials for CMS
계산과학에 유용한 파이썬 예제 모음입니다.    
Python tutorials for CMS (Computational Materials Science)
### 참고사항
- 학습전 기본적인 파이썬 사용법(for 반복문, list, dictionary 등) 숙지 필요 (점프투 파이썬 등 교재 이용)
- 난이도가 어려워 해결이 안되는 경우에도 다른사람이 작성한 코드 참고는 지양
- 예제 완성 후 서로 확인하여 효율적인 방법 공유
### 예제 일괄 다운로드
##### git 이 설치된 경우
- 연구실 서버에서 실행 <code>git clone https://github.com/91bsjun/cms_python_tuto.git</code>
- Github desktop 에서 repo 복사     
##### 쉬운 다운로드
- 우측상단 녹색 버튼 (Code) 에서 Download - zip 파일 다운로드
# 튜토리얼 목록
### 1. VASP 관련 파일 읽고 쓰기 ([링크](https://github.com/91bsjun/cms_python_tuto/tree/master/01_VASP_Files))
#### POSCAR
예제 1-1) W 를 Mo 로 치환 후 저장하고 원본은 POSCAR.ori 로 백업     
예제 1-2) Selective dynamics 가 적용된 POSCAR 파일 만들기
#### OUTCAR
예제 1-3) OUTCAR 파일 내에 optimize 동안 volume, energy 변화 확인    
#### INCAR
예제 1-4) ISIF=3, ISPIN=1, LCHARG=False, EDIFF=1E-05, PREC=Normal 로 수정 후  원본은 INCAR.ori 로 백업    
예제 1-5) MAGMOM, LDAUL, LDAUU, LDAUJ 값이 설정 되지 않은 INCAR 파일 수정하기 (각 POSCAR 읽어서)    

### 2. VASP 파일 읽고 쓰기 [심화]

추후 업데이트 예정
