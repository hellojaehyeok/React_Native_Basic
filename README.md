# React_Native_Basic
React_Native 기초 공부입니다.



## Style
1. CSS를 설정할 때 object의 namespace를 이용한다.
2. 각 스타일의 속성의 구분은 ; 가 아닌 , 로 구분한다.
3. 스타일 속성 명의 구분은 -이 아닌 대문자로 구분한다. (font-weight  -> fontWeight)
4. 'px', 'em' 등의 단위는 생략한다.

RN

    bigBlue: {
        color: 'blue',
        fontWeight: 'bold',
        fontSize: 30,
    },

5. 축약형이 존재하지 않는다. 대신 상하, 좌우 값을 한 번에 조정할 수 있다.

css

    .item {
        margin: 0 4px 0 6px; 
    }

RN

    item: {
        marginVertical: 0,
        marginBottom: 4,
        marginLeft: 6,
    },

6. :first-child, :nth-child, :focus 등의 가상, 의사, 자식, 형제 선택자를 이용할 수 없다.
7. display 속성의 값이 flex와 none 두 가지 밖에 없다.

## Component
기본 HTML 태그를 사용하지 못하고 RN은 UI를 구현을 위한 기본 컴포넌트를 제공한다.


### View
