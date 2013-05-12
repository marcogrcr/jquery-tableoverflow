jquery-tableoverflow
====================

*jquery-tableoverflow* is a jQuery plugin for dynamic table content overflowing. For more information about the problem it solves, see http://stackoverflow.com/questions/5239758/css-truncate-table-cells-but-fit-as-much-as-possible

**HOW TO USE**

To set a table for dynamic table content overflowing simply use:

    $('selector').tableoverflow();

To remove a table from dynamic table content overflowing simply use:

    $.tableoverflow.removeTable($('selector'));

**RESTRICTIONS**

* The **table** must have a **thead** section and a **th** for each column.

**HOW IT WORKS**

* For each column, the plugin sets a min width (the width of the **th** content) and a max width (the width of the largest **td** content).
* After every resize of the browser window, the plugin resizes the columns of the table so that the cells overflow evently, and only when they've all given up all their whitespace.
* If a cell text is truncated after the column resize, a tooltip is placed so that the text can be read if the mouse is hovered.

**TESTED ON**

* Google Chrome (26).
* Firefox (20).
* IE 8+.

**EXAMPLE**

Please view the example.html file.