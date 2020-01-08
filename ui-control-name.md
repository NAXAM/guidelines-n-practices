# UI Control Naming Convention

## Key takeaways

All control names must be:

- Written in camel case.

E.g. ```btnSignIn```

- Comprehensive and descriptive.

E.g. ```aButton```, ```btnLeft```, ```btnSI``` are NOT preferred.

- Based on role, not appearence.

E.g. ```btnToggleAlert``` is more preferable than ```btnBell```. ```btnFavorite```, ```btnLike``` are more preferable than ```btnStar```, ```btnHeart```.

## Prefix rule

|Prefix| XF       | Android         | iOS               | Web                | Windows             |
|------|----------|-----------------|-------------------|--------------------|---------------------|
|btn   | Button, ImageButton   | Button          | UIButton          | button, `input[type=button]`, `a.btn` | Button
|clv   | CollectionView | RecyclerView | UICollectionView |                  |                     |
|lbl   | Label    | TextView        | UILabel           | Label              | Label               |
|lst   | ListView, TableView | ListView, RecyclerView | UITableView, UICollectionView | N/A           | List                |
|sld   | Slider   | SeekBar         | UISlider          |                    |                     |
|sw  | Switch   | Switch           | UISwitch          |                    |                     |
|txt   | Entry, Editor    | EditText        | UITextField, UITextEditor       | input              | TextBox             |

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
