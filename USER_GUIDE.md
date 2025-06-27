# eBay Listing Creator - User Guide

## Table of Contents
1. [Getting Started](#getting-started)
2. [Creating Listings](#creating-listings)
3. [Managing Listings](#managing-listings)
4. [Variation Generator](#variation-generator)
5. [Troubleshooting](#troubleshooting)
6. [Tips & Best Practices](#tips--best-practices)

---

## Getting Started

### Logging In
1. Open the eBay Listing Creator in your web browser
2. Enter your login credentials:
   - **Username**: Scotspeed
   - **Password**: (provided separately)
3. Click "Login"

### Main Navigation
Once logged in, you'll see three main tabs at the top:
- **Create Listings** - Upload Excel files to create new listings
- **Manage Listings** - Search and modify existing listings
- **Variation Generator** - Create color/trim variations quickly

---

## Creating Listings

### Overview
This feature allows you to upload Excel files and create eBay listings in bulk. You can upload listings with or without vehicle compatibility data.

### Step-by-Step Process

#### Step 1: Choose Upload Mode
You'll see three options:
- **Listings Only** - When you only have product listings
- **Compatibility Only** - When updating vehicle compatibility for existing items
- **Both Files** - When you have both listings and compatibility data

#### Step 2: Upload Your Files

**For "Listings Only" mode:**
1. Click the upload area or drag your Excel file
2. The file should contain columns like:
   - `CustomLabel` (SKU)
   - `*Title` (Product title)
   - `*Description` (Product description)
   - `*StartPrice` (Price)
   - `*Quantity` (Stock quantity)

**For "Compatibility Only" mode:**
1. Upload your compatibility Excel file
2. Format should be:
   ```
   ItemID | RelationshipDetails
   SKU1   |
          | Ktype=12345
          | Ktype=12346
   SKU2   |
          | Ktype=12347
   ```

**For "Both Files" mode:**
1. Upload both files using the separate drop zones
2. Files with "compat" in the name are auto-detected as compatibility files

#### Step 3: Configure Processing Options
1. **Select Store**: Choose which eBay store to use
2. **Processing Mode**:
   - **Verify Only (Dry Run)** - Test without creating listings (RECOMMENDED for first time)
   - **Create Listings** - Actually create listings on eBay
3. **Batch Size**: How many listings to process at once (default: 50)
4. **Start Row**: Which row to start from (useful for resuming)

#### Step 4: Process
1. Click "Verify" to test or "Create Listings" to proceed
2. Monitor progress in real-time
3. Check the summary for any errors

### Important Notes
- Always use "Verify Only" first to check for errors
- Created listings go live on eBay immediately
- There's no built-in way to delete listings - use eBay Seller Hub

---

## Managing Listings

### Overview
This feature helps you:
- Remove vehicle compatibility from listings (e.g., if wrong compatibility was added)
- Delete/end active listings

### Removing Compatibility

#### When to Use
- Electric car mats have petrol/diesel compatibility by mistake
- Wrong vehicle years attached to a product
- Any incorrect Ktype assignments

#### How to Use
1. Click the "Manage Listings" tab
2. Select "Remove Compatibility" sub-tab
3. **Search for Listings**:
   - Choose "Search by SKU" or "Search by Title"
   - Enter your search term (e.g., "F5" or "BMW")
   - Click "Search"
4. **Select Listings**:
   - Check the boxes next to listings you want to modify
   - Use "Select All" for bulk operations
5. **Remove Compatibility**:
   - Click "Remove Compatibility (X)" button
   - Confirm the action
   - Wait for processing to complete

### Deleting Listings

#### When to Use
- Remove test listings
- End listings that are no longer needed
- Clean up after testing

#### How to Use
1. Select "Delete Listings" sub-tab
2. Search and select listings (same as above)
3. Click "Delete Listings (X)" button
4. Choose ending reason:
   - **NotAvailable** (default) - Item is no longer available
   - **Incorrect** - Listing has errors
   - **LostOrBroken** - Item is damaged
   - **OtherListingError** - Other issues
5. Confirm deletion (this CANNOT be undone)

### Search Tips
- SKU search is exact match (case-insensitive)
- Title search finds partial matches
- The green "Yes" badge shows listings with compatibility
- Check multiple listings for bulk operations

---

## Variation Generator

### Overview
Create color/trim variations quickly without manual copying. Perfect for creating mat variations like:
- Black with Black Trim
- Black with Red Trim
- Black with Blue Trim
- Black with Grey Trim

### Step-by-Step Process

#### Step 1: Upload Template
1. Click "Variation Generator" tab
2. Prepare a template:
   - Use an existing listing Excel export
   - Or create a single row with all product details
3. Drag and drop or click to upload the template file
4. Review the extracted information

#### Step 2: Configure Variations

**Base SKU**
- Enter the main SKU (e.g., "F5", "BMW3", "X142")
- This will be used for all variations

**Variation Type**
- **Standard (4 colors)** - Creates the standard Mat Kings colors
- **Custom Selection** - Choose specific colors you want

**Color Options (for Custom)**
- Standard: Black, Red, Blue, Grey trim
- Additional: White, Green, Orange, Purple, Yellow, Pink trim

**SKU Pattern**
- **Full suffix**: Creates "F5 - Black with Red Trim"
- **DS pattern**: Creates "F5 - RedDS" (Double Stitched)

**Include Parent Listing**
- Check this to create a parent listing that contains all variations
- Uncheck if you only want individual variation listings

#### Step 3: Generate & Download
1. Click "Generate Variations"
2. Review the preview table
3. Click "Download Excel" to get the file
4. Upload this file using "Create Listings" feature

### Example Variations
Starting with base SKU "F5", you'll get:
```
F5 (Parent listing - contains all variations)
F5 - Black with Black Trim
F5 - Black with Red Trim
F5 - Black with Blue Trim
F5 - Black with Grey Trim
```

---

## Troubleshooting

### Common Issues & Solutions

#### "Token expired"
- The app automatically refreshes tokens
- If it fails, contact technical support

#### "Category invalid"
- Check the category ID matches UK eBay
- US and UK use different category numbers

#### "Title too long"
- eBay limit is 80 characters
- Shorten titles in your Excel file

#### "Upload failed"
- Check file is .xlsx or .xls format
- Ensure all required columns are present
- File size should be under 10MB

#### "No listings found"
- Check your search term spelling
- Try searching by a different field
- Ensure listings are active on eBay

#### Variations not showing on eBay
- Parent listing must be created first
- All variations need the same base attributes
- Check RelationshipDetails format is correct

---

## Tips & Best Practices

### Before Creating Listings
1. **Always verify first** - Use dry run mode
2. **Start small** - Test with 1-2 listings
3. **Check your template** - Ensure all required fields have data
4. **Backup your files** - Keep original Excel files

### File Preparation
1. **Use consistent SKUs** - Makes searching easier
2. **Check image URLs** - Ensure they're accessible
3. **Validate Ktypes** - Use recent vehicle data
4. **Format prices** - Use numbers only, no currency symbols

### Batch Processing
1. **Default batch size (50)** works well
2. **For large uploads** (1000+ listings):
   - Process in multiple batches
   - Take breaks between batches
   - Monitor for any errors
3. **Keep logs** - Note which batches are completed

### Variation Best Practices
1. **Consistent naming** - Use the same pattern for all products
2. **Test one product first** - Ensure variations display correctly
3. **Check parent listing** - Must include all variation options
4. **Update inventory** - Ensure adequate stock for each variation

### Safety Tips
1. **Never share login credentials**
2. **Log out when finished**
3. **Verify mode is your friend** - Use it liberally
4. **Double-check before deleting** - Deletions cannot be undone
5. **Keep records** - Save processing logs and reports

### When Things Go Wrong
1. **Don't panic** - Most issues are fixable
2. **Check the logs** - Error messages provide clues
3. **Try a smaller batch** - Isolate problem listings
4. **Contact support** - With specific error messages

---

## Quick Reference

### Required Excel Columns for Listings
- `CustomLabel` - Your SKU
- `*Title` - Product title (max 80 chars)
- `*Description` - HTML description
- `*Category` - eBay category ID
- `*StartPrice` - Price in GBP
- `*Quantity` - Stock amount
- `*Location` - Item location

### Compatibility File Format
```
ItemID | RelationshipDetails
SKU    |
       | Ktype=12345
       | Ktype=12346
```

### File Upload Modes
- **Listings Only** - Just product data
- **Compatibility Only** - Just Ktype data  
- **Both Files** - Complete listing with compatibility

### Processing Modes
- **Verify Only** - Test run, no listings created
- **Create Listings** - Live mode, creates real listings

---

## Need Help?

If you encounter issues not covered in this guide:
1. Take a screenshot of the error
2. Note what you were trying to do
3. Check if the issue persists after refreshing
4. Contact technical support with details

Remember: It's always better to ask before making changes you're unsure about, especially when deleting or modifying live listings.

---

*Last updated: January 2025*