# Radar Charts

Basic Radar Chart
```javascript
render() {
  let data = [{
    "speed": 74,
    "balance": 29,
    "explosives": 40,
    "energy": 40,
    "flexibility": 30,
    "agility": 25,
    "endurance": 44
  }]

  let options = {
    width: 290,
    height: 290,
    margin: {
      top: 20,
      left: 20,
      right: 30,
      bottom: 20
    },
    r: 150,
    max: 100,
    fill: "#2980B9",
    stroke: "#2980B9",
    animate: {
      type: 'oneByOne',
      duration: 200
    },
    label: {
      fontFamily: 'Arial',
      fontSize: 14,
      fontWeight: true,
      fill: '#34495E'
    }
  }

  return (
    <View>
      <Radar data={data} options={options} />
    </View>
  )
}
```


Radar Chart with Circles
> With circles on the label points
```javascript
// OPTIONAL
handleOnCirclePress(key, value) {
  // example:
  // key -> "speed"
  // value -> 74
}

render() {
  let data = [{
    "speed": 74,
    "balance": 29,
    "explosives": 40,
    "energy": 40,
    "flexibility": 30,
    "agility": 25,
    "endurance": 44
  }]

  let options = {
    width: 290,
    height: 290,
    margin: {
      top: 20,
      left: 20,
      right: 30,
      bottom: 20
    },
    r: 150,
    max: 100,
    rings: 3,
    valueColorPoints: 1,
    colorCircleSize: 5,
    circleColors: {
      "speed": '#9b58b5',
      "balance": '#e84c3d',
      "explosives": '#e77e23',
      "energy": '#f1c40d',
      "flexibility": '#23a086',
      "agility": '#e3a086',
      "endurance": '#000000'
    },
    fill: "#2980B9",
    stroke: "#2980B9",
    animate: {
      type: 'oneByOne',
      duration: 200
    },
    label: {
      fontFamily: 'Arial',
      fontSize: 14,
      fontWeight: true,
      fill: '#34495E'
    }
  }

  return (
    <View>
      <Radar data={data} options={options} onCirclePress={this.handleOnCirclePress}/>
    </View>
  )
}
```
