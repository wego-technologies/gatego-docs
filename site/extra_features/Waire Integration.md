---
label: Waire Program Integration
order: 1
icon: number
---

# WAIRE Program Integration

## Warehouse Actions and Investments to Reduce Emissions Program

### What is WAIRE?
The Warehouse Actions and Investments to Reduce Emissions (WAIRE)
Program aims to reduce nitrogen oxide and diesel emissions associated
with warehouses, help meet federal standards and improve public health,
especially in communities located near warehouses in the South Coast AQMD.

### Who Must Comply?
Owners and operators of warehouses that have 100,000 square feet or more
of indoor floor space in a single building.

[!ref target="blank" text="Waire Program Official Site"](http://www.aqmd.gov/home/rules-compliance/compliance/waire-program)


## Gatego Integration

When enabled in settings, Gatego keeps track of WAIRE compliance in real time, including Waire Points Compliance Obligation and Waire points earned.

The information accessible in a panel on the summary dashboard:

![Gatego Waire Panel](/static/site/extra_features/waire/waire_panel.png)


### How does it work

When enabled, the Waire calculations are available in real time after each _check out_.

When a truck is checked in, its type and fuel type are entered in the Gatego movement form if the truck was not registered before.
When a truck is checked out its type and fuel type are automatically filled in the Gatego movement form.

!!!light Waire visits VS trips
A truck entering a site is one trip, and a truck leaving the site is a second trip. 1 Visit equals 2 Trips.
Waire points are based on _visits_. In Gatego, a visit is equivalent to a **check out**, when a truck entered the site (checked in)
and then left the site (checked out).
!!!

Both values truck type, and fuel type are used to calculate the Waire compliance.

More specifically:

- The **fuel type** is used to determine the level of emissions of the truck. 
- The **truck type** is used to determine Waire truck category. 

||| Fuel Type Emissions Mapping

Fuel Type   | Emissions Category
---    | ---
Electric | Zero emissions truck
CNG | Near-zero emissions truck
Hydrogen | Near-zero emissions truck
Diesel | Non-low emissions truck


||| Truck Type Category Mapping

Truck Type   | Truck class / Truck class range
---    | ---
Pick Up Truck | Class 2b-3
Box Truck | Class 4-7
Semi Truck | Class 8
Semi Truck + Trailer | Class 8

!!!light Guest visits to the yard
Please note that guest visits to the yard are deliberately ignored in the calculation of Waire points. 
!!!
|||

When the emissions category and truck class range is determined, Gatego performs the necessary calculations to work out the WAIRE compliance according to the official WAIRE Calculator formulas, so the result can be consulted in real time the Gatego summary dashboard.

Basically WAIRE points are earned with _zero_ or _near-zero_ emission trucks visits, and obligation points are generated with any other truck visit. Then the bigger the Gross Vehicle
Weight Rating (GVWR) of the truck is, the more points are earned or penalized. 

Please note, that the WAIRE points are always calculated using the movements since January 1st of the current year till the current date. They are not _annualized_ (the information is not extrapolated to the rest of the year) , in the future Gatego might show both the points up to date and also the equivalent annualized points as if the year had ended.

### Settings

There are two setting properties controlling the Gatego Waire feature:

- `waire.enabled`
- `waire.stringency`

Both can be set for a particular yard, or as a default, for the whole organization.
So one organization can enable Waire calculations for only some yards, then set a default `stringency` value for all yards, while overriding the `stringency` for some specific yards.

If Waire is enabled but no `stringency` is set, then the recommended default of `0.0025` will be used.

In the future, yard size and desired compliance year will be accepted as an alternative to `stringency` property.


!!!success That's it!
Basically just set your stringency (or use the Waire default) and no more manual actions will be required. Just use Gatego normally and see the Waire panel updating.
!!!

### Disclaimer

Please note, that the Waire panel is an estimation of the compliance of your organizaiton based only on the information that Gatego has access to and the official Waire calculator.
In the future, Gatego might be able to collect other information to improve the accuracy of the Waire panel, such as low emission trucks acquisitions, or the use incentive funding programs that prohibit using the funds to comply with a regulation.

