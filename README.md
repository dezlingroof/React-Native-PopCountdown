# react-native-popcountdown

React Native PopCountDown

## Installation

Run `npm install react-native-popcountdown --save` OR `yarn add react-native-popcountdown --save`

## Props

| Name           | Description                                                  | Type   |                                      Default Value                                      |
| :------------- | :----------------------------------------------------------- | :----- | :-------------------------------------------------------------------------------------: |
| id             | Counter id, to determine whether to reset the counter or not | string |                                          null                                           |
| style          | Override the component style                                 | object |                                           {}                                            |
| digitStyle     | Digit style                                                  | object | {backgroundColor: ![#FAB913](https://placehold.it/15/FAB913/000000?text=+) `'#FAB913'`} |
| digitTxtStyle  | Digit Text style                                             | object |       {color: ![#FAB913](https://placehold.it/15/000000/000000?text=+) `'#000'`}        |
| timeLabelStyle | Time Label style                                             | object |       {color: ![#FAB913](https://placehold.it/15/000000/000000?text=+) `'#000'`}        |
| separatorStyle | Separator style                                              | object |       {color: ![#FAB913](https://placehold.it/15/000000/000000?text=+) `'#000'`}        |
| size           | Size of the countdown component                              | number |                                           15                                            |
| until          | Number of seconds to countdown                               | number |                                            0                                            |
| onFinish       | What function should be invoked when the time is 0           | func   |                                          null                                           |
| onChange       | What function should be invoked when the timer is changing   | func   |                                          null                                           |
| onPress        | What function should be invoked when clicking on the timer   | func   |                                          null                                           |
| timeToShow     | What Digits to show                                          | array  |                                  ['D', 'H', 'M', 'S']                                   |
| timeLabels     | Text to show in time label                                   | object |                   {d: 'Days', h: 'Hours', m: 'Minutes', s: 'Seconds'}                   |
| showSeparator  | Should show separator                                        | bool   |                                          false                                          |
| running        | a boolean to pause and resume the component                  | bool   |                                          true                                           |

## Code

```javascript
import CountDown from 'react-native-popcountdown';

render() {
    return (
      <CountDown
        until={10}
        onFinish={() => alert('finished')}
        onPress={() => alert('Pressed')}
        size={18}
      />
    )
}
```

## Custom Styling Example

## Code

```javascript
import CountDown from 'react-native-popcountdown';

render() {
    return (
      <CountDown
        until={60 * 10 + 30}
        size={30}
        onFinish={() => alert('Finished')}
        digitStyle={{backgroundColor: '#FFF'}}
        digitTxtStyle={{color: '#333333'}}
        timeToShow={['M', 'S']}
        timeLabels={{m: 'MM', s: 'SS'}}
      />
    )
}
```

## Separator Example

## Code

```javascript
import CountDown from 'react-native-popcountdown';

render() {
    return (
      <CountDown
        size={30}
        until={1000}
        onFinish={() => alert('Finished')}
        digitStyle={{backgroundColor: '#FFF', borderWidth: 2, borderColor: '#1CC625'}}
        digitTxtStyle={{color: '#1CC625'}}
        timeLabelStyle={{color: 'red', fontWeight: 'bold'}}
        separatorStyle={{color: '#1CC625'}}
        timeToShow={['H', 'M', 'S']}
        timeLabels={{m: null, s: null}}
        showSeparator
      />
    )
}
```
