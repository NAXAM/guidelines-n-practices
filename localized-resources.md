# Localized Resources Naming Convention

Each localized resource will be composed of a KEY and a VALUE.

This is the way we define our KEY to make it consistent regardless of platform/technology

```{pageName}_{controlName}_{controlProperty}```

- **pageName**: is the name of the page/screen, it should be in camel case
- **controlName**: is the name of UI control, it should be in camel case
- **controlProperty**: is the name of UI control propety, it shuold be in Pascal case

E.g. 

1. `loginPage_btnLogin_Text`
2. `loginPage_txtUsername_Placeholder`
3. `loginPage_txtPassword_Placeholder`


NOTE: To read more about how to define a control name, plz read [here](./ui-control-name.md).