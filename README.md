# Aimport pandas as pd

# Sample data
data = {
    'Item': ['Apples', 'Bananas', 'Oranges'],
    'Quantity': [50, 75, 40],
    'Price per Unit': [0.5, 0.3, 0.4]
}

df = pd.DataFrame(data)

# Generate report as a string
report = f"""
Automated Inventory Report
==========================

Items Summary:
---------------
{df.to_string(index=False)}

Total Quantity: {df['Quantity'].sum()}
Total Value: ${ (df['Quantity'] * df['Price per Unit']).sum():.2f}

Note: This report is generated automatically.
"""

print(report)UTOMATED-REPORT-GENERATION
