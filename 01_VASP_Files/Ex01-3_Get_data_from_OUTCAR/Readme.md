# 예제 1-3
Optimize 동안 OUTCAR 파일 내에 volume, energy 변화 확인
- volume, energy 를 나타내는 데이터를 추출하여 list 로 작성
- OUTCAR 에 쓰여있는 volume 정보: <code> volume of cell</code> 를 검색하여 volume 에 해당하는 부분 추출
- OUTCAR 에 쓰여있는 energy 정보: <code> free  energy   TOTEN</code> 를 검색하여 energy 에 해당하는 부분 추출

# 예상 결과물
- 데이터 타입: float
- 두 list 의 크기가 같아야함 (포함한 데이터 개수)
<pre>
volume_list = [1086.22, 1069.81, 1031.78, ... ]
energy_list = [-205.53787044, -206.00862023, ...]
</pre>
