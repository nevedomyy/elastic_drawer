# Elastic Drawer

Elastic panel that slides in horizontally to show fully customize content (navigation links, menu items, notes etc.)

![img](demo1.gif)  ![img](demo2.gif)

## How to use

```
@override
  Widget build(BuildContext context) {
    return ElasticDrawer(
      mainColor: Colors.white,
      drawerColor: Color(0xff3C3F41),
      mainChild: Column(
        children: [
          Text('MAIN content'),
          ...
        ]
      ),
      drawerChild: Column(
        children: [
          Text('DRAWER content'),
          ...
        ]
      ),
    );
  }
```

If you want to navigate inside use **ElasticDrawerKey.navigator**
```
InkWell(
  onTap: (){
    ElasticDrawerKey.navigator.currentState.push(
      MaterialPageRoute(
        builder: (context) => YourNextPage()
      )
    );
    ...
  },
)
```

If you want to close drawer programmatically use **ElasticDrawerKey.drawer**
```
InkWell(
  onTap: (){
    ElasticDrawerKey.drawer.currentState.closeElasticDrawer(context);
    ...
  },
)
```