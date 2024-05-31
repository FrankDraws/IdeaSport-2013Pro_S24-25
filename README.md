# IdeaSport Boys 2013 Pro - Roster for 2024-2025

Welcome to the IdeaSport 2013 Pro boys team roster. This is a way for us to get to know our kids' names, numbers, and parent names.

You can view the live site here: https://frankdraws.github.io/IdeaSport-2013Pro_S24-25/

# Code
This is a typical data table (cloned from FC2013 roster). I used JavaScript to add sequential numbering in the first cell of each row in order to get the count of total players.

The benefit of the sequential numbering code is that if a player is deleted or added, you don't have to manually update the numbers. If one player is added or removed, especially at the top of the table, you'd have to manually update the entire sequence. With the sequential numbering code, you can make any changes as needed and JavaScript will take care of the numbering.

The following code was written by ChatGPT:
```javascript
    // Wait for the DOM content to be loaded
    document.addEventListener('DOMContentLoaded', function () {
      // Get the first table on the page
      var table = document.querySelector('tbody');

      // Get all the table rows within the first table
      var rows = table.querySelectorAll('tr');

      // Loop through each row and set the sequential number
      for (var i = 0; i < rows.length; i++) {
        // Get the first cell in the current row
        var cell = rows[i].querySelector('td:first-child');

        // Create a span element for the number
        var numberSpan = document.createElement('span');

        // Set the sequential number as the span's text
        numberSpan.textContent = i + 1;

        // Append the span element to the cell
        cell.appendChild(numberSpan);
      }
    });
```

This was the code I initially used and it worked. Then I received an email from Hashnode about their new chatbot [Rix.chat](https://hashnode.com/rix), so I tried it out. Here's the result (and the code I'm using for this table):

```javascript
    const table = document.getElementById("main");
    const rows = table.rows;

    for (let i = 0; i < rows.length; i++) {
      rows[i].cells[0].textContent = i + 1;
    }
```

In this version, I decided to go with an `ID` to target the table.

Although the Rix.chat version is shorter, I do like that ChatGPT uses comments to explain each line. It really helps me better understand. I decided to ask Rix.chat to comment the code it wrote, and it did. It output a concise and clean answer.

Here's the commented version from Rix.chat:

```javascript
  // Get the table element
  const table = document.getElementById("myTable");

  // Get all the rows in the table
  const rows = table.rows;

  // Loop through each row
  for (let i = 0; i < rows.length; i++) {

    // Get the first cell (column 0) of the current row
    const firstCell = rows[i].cells[0];

    // Set the text content of the first cell to the row number
    firstCell.textContent = i + 1;

  }
```
