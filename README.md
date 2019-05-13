## list_view_item_builder

The item builder of the listView.

### Usage

```dart
  Example:
1.Create an instance of the ListViewItemBuilder
  _itemBuilder = ListViewItemBuilder(
  rowCountBuilder: (section) => 10,
  itemsBuilder: (BuildContext context, int section, int index) {
    return Container(
      height: 44,
      child: Text('item:${section.toString()}+${index.toString()}'),
    );
  },
);

2.Pass the values of itemBuilder and itemCount of _itemBuilder to the ListView
  ListView.builder(
  itemBuilder: _itemBuilder.itemBuilder,
  itemCount: _itemBuilder.itemCount,
);
```



### Other properties of the ListViewItemBuilder

```
/// How many sections are there in total. If null. Default is 1 section.
ListViewSectionCountBuilder sectionCountBuilder;

/// How many rows are in each section.
ListViewRowCountBuilder rowCountBuilder;

/// Builder of items for each section.
ListViewItemWidgetBuilder itemsBuilder;

/// Header for each section builder, null by default.
ListViewReusableWidgetBuilder headerBuilder;

/// Footer for each section builder, null by default.
ListViewReusableWidgetBuilder footerBuilder;

/// The item callback is OnTaped, which defaults to null.
/// If it is null, all items cannot be clicked, and there is no ripple effect
ListViewItemOnTapCallback itemOnTap;

/// Determines whether the item callback can be clicked on.
/// If itemOnTap == null, none of them are clickable.
/// If itemOnTap! = null, the return value of itemShouldTap determines whether an item can be clicked or not.
ListViewItemShouldTapCallback itemShouldTap;

/// The header widget for the entire listView, which defaults to null.
Widget headerWidget;

/// The footer widget for the entire listView, which defaults to null.
Widget footerWidget;

/// Gets the Context of the listView.
BuildContext get listViewContext => _listViewContext;

/// listViewContext
BuildContext _listViewContext;
```



### Screenshot

<img src="https://upload-images.jianshu.io/upload_images/3537150-cc4ba38a9a08b0af.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240" width="50%" height="50%" div align=center />