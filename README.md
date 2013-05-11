jquery-tableoverflow
====================

jquery-tableoverflow is a jQuery plugin for dynamic table content overflowing.

Example:

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