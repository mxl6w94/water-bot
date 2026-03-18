# Local Water Treatment \& Locating AI

A local AI chatbot dedicated to providing information on water locating, purification, and testing. Designed for offline use in emergency and disaster response scenarios.

# Features

Water Locating: Identifies established water sources using geographical datasets.

Water Purification: Provides DIY, emergency, and advanced water treatment methods.

Water Testing: Details protocols for testing and identifying contaminants.

Source-Backed Recommendations (RAG): Utilizes a retrieval-augmented generation architecture to pull directly from embedded file sources, ensuring all advice is backed by verified data.

Transparent Citations: Directly displays the specific source documents and text excerpts used to generate each response for user verification.

Local Execution: Runs entirely offline to ensure availability during outages.

# Training Data \& Databases

This project utilizes the following datasets for training and retrieval:

Humanitarian Data Exchange (HDX) WASH Datasets: Contains GPS coordinates and status of rural water points. https://data.humdata.org/dataset?vocab\_Topics=water+sanitation+and+hygiene-wash

WHO/UNICEF Joint Monitoring Programme (JMP) Global WASH Data Portal: Global water and sanitation data.

CRAWLED-mattv: CAWST WASH Education and Training Resources: Guides for household water treatment and emergency batch chlorination. https://washresources.cawst.org/en

CRAWLED-michael: Appropedia (Water Purification Wiki): Open-source wiki for DIY and low-cost water filtration methods. https://www.appropedia.org/Point-of-use\_water\_treatment

EPA Drinking Water Treatability Database (TDB): Technical database detailing over 35 treatment processes for regulated and unregulated contaminants. https://www.epa.gov/water-research/drinking-water-treatability-database-tdb

CRAWLED-ColeU: FDA - Water Safety During Power Outage: https://www.fda.gov/food/buy-store-serve-safe-food/food-and-water-safety-during-power-outages-and-floods#if 

CRAWLED-ColeU: CDC - Emergency Water Storage: https://www.cdc.gov/water-emergency/about/how-to-create-and-store-an-emergency-water-supply.html 

CRAWLED-ColeU: CDC - Safe Water Storage: https://www.cdc.gov/global-water-sanitation-hygiene/about/about-safe-water-storage.html 

CRAWLED-ColeU: Ready.gov - General Water Knowledge (site): https://www.ready.gov/water 

CRAWLED-ColeU: EPA - Emergency Water Disinfection: https://www.epa.gov/ground-water-and-drinking-water/emergency-disinfection-drinking-water 

CRAWLED-ColeU: FDA - Water and Flood tips: https://www.fda.gov/food/food-safety-during-emergencies/floods-key-tips-consumers-about-food-and-water-safety 

CRAWLED-ColeU: USDA - Emergency Drinking Water (PDF - Booklet): https://www.ams.usda.gov/sites/default/files/media/AA_20332D_Water_Drinking_Emergency.pdf

# Training Data Disregarded (with Reason)

USDA - Water Safety: https://www.fns.usda.gov/fs/water-safety - Not used due to lack of useful information over other sources already crawled. If anyone disagrees with this, feel free to reinstate - Cole U.

# Tools

Crawl tool: Fire Crawl

Database: supabase

Agent: Ollama-3.2-3B (Q4_K_M) - LM Studio

# Reminder of Implementation:

needs chunking for the RAG implementation

# Needs Development:

Sets of testing questions - Insert below if you think of any solid questions. (Questions - w/Expected Answer)

* "Can i drink my water if it is brown?" -  " I need to know why the water turned brown to be able to answer that"

(we want our AI to NOT guess because that will get people hurt so asking user for more inrofmation is better)
* "Can i purify water by adding bleach to it?" -  "You cannot purify water with bleach, try other methods like boiling water or using water filters

(Some other chatbots will tell you that adding bleach to water is safe to drink)
* "


Testing framework for the chatbot capability (Correctness, Comprehensiveness, any other matricies)

Additional sources of information Needed as determined by AI Judge (if we choose to do this method of judging)



