# Delivery-Performance
This project presents an interactive Power BI dashboard created from a dataset of 11k shipment records. The data includes customer details, shipment modes, delivery performance, customer service interaction, and product information.

Import Datasets from files into Power Query Editor.

Data cleaning.

Dax expressions.

creating measure table avg customer rating,  Avg customer Rating = 
AVERAGE(
Shipments[Customer_rating]
).

creating delayed shipments , DelayedShipments = 
CALCULATE(
    COUNTROWS(Shipments),
    Shipments[Reached.on.Time_Y.N] = 1
).

creating total shipments, Total Shipments = COUNT(Shipments[ID]).

