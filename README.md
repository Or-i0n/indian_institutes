# Indian Central Government Research Institutes & Specialized Facilities

This repository provides a structured JSON dataset mapping major central government research institutions, space centres, agricultural research institutes (primarily under ICAR), CSIR laboratories, DRDO establishments, ISRO centres, and other key scientific facilities across India to their respective states/union territories and cities/towns.

The data is organized as a nested JSON object: `state/UT` → `city/town` → `array of institute names`. It's designed for easy querying, visualization, or integration into apps, maps, or study tools.

## Purpose
This dataset is ideal for:
- **Exam Preparation**: UPSC, SSC, State PSCs, Banking exams (Geography, Science & Technology sections)
- **GK Quizzes**: Quick lookups for institute locations
- **Educational Tools**: Building interactive maps or flashcards
- **Research & Journalism**: Reference for scientific infrastructure distribution
- **Data Analysis**: Exploring regional hubs of innovation (e.g., Bengaluru's cluster)

Data is sourced from official government websites (ICAR, CSIR, ISRO, DRDO, etc.) and cross-verified for accuracy as of the compilation date.

## Files
- **`institutes.json`**: The core dataset in JSON format. Human-readable and compact (~50 KB).
- **`README.md`**: This file.

## Dataset Structure
The JSON follows this schema:
```json
{
  "State/UT Name": {
    "City/Town": [
      "Institute Full Name",
      "Another Institute"
    ]
  }
}
```

### Coverage
- **Total States/UTs**: 28 states + 8 UTs (comprehensive for India).
- **Total Cities/Towns**: ~150 unique locations.
- **Total Institutes**: ~300+ major facilities.
- **Focus Areas**: ICAR (agriculture/horticulture), CSIR (science/tech), ISRO/DRDO (space/defence), DBT/DST (biotech/advanced research), medical (AIIMS/NIPER), and more.

Major hubs include:
- **Bengaluru, Karnataka**: IISc, ISRO HQ, NCBS, NAL – India's Silicon Valley for science.
- **Delhi (NCT)**: Multiple CSIR labs, IIT Delhi, AIIMS.
- **Lucknow, Uttar Pradesh**: CSIR-CDRI, CIMAP, NBRI.
- **Mumbai, Maharashtra**: BARC, TIFR, NCL.

### Sample Data
```json
{
  "Andaman and Nicobar": {
    "Port Blair": ["Central Island Agricultural Research Institute"]
  },
  "Andhra Pradesh": {
    "Sriharikota": ["Satish Dhawan Space Centre (SDSC)"],
    "Rajahmundry": ["Central Tobacco Research Institute (CTRI)"],
    "Visakhapatnam": ["Dredging Corporation of India"]
  },
  "Karnataka": {
    "Bengaluru": [
      "Indian Institute of Science (IISc)",
      "Indian Space Research Organisation (ISRO) Headquarters",
      "National Aerospace Laboratories (CSIR-NAL)",
      "Raman Research Institute",
      "Jawaharlal Nehru Centre for Advanced Scientific Research (JNCASR)"
    ]
  },
  "Uttar Pradesh": {
    "Lucknow": [
      "Central Drug Research Institute (CSIR-CDRI)",
      "Central Institute of Medicinal and Aromatic Plants (CSIR-CIMAP)",
      "National Botanical Research Institute (CSIR-NBRI)"
    ],
    "Jhansi": ["Indian Grassland and Fodder Research Institute (IGFRI)"]
  }
}
```

For the full list, see [institutes.json](institutes.json).

## Usage
### Quick Query (Python Example)
```python
import json

with open('institutes.json', 'r') as f:
    data = json.load(f)

# Find institutes in Bengaluru
bengaluru_institutes = data['Karnataka']['Bengaluru']
print(bengaluru_institutes)
# Output: ['Indian Institute of Science (IISc)', 'Indian Space Research Organisation (ISRO) Headquarters', ...]
```

### Visualization Ideas
- Use D3.js or Leaflet to plot on an India map.
- Generate a heatmap of institutes per state with Matplotlib/Pandas.

## Contributing
Contributions are welcome! To add/correct data:
1. Fork the repo.
2. Edit `institutes.json` (add entries in alphabetical order by state/city).
3. Provide sources (e.g., official website links) in a PR description.
4. Submit a pull request.

Common additions: New institutes, relocations, or expansions (e.g., post-2023 updates).

If you spot errors, open an issue with details.

## License
This dataset is released under the **CC0 1.0 Universal (Public Domain Dedication)**.  
You may use, modify, and distribute it freely for any purpose, including commercial, without attribution.

## Credits & Updates
- **Compiler**: Or-i0n
- **Last Updated**: December 2025 (based on official sources; check for post-2025 changes).
- **Sources**: ICAR.gov.in, CSIR.res.in, ISRO.gov.in, DRDO.gov.in, and ministry portals.

For questions or collaborations, open an issue! 🇮🇳
