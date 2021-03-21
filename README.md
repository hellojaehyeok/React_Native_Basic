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
div 같은 역할을 한다. (구역을 나눌 때 사용)

### Text 
p 같은 역할을 한다. 텍스트를 입력 시 Text 안에 넣어 사용한다.

### Image
img 를 넣을 시 사용한다.
경로는 아래 코드와 같이 지정한다.

    source={require('../img/logo.png')}

### TouchableOpacity
버튼을 만들 때 주로 사용한다.
터치 시 opacity의 변화를 주며 이벤트가 실행된다.

    <TouchableOpacity
    activeOpacity={0.8}>
        <Tex>버튼</Tex>
    </TouchableOpacity>

### ScrollView
RN에서는 컨텐츠의 양이 많다고 해서 자동적으로 스크롤이 생기는 게 
아니기 때문에 ScrollView를 사용하여 스크롤이 가능하도록 만들어 주어야 한다.

### TextInput
input 같은 역할을 한다.
onChange를 사용하여 이벤트를 주어도 괜찮지만 onChangeText를 사용하면 더욱 편하게 
조작 가능하다. e.target.value를 사용하지 않아도 현재의 값을 가져올 수 있다.
비밀번호를 입력 시 값이 보이지 않아야 하기 때문에
secureTextEntry={true} 를 사용하여야 한다.

    const onChangeName = (e) => {
        setUserName(e);
    }
    .
    .
    .
    <TextInput 
    placeholder="이름을 입력해 주세요"
    value={userName}
    style={styles.inputBox}
    onChangeText={(e) => {onChangeName(e)}}
    />
