# Common Scenarios & Solutions

## Scenario 1: "I need to upload 500 new car mat listings"

### Best Approach:
1. **Prepare your files**
   - Split into batches of 100 listings each
   - Name them: batch1.xlsx, batch2.xlsx, etc.

2. **Test first batch**
   - Upload batch1.xlsx in "Verify Only" mode
   - Fix any errors in Excel
   - Create the first 100 listings

3. **Process remaining batches**
   - Wait 5 minutes between batches
   - Monitor for any errors
   - Keep notes of completed batches

### Time Estimate: 
- 100 listings = ~5-10 minutes
- 500 listings = ~30-45 minutes total

---

## Scenario 2: "Electric car mats show diesel compatibility"

### Quick Fix:
1. **Go to Manage Listings**
   - Search for the affected SKUs
   - Example: Search "TESLA" or "EV-"

2. **Remove all compatibility**
   - Select all affected listings
   - Click "Remove Compatibility"
   - This removes ALL vehicle compatibility

3. **Add correct compatibility**
   - Prepare new compatibility Excel
   - Use "Compatibility Only" upload mode
   - Upload just the Ktype data

### Important: 
- You cannot selectively remove compatibility
- Must remove all, then re-add correct ones

---

## Scenario 3: "I need variations for 20 different car models"

### Efficient Method:
1. **Create templates**
   - Export one listing per car model
   - Save as individual Excel files

2. **Use Variation Generator**
   - Process each template:
     - Upload template
     - Set base SKU (F5, F6, etc.)
     - Generate variations
     - Download Excel

3. **Bulk upload**
   - Combine all variation files
   - Upload in one batch
   - Total: 20 models × 5 variations = 100 listings

### Time Saver:
- Use "DS" pattern for consistent SKUs
- Keep same price for all variations
- Use standard 4 colors unless requested otherwise

---

## Scenario 4: "Listing creation failed halfway through"

### Recovery Steps:
1. **Check what was created**
   - Note the last successful SKU
   - Go to eBay Seller Hub to verify

2. **Adjust your file**
   - Remove already created listings
   - Or use "Start Row" option

3. **Resume processing**
   - Set "Start Row" to where it failed
   - Reduce batch size to 25
   - Process remaining items

### Prevention:
- Always verify first
- Use smaller batches for new templates
- Check for special characters in data

---

## Scenario 5: "Wrong prices on 50 listings"

### Current Limitation:
- App cannot modify prices
- Must use eBay Seller Hub

### Workaround:
1. **Export from eBay**
   - Use eBay File Exchange
   - Download current listings

2. **Update prices**
   - Modify in Excel
   - Use eBay's bulk edit tool

3. **Future uploads**
   - Correct template prices
   - Verify before creating

---

## Scenario 6: "Need to add variations to existing listing"

### Two Options:

**Option A: Start Fresh**
1. Delete existing listing (Manage Listings tab)
2. Use Variation Generator with template
3. Upload complete variation set

**Option B: Manual Method**
1. Cannot add variations to existing via app
2. Must use eBay Seller Hub
3. Or delete and recreate with variations

### Best Practice:
- Plan variations before initial upload
- Always create parent + variations together

---

## Scenario 7: "Uploaded wrong compatibility file"

### Quick Resolution:
1. **Don't panic** - fixable!
2. **Manage Listings** → Search affected SKUs
3. **Select all** → Remove Compatibility
4. **Create Listings** → Compatibility Only mode
5. Upload correct compatibility file

### Time: ~5 minutes to fix

---

## Scenario 8: "Need different trim colors for different models"

### Custom Variation Setup:
1. **BMW Models** (sporty colors)
   - Use custom colors: Black, Red, Blue, White
   
2. **Mercedes Models** (luxury colors)
   - Use custom colors: Black, Grey, Beige
   
3. **Generate separately**
   - One template per color scheme
   - Download each variation set
   - Combine for upload

---

## Scenario 9: "Test listings before going live"

### Safe Testing Process:
1. **Create test SKUs**
   - TEST-001, TEST-002, etc.
   
2. **Set high prices**
   - £999 prevents accidental sales
   
3. **Verify appearance**
   - Check on eBay
   - Test all variations show correctly
   
4. **Delete test listings**
   - Use Manage Listings tab
   - Select all test SKUs
   - Delete with reason "OtherListingError"

---

## Scenario 10: "Monthly bulk upload routine"

### Optimized Workflow:
1. **Week 1: Preparation**
   - Gather all product data
   - Prepare images, upload to hosting
   - Create master Excel file

2. **Week 2: Testing**
   - Upload 10 items in verify mode
   - Create test listings
   - Check on eBay
   - Fix any issues

3. **Week 3: Bulk Processing**
   - Split into daily batches (200/day)
   - Process morning: less eBay traffic
   - Monitor for errors

4. **Week 4: Compatibility**
   - Add vehicle compatibility
   - Generate variations as needed
   - Quality check random samples

---

## Emergency Procedures

### "I created 100 wrong listings!"
1. **Stop immediately**
2. **Go to Manage Listings**
3. **Search and select all wrong items**
4. **Delete with "Incorrect" reason**
5. **Document what happened**

### "The app is not responding"
1. **Don't repeatedly click**
2. **Wait 2 minutes**
3. **Refresh page once**
4. **Check if listings were created**
5. **Continue from last successful point**

### "Excel file corrupted during process"
1. **Always keep backup**
2. **Check downloads folder for temp files**
3. **Recreate from eBay export if needed**
4. **Use CSV as last resort**

---

## Pro Efficiency Tips

### Keyboard Shortcuts
- `Ctrl+A` - Select all in search results
- `Enter` - Submit search
- `Tab` - Navigate between fields

### File Organization
```
/eBay Listings
  /2025-01
    /Uploads
      - batch1_created.xlsx ✓
      - batch2_created.xlsx ✓
      - batch3_pending.xlsx
    /Templates
      - BMW_template.xlsx
      - Mercedes_template.xlsx
    /Compatibility
      - ktypes_january.xlsx
```

### Naming Convention
- SKU: `BRAND-MODEL-YEAR-TYPE`
- Example: `BMW-3SER-2020-STD`
- Variations: `BMW-3SER-2020-STD-RedDS`

---

*Remember: Every mistake is fixable. Stay calm and methodical.*