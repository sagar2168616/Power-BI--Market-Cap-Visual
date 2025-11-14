🚀 Market Cap Comparison Visualization — From Raw Data to Insightful Storytelling

This project started with a simple question:

“How big is NVIDIA compared to the rest of the world’s largest companies?”

What followed was an end-to-end data analytics journey — covering data sourcing, cleaning, modeling, and visualization using Excel, Power Query, DAX, and Power BI.

Below is a breakdown of the full workflow.

🔍 1. Data Sourcing

Market capitalization data was extracted from reliable public sources: CompaniesMarketCap

The raw data included mixed units like billions (B) and trillions (T), as well as symbols like $.

🧹 2. Data Cleaning Using Power Query (M Language)

The Market Cap column contained inconsistent formats:

$4.718 T
$912.39 B
$1.085 T

Power BI cannot evaluate these directly, so Power Query was used to:

Remove $

Strip trailing T / B

Extract the unit separately

Convert billions → trillions

Generate a clean numeric column ready for visuals

Power Query techniques used:

Replace Values

Custom Columns

Text.End()

Text.Replace()

Number.From()

📊 3. Data Modeling with DAX

A custom DAX column was created to group companies meaningfully:

Custom Grouping:

NVIDIA alone

Alphabet + Meta

Apple

Microsoft

Semiconductors (TSMC, Broadcom, AMD)

E-Commerce (Amazon, Walmart)

Finance (JPMorgan, Berkshire, Visa, Mastercard)

Healthcare (Eli Lilly)

Energy (Saudi Aramco, Exxon)

Asian Tech (Tencent)

DAX techniques used:

SWITCH()

IN { }

Logical grouping

Category ordering via prefix numbers ("1. NVIDIA", "2. Alphabet + Meta")

This ensured the bar chart was sorted in descending order and easy to read.

🧮 4. Supporting Excel Work

Before loading the dataset into Power BI, Excel was used to prototype transformations:

Extraction formulas

RIGHT() and SUBSTITUTE()

Unit detection tests

Validation of numeric conversions

This provided a quick validation layer before applying transformations in Power Query / DAX.

📈 5. Final Visualization in Power BI

A Stacked Bar Chart was used to compare NVIDIA with grouped industry categories.

Features applied:

Sorted bars (highest → lowest)

Category labels with included company names

Word wrap for long labels

Clean legend by company

Market cap displayed in trillions for consistency

Insight:

NVIDIA’s market cap remains dominant even when compared to entire sectors like Big Tech, Semiconductors, and Finance.

🎯 Key Skills Demonstrated

Data Sourcing

Excel Formula Prototyping

Power Query (M Language)

DAX Modeling & Grouping

Custom Columns

Data Cleaning & Standardization

Power BI Visualization

Story-focused Data Presentation

📌 Takeaways

Clean data drives meaningful insights.

Power Query + DAX together provide tremendous transformation power.

Grouping logic transforms raw numbers into compelling stories.

Effective BI is not just charts — it’s clarity and impact.
