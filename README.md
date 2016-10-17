## react-native-countdown

A <CountDown> component for react-native

### Add it to your project

Run `npm install react-native-countdown --save`

```javascript
// Within your render function. Count down after press it.
<CountDown
  onPress={this.sendAgain} //default null
  text={'Try again'} //default ''
  time={60} //default 60
  buttonStyle={{padding:20}}
  textStyle={{color:'black'}} //default black
  disabledTextStyle={{color:'gray'}} //default gray
/>
```
## TODOS

- [x] Add custom style

## this is a simple demo

```
 static defaultProps = {
    isChecked: false
  };
  static propTypes = {
    isChecked: React.PropTypes.bool
  };

  constructor(props) {
    super(props);
    this.state = {
      isChecked: props.isChecked
    }
  }

  renderCountDown(){
    if (this.state.isChecked) {
       return(   
    <CountDown
  onPress={this.sendAgain.bind(this)} //default null
  text={'重新获取'} //default ''
  time={60} //default 60
  buttonStyle={{padding:20}}
  textStyle={{color:'black'}} //default black
  disabledTextStyle={{color:'gray'}} //default gray
  />)
       }
else{
       return(
        <Text style ={styles.tip} onPress={this.sendCode.bind(this)}>获取验证码</Text> 
       )
}
   }




  sendAgain(){

    
  }

  sendCode(){

    this.setState({ isChecked: !this.state.isChecked });
  }
  render(){
    return (
      <View style={styles.container}>

        <Text style={styles.tip}>{'CountDown in timestamp \n 以日期-时间为单位的倒计时'}</Text>
        <View style={styles.row}>
        {this.renderCountDown()}
        </View>
      </View>
    )
  }
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: 'space-around',
    alignItems: 'center',
    backgroundColor: '#F5FCFF',
  },
  row: {
    padding: 7,
    backgroundColor: 'red',
    borderRadius: 7,
  },
  tip: {
    fontSize: 20,
  },
  cd: {
    textAlign: 'center',
    color: 'white',
    fontSize: 20,
  },
});
```
