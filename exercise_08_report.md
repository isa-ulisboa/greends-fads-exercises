## 1. Identification of Platform APIs

The table below summarizes the availability of web service APIs across major environmental and statistical data portals, outlining navigation paths, documentation URLs, example query endpoints, and supported data formats.

| Platform | URL | Path to API information | Documentation URL | API URL | Data format |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **GBIF** | [gbif.org](https://www.gbif.org/) | Home --> Developer --> Summary | [GBIF OpenAPI Docs](https://techdocs.gbif.org/en/openapi/) | `https://api.gbif.org/` | json |
| **Eurostat** | [ec.europa.eu/eurostat](https://ec.europa.eu/eurostat/) | Home --> Support --> Web Services / API | [Eurostat User Guide](https://ec.europa.eu/eurostat/web/user-guides/data) | `https://ec.europa.eu/eurostat/api/` | json, xml, sdmx |
| **INE** | [ine.pt](https://www.ine.pt/) | Home --> Serviços --> API Catálogo de Indicadores | [INE API Catálogo](https://www.ine.pt/xportal/xmain?xpid=INE&xpgid=ine_api_catalogo) | `https://www.ine.pt/ine/xml_indic.jsp?opc=1&varcd={code}&lang=PT` | xml, json |
| **Climate Data Store** | [cds.climate.copernicus.eu](https://cds.climate.copernicus.eu/) | Home --> Download data / API guide | [CDS API How-to](https://cds.climate.copernicus.eu/how-to-api) | `https://cds.climate.copernicus.eu/api` | netcdf, grib, json |
| **Copernicus Data Space Ecosystem** | [dataspace.copernicus.eu](https://dataspace.copernicus.eu/) | Home --> Analyse --> APIs | [CDSE API Documentation](https://documentation.dataspace.copernicus.eu/APIs.html) | `https://sh.dataspace.copernicus.eu/` | json, geojson, tiff |
| **WMO** | [worldweather.wmo.int](https://worldweather.wmo.int/en/home.html) | Home --> Resources / Services | [WMO Homepage](https://worldweather.wmo.int/) | `https://worldweather.wmo.int/` | json, xml |
| **Agri4Cast** | [agri4cast.jrc.ec.europa.eu](https://agri4cast.jrc.ec.europa.eu/DataPortal/) | Home --> Help / Data Portal Resources | [JRC Data Catalogue](https://data.jrc.ec.europa.eu/collection/agri4cast) | OGC SensorThings / JRC API endpoints | netcdf, csv, json |
| **European Environment Agency** | [eea.europa.eu](https://www.eea.europa.eu/) | Home --> Data and maps --> APIs | [EEA Developer Docs](https://www.eea.europa.eu/) | EIONET / EEA REST Endpoints | json, csv, rdf, xml |

---

## 2. Web Scraping Discussion Questions

### Q1: How can I detect that a web site has hidden data?
To detect hidden data or background requests on a website, you can use browser Developer Tools (`F12`):
1. Open the **Network** tab in Developer Tools before performing an action on the page.
2. Filter the requests by **Fetch/XHR**.
3. Interact with the website (e.g., select a date range, change a region dropdown, or click a search button).
4. Observe newly generated background requests. If the page updates data dynamically without reloading the entire HTML document, it is likely fetching structured data (such as JSON or XML) from an unlisted internal endpoint or API.

### Q2: When should I decide to do steps in web scraping manually versus doing everything automatically?
* **Manual Steps:** Best chosen for one-off data pulls, very small datasets, pages heavily protected by complex anti-scraping CAPTCHAs, or when website structures change unpredictably and automation maintenance costs outweigh the time saved.
* **Automated Scripts:** Best chosen for large-scale data collection, repetitive or scheduled tasks (e.g., hourly air quality logs, daily meteorological reports), and consistent web page layouts where manual extraction would be excessively tedious and prone to human error.

### Q3: What advantages and problems do I have doing web scraping?
* **Advantages:**
  * Allows data extraction even when an official public API is not provided.
  * Eliminates tedious manual copy-pasting.
  * Unlocks legacy data locked inside standard web pages.
* **Problems:**
  * **Fragility:** Any minor change in the website’s HTML structure (tags, classes, IDs) will break the scraping script.
  * **Legal & Ethical Risks:** Potential violations of Terms of Service (ToS), copyright laws, or scraping sensitive/personal information.
  * **Technical Barriers:** Rate-limiting, IP address blocking, and handling heavy JavaScript rendering (which may require headless browsers like Selenium or Playwright).

### Q4: What are the differences in getting data by web scraping compared to an API? Which approach do I prefer and why?
* **Differences:** An **API** is an official, structured interface explicitly built by developers to serve data reliably with clear parameters and format guarantees (JSON/XML). **Web scraping**, on the other hand, parses human-readable HTML user interfaces, extracting text tags meant for browser display rather than direct machine consumption.
* **Preference:** I strongly prefer **APIs** because they are robust, stable, legal, and significantly faster to query. Web scraping should only be used as a secondary fallback option when an official API is entirely unavailable.

---

## 3. Plan a Web Scraping Exercise: SASSCAL WeatherNET

### Can I do it legally? Why?
Yes, provided it is approached responsibly. Extracting open environmental data for academic research or non-commercial scientific analysis generally falls under permissible use. However, you must always check the platform's `robots.txt` file and Terms of Service, implement reasonable delays (rate-limiting) between requests to avoid overloading their servers, and refrain from commercializing or redistributing proprietary datasets.

### Which items of information (IDs, parameters, etc.) are available to use in web scraping?
To scrape historical or real-time weather data from SASSCAL WeatherNET, the scraping workflow would target:
* **Station Metadata:** Station unique identifiers (`station_id`), station names, and geographic coordinates (latitude, longitude, elevation).
* **Temporal Parameters:** Date selectors (`start_date`, `end_date`), operating years, and recording frequencies (hourly, daily, monthly).
* **Meteorological Variables:** Air temperature, relative humidity, atmospheric pressure, wind speed and direction, precipitation/rainfall totals, and solar radiation.
