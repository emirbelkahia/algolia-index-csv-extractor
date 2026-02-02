# Algolia Attribute Exporter

Extract a single attribute from Algolia index hits and export to CSV.

**🔗 Tool:** [emirbelkahia.com/algolia-attribute-exporter](http://emirbelkahia.com/algolia-attribute-exporter/)

## What it does

This web-based tool performs an empty query (`""`) on an Algolia index and extracts a specific attribute from all returned hits. Results are displayed in a table and can be downloaded as CSV.

**Key features:**
- Empty query search (returns all hits up to pagination limit)
- Optional rule context to test conditional rules
- Configurable attribute extraction (any attribute name)
- Automatic pagination (up to 10 pages / 10,000 hits)
- CSV export with timestamp and context in filename

## Use Cases

- **Extract product SKUs/references** for a specific rule context (mobile, desktop, promo)
- **Test rule behavior** by seeing which hits are returned with a given context
- **Quick data export** from an Algolia index without API coding
- **Catalog validation** - verify specific attributes across your index

## How to Use

1. **Access the tool:** Visit [emirbelkahia.com/algolia-attribute-exporter](http://emirbelkahia.com/algolia-attribute-exporter/)

2. **Enter credentials:**
   - Algolia Application ID
   - Algolia API Key (Search API Key or Admin API Key)
   - Index Name

3. **Configure extraction:**
   - **Rule Context (optional):** Leave empty or specify a context (e.g., `mobile`, `promo`)
   - **Attribute to extract:** The attribute name to export (e.g., `objectID`, `sku`, `name`, `reference_catalogue`)

4. **Generate and download:**
   - Click Submit to fetch data
   - View results in the table
   - Click "Download CSV" to export

## Technical Details

- **Frontend only:** Pure JavaScript with Algolia JavaScript client
- **No backend:** API keys stay in your browser
- **Pagination:** Fetches up to 10 pages (10,000 hits max)
- **CSV format:** One attribute value per line

## Limitations

- **10,000 hits maximum** due to pagination limit (10 pages × 1,000 hits/page)
- **Empty query only** - no search term filtering
- **Single attribute export** - exports one attribute at a time

## About

Built by [Emir Belkahia](https://www.linkedin.com/in/emirbelkahia/), Customer Success Manager at Algolia.

Not an official Algolia product.

## License

MIT License
