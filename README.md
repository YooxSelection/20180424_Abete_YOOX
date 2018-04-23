# 20180424_Abete_YOOX

My project consists of two views: a first view, that displays a TableView, and a second view, which the user can access simply tapping any of the elements of the TableView.

The tableView (see TableViewController.swift) is filled with items, whose informations come from the decode of a JSON file. In particular, brand name, category name, price ( discounted or full) and a little image are shown.
At the beginning, only 40 elements are displayed, but scrolling down the view will allow the user to visualize 80 more elements, all coming from the decode of two more JSON's . The JSON's decoding system is implemented inside the Item.swift file.

In this first view, a searchBar is also implemented, to let the user search the elements by two main filters: brand and category. If the query matches a result, items are shown (with correct price and image, too). If the query doesn't match a result, a "no items found" label will be displayed.
The tableView is embedded inside an empty ViewController (see FirstPageController.swift ).

In the second view, the user will get some information about a specific item. The informations come from the decode of another JSON (see Json.swift) and are organized in a stack view inside a scrollView (see SecondPageController.swift).

A Navigation Controller is also implemented to link the two views.
