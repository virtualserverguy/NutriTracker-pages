---
layout: page
title: Export & Sharing Guide
permalink: /ios/docs/export/
---

# Export & Sharing Guide

Export your activity data for analysis, coaching, backup, or sharing. FuelFlow provides flexible export options to suit different needs.

---

## Overview

**Export Capabilities**:
- CSV files for spreadsheet analysis
- PDF reports for sharing and printing
- Email integration with attachments
- iOS Share Sheet for flexible sharing
- iCloud Drive for automatic backup

**Import Capabilities**:
- HealthKit workout data
- FIT files from Garmin, Wahoo, etc.
- GPX files with GPS routes
- TCX files from training platforms

---

## Export Formats

### CSV (Comma-Separated Values)

**Best for**: Spreadsheet analysis, data science, training logs

**What's included**:
- Activity summary (date, duration, type)
- Nutrition totals (carbs, sodium, water)
- Activity metrics (distance, pace, heart rate, elevation)
- Location and weather data
- Hourly breakdown with rates per hour
- Food and water consumption logs

**Use cases**:
- Import into Excel, Numbers, or Google Sheets
- Analyze trends over multiple activities
- Share with coaches for review
- Create custom charts and reports

**File location**:
- Saved to **iCloud Drive** (default) or local storage
- Folder: `FuelFlow/Exports/` (customizable)
- Filename format: `FuelFlow-YYYY-MM-DD-HHmmss.csv`

---

### PDF (Portable Document Format)

**Best for**: Sharing, printing, archiving

**What's included**:
- Professional formatted report
- Activity summary and metadata
- Nutrition summary with per-hour averages
- Location and weather conditions
- Hourly breakdown table
- Data source attribution
- Generated timestamp

**Use cases**:
- Share with coaches, nutritionists, or training partners
- Print for race reports or journals
- Archive important activities
- Present at team meetings

**Page size options**: Letter, A4 (configurable in settings)

**File location**:
- Saved to **iCloud Drive** (default) or local storage
- Folder: `FuelFlow/Exports/` (customizable)
- Filename format: `FuelFlow-YYYY-MM-DD-HHmmss.pdf`

---

## How to Export

### Quick Export (After Activity)

1. End your activity in FuelFlow
2. View the activity detail screen
3. Tap the **menu** icon (three horizontal lines)
4. Choose export option:
   - **Share Activity** - Opens iOS share sheet
   - **Email Activity** - Compose email with attachment

**Note**: Quick exports use your configured format preferences.

---

### Share Sheet Export

The Share Sheet provides maximum flexibility for sharing:

**What you can do**:
- AirDrop to nearby devices
- Send via Messages or WhatsApp
- Save to Files app (any cloud service)
- Open in other apps (Numbers, Excel, etc.)
- Print directly
- Add to Notes or Reminders

**How to use**:
1. Activity detail screen → **menu** → **Share Activity**
2. Choose sharing destination
3. Select format if prompted (PDF, CSV, or TXT)

**Tip**: The share sheet generates all three formats (PDF, CSV, TXT) so you can choose based on the destination.

---

### Email Export

Send activity reports directly from FuelFlow:

**Setup** (one-time):
1. History tab → Tap **menu** (top right)
2. Tap **Export Settings**
3. Enable **Email** as export destination
4. Tap **Configure Email Export**
5. Add default recipients (optional)
6. Choose attachment format: PDF, CSV, or Text
7. Toggle **Include Attachment** on/off

**Sending email**:
1. Activity detail screen → **menu** → **Email Activity**
2. Email composer opens with:
   - Pre-filled subject line
   - Activity summary in body
   - Attachment in selected format (if enabled)
3. Edit recipients, subject, or body as needed
4. Tap **Send**

**Email formats**:
- **PDF attachment**: Short summary in body + detailed PDF
- **CSV attachment**: Short summary in body + CSV data file
- **Text format**: Full report in email body (no attachment)

**Tip**: Use text format for coaches who prefer inline data. Use PDF for professional reports.

---

## Automatic Exports

Set up automatic exports to save data after every activity:

### Configuring Auto-Export

1. **History** tab → Tap **menu** (top right)
2. Tap **Export Settings**
3. Toggle **Enable Automatic Exports** ON
4. Choose **Export Timing**:
   - **After Run** - Export immediately when activity ends
   - **Manual** - No auto-export (export manually)
5. Select **Export Destinations**:
   - iCloud Text File
   - CSV
   - PDF
   - Email
   - Or multiple destinations
6. Configure each destination (folder paths, file formats, etc.)

**Supported auto-export destinations**:
- iCloud Drive (text, CSV, or PDF)
- CSV to iCloud/local storage
- PDF to iCloud/local storage
- Email (if recipients configured)

**Not supported for auto-export**:
- Share Sheet (manual only)

---

### iCloud Drive Configuration

**Setup**:
1. Export Settings → Enable **iCloud Text File** destination
2. Tap **Configure iCloud Export**
3. Choose settings:
   - **Folder Path**: `FuelFlow/Exports` (default)
   - **File Format**: Text, CSV, or PDF
   - **File Name Format**: Custom prefix
   - **Include Timestamp**: ON (recommended)
4. Tap **Done**

**Finding exported files**:
- Open **Files** app on iPhone or Mac
- Navigate to: **iCloud Drive** → **FuelFlow**
- Exports appear in configured folder

**Important**: Files sync to iCloud Drive root, NOT the Documents subfolder.

**Troubleshooting**:
- If exports don't appear, check iCloud Drive is enabled in Settings → Apple ID → iCloud
- Debug builds: Use **iCloud Diagnostics** in Export Settings to check container access

---

## Importing Workout Data

Add GPS routes, heart rate, and metrics to manually tracked activities:

### HealthKit Import

**What you can import**:
- Distance and pace
- Heart rate (average and max)
- Elevation gain and loss
- GPS route with timestamps
- Calories burned

**How to import**:
1. Track activity with Apple Watch or other HealthKit app
2. In FuelFlow, track nutrition during same activity
3. End activity in FuelFlow
4. Activity detail screen → **menu** → **Attach Workout Data**
5. Tap **From HealthKit**
6. Select matching workout from list
7. Review data → Tap **Import**

**Matching workouts**:
- FuelFlow searches ±30 minutes from your activity start time
- Filters by activity type (run, cycle, swim, etc.)
- Shows duration and distance for easy identification

**Note**: Already imported? Button shows green checkmark.

---

### FIT File Import

**What are FIT files?**
- Industry-standard fitness data format
- Used by Garmin, Wahoo, Polar, Suunto, etc.
- Contains GPS route, heart rate, power, cadence, and more

**How to import**:
1. Get FIT file from your device:
   - Garmin Connect: Download .fit file
   - Wahoo: Export from Elemnt app
   - Computer: Transfer from device via USB
2. Activity detail screen → **menu** → **Attach Workout Data**
3. Tap **From FIT File**
4. Choose file from Files app
5. Review imported data → Tap **Import**

**What gets imported**:
- GPS route with full position history
- Distance (meters)
- Elevation gain/loss (meters)
- Average and max heart rate
- Calories burned
- Timestamps for all data points

**File sources**:
- Download from Garmin Connect, Strava, TrainingPeaks
- Transfer from device via USB
- Email to yourself and save to Files app
- AirDrop from Mac/other iOS device

---

### GPX File Import

**What are GPX files?**
- GPS Exchange Format (XML-based)
- Common export from Strava, MapMyRun, Komoot, etc.
- Contains GPS track points with elevation and timestamps

**How to import**:
1. Get GPX file from training platform
2. Save to Files app on iPhone
3. Activity detail screen → **menu** → **Attach Workout Data**
4. Tap **From FIT File** (handles both FIT and GPX)
5. Choose .gpx file
6. Review imported data → Tap **Import**

**What gets imported**:
- GPS route with position history
- Distance calculated from GPS points
- Elevation gain/loss from GPS elevation data
- Heart rate (if included in GPX)
- Timestamps for route visualization

**Common sources**:
- Strava (Activity → Export GPX)
- MapMyRun (Export workout)
- Komoot (Planned route export)
- Ride with GPS

---

### TCX File Import

**What are TCX files?**
- Training Center XML format (Garmin)
- Used by TrainingPeaks, Garmin Connect
- Contains detailed workout data and routes

**How to import**:
Same process as FIT files - FuelFlow automatically detects file type.

---

## Privacy & Data Ownership

### Your Data, Your Control

**What FuelFlow stores**:
- All activity data stored in **your iCloud account**
- Exports saved to **your iCloud Drive** or local storage
- No data sent to third-party servers
- No analytics or tracking

**Data sync**:
- CloudKit syncs across your devices (iPhone, iPad, Mac, Apple Watch)
- End-to-end encryption via iCloud
- Only you can access your data

**Deleting data**:
- Delete activities in FuelFlow → Removes from all devices
- Delete app → Data remains in iCloud (can restore)
- Sign out of iCloud → Data removed from device

**Sharing control**:
- Exports only happen when you initiate them
- No automatic sharing or uploads
- Share sheets show what you're sharing before sending

---

## Batch Export

Currently, FuelFlow exports one activity at a time.

**Workaround for multiple activities**:
1. Enable **Automatic Exports** to CSV
2. After several activities, find CSV files in iCloud Drive
3. Combine CSV files in spreadsheet app
4. Or: Use third-party CSV merge tools

**Coming soon**: Multi-select export from History view.

---

## Use Cases

### For Coaches

**Share activity reports**:
1. Export to PDF for professional presentation
2. Include weather and terrain data for context
3. Email directly with pre-configured recipient
4. Coach sees nutrition strategy alongside performance

**Bulk analysis**:
1. Enable automatic CSV export
2. Share iCloud folder with coach
3. Coach imports into analysis tools
4. Identify patterns across training block

---

### For Training Analysis

**Spreadsheet analysis**:
1. Export activities to CSV
2. Import into Excel, Numbers, or Google Sheets
3. Create pivot tables for:
   - Average carbs/hour by activity type
   - Hydration trends vs temperature
   - Sodium intake vs sweat rate
   - GI issues vs nutrition timing

**Data science**:
- CSV format includes all metrics and timestamps
- Easy to parse and analyze programmatically
- Combine with power, pace, or other data sources

---

### For Race Reports

**Create race documentation**:
1. Export race to PDF
2. Includes all nutrition details automatically
3. Share with team or post to blog
4. Professional formatting, ready to print

**Archive important events**:
- Save PDFs to Notes with photos
- Add to training journal
- Reference for future race planning

---

### For Backup

**Automatic backup strategy**:
1. Enable automatic export to iCloud Drive
2. Choose CSV format (most portable)
3. Every activity auto-saves after ending
4. Files sync to Mac/PC via iCloud Drive
5. Time Machine or other backup captures them

**Manual backup**:
- Periodically export all activities to CSV
- Save to external cloud (Dropbox, Google Drive)
- Provides redundancy beyond iCloud

---

## Troubleshooting

### Exports not appearing in iCloud Drive

**Check iCloud settings**:
1. Settings app → [Your Name] → iCloud
2. Ensure **iCloud Drive** is enabled
3. Scroll down → Ensure **FuelFlow** is toggled ON

**Check folder location**:
- Files app → iCloud Drive → **FuelFlow** (root level)
- NOT in: iCloud Drive → FuelFlow → Documents
- Use **iCloud Diagnostics** (Debug builds) to verify container access

**Sync delay**:
- iCloud may take 1-2 minutes to sync files
- Ensure device has internet connection
- Check Files app → iCloud Drive shows sync status

---

### Email composer not showing

**Check mail configuration**:
1. Ensure Mail app is configured on device
2. Settings → Mail → Accounts → Add account
3. Or use **Share Activity** → Messages/WhatsApp instead

**Alternative**:
- Use Share Sheet export instead
- Save to Files → Email manually
- Or: AirDrop to Mac and email from there

---

### HealthKit workouts not found

**Check authorization**:
1. Settings → Privacy & Security → Health
2. Tap **FuelFlow**
3. Ensure **Workouts** is enabled for reading

**Timing mismatch**:
- FuelFlow searches ±30 minutes from activity start
- If workout started >30 min before/after, won't match
- Import from FIT file instead if available

**Wrong activity type**:
- FuelFlow filters by activity type
- Swimming workouts won't match running activities
- Check you selected correct type when starting FuelFlow activity

---

### FIT file import failed

**Check file format**:
- Ensure file is .fit, .gpx, or .tcx (case-insensitive)
- Some platforms export .zip - extract first
- If file is corrupted, re-download from source

**File size**:
- Very large files (>10MB) may be slow
- Activities >12 hours may have large GPS tracks
- Be patient - import can take 30-60 seconds

**Unsupported data**:
- FuelFlow extracts: GPS, HR, distance, elevation
- Ignores: Power, cadence, temperature sensors
- Missing data? File may not include those fields

---

### CSV file won't open

**Choose right app**:
- Numbers (Mac/iOS) - Tap file → Open in Numbers
- Excel (Mac/PC) - Import from Data tab
- Google Sheets - Upload to Drive → Open

**Character encoding**:
- FuelFlow uses UTF-8 encoding
- If special characters look wrong, check app import settings

---

## Advanced Tips

### Custom Export Workflows

**Automated backups**:
1. Enable auto-export to iCloud Drive
2. Use Mac Automator or Shortcuts to:
   - Copy from iCloud Drive to Dropbox
   - Email weekly summary
   - Archive to external drive

**Integration with analytics tools**:
- Export CSV to cloud folder
- Python/R scripts can auto-process
- Generate charts, insights, predictions

---

### Multi-Device Workflow

**iPhone + iPad**:
- Activities sync via CloudKit
- Export from either device
- Files appear in iCloud Drive on both

**iPhone + Mac**:
- Export on iPhone after activity
- Files automatically sync to Mac via iCloud
- Open in Numbers/Excel on Mac for analysis
- Or: AirDrop PDF directly to Mac

---

### Sharing Privacy Tips

**Before sharing**:
- Review location data (home address visible?)
- Check if you want to share weather data
- Consider anonymizing personal food items
- PDF includes everything - no privacy filters yet

**Share selectively**:
- Use CSV for coaches (data only, no formatting)
- Use PDF for public sharing (looks professional)
- Use Text format for quick summaries

---

## Requirements

- **iOS**: 18.0 or later
- **watchOS**: 11.0 or later (Apple Watch Series 5+)
- **iCloud**: Required for automatic exports and sync
- **Mail app**: Required for email export
- **HealthKit**: Required for HealthKit import

---

## Related Guides

- [Activity Tracking Guide](/ios/docs/activity-tracking/) - Learn how to track activities
- [Nutrition Logging Guide](/ios/docs/nutrition-logging/) - Build your food library
- [Shortcuts Guide](/ios/docs/shortcuts/) - Automate exports with Siri

---

**Last Updated**: November 7, 2025

For support or feedback, visit [fuelflow.run](https://fuelflow.run)
