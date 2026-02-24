# Local Water Treatment & Locating AI
A local AI chatbot dedicated to providing information on water locating, purification, and testing. Designed for offline use in emergency and disaster response scenarios.

# Features
Water Locating: Identifies established water sources using geographical datasets.

Water Purification: Provides DIY, emergency, and advanced water treatment methods.

Water Testing: Details protocols for testing and identifying contaminants.

Source-Backed Recommendations (RAG): Utilizes a retrieval-augmented generation architecture to pull directly from embedded file sources, ensuring all advice is backed by verified data.

Transparent Citations: Directly displays the specific source documents and text excerpts used to generate each response for user verification.

Local Execution: Runs entirely offline to ensure availability during outages.

# Training Data & Databases
This project utilizes the following datasets for training and retrieval:

Humanitarian Data Exchange (HDX) WASH Datasets: Contains GPS coordinates and status of rural water points. https://data.humdata.org/dataset?vocab_Topics=water+sanitation+and+hygiene-wash

WHO/UNICEF Joint Monitoring Programme (JMP) Global WASH Data Portal: Global water and sanitation data.

CAWST WASH Education and Training Resources: Guides for household water treatment and emergency batch chlorination. https://washresources.cawst.org/en

Appropedia (Water Purification Wiki): Open-source wiki for DIY and low-cost water filtration methods. https://www.appropedia.org/Point-of-use_water_treatment

EPA Drinking Water Treatability Database (TDB): Technical database detailing over 35 treatment processes for regulated and unregulated contaminants. https://www.epa.gov/water-research/drinking-water-treatability-database-tdb


# tools 
Crawl tool: fire crawl

Database:supabase
