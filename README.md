# table_sticky_headers

This package for [Flutter](https://flutter.io) allows you to display two-dimension table with both sticky headers.

Key of this package is sticky headers. Cells aren't much customizable now. It's quite easy to see in separate class all parameters and change them. In future I plan to add customization in table constructor. Feature requests and PRs are welcome.  

Usage example:

```dart
import 'package:flutter/material.dart';

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    List<String> tops = List.generate(20, (i) => '${i + 1}');
    List<String> lefts = List.generate(20, (i) => '${i + 1}');

    return MaterialApp(
      title: 'Flutter Demo',
      home: Scaffold(
        appBar: AppBar(
          title: Text('Sticky Headers Two-Dimension  Table'),
          backgroundColor: Colors.amber,
        ),
        body: StickyHeadersTable(
          columnsLength: tops.length,
          rowsLength: lefts.length,
          columnsTitleBuilder: (i) => 'Top ${tops[i]}',
          rowsTitleBuilder: (i) => 'Left ${lefts[i]}',
          contentCellBuilder: (i, j) => 'T${tops[i]} : L${lefts[j]}',
          legendCell: 'Permanently Sticky',
        ),
      ),
    );
  }
}
```

## Support

Please file [issues and feature requests](https://github.com/AlexBacich/sticky-headers-table).

## Getting Started

This project is a starting point for a Dart
[package](https://flutter.dev/developing-packages/),
a library module containing code that can be shared easily across
multiple Flutter or Dart projects.

For help getting started with Flutter, view our 
[online documentation](https://flutter.dev/docs), which offers tutorials, 
samples, guidance on mobile development, and a full API reference.