---
layout: page
title: Sync & Data Management
permalink: /docs/sync-and-data/
---

# Sync & Data Management

FuelFlow uses a sophisticated dual-sync system to keep your data synchronized across your iPhone and Apple Watch. This guide explains how it works, what happens in different scenarios, and how to manage your data.

## The Dual-Sync Architecture

FuelFlow uses **two independent sync methods** that work together seamlessly:

### 1. Instant Local Sync (Primary)

**Technology:** WatchConnectivity framework (Apple's native iPhone-Watch communication)

**Speed:** Less than 1 second

**Connection:** Bluetooth or WiFi Direct

**Internet required:** No

**Range:** Typical Bluetooth range (about 10 meters / 30 feet)

**When it works:**
- Both devices are powered on
- Bluetooth is enabled on both devices
- Devices are within range
- Apps are installed on both devices

**What syncs:**
- Starting a new session
- Ending a session
- Logging food
- Logging water
- Session updates
- Library changes

### 2. CloudKit Sync (Backup)

**Technology:** Apple's CloudKit framework

**Speed:** 2-10 seconds (varies with network)

**Connection:** Internet (WiFi or Cellular)

**Internet required:** Yes

**Range:** Unlimited (anywhere with internet)

**When it works:**
- Device has internet connection
- Signed into iCloud
- iCloud Drive enabled

**What syncs:**
- All sessions
- Complete food library
- Settings and preferences
- Historical data

## How the Dual-Sync System Works

The beauty of FuelFlow's sync is that **you don't have to think about it**. The app intelligently chooses the best method:

### Scenario 1: Devices Together (Most Common)

**Situation:** You're out for a run with your Apple Watch. Your iPhone is in your pocket or armband.

**What happens:**
1. You log a gel on your Apple Watch
2. **Instant sync** sends data to iPhone via Bluetooth
3. iPhone receives data in < 1 second
4. iPhone display updates immediately
5. **CloudKit** syncs in background (backup)

**Why it's great:** Instant feedback, works offline (airplane mode + Bluetooth), no internet data used.

### Scenario 2: Devices Apart

**Situation:** You're on a run with just your Apple Watch. iPhone is at home.

**What happens:**
1. You log nutrition on your Watch
2. Data is saved locally on Watch
3. When you get home and Watch reconnects to iPhone:
   - **Instant sync** transfers data immediately
   - Or **CloudKit sync** transfers when Watch gets WiFi
4. iPhone updates with all your logs

**Why it's great:** Never lose data, syncs automatically when devices reunite.

### Scenario 3: Offline Everywhere

**Situation:** You're in an area with no internet and devices are apart.

**What happens:**
1. Each device stores data locally
2. When either device gets internet:
   - **CloudKit sync** synchronizes all changes
3. When devices reconnect:
   - **Instant sync** ensures perfect synchronization

**Why it's great:** Keep logging even without connectivity. Everything syncs when possible.

### Scenario 4: Cellular Apple Watch

**Situation:** You have cellular Apple Watch and left iPhone at home.

**What happens:**
1. You log nutrition on Watch during your run
2. Watch uses cellular to sync via **CloudKit**
3. iPhone at home receives CloudKit sync
4. Data appears on iPhone automatically

**Why it's great:** Complete independence while still staying in sync.

## What Data Is Synchronized

### Always Synced

**Sessions:**
- All active and past sessions
- Session start/end times
- Activity types
- Nutrition goals
- All logs (food and water)
- Timestamps

**Food Library:**
- All food items
- Names, carbs, sodium
- Categories
- Custom entries

**Settings:**
- Notification preferences
- Units (metric/imperial)
- Display preferences

### Device-Specific (Not Synced)

**iPhone:**
- Lock Screen Live Activity state
- App-specific UI state
- Notification badges

**Apple Watch:**
- Watch complication settings
- Watch face configurations
- Haptic feedback preferences

## Understanding Sync Status

### Status Indicators

**iPhone:**
- **Green checkmark (✓):** All data synced successfully
- **Syncing (↻):** Sync in progress
- **Cloud (☁):** CloudKit sync active
- **Warning (⚠):** Sync issue (see troubleshooting)

**Apple Watch:**
- **Checkmark (✓):** Synced with iPhone
- **Syncing (↻):** Sync in progress
- **Cloud (☁):** Using CloudKit

### Where to Check Sync Status

**iPhone:**
- Settings tab → iCloud Sync status
- Pull down on any screen to see sync indicator

**Apple Watch:**
- Force touch on main screen
- Check sync status

## Data Privacy & Security

### End-to-End Encryption

All data synced via CloudKit is **end-to-end encrypted**:
- Apple cannot read your data
- Data is encrypted on device before upload
- Only your devices can decrypt the data
- Secure in transit and at rest

### Local Sync Security

Instant sync via Bluetooth:
- Uses Apple's WatchConnectivity framework
- Encrypted by iOS/watchOS automatically
- Requires devices to be paired (secure pairing process)
- Data never leaves your personal device network

### What Data Does FuelFlow Store?

**On Apple's Servers (CloudKit):**
- Your sessions (encrypted)
- Your food library (encrypted)
- Your settings (encrypted)

**Not stored anywhere:**
- No account information (uses iCloud)
- No personal data beyond what you enter
- No tracking or analytics data
- No sharing with third parties

### Data Ownership

**You own all your data:**
- Export anytime (Settings → Export Data)
- Delete anytime (Settings → Delete All Data)
- Data deleted from CloudKit when you delete locally

## Managing Your Data

### Exporting Data

**Why export?**
- Backup your sessions
- Share with coaches
- Analyze in spreadsheets
- Archive for long-term records

**How to export:**
1. Open FuelFlow on iPhone
2. Go to **Settings** tab
3. Tap **Export Data**
4. Choose format:
   - **CSV** - Spreadsheet compatible
   - **JSON** - Raw data format
5. Select date range:
   - Last 30 days
   - Last 90 days
   - All time
   - Custom range
6. Tap **Export**
7. Share via:
   - Email
   - Files app
   - iCloud Drive
   - AirDrop

**What's included:**
- All sessions in selected range
- Complete nutrition logs
- Timestamps and duration
- Calculated statistics

### Deleting Data

**Delete individual sessions:**
1. History tab
2. Swipe left on session
3. Tap **Delete**
4. Confirm

**Delete all data:**
1. Settings tab
2. **Delete All Data** (at bottom)
3. Enter confirmation
4. All data removed from device and CloudKit

**Note:** Deletions sync across devices. This is permanent.

### Storage Usage

**iCloud Storage:**
- Typical usage: 1-10 MB
- Even with years of data: < 50 MB
- Very minimal impact on iCloud storage

**Device Storage:**
- iPhone: 10-20 MB (app + data)
- Apple Watch: 5-10 MB

## Troubleshooting Sync Issues

### "Data not syncing between devices"

**Check 1: Bluetooth (for Instant Sync)**
- Settings → Bluetooth → On (both devices)
- Bring devices close together
- Restart Bluetooth if needed

**Check 2: iCloud (for CloudKit Sync)**
- Settings → [Your Name] → iCloud
- Ensure iCloud Drive is ON
- Check available iCloud storage
- Ensure FuelFlow has iCloud permission

**Check 3: Internet Connection**
- CloudKit requires internet
- WiFi or cellular data
- Check connection speed

**Check 4: App Versions**
- Ensure both devices have latest FuelFlow version
- Update from App Store if needed

### "Sync stuck at 'Syncing...'"

**Fixes:**
1. **Force quit** FuelFlow on both devices
2. **Reopen** the app
3. Wait 30 seconds for sync to complete
4. If still stuck, check internet connection
5. Try toggling Airplane mode on/off

### "Session started on iPhone not appearing on Watch"

**Immediate fix:**
1. Open FuelFlow on Apple Watch
2. Pull down to refresh
3. Session should appear

**If not working:**
1. Check Bluetooth is enabled
2. Force quit and reopen Watch app
3. Wait for CloudKit sync (few seconds with internet)

### "Duplicate sessions appearing"

**Rare but possible causes:**
- Editing same session on both devices simultaneously
- Sync conflict during poor connectivity

**Fix:**
1. Keep the correct session
2. Delete the duplicate
3. Deletion syncs to other device

**Prevention:** Avoid editing same session on both devices at same time

### "Lost data after device died"

**Don't worry:**
- Data is saved locally even without sync
- When device charges and turns on:
  - CloudKit syncs automatically
  - All data recovers
- May take a few minutes to fully sync

### "Changed food item, changes not syncing"

**Expected behavior:**
- Changes to food items sync via CloudKit
- May take 5-10 seconds
- Pull down to refresh if needed

**If not syncing:**
1. Check iCloud connection
2. Wait 30 seconds
3. Force quit and reopen app

## Sync in Different Scenarios

### Airplane Mode

**Bluetooth ON, WiFi OFF, Cellular OFF:**
- ✅ Instant local sync works
- ❌ CloudKit sync not available
- Data syncs when airplane mode disabled

**Use case:** Flying to a race, tracking nutrition on plane

### Ultra-Distance Events

**Long events with spotty connectivity:**
- Both devices store data locally
- Instant sync when devices reconnect
- CloudKit syncs when internet available
- No data loss regardless of connectivity

### International Travel

**Cellular data disabled, WiFi only:**
- Instant sync via Bluetooth always works
- CloudKit syncs when connected to WiFi
- Use airplane mode + Bluetooth to preserve battery

### Device Upgrade

**Getting new iPhone or Apple Watch:**
1. Sign into iCloud on new device
2. Install FuelFlow
3. CloudKit automatically syncs all data
4. Complete history and library restored

### Using Multiple Devices

**Example: iPhone, iPad, Apple Watch:**
- All devices sync via CloudKit
- Instant sync works between iPhone and Watch
- iPad syncs via CloudKit only
- All devices stay synchronized

## Advanced Data Topics

### Conflict Resolution

**What happens if you edit same session on both devices?**
- FuelFlow uses "last write wins"
- Most recent change is kept
- Very rare in practice (sessions typically edited on one device)

### Sync Frequency

**Instant Sync:**
- Happens immediately when you make a change
- < 1 second latency
- Event-driven (not polling)

**CloudKit Sync:**
- Automatic background sync
- Triggered by changes
- Also syncs every few minutes as backup
- Efficient - only syncs changes

### Offline Queueing

**Multiple changes while offline:**
- All changes queued locally
- When connectivity restored:
  - All changes sync in order
  - Maintains correct timestamps
  - Preserves data integrity

## Best Practices

### For Reliable Sync

1. **Keep Bluetooth enabled** - Allows instant sync
2. **Stay signed into iCloud** - Ensures CloudKit backup
3. **Keep apps updated** - Latest sync improvements
4. **Charge devices** - Low battery can pause background sync
5. **Don't force quit** - Let apps sync in background

### For Long Events

1. **Start with full battery** - Both devices
2. **Enable airplane mode + Bluetooth** - Saves battery, keeps instant sync
3. **Trust the sync** - Don't worry about connectivity during event
4. **Review after finish** - All data will be synchronized

### For Data Safety

1. **Regular exports** - Backup important sessions
2. **Keep iCloud enabled** - Automatic cloud backup
3. **Don't delete iCloud data** - Unless you're sure
4. **Update devices** - Latest sync reliability improvements

## Related Guides

- [Getting Started](/docs/getting-started/) - Setup and basics
- [iPhone App Guide](/docs/iphone-app/) - iPhone features
- [Apple Watch Guide](/docs/apple-watch/) - Watch features
- [FAQ](/faq/) - Common questions

## Need Help?

**Email:** support@fuelflow.run
**Website:** [fuelflow.run](https://fuelflow.run)

---

**Your data is always safe, always synchronized, and always accessible.** FuelFlow's dual-sync system ensures you never lose a single nutrition log, no matter what happens.
