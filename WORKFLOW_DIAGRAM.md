# eBay Listing Creator - Visual Workflows

## 📊 Main Workflow Overview

```
┌─────────────┐
│   LOGIN     │
│ Username:   │
│ Scotspeed   │
└──────┬──────┘
       │
       ▼
┌─────────────────────────────────────────┐
│          CHOOSE YOUR TASK               │
├─────────────┬─────────────┬─────────────┤
│   CREATE    │   MANAGE    │  VARIATION  │
│  LISTINGS   │  LISTINGS   │ GENERATOR   │
└──────┬──────┴──────┬──────┴──────┬──────┘
       │             │             │
       ▼             ▼             ▼
```

---

## 🔄 Create Listings Workflow

```
CREATE LISTINGS
      │
      ▼
┌─────────────────┐
│ Select Upload   │
│     Mode        │
├─────────────────┤
│ • Listings Only │
│ • Compat Only   │
│ • Both Files    │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│  Upload Files   │
│  📁 Drag here   │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│ Configure       │
│ • Store         │
│ • Batch Size    │
│ • Start Row     │
└────────┬────────┘
         │
         ▼
    ⚠️ IMPORTANT
┌─────────────────┐
│  Verify First!  │
│  [Verify Only]  │
└────────┬────────┘
         │
     No Errors?
         │
         ▼
┌─────────────────┐
│ Create Listings │
│ [Create Button] │
└────────┬────────┘
         │
         ▼
    ✅ COMPLETE
```

---

## 🔧 Manage Listings Workflow

```
MANAGE LISTINGS
      │
      ├──────────────┬──────────────┐
      ▼              ▼              │
┌──────────┐  ┌──────────┐         │
│  REMOVE  │  │  DELETE  │         │
│  COMPAT  │  │ LISTINGS │         │
└────┬─────┘  └────┬─────┘         │
     │             │                │
     ▼             ▼                │
┌─────────────────────┐             │
│   Search Listings   │◄────────────┘
│ • By SKU           │
│ • By Title         │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│   Select Items      │
│ ☐ Item 1 (Yes)     │
│ ☐ Item 2 (Yes)     │
│ ☐ Item 3 (No)      │
└──────────┬──────────┘
           │
      ┌────┴────┐
      ▼         ▼
┌──────────┐ ┌──────────┐
│  Remove  │ │  Delete  │
│  Compat  │ │ Listings │
└────┬─────┘ └────┬─────┘
     │            │
     ▼            ▼
 ⚠️ CONFIRM    ⚠️ CONFIRM
     │            │
     ▼            ▼
✅ REMOVED   ✅ DELETED
```

---

## 🎨 Variation Generator Workflow

```
VARIATION GENERATOR
        │
        ▼
┌───────────────┐
│Upload Template│
│ 📄 (1 row)    │
└───────┬───────┘
        │
        ▼
┌───────────────┐
│ Set Base SKU  │
│ Example: F5   │
└───────┬───────┘
        │
        ▼
┌───────────────────────┐
│   Choose Options      │
├───────────────────────┤
│ Type:                 │
│ ○ Standard (4 colors) │
│ ○ Custom              │
├───────────────────────┤
│ Pattern:              │
│ ○ Full (F5 - Black..)│
│ ○ DS (F5 - BlackDS)  │
├───────────────────────┤
│ ☑ Include Parent      │
└──────────┬────────────┘
           │
           ▼
┌───────────────────────┐
│  Generate Variations  │
│     [Generate]        │
└──────────┬────────────┘
           │
           ▼
┌───────────────────────┐
│   Preview Results     │
├───────────────────────┤
│ F5 (Parent)          │
│ F5 - BlackDS         │
│ F5 - RedDS           │
│ F5 - BlueDS          │
│ F5 - GreyDS          │
└──────────┬────────────┘
           │
           ▼
┌───────────────────────┐
│   Download Excel      │
│   [Download] 💾       │
└───────────────────────┘
           │
           ▼
    📁 variations_F5.xlsx
           │
           ▼
    Upload in Create
    Listings Tab
```

---

## 📁 File Format Examples

### Listings File Structure
```
┌─────────────┬──────────────────┬────────┬──────────┬───────────┐
│ CustomLabel │ *Title           │ *Price │ *Quantity│ *Category │
├─────────────┼──────────────────┼────────┼──────────┼───────────┤
│ BMW-001     │ BMW 3 Series ... │ 15.99  │ 10       │ 36678     │
│ BMW-002     │ BMW 5 Series ... │ 17.99  │ 15       │ 36678     │
└─────────────┴──────────────────┴────────┴──────────┴───────────┘
```

### Compatibility File Structure
```
┌─────────────┬─────────────────────┐
│ ItemID      │ RelationshipDetails │
├─────────────┼─────────────────────┤
│ BMW-001     │                     │
│             │ Ktype=12345         │
│             │ Ktype=12346         │
│ BMW-002     │                     │
│             │ Ktype=12347         │
└─────────────┴─────────────────────┘
```

### Variation Structure (Generated)
```
┌─────────────────────┬──────────────┬─────────────────────────┐
│ CustomLabel         │ Relationship │ RelationshipDetails     │
├─────────────────────┼──────────────┼─────────────────────────┤
│ F5                  │ (empty)      │ Trim Colour=Black wi... │
│ F5 - BlackDS        │ Variation    │ Trim Colour=Black wi... │
│ F5 - RedDS          │ Variation    │ Trim Colour=Black wi... │
│ F5 - BlueDS         │ Variation    │ Trim Colour=Black wi... │
│ F5 - GreyDS         │ Variation    │ Trim Colour=Black wi... │
└─────────────────────┴──────────────┴─────────────────────────┘
```

---

## 🚦 Decision Flow

```
Need to create listings?
         │
         ├─── Have variations? ──── YES ──→ Use Variation Generator
         │                                          │
         │                                          ▼
         │                                   Generate Excel
         │                                          │
         ▼                                          ▼
    Create Listings ◄───────────────────────────────┘
         │
         ├─── Have compatibility? ── YES ──→ Use "Both Files"
         │                            │
         │                            NO ──→ Use "Listings Only"
         ▼
    Always Verify First!
         │
         ▼
    Then Create
```

---

## ⏱️ Time Estimates

```
Task                          Time per 100 items
─────────────────────────────────────────────────
Verify Listings               2-3 minutes
Create Listings               5-10 minutes
Remove Compatibility          3-5 minutes
Delete Listings              2-3 minutes
Generate Variations          1 minute per model
Search & Select              1-2 minutes

TOTAL SESSION EXAMPLE:
- 500 listings with compatibility
- 5 batches × 10 minutes = 50 minutes
- Plus setup/verification = 60 minutes total
```

---

## 🔐 Safety Checklist

```
Before ANY Operation:
┌─┐ Logged in correctly?
├─┤ Files backed up?
├─┤ Using correct store?
├─┤ Verified first?
└─┘ Ready to proceed?

After Bulk Operations:
┌─┐ Check eBay Seller Hub
├─┤ Verify listings appear
├─┤ Check variations display
├─┤ Save completion log
└─┘ Log out when done
```

---

*These workflows represent the most efficient paths through the system. Always prioritize accuracy over speed.*