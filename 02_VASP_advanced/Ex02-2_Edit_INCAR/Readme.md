# 예제 2-2
- 예제 1-4의 응용버전
- INCAR 내용을 수정하는 def 작성
#### 2-2-1. INCAR 파일을 읽어 dictionary 타입으로 변환시키는 def 작성
def 예시
<pre>
def incar_to_dict(incar_file="INCAR"):
    ...
    ...
    ...
    
    return incar_dict
</pre>
#### 2-2-2. 수정할 option 의 dictionary 를 input 으로 받아 dictionary 타입 incar를 수정하는 def 작성
def 예시
<pre>
incar_dict = {"ENCUT": 1E-05, "ISIF": 2, "ISYM=0"}   # 예시

def edit_incar(incar_dict, input_dict):
    ...
    ...
    ...
    
    return incar_dict
</pre>
#### 2-2-3. dictionary 타입 incar 를 INCAR 파일로 쓰게하는 def 작성
def 예시
<pre>
def write_incar(incar_dict):
    ...
    ...
    ...
    
</pre>
