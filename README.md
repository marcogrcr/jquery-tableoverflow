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

**EXAMPLE**

    <!DOCTYPE html>
    <html>
        <head>
            <title>jquery-tableoverflow example</title>
            <script src="jquery.js"></script>
            <script src="jquery-tableoverflow.js"></script>
            <script>
                $(function () {
                    $('table').tableoverflow();
                });
            </script>
        </head>
        <body>
            <table border="1">
                <thead>
                    <tr>
                        <th>Col 1</th>
                        <th>Col 2</th>
                        <th>Col 3</th>
                        <th>Col 4</th>
                        <th>Col 5</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>Small text</td>
                        <td>This is a large sized text</td>
                        <td>Medium sized text</td>
                        <td>This is a super large sized text additional text</td>
                        <td>This is an incredibly monstruous large text that no display on the world is capable of render completely</td>
                    </tr>
                </tbody>
            </table>
        </body>
    </html>