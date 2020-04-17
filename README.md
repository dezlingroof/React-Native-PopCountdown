# react-native-popcountdown

React Native PopCountDown

## Installation

Run `npm i react-native-popcountdown --save` OR `yarn add react-native-popcountdown --save`

## Props

| Name            | Description                                                  | Type   |                                      Default Value                                      |
| :-------------- | :----------------------------------------------------------- | :----- | :-------------------------------------------------------------------------------------: |
| id              | Counter id, to determine whether to reset the counter or not | string |                                          null                                           |
| style           | Override the component style                                 | object |                                           {}                                            |
| digitStyle      | Digit style                                                  | object | {backgroundColor: ![#FAB913](https://placehold.it/15/FAB913/000000?text=+) `'#FAB913'`} |
| digitTxtStyle   | Digit Text style                                             | object |       {color: ![#FAB913](https://placehold.it/15/000000/000000?text=+) `'#000'`}        |
| timeLabelStyle  | Time Label style                                             | object |       {color: ![#FAB913](https://placehold.it/15/000000/000000?text=+) `'#000'`}        |
| size            | Size of the countdown component                              | number |                                           15                                            |
| until           | Number of seconds to countdown                               | number |                                            0                                            |
| onFinish        | What function should be invoked when the time is 0           | func   |                                          null                                           |
| onChange        | What function should be invoked when the timer is changing   | func   |                                          null                                           |
| onPress         | What function should be invoked when clicking on the timer   | func   |                                          null                                           |
| timeToShow      | What Digits to show                                          | array  |                                  ['D', 'H', 'M', 'S']                                   |
| timeLabels      | Text to show in time label                                   | object |                   {d: 'Days', h: 'Hours', m: 'Minutes', s: 'Seconds'}                   |
| running         | a boolean to pause and resume the component                  | bool   |                                          true                                           |
| showLeftKeyword | a boolean to show Left Text                                  | bool   |                                          true                                           |

## Code

```javascript
import {Countdown} from 'react-native-popcountdown';

render() {
    return (
      <Countdown
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
import {Countdown} from 'react-native-popcountdown';

render() {
    return (
      <Countdown
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
import {Countdown} from 'react-native-popcountdown';

render() {
    return (
      <Countdown
        size={30}
        until={1000}
        onFinish={() => alert('Finished')}
        digitStyle={{backgroundColor: '#FFF'}}
        digitTxtStyle={{color: '#211111'}}
        timeLabelStyle={{color: 'red', fontWeight: 'bold'}}
        timeToShow={['H', 'M', 'S']}
        timeLabels={{h:null, m: null, s: null}}
      />
    )
}
```

## You can use moment library to convert time.

install that library first.

#### Example

for Reverse Time countdown

```javascript
import {Countdown} from 'react-native-popcountdown';
import Moment from 'moment'

Moment("2020-04-05T20:00:00Z").unix() - Moment().unix()

<Countdown
   until={Moment("2020-04-05T20:00:00Z").unix() - Moment().unix()}
   onFinish={() => <Text>Live</Text>}
   digitStyle={{}}
   digitTxtStyle={{ color: '#444' }}
   timeToShow={['D', 'H', 'M', 'S']}
   size={12}
   showLeftKeyword={true}
   LeftStyle={{color:'#c22222'}}
   running={true}
/>
```

#### Change Log

```javascript
removed showSeparator variable
------ indivisualy it will show time tag (h m s) after the digit
added showLeftKeyword variable
------ leftKeywordStyle

```

in future we will add new separator style

Thank you for support Please share if you like this project.
