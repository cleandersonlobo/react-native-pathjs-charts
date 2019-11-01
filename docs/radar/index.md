# Radar Charts

## Basic Radar Chart
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


## Radar Chart with Circles
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


## Radar Chart with Text List
> Solution for compound texts
```javascript
// OPTIONAL
handleOnLabelPress(key, value) {
  // example:
  // key -> "speed"
  // value -> 74
}

render() {
  let data = [{
    "DUAL WEAPON": 74,
    "WHITE WEAPONS SKILL": 29,
    "SHOT EXPERTISE": 40,
    "MAGIC SKILL": 40,
    "PRODIGY": 30,
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
    rings: 5,
    valueLinePoints: 1,
    textArray: {
      "DUAL WEAPON": {
        texts: ['DUAL', 'WEAPON'],
        textAnchor: 'middle', // start, middle, end
        x: 0, // adjusts
        y: 0,
      },
      "WHITE WEAPONS SKILL": {
        texts: ['WHITE WEAPONS' 'SKILL'],
        textAnchor: 'middle', // start, middle, end
        x: 10, // adjusts
        y: 0,
      },
      "SHOT EXPERTISE": {
        texts: ['SHOT', 'EXPERTISE'],
        textAnchor: 'middle', // start, middle, end
        x: 0, // adjusts
        y: 0,
      },
      "MAGIC SKILL": {
        texts: ['MAGIC', 'SKILL'],
        textAnchor: 'start', // start, middle, end
        x: 0, // adjusts
        y: 0,
      },
      "PRODIGY": {
        texts: ['PRODIGY'],
        textAnchor: 'end', // start, middle, end
        x: 0, // adjusts
        y: 0,
      },
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
      <Radar data={data} options={options} onLabelPress={this.handleOnLabelPress}/>
    </View>
  )
}
```

