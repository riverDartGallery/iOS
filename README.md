# Material Kit PRO - React Native

Plugins:
- expo: 31.0.2
- galio-framework: ^0.4.2
- react: 16.5.0
- react-native: expo sdk-31
- react-native-modal-dropdown: 0.6.2
- react-navigation: 2.18.2

Examples / Screens:
- Onboarding

- Home
  - Kids
  - Man
  - Woman
  - NewCollection
- Deals
- Search
- Chat
- Profile

- Categories
- Category
- Product
- Gallery

- Cart
- SignIn
- SignUp

- Components

- Settings
  - About
  - Agreement
  - Privacy
  - Notifications

Components:
- Button.js - custom component build with galio-framework & gradient option for LinearGradient
- Drawer.js - drawerLabel as custom label used in navigation/Screens.js
- Menu.js - DrawerNavigatorConfig for createDrawerNavigator in navigation/Screens.js
- Header.js - header property for navigationOptions for each navigation screen
- Icon.js - extended Icon component with new set of icons 
- Product.js - custom component build with galio-framework
- Select.js - custom component build with galio-framework & react-native-modal-dropdown
- Switch.js - extended Switch component with custom style
- Tabs.js - horizontal FlatList built with Animated Text & galio-framework

How to use custom components:
```js
const AppStack = createDrawerNavigator(
    Home: {
      screen: HomeStack,
      navigationOptions: (navOpt) => ({
        drawerLabel: ({focused}) => (
          <Drawer focused={focused} screen="Home" title="Home" />
        ),
      }),
    },
    Menu
)

const HomeStack = createStackNavigator({
  Home: {
    screen: HomeScreen,
    navigationOptions: ({navigation}) => ({
      header: <Header search options title="Home" navigation={navigation} />,
    })
  },
})
```
### Header
```js
// simple header
<Header title="Home" navigation={navigation} />

// with back button
<Header back title="Home" navigation={navigation} />

// with search input
<Header search title="Home" navigation={navigation} />

// with option buttons
<Header options title="Home" navigation={navigation} />

// with tabs buttons
const tabs = [
 { id: 'popular', title: 'POPULAR', },
 { id: 'beauty', title: 'BEAUTY', },
 { id: 'cars', title: 'CARS', },
 { id: 'motocycles', title: 'MOTOCYCLES', },
];
<Header tabs={tabs} title="Home" navigation={navigation} />
```

### Tabs
```js
// custom component based on Animated.View & FlatList react-native
const tabs = [
 { id: 'popular', title: 'POPULAR', },
 { id: 'beauty', title: 'BEAUTY', },
 { id: 'cars', title: 'CARS', },
 { id: 'motocycles', title: 'MOTOCYCLES', },
];
<Tabs data={tabs} initialIndex='beauty' />
```# iOS
