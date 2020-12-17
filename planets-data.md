Marking guide for "Structuring planet data"

The following guide outlines a marking guide for the MDN Learning Area HTML Topic — Structuring planet data. Each subtask detailed in the assessment is listed below, along with an explanation of how many marks the task is worth.

Note: These are guidelines, not set in stone rules — you are of course free to use your judgement on mark awarding when you meet an edge case, or something that isn't clearly cut.

The overall mark awarded is out of 34. Work out their final mark, and then divide by 34 and multiply by 100 to give a percentage mark. For reference, you can find a finished marked up page that would be awarded top marks.
Block/structural semantics

Giving the table a basic high level structure — an outer container, a table header, and a table body (3 marks.)
    This is pretty simple. The student just needs to include a <table> element in the page, with a <thead> and <tbody> as children.
Add the provided caption to your table. (2 marks)
    Again, simple, but it needs it be put in the right place — the provided caption needs to be put in a <caption> element, right below the opening <table> tag.
Add a row to the table header containing all the column headers (5 marks).
    The student needs to:

        Put the cells of the row inside a <tr> element and use <th> elements for the cells because they are headers (2 marks).
        Put the column header text in each cell correctly, copied from the raw data (1 mark).
        Leave a two-column gap at the start of the row — this is best done with a single cell with colspan="2" set on it, but we would accept two cells (2 marks).

Note: Giving the planet names column a header of "Name" is recommended, but they won't lose a mark if they forget this.
Create all the content rows inside the table body, remembering to make all the row headings into headings semantically (15 marks).
    This is the most difficult part of the table — it requires getting all the group row headings in the right rows, and making them span the right number of rows and columns.

        First of all, each row needs to be put inside the <tbody> (1 mark).
        Each row needs to contain a <th> element containing the planet name at the start followed by nine <td> elements containing the planet's data (5 marks). Give full marks if this is mostly right with a couple of typos, but start to reduce the mark at your discretion if significant data points are wrong, wrongly placed, or omitted. Take two marks off if the planet names are not put in headers.
        The first body row needs to contain an extra <th> element at the start of it, containing "Terrestial planets", with rowspan="4" and colspan="2" (2 marks).
        The fifth body row needs to contain two extra <th> elements at the start, containing "Jovian planets" and "Gas giants" respectively. The former needs rowspan="4", and the latter needs rowspan="2" (3 marks).
        The seventh body row needs to contain an extra <th> element at the start, containing "Ice giants", with rowspan="2" (2 marks).
        The ninth body row needs to contain an extra <th> element at the start, containing "Dwarf planets", with colspan="2" (2 marks).

Add attributes to make the row and column headers unambiguously associated with the rows, columns, or rowgroups that they act as headings for (5 marks).
    The student needs to add the scope value to all the <th> elements, giving them appropriate values as shown below:

        col: All the <th> elements in the table header row.
        row: All the <th> elements containing planet names, and the one containing "Dwarf planets" (it is also a heading over only one row).
        rowgroup: The <th> elements containing "Terrestial planets", "Jovian planets", "Gas giants", and "Ice giants".

Add a black border just around the column that contains all the planet name row headers (4 marks).
    The easiest way to do this is to:

        Add a <colgroup> element just below the <caption> element.
        Inside this, nest two <col> elements, one with a span="2" attribute, and the other with a style attribute along the lines of style="border: 2px solid black".
        Notes: It would be acceptable to define all the columns in the table inside the colgroup, although you don't need to. Adding the style to each cell in the column individual would not be acceptable — this would put the styling around every cell in the column, not the column.

