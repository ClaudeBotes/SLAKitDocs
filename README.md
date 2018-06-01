# Overview
The purpose of this project is to show how the SLA Kit can be used to build any mobile app that can be customised in minutes to support a wide variaty of designs, user interactions and animations.

* [Our Philosophy](#Philosophy)
* [Features for Designing Your App](#ForDesigners)
  * [Design Properties](#DesignProperties)
  * [Brand / Color Palette](#Brand)
  * [Colors](#Colors)
  * [Layout](#Layout)
  * [Symbols ( Common Components )](#Symbols)
  * [Animations](#Animation)
* [Features for Developers](#ForDevs)

# <a name="Philosophy"></a>Our Philosophy

All features are built according to three principles:

* All features are created with both **developers** and **designers** in mind. We believe this is the only way for any projet to experiment, itterate and move forward fast.

* All features should ( as far as posible ) be supported without the need for an end user  to resinstal his / her mobile app.

* Descion making logic will always change, so move as much as posible our of compiled code. ( where safe )

* We want to be able to build and design in real time and see our changes on our devices without the need to recompile.

# Supported Features

## <a name="ForDesigners"></a>For Designsers and Business

Style any of the properties for any element on screen, same way designers would in **Sketch** or **any other design tool**.

### <a name="DesignProperties"></a>**Design Properties**
 
* Text
* Text Color
* Text Alignment
* Shadow Radius
* Shadow Opacity
* Shadow OffsetY
* Shadow Color
* Corner Radius
* Border Width
* Border Color
* Background Color
* Asset Name ( name of your exported assets )
* Left Padding For Text ( iOS developers use this for Text Fields )
* Right Padding For Text ( iOS developers use this for Text Fields )
* Line Height
* Placeholder Text
* Placeholder Text Color
* Tint Color ( developers will need this when styling the navbar, app icons or other used assets )
* Opacity
* Text Style
* Text Weight
* Italics
* Prefered Status Bar Style

### <a name="Brand"></a>**Brand**

Same as when you design your brand, we also support the ability to define your brand or color pallete. You will notice that with all the color properties you need to provide a color name. This is to ensure your StyleKit uses your defined brand, and prevents your application and developers from using 50 different shades of a particular color. 

**Brand / Color Pallete supports:**
* 14 pre defined properties which you can assign colors to.
* In case 14 colors are not enough, it is posible to extend your color pallete with as many colors as you may need.

#### <a name="Colors"></a>Color Palette

* primary
* secondary 
* success
* danger
* warning
* info
* light
* dark
* white
* black
* appBackground
* special1
* special2
* special3
* custom

### <a name="Layout"></a>**Layout**
Everything on the UI is ofcourse concerned about how it needs to be positioned related to other UI elements. Depending on your experience as a designer, definately as a developer - we talk about anchoring and how many units from a particular anchor. This ensure we can design and build for auto layout, supporting multiple device sizes.

At this point we do not support defining anchors, but **we do support defining layout configurations for:**

* Left Padding
* Top Padding
* Right Padding
* Bottom Padding
* Width
* Height


### <a name="Symbols"></a>**Symbols ( Common Components )**

As in design, and as in development, you can define a set of symbols or common components that can be reused accross your application to reduce duplication. As with symbols and common components, it is also posible to override these with isntance values.

### <a name="Animation"></a>**Animation**

In the SLA Kit we made provision for designers and developers to define custom preferences ( variables ) which can be used for any purpose you can dream of. One of the first places you would want to use these custom preferences are when you need to deal with Animations.

TODO: Add example
#
##  <a name="ForDevs"></a>For Developers

If you're a developer and you've read this far, you may already know that we've made sure developers can take advantage of some key patterns they're already familiar with, starting with simpliyfing your application code.

#### Features for developers:
* Abstraction of most of your style, layout and animation related code from of your views / compiled code. ( UI Code )

* One place to manage and retrieve all colors and other styling related information.

* Complete 80% of any UI without requiring designs up front.

* Common components with the ability to override with instance properties.

* Develop more applications and views faster with less code.

* No need to write code related to any properties mentioned above. UI elements supported, but not limted to:
  * Buttons
  * Labels
  * Views
  * Table Cells
  * Table Headers
  * Table Footers
  * Stack Views
  * Collection Views
  * Image Views
  * for almost any UI element.

* To create any UI element, just ask the SLA Kit for the component you wish to create, and the SDK will take care of all the rest. 

* **No hard coded layout values other than your anchors. Once an anchor is set and compiled, it can't be changed.** Ask the SLA Kit for a component's layout information and anchor the element to your view in one line. This means developers.

* Our Styled Components packed inside the SLA kit all inherit from it's base classes, we've only supper charged them with addition properties that makes them easier to style and animate so you don't have to. You can make use of these as is with the SLA Kit, or **if you prefer to use your own components ( in typical developer fashion ), that is posible too with no restrictions or loss of features already mentioned.**

* Abiilty to dynamically load **style, layout, animation and preference / parameter information** in realtime while the app is running on the device.

* Ability to dynamically load different **classes** for views in realtime while the app is running on the device.





### **Examples**

*  **Text**
```json
"text": "Sign up today"
``` 
* **Text Color**
```json
"textColorName": "primary"
``` 
* **Text Alignment**
```json
"textAlign": "left"
``` 
* **Shadow Radius**
```json
"cornerRadius": "4.0"
``` 
* **Shadow Opacity**
```json
"shadowOpacity": "0.15"
``` 
* **Shadow OffsetY**
```json
"shadowOffsetY": "3.0"
``` 
* **Shadow Color**
```json
"shadowColorName": "dark"
``` 
* **Corner Radius**
```json
"shadowRadius": "2.0"
```
* **Border Width**
```json
"borderWidth": "1.0"
```
* **Border Color**
```json
"borderColorName": "secondary"
```
* **Background Color**
```json
"backgroundColorName": "secondary"
```
* **Asset Name** ( name of your exported assets )
```json
"assetName": "backgroundImage"
```
* **Left Padding For Text**
```json
"leftPaddingForText": "15"
```
* **Right Padding For Text**
```json
"rightPaddingForText": "15"
```
* **Line Height**
```json
"lineHeight": "1.5"
```
* **Placeholder Text***
```json
"placeholderText": "Username"
```
* **Placeholder Text Color**
```json
"placeholderTextColorName": "secondary",
```
* **Tint Color** ( developers will need this when styling the navbar, app icons or other used assets )
```json
"tintColorName": "primary"
```
* **Opacity**
```json
"opacity":"0.25"
```
* **Text Style**
```json
"fontTextStyle": "body"
```
* **Text Weight**
```json
"fontWeight": "regular"
```
* **Italics**
```json
"italics": "true"
```
