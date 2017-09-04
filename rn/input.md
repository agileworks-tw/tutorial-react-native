# TextInput
輸入框元件，最常用的使用方式為 onChangeText callback 輸入的內容，然後使用 setState 更改 state 內的資料 


常用 props:
```
autoCapitalize: 自動大小寫 'none', 'sentences', 'words', 'characters'
autoCorrect: 自動修正單字，預設為 true
defaultValue: 預設值
placeholder: 描述輸入字段預期值的提示信息
keyboardType: 鍵盤類型
returnKeyType: 送出按鈕的文字跟行為
'done', 'go', 'next', 'search', 'send', 'none', 'previous', 'default', 'emergency-call', 'google', 'join', 'route', 'yahoo'
secureTextEntry: 隱藏輸入
maxLength: 最長長度

```

```
import React, { Component } from 'react';
import {
  View,
  Text,
  TextInput
} from 'react-native';

export default class InputSample extends Component {
  constructor(props) {
    super(props);
    this.state = {
      name: ''
    };
  }
  render() {
    return (
      <View style={{ flex: 1, justifyContent: 'center', alignItems: 'center'  }}>
        <Text>我的名字是: {this.state.name}</Text>
        <TextInput
          value={this.state.name}
          onChangeText={(value) => {
            this.setState({
              name: value
            })
          }}
          style={{ width: 200, height: 44, padding: 8 }}
        />
      </View>
    );
  }
}
```
