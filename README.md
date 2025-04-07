# Free Palestine 🇵🇸✌️

## Overview 🌍

This repository hosts a list of publicly traded companies that are known or suspected to support Israel and the IDF, created using resources like [AFSC](https://afsc.org/gaza-genocide-companies) and [BDS Movement](https://bdsmovement.net/Act-Now-Against-These-Companies-Profiting-From-Genocide), focusing on those with military contracts, settlement operations, or other forms of involvement. The list aims to raise awareness about corporate involvement in the ongoing conflict in Palestine and Gaza, particularly regarding alleged crimes and human rights issues. It is not financial advice and is for informational purposes only. Users should conduct their own research before making investment decisions, acknowledging the complexity and sensitivity of the topic. 🇵🇸

## Purpose ✊

Free Palestine 🇵🇸 is an open-source initiative to document and share information about companies potentially complicit in the conflict, empowering individuals to make informed choices about their investments. Together, we can raise awareness and support the cause for justice and freedom in Palestine. ✌️

## Boycott List 📜

### Human-Readable Format
Check out the [supporting_list.md](supporting_list.md) file for the detailed list of companies in a human-readable table format, including:
- Company Name
- Stock Code
- Reason for Boycotting
- Source Link
- Embedded Link

**Note on the List**: The boycott list includes companies with confirmed support for Israel and the IDF, as well as those where support is suspected but not 100% confirmed. For the latter, we have clearly noted "Not 100% confirmed" in the "Reason for Boycotting" column. Some companies listed may not be publicly traded (e.g., Chanel, Nutella) but are included due to community allegations of involvement. We encourage users to verify all information independently, as corporate involvement can change, and some allegations may not be fully substantiated. 🇵🇸

### Machine-Readable Format (JSON)
For developers and applications, we provide a machine-readable version of the boycott list in JSON format. You can find it in [boycott_list.json](boycott_list.json). The JSON file contains the same data as the markdown table, structured as an array of objects with the following fields:
- `company_name`
- `stock_code`
- `reason_for_boycotting`
- `source_link`
- `embedded_link`

**Raw URL for Programmatic Access**:  
You can fetch the JSON directly using the following URL:  
`https://raw.githubusercontent.com/steityeh/freepalestine/main/boycott_list.json`

**Example Usage in Python**:  
Here’s a simple Python script to fetch and parse the JSON file:

```python
import requests
import json

# Fetch the JSON data
url = "https://raw.githubusercontent.com/steityeh/freepalestine/main/boycott_list.json"
response = requests.get(url)
data = response.json()

# Print the first few entries
for company in data[:3]:
    print(f"Company: {company['company_name']}")
    print(f"Stock Code: {company['stock_code']}")
    print(f"Reason: {company['reason_for_boycotting']}")
    print(f"Source: {company['source_link']}")
    print("---")
