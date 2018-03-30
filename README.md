# Tableau-circular-network-layout

When recreating start by loading the links.csv and then pivoting the 'Source' and 'Target' fields. In the sample workbook the resulting 'Pivot Field Names' and 'Pivot Field Values' fields were renamed to 'source/target' and 'node id' respectively. After this you can join the nodes.csv data based on the newly created 'node id' field.

The layout works by first positioning the nodes based on their indices (trigonometry ftw) and then the links between them. In the x measure that creates the links by line charts, the 'Link ID' field must be on either the Color or the Label shelves, but not Detail.

The network can be filtered based on both node and link attributes.

If orphan nodes are needed in the network those need to be created via self-loops in the links data.
