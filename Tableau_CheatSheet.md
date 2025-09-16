Tableau:

        # Connect to a data source (Excel, CSV, SQL, etc.)
                Data → Connect to Data

        # Create a new worksheet
                Click the “New Worksheet” button (bottom tab bar)

        # Create a new dashboard
                Click the “New Dashboard” button (bottom tab bar)

Data Basics:

        # Dimensions vs Measures
                Dimensions = qualitative fields (e.g., Category, Date)
                Measures   = quantitative fields (e.g., Sales, Profit)

        # Drag a field to Columns or Rows to create a view
                Example: Drag “Category” to Columns and “Sales” to Rows

Charts:

        # Bar chart
                Show Me → Bar

        # Line chart
                Show Me → Line

        # Scatter plot
                Show Me → Scatter Plot

        # Map (requires geographic dimension)
                Show Me → Map

Filters & Parameters:

        # Add a filter
                Drag field to Filters shelf

        # Create a parameter
                Right-click in Data pane → Create Parameter

        # Use parameter in a calculated field
                [Sales] > [Threshold Parameter]

Calculated Fields:

        # Create a calculated field
                Analysis → Create Calculated Field

        # Example: Profit Ratio
                SUM([Profit]) / SUM([Sales])

        # Example: Conditional Label
                IF [Profit] > 0 THEN "Positive" ELSE "Negative" END

Dashboards:

        # Add sheets to dashboard
                Drag sheets from left pane to dashboard canvas

        # Add an action (Filter)
                Dashboard → Actions → Add Action → Filter

Export & Publish:

        # Export to PDF
                File → Export as PDF

        # Save to Tableau Public
                File → Save to Tableau Public

        # Publish to Tableau Server
                Server → Publish Workbook
