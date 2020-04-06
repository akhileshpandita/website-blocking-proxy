# Internationally Blocked Domains Demo
The code in this repo generates an interactive demo that allows the user to select a country on a world map to visualize common web domains blocked in other countries.

Below are explanations of key folders / files:
- local_country_variables/ : contains a JS file with a list of all countries included in the demo and a JS file with a list of all GDPR countries to prevent multiple unnecessary loads / data file reading delay in the page scripts
- notebooks/ : contains raw and cleaned data, and starting IPython analysis
-- cleaned_data/ : contains domain data scraped from URLs in Acknowledgements (see `scrape-blocked-websites.ipynb`)
-- common_domains/ : contains subsets of rows from combined_similarities.json in a more readable CSV format, corresponding to specific countries (see `preliminary_blocked_site_overlap.ipynb`)
- combined_similarities.json : initially-loaded file with country-specific similarity data to generate map colors
- index.html : main demo page

## Getting Started
To run the web server locally, download the repo and enter the main directory containing "index.html." Run `npm start` and access either the local or network links.

To view the public copy of the demo, click [here](https://pair-interoperability-demo.herokuapp.com/).

## License
BSD-3

## Acknowledgements
The following links / sources were used to generate the domain data for currently-enabled countries:
- [Iraq](https://www.theregister.co.uk/2014/07/01/revealed_the_great_firewall_of_iraq/)
- [China](https://cyber.harvard.edu/filtering/china/)
- [Saudi Arabia](https://cyber.harvard.edu/filtering/saudiarabia/)
- [India](https://www.medianama.com/2012/05/223-isp-wise-list-of-blocked-sites-indiablocks/)
- [Russia](https://web.archive.org/web/20140710063312/http://www.antizapret.info/)
- [All EU Nations](https://data.verifiedjoseph.com/dataset/websites-not-available-eu-gdpr)
-- Note: This visualization currently applies GDPR regulations to the UK. According to several sources, including [IT Governance](https://www.itgovernance.co.uk/eu-gdpr-uk-dpa-2018-uk-gdpr), EU GDPR will continue to apply to the UK until the Brexit transition period ends, at which point a UK GDPR may be negotiated.
- [Pakistan](https://propakistani.pk/wp-content/uploads/2010/05/blocked.html)
- [United Arab Emirates](https://pastehtml.com/view/c3321xhl7.rtxt) (leaked by Anonymous)

The following country data will be integrated in the future:
- [North Korea](https://www.npr.org/sections/thetwo-way/2016/09/21/494902997/north-korea-accidentally-reveals-it-only-has-28-websites)
