##### class_80

Topic Logout and Side Drawer

Goal 

● Inspect other apps to identify side drawer UI

 ● Build side drawer menu for Book Santa App 

● Allow user to logout of the app

We Created two screens BookRequest and BookDonate screen. We created a form in the BookRequest screen . The form had Two TextInputs and A Request button where user entered the name of book and the reason user wanted to request that book. In BookDonate Screen we have used Flatlist to show all the book requests and user can also donate the book by clicking on the donate button.

the side drawer which these apps have which have a menu and which allow users to logout.

In the CustomSideBarMenu we'll be using drawerItems to add screens to the drawer.

We will install the react-navigation-drawer library using commands yarn add react-navigation-drawer or npm install react-navigation-drawer.

We have to  import drawerItems in our CustomSideBarMenu component . Now we have to pass the screens to the drawerItems .

Now we have the screens in our sideBarMenu. But we still can't access them. Because we haven't added it to any navigator.

What all steps do we follow to create an AppDrawNavigator container?

We import the createDrawerNavigator from react-navigation-drawer. Then in variable AppDrawNavigator we use createDrawerNavigator and pass our screens to it.

so let's create the AppDrawerNavigator screen in our components folder and import it in App.js file.

While passing our screens we still want our BookRequestScreen and BookDonateScreen to be in tabs. So what will we do?

We can pass AppTabNavigator as a screen in AppDrawNavigator. How do we do that?

We can pass the AppTabNavigator that we created as a screen in App DrawNavigator.

We also have to import and add our SideBarMenu component to the AppDrawNavigator.

We will import CustomSideBarMenu from '../components/CustomSide BarMenu.js We can pass it as a screen as we did before in other Navigators that we created

But we'll be using contentComponent to pass the CustomSideBarMenu component. we use contentComponent to render all the components from CustomSideBarMenu. And our initial route will be Home which has tabNavigation



Now as we passed the AppTabNavigator inside AppDrawNavigator , we are going to pass the AppDrawNaviagtor to our main SwitchNavigator in the App.js .