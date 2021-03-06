# Listing Pages

Serene has listing pages and editing interface for Northwind database. Let's have a look at the Products page under Northwind module.

![Products Page Initial](img/products_page_initial.png)

Here we see list of products sorted by product name (initial sort order).

> Grid component is SlickGrid with a customized theme.

> https://github.com/mleibman/SlickGrid

You can change order by clicking column headers. To sort descending, click the same column header again.

To sort by multiple columns, you can use Shift+Click.

Here is what it looks like after sorting by Category then Supplier columns:

![Products Category Supplier Sort](img/products_category_supplier.png)

When you changed sort order, grid loaded data from a service with an AJAX request. 

> When you open the page first time, initial records were also loaded by an AJAX call.

By default grid loads records by 100 page size. Only records in current page are loaded from server. In the sample image, i changed page size to 20 (bottom left of grid) to show paging in effect.

On top left of the grid, you can type something to do a simple search.

Type *coffee* for example to see products containing it in their names.

![Products Coffee Search](img/products_coffee_search.png)

It searched in product name field. It is also possible to use another, or multiple fields for quick search. We'll see how in later chapters.

On top right of the grid, there are quick filtering dropdowns for *Supplier* and *Category* fields.

> Dropdown component used is Select2

> https://github.com/select2/select2

Choose *Seafood* as *Category* and it will show only products in that category.

![Products Seafood](img/products_seafood.png)

> All sorting, paging and filtering is done on server side with dynamic SQL queries generated by Serenity service handlers.

It is also possible to filter by any column by clicking *edit filter* link at bottom right of the grid.

![Products Edit Filter](img/products_edit_filter.png)

Here you can add criteria by any column by clicking *add criteria* and choosing column name, choosing comparison operator from next dropdown, and setting a value. 

Some value editors are simple textboxes while some others may have dropdowns and other custom editors depending on column type.

It is also possible to change *and* to *or* by clicking on it.

You can also group criteria by clicking parenthesis. Groups will have a bit more space between them than ordinary lines.





