# SAPataaars: Avataaars with an SAP Twist

React component derived from the [Avataaars package](https://github.com/fangpenlin/avataaars). Built on TypeScript, bundled with Webpack, and published on NPM.

This modification of [Avataaars 1.2.1](https://www.npmjs.com/package/avataaars/v/1.2.1) includes new SAP-branded clothing and hat options.

<p align="center"><img src='sapataaars-example.png?raw=true' style='width: 300px; height: 300px;' /></p>

**Install** this package from NPM [here](https://www.npmjs.com/package/sapataaars).

___

## SAP Clothing and Hats

The available clothes are:
* SapBestRunHoodie
* SapCrewneckShirt
* SapIxpBlazer

The available tops (hats) are:
* SapBaseballCap
* SapCowboyHat
* SapToque

All other avatar customizations from [Avataaars 1.2.1](https://www.npmjs.com/package/avataaars/v/1.2.1) are also available. To explore non-SAPataaar options, see [Avataaars Generator](https://getavataaars.com/).

## Credits

The original [Avataaars Generator](https://getavataaars.com/) is developed by [Fang-Pen Lin](https://twitter.com/fangpenlin), and was based on the Sketch library [Avataaars](https://avataaars.com/) designed by [Pablo Stanley](https://twitter.com/pablostanley).

## Usage

A working React project is required as a base.

Install the package:
```shell
yarn add sapataaars

// or

npm install sapataaars --save
```

In the React project, import the SAPataaar component with the preferred character customization:
```jsx
import * as React from 'react'
import Avatar from 'sapataaars'

export default class MyComponent extends React.Component {
  render () {
    return
      <div>
        Your avatar:
        <Avatar
          style={{width: '100px', height: '100px'}}
          avatarStyle='Circle'
          topType='SapBaseballCap'
          accessoriesType='Prescription02'
          hairColor='BrownDark'
          facialHairType='Blank'
          clotheType='SapBestRunHoodie'
          clotheColor='PastelBlue'
          eyeType='Happy'
          eyebrowType='Default'
          mouthType='Smile'
          skinColor='Light'
        />
      </div>
  }
}
```

## Building the Component for NPM Release

TypeScript and Webpack are both required to build the component.

Install all dependencies:
```shell
npm install
```

Update `package.json` with the version number to publish, and optionally create a [Git tag](https://git-scm.com/book/en/v2/Git-Basics-Tagging) for tracking.

Create the package to publish:
```shell
npm run build
```

Finally, publish the package to NPM:
```shell
npm publish
```