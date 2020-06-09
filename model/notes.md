# Model

## User input
`Trajectory` values for supply and demand, ranging 1 to 4. Each value represents specific attitude or status.

For example:
- Nuclear power stations
    - 1: No new nuclear
    - 2: 13 3GW power stations
    - 3: 30 3GW power stations
    - 4: 50 3GW power stations

- Average temperature of homes
    - 1: 20'C (high)
    - 2: 18'C
    - 3: 17'C
    - 4: 16'C (low)


The `goals` are treated linearly, from present time to 2050. For example, for the nuclear
reactor example, if the trajectory is 2, 13 reactors are deployed linearly from 2020 to 2050
(approx. 2.3 reactors per year)



## Assumptions


### [Cost Assumptions](http://2050-calculator-tool-wiki.decc.gov.uk/pages/28)

Mostly from MARKAL

Energy supply:
    - power stations
    - energy sources (fossil fuels, uranium, biomass)
    - transmission networks
Energy demand:
    - energy users (heating systems, cars, industrial plants)
    - demand reducing agents (e.g. insulation)


#### Technology cost predictions
For every technology (e.g. off-shore wind), there is a projected
cost curve.

Finance costs are at 7% default ([details](http://2050-calculator-tool-wiki.decc.gov.uk/pages/106)).

fossil fuel prices set at $130/barrel (large overestimation, I think)

#### Discount rate

Set as default 3.5%.

Standard green book discount rate ([details and argument](http://2050-calculator-tool-wiki.decc.gov.uk/pages/107))
    - 0-30 years: 3.5%
    - 31-75: 3.0%
    - 76-125: 2.5%
    - 126-200:2.0%
    - 201-300: 1.5%
    - 301+: 1.0%


#### Incremental Costs

Compares best, worst ([details](http://2050-calculator-tool-wiki.decc.gov.uk/pages/108))



## Technologies

There are 130 technologies, and they have:
    - capital cost
    - operating cost
    - fuel cost


## Data / Assumptions
The purple colored sheets have the assumptions / data that pertain to the rates / coefficients
- Conversions
    - Unit conversions
    - Currency conversions
    - Deflation of GDP
- Global assumptions
    - Population projection
    - GDP projection
    - Discounting
    - Financing costs
- Constants
    - Calorific values from fuels (TWh/kg or TWh/m3 or TWh/l)
    - Combustion emissions factor
    - Global Warming potential


## Hard-coded variables
The red sheets (`I.a` to `XVIII.a`) have data for each section:
    I. Hydrocarbon fuel power generation
        a. Biomass/Coal power stations
        b. CCS power
    II. Nuclear power generation
        a. Nuclear power
    III. National renewable power generation
        a. Wind
            1. Onshore wind
            2. Offshore wind
        b. Hydroelectric power stations
        c. Tidal & wave
            - Wave
            - TidalStream
            - TidalRange
        d. Geothermal electricity
        e. Tidal (unused)
    IV. Distributed renewable power generation
        a. Solar PV
        b. Solar thermal
        c. Small-scale wind
    V. Bioenergy
        a. Types of fuel from biomass
        b. Bioenergy imports
    VI. Argriculture and waste
        a. Agriculture and land use
        b. Volume of waste and recycling
        c. Marine algae
    VII. Electricity distribution, storage and balancing
        a. Electricity imports
        b. Electricity grid distribution
        c. Storage, demand shifting, interconnection
    VIII. H2 production
        a. H2 production for transport
    IX. Heating
        a. Domestic space heating and hot water
            - CHP
            - Insulation
        b. Domestic hot water (unused)
        c. Commercial heating and cooling
            - CHP
        d. Commercial hot water (unused)
    X. Lighting & Appliances
        a. Domestic lighting, appliances, appliances, and catering
        b. Commercial lighting, appliances, and catering
    XI. Industry
        a. Industrial processes
    XII. Transport
        a. Domestic passenger transport
        b. Domestic freight
        c. International aviation
        d. Domestic aviation (unused)
        e. International shipping
        f. National navigation (unused)
    XIII. Food consumption (unused)
        a. food consumption (unused)
    XIV. Geosequestration
        a. geosequestration
    XV. Fossil fuel production
        a. Petroleum refineries
        b. Indigenous fossil-fuel production
    XVI. Transfers
        a. Fossil fuel transfers
        b. Balancing imports
    XVII. District heating
        a. District heating effective demand
    XVIII. Storage of captured CO2
        a. Storage of captured CO2


For each section, there are values such as:
- Trajectory choices and trajectory values
- Fixed assumptions
    - cost assumptions
    - efficiency
    - load factors
    - emission factors
    - etc.



### Transport Sector

Four transport sectors:
    - Domestic passenger transport (also domestic aviation): XII.a
    - Domestic freight (domestic shipping): XII.b
    - International aviation: XII.c
    - International shipping: XII.e

#### Domestic Passenger Transport Sector (XII.a)

- Domestic transport behaviour: distance traveled per person (km), and mode used
- Shift to zero emissions transport: like electric cars
- Choice of car and van technology: electric cars / hydrogen vehicle

