# Overview
The purpose of this project is to show how the SLA-Kit can be used to build any mobile app that can be customised in minutes to support a wide variaty of designs, user interactions and animations, using the same compiled source code.

* [Our Philosophy](#Philosophy)
* [Features for Designing Your App](#ForDesigners)
  * [Design Properties](#DesignProperties)
  * [Brand / Color](#Brand)
  * [Colors Palette](#Colors)
  * [Layout](#Layout)
  * [Symbols ( Common Components )](#Symbols)
  * [Animations](#Animation)
* [Features for Developers](#ForDevs)
* [Getting Started](#GettingStarted)
  * [Design Properties](#StartDesignProperties)
  * [Brand / Colors](#StartColors)
  * [Symbols ( Common Components )](#StartSymbols)

# <a name="Philosophy"></a>Our Philosophy

All features are guided by four principles:

* Features should be created with both **developers** and **designers** in mind. We believe this is the only way for any projet to experiment, itterate and move forward fast.

* User experiences should ( as far as posible ) be delivered without the need for consumers to resinstall their app. This reduces time to market, costs to business and reults in less friction between the end consumer and the product.

* Descion making logic will always change, so remove as much as posible from the compiled source code. ( where safe )

* We believe product creators should create and experiment in real time, without the need to wait for developers to develop, compile and install before experiencing an idea. Real time design and develop increases the amount of ideas that can be tested in the same amount of time as traditional development cycles.

# Supported Features

## <a name="ForDesigners"></a>For Designsers and Business

Style any property for a given UI element you would in **Sketch** or **any other design tool**.

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

When creating any design system, it is critical to establish your brand and color palette. The SLA-Kit allows you to define your brand and color palette for consistency arcross multiple applications.

**Brand / Color Pallete supports:**
* 14 pre-defined colors which you can assign colors values to.
* 14 colors not enough? You can always  to extend your color pallete with as many colors as you may need.

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
 UI elements are positioned related to other UI elements on screen. Depending on your experience as a designer, definately as a developer - we position elements / views / layers relative to other elements on screen. We do this by defining one or more anchors for a given element, and how many units from those particular anchors we want to position our element. This is refer to as responsive designing or autolayout in the context of iOS development. It ensures our designs and implimentations supports multiple device sizes when they need to scale or shrink.

At this point we do not support defining anchors, but **we do support defining layout configurations for:**

* Left Padding
* Top Padding
* Right Padding
* Bottom Padding
* Width
* Height

Thus it is up to designers and developers to collaborate on defining the best anchors to ensure a fexible UI.

**Once an anchor is set and the app installed, it can't be changed unless changes are made to the compiled code - forsiing the user to reinstall his/her app. This is one of the few features by the SLA-Kit that is not dynamically supported.**

### <a name="Symbols"></a>**Symbols ( Common Components )**

As in design, and in development, you can define a set of symbols or common components that can be reused accross your application(s) to reduce duplication of work. As with symbols and common components, it is also posible to override isntance values.

### <a name="Animation"></a>**Animation**

In the SLA-Kit we made provision for designers and developers to define custom preferences ( variables ) which can be used for any purpose you can dream of. One of the first places you would want to use these custom preferences are when you need to deal with Animations.

TODO: Add example
#
##  <a name="ForDevs"></a>For Developers
#

If you're a developer and you've read this far, you may already know that we've made sure developers can take advantage of some key patterns they're already familiar with, starting with simplifying your application code by means of style kits and inheritance.

#### Features for developers:
* Abstraction of most style, layout and animation related code from of views / compiled code. ( UI Code )

* Central place to manage and retrieve all colors and brand.

* Complete 80% of any UI without requiring designs up front.

* Common components with the ability to override with instance values.

* Develop more features faster, with less code.

* No need to write any code  related to UI. ( apart from creation and layout ) UI elements supported, but not limted to:
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

* To create any UI element, just ask the SLA-Kit for the component you wish to create, and the SLA-Kit will take care of all the rest. 

* **No hard coded layout values other than anchors. Once an anchor is set and installed, it can't be changed.** Ask the SLA-Kit for a component's layout information and anchor the element to your view.

* Our Styled Components included in the SLA-Kit comes packed with styling and animation features. They all inherit from their respective base classes, we've only supper charged them with additional capabilities so you can style and animate them faster and easier. You can make use of these as is with the SLA-Kit, or **if you prefer to use your own components ( in typical developer fashion ), that is posible too with no restrictions or loss of features provided by the SLA-Kit.**

* Abiilty to dynamically load **style, layout, animation and preference / parameter information** in realtime while the app is running on the device.

* Ability to dynamically load different **classes** for any UI element ( headers, buttons, cells etc ) in realtime while the app is running on the device.

#

# <a name="GettingStarted"></a>Getting Started

The SLA-Kit is driven by JSON definitions. That goes for every component, screen, color or preference you would like to define. You can split or group these JSON files or nodes in any way you choose to - as long as you tell the SLA-Kit where to find them. We recomend following a structure that is mostly followed by designers and developers for ease of use and keeping things simple.

**Recomended structure:**

* **Brand / Color Palette**
  * primary
  * secondary
  * success
  * fail 
* **Common Components / Symbols**
  * Buttons
  * Text Fields
  * Cards
  * etc
* **Screens**
  * Sign Up
    * UsernameTextField
    * PasswordTextField
    * SignUpButton
  * News Feed
    * Table Header
    * Table View
    * Table Cell

Here is a screenshot of that structure in practice: TODO - Add screenshot


What follows is a set of examples starting from the smallest part of this solution, to the biggest.


## <a name="StartColors"></a>Colors

Lets start with the easiet part - defining your color pallete. Here is an example of a color palette in practice.
```json
  {
         "colors": {
             "primary": "4F2B81",
             "secondary": "7F7F7F",
             "success": "759A3D",
             "danger": "C22327",
             "warning": "FEC61D",
             "info": "3EBFED",
             "light": "E5E5E5",
             "dark": "4A4A4A",
             "white": "FFFFFF",
             "black": "000000",
             "appBackground":"F9F9F9",
             "special1":"000000",
             "special2":"015B78",
             "special3":"80ADBC",
             "custom": {
                 "loginPlaceholderTextColor": "DCD2CE",
                 "gold": "F9A825",
                 "tabBarTint": "4F2B81",
                 "tabBarBackground": "F9F9F9",
                 "tabBarUnselected": "4F2B81"
             }
         }
     }
``` 

## <a name="StartDesignProperties"></a>Design Properties

Style properties are defined in Style Kits for every part of your UI. Generally speaking for:

* Components
* Nested Components, and
* Screens

Starting at the **smallest components**, you can define a style kit for a:
* Button
* Label
* Text Field
* etc

An example would be if you need to define a style kit for all your primary action buttons and text fields across your app for consistency.

Because a button or a label generally don't contain any sub views or elements, style kits for these only need to define its **style**. It does not need to define any layout information for itself,  unless you choose it to be so where you want to enforce layout details across your app. But generally speaking, layout information will most of the time be defined where the button or label will be used.

**Example of a style kit for a Button:**

```json
 {
    "views": [
      {
        "name": "global",
        "components": [
          {
            "name": "primaryActionButton",
            "style": {
              "fontTextStyle": "body",
              "fontWeight": "medium",    
              "text":"Some Text",
              "textAlign": "center",
              "shadowColorName": "dark",
              "shadowRadius": "4.0",
              "shadowOpacity": "0.55",
              "shadowOffsetY": "3.0",
              "cornerRadius": "4.0",
              "borderWidth": "0.5",
              "backgroundColorName": "primary",
              "borderColorName": "primary",
              "textColorName": "white"
            }
          }
        ]
      }
    ]
  }
```

All of its style properties are enclosed in a node called **style**.

It also has a unique **name** in order to identify it amongst all the other global components.

**Nested Components :**
* Cells
* Headers
* Footers
* etc

Components can contain any number of nested elements such as buttons , labels or text fields - or any other UI element. Think of cells for a table or a header or any other view that makes one part of a bigger screen.

Because of the nested components, **layout** information is needed to know how nested componets should be positioned relative to each other.

**Example of a style kit for a component with nested components:**
```json
{
    "views": [
      {
        "name": "tableCell",
        "components": [
          {
            "name": "view",
            "style": {
              "backgroundColorName": "appBackground"
            }
          },
          {
            "name": "card",
            "layout": {
              "paddingLeft": "18",
              "paddingTop": "0",
              "paddingRight": "18",
              "paddingBottom": "3"
            }
          },
          {
            "name": "title",
            "style": {
              "fontTextStyle": "callout",
              "textColorName": "primary",
              "fontWeight": "medium"
            },
            "layout": {
              "paddingLeft": "0",
              "height": "22"
            }
          }
        ]
      }
}
```
In this example we've added a **layout** node for every component. Note that components does not know of each other, and the layout information as shown has nothing to do with each other. The layout information will be used once you decide your layout anchors in code.

**Screens**

Screens are basically exactly the same as **nested components.** The only difference really is how they are used in practice.

**Example of a style kit for a Screen:**

```json
 {
    "views": [
      {
        "name": "transactions",
        "components": [
          {
            "name": "view",
            "style": {
              "text": "Transactions",
              "textColorName": "primary",
              "backgroundColorName": "primary"
            }
          },
          {
            "name": "navigationBar",
            "style": {
              "text": "",
              "backgroundColorName":"primary",
              "tintColorName": "gold",
              "textColorName": "gold"
            }
          },
          {
            "name": "tableHeader",
            "style": {
              "backgroundColorName": "danger"
            },
            "layout": {
              "height": "177"
            }
          },
          {
            "name": "tableFooter",
            "layout": {
              "height": "0"
            }
          },
          {
            "name": "tableCell",
            "layout": {
              "height": "95"
            }
          },
          {
            "name": "transactionsHeader",
            "layout": {
              "paddingLeft": "0",
              "paddingTop": "0",
              "paddingRight": "0",
              "paddingBottom": "0"
            }
          }
        ]
      }
    ]
  }
```

Notice how in the style kit for a **screen** , we start seeing less style related definitions, and more layout definitions. This is because everything related to styling for those components can be defined in reusable style kits for those components elsewhere.

**By now it should be obvious that the structure of a style kit is the same for any UI element, regardless of what it is for. There is a view, with an array of components, each component has a name, style and layout definition**

A list of **all style properties** can be viewed here:  TODO: Add link to example of all properties.

## <a name="StartSymbols"></a>Symbols ( Common Components )

### **Button**
In this example, we've defined how all primary action buttons in your application should be styled.

Noticed that for color related properties we are using a name, and not RGB or hex values. This is to ensure an app does not have 50 shades of gray defined somewhere in the compiled code. Every component and instance property should use the color names defined in the above color palette.

```json
 {
    "views": [
      {
        "name": "global",
        "components": [
          {
            "name": "primaryActionButton",
            "style": {
              "fontTextStyle": "body",
              "fontWeight": "medium",    
              "text":"Some Text",
              "textAlign": "center",
              "shadowColorName": "dark",
              "shadowRadius": "4.0",
              "shadowOpacity": "0.55",
              "shadowOffsetY": "3.0",
              "cornerRadius": "4.0",
              "borderWidth": "0.5",
              "backgroundColorName": "primary",
              "borderColorName": "primary",
              "textColorName": "white"
            }
          }
        ]
      }
    ]
  }
```
### **Text Field**

The structure for defining a style kit for a text field is exactly the same as for a button.

```json
{
    "views": [
      {
        "name": "global",
        "components": [
          {
            "name": "loginTextField",
            "style": {
              "fontTextStyle": "body",
              "fontWeight": "regular",    
              "textColorName": "white",
              "textAlign": "left",
              "shadowRadius": "4.0",
              "shadowOpacity": "0.15",
              "shadowOffsetY": "3.0",
              "cornerRadius": "4.0",
              "borderWidth": "1.0",
              "borderColorName": "black",
              "backgroundColorName": "black",
              "leftPaddingForText": "15",
              "rightPaddingForText": "15",
              "placeholderText": "Username",
              "placeholderTextColorName": "loginPlaceholderTextColor",
              "tintColorName": "white",
              "opacity":"0.25"
            }
          }
        ]
      }
    ]
  }
```


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
