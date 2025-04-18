# 1. 제목
- 1~6개의 # 기호를 사용하여 제목 수준을 지정합니다.

## 예시 중제목

# 2. 텍스트 스타일
- 굵게 : **단어**
- 기울임 : *단어*
- 취소 : ~~단어~~
- 굴고 기울게 : ***단어***

# 3. 텍스트 인용

> 인용구문 (왼쪽화살표 이용)
> 여러줄도 가능합니다.

# 4. 코드 인용

- 인라인 코드 인용 => 이것은 `code` 입니다. (백틱으로 감싸준다)

- 코드 블럭 (백틱 세개로 감싸준다)
```python
def hello():
    print("hello!")
```

```javascript
console.log("hello")
```

# 5. 링크
- [구글](https://google.com)
- 대괄호 안에는 대체텍스트, 소괄호 안에 주소

# 6. 이미지
- ![사진](https://png.pngtree.com/background/20230401/original/pngtree-beautiful-scenery-suitable-for-summer-travel-picture-image_2253560.jpg)
- 느낌표, 대괄호, 소괄호
- 주소 오류났을 때 대괄호 안에 쓴게 보여진다
- ![고양이](../assets/cat.jpeg)
- 상대경로: 나 자신을 기준으로 상대적으로 이동하는것, ..은 상위폴더로 가는것, 지금 markdown 폴더에 있었으니 상위폴더는 TIL임.

# 7. 목록

## 순서 있는 목록
1. 첫번째
2. 두번째
3. 세번쩨

## 순서 없는 목록
- 첫번째
    - 1-1  
    - 1-2
    - 하위항목 만들려면 tab 누르고 -
- 두번째
- 세번째

[출처](https://docs.github.com/ko/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)