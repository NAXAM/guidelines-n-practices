# UI Control Naming Convention

## First rule

All control name must be written in camel case

E.g. ```btnSignIn```


## Prefix rule

|Prefix| XF       | Android         | iOS               | Web                | Windows             |
|------|----------|-----------------|-------------------|--------------------|---------------------|
|btn   | Button   | Button          | UIButton          | button, `input[type=button]`, `a.btn` | Button
|lbl   | Label    | TextView        | UILabel           | Label              | Label               |
|txt   | Entry    | EditText        | UITextField, UITextEditor       | input              | TextBox             |
|lst   | ListView | ListView, RecyclerView | UITableView, UICollectionView | N/A           | List                |

Other than those short prefix, we might use
- tab: To indicate a TabPage or the like
- page: To indicate a screen or the like

And we could use our common prefix as below

|Prefix| Purpose       | 
|------|---------------|
|btn   | To use on any controls that lead user to action                | 
|lbl   | To use on any controls that show a static text to our users    | 
|txt   | To use on any controls that lead user to key in                |
|lst   | To use on any controls that show users a list of values        |