---
layout: page
title: Sync & iCloud Guide
permalink: /ios/docs/sync/
---

# Sync & iCloud Guide - FuelFlow

## Overview

FuelFlow uses **Apple iCloud** to automatically sync your nutrition data across all your devices. Track a workout on your Apple Watch, and instantly see it on your iPhone and iPad. Your entire food library, activity history, and preferences stay perfectly in sync.

**Key Features:**
- Automatic background sync when online
- Offline-first design (track without internet, sync later)
- Instant Apple Watch to iPhone sync via Bluetooth
- Intelligent conflict resolution
- End-to-end encrypted via iCloud
- Works across iPhone, iPad, and Apple Watch

**Requirements:**
- iOS 18.0+ or iPadOS 18.0+
- watchOS 11.0+ (Apple Watch Series 5 or later)
- iCloud account signed in on all devices
- iCloud Drive enabled in Settings

---

## What Data Syncs

FuelFlow syncs everything you need to track nutrition across devices:

### Activity Sessions
- All workout sessions (past and current)
- GPS routes and elevation data
- Heart rate samples
- Weather conditions
- Interval splits and pacing metrics
- Session notes and custom fields

### Nutrition Logs
- Food consumption logs (carbs, sodium, calories)
- Hydration logs (water intake)
- Timestamps and quantities
- Product-specific details

### Food Library
- All food items (gels, drinks, bars, real food)
- Custom foods you create
- Nutritional values (carbs, sodium, calories)
- Food categories and organization
- Favorite foods

### User Preferences
- Default nutrition goals per activity type
- Unit preferences (metric/imperial)
- Activity type customizations
- Display settings
- Sweat profiles (when enabled)

### What Doesn't Sync
- App-specific UI state (selected tabs, scroll position)
- Temporary data (in-progress form inputs)
- Debug logs and diagnostics

---

## How Sync Works

### CloudKit Technology

FuelFlow uses Apple's **CloudKit** framework for secure, automatic syncing:

1. **Offline-First**: All changes are saved locally first, so the app works perfectly without internet
2. **Background Sync**: When online, changes sync automatically in the background
3. **Efficient**: Only changed data is uploaded/downloaded, not entire databases
4. **Encrypted**: All data is end-to-end encrypted using your iCloud account
5. **Reliable**: Built-in retry logic handles temporary network issues

### Automatic vs Manual Sync

**Automatic Sync (Default)**
- Triggers when you make changes (start activity, log food, create custom food)
- Runs in the background every few minutes when app is active
- Happens automatically when you open the app
- No action required from you

**Manual Sync (Force Refresh)**
- Use when you want to pull latest changes immediately
- Helpful if another device made changes you want to see now
- Available in About screen (Debug builds only in current version)

### Sync Architecture

FuelFlow uses a **repository pattern** for data management:

- `SessionRepository` - Manages activity sessions
- `FoodRepository` - Manages food library and categories
- `FavoritesRepository` - Manages favorite foods
- `SweatProfileRepository` - Manages sweat profiles

Each repository handles:
- Local data storage
- CloudKit sync operations
- Conflict detection and resolution
- Data validation

---

## iPhone-to-iPhone Sync

### Setup

1. **Sign in to iCloud** on both iPhones:
   - Settings → [Your Name] → iCloud
   - Ensure iCloud Drive is ON

2. **Install FuelFlow** on both devices

3. **Grant iCloud Permission**:
   - First launch will prompt for iCloud access
   - Tap "Allow" to enable sync

4. **Wait for Initial Sync**:
   - First sync downloads all data from iCloud
   - May take 1-2 minutes if you have lots of activities
   - Look for sync icon in app (when available)

### How It Works

1. Make changes on iPhone A (log food, start activity, etc.)
2. Changes save locally immediately
3. Background sync uploads to iCloud (usually within seconds)
4. iPhone B downloads changes next time it syncs
5. Data appears on iPhone B automatically

**Timeline:**
- **Immediate**: Changes saved locally
- **5-30 seconds**: Upload to iCloud (when online)
- **Variable**: Other devices download changes
  - If app is open: Within 1-2 minutes
  - If app is closed: Next time you open the app

---

## Apple Watch Sync

### Two-Stage Sync Process

Apple Watch uses a **two-stage sync** for maximum reliability:

#### Stage 1: Watch → iPhone (Instant)
- Uses **Bluetooth** via WatchConnectivity framework
- Transfers data directly between devices
- Happens immediately when watch is in range
- No internet required
- Typical speed: 1-3 seconds

#### Stage 2: iPhone → iCloud (Background)
- iPhone uploads watch data to iCloud
- Other devices download from iCloud
- Requires internet connection
- Typical speed: 5-30 seconds

### Watch Sync Scenarios

**Scenario 1: Start Activity on Watch**
1. Tap "Start" on Apple Watch
2. Session syncs to iPhone via Bluetooth instantly
3. iPhone shows Live Activity notification
4. Session uploads to iCloud in background
5. Available on iPad/other iPhones within 1-2 minutes

**Scenario 2: Log Food on Watch**
1. Log gel/water on Apple Watch during workout
2. Logs sync to iPhone immediately
3. iPhone updates Live Activity display
4. Logs upload to iCloud automatically
5. Available on other devices next sync

**Scenario 3: End Activity on Watch**
1. Tap "End" on Apple Watch
2. Final session data syncs to iPhone
3. iPhone processes final metrics (pace, totals, etc.)
4. Complete session uploads to iCloud
5. Appears in History on all devices

### Watch Connectivity Status

**Reachable (Green)**
- Watch and iPhone are connected via Bluetooth
- Instant sync available
- Best experience

**Not Reachable (Amber/Red)**
- Devices not connected (out of range, Bluetooth off, etc.)
- Changes still save locally on each device
- Will sync via iCloud when online
- May see duplicates if you log same thing on both devices

**Tip**: Keep iPhone nearby during workouts for instant sync and Live Activity support.

---

## Setting Up iCloud Sync

### First-Time Setup

1. **Enable iCloud on iPhone**:
   ```
   Settings → [Your Name] → iCloud
   - Sign in with Apple ID if not already
   - Enable "iCloud Drive"
   ```

2. **Enable iCloud on Apple Watch**:
   ```
   Watch app on iPhone → General → iCloud
   - Ensure watch uses same Apple ID
   ```

3. **Install FuelFlow**:
   - Download from App Store
   - Install watch app when prompted

4. **Grant Permissions**:
   - First launch: Tap "Allow" for iCloud access
   - Watch: Accept permissions on first launch

5. **Verify Sync**:
   - Create a test food item on iPhone
   - Wait 30 seconds
   - Check iPad/other devices
   - Should appear automatically

### Troubleshooting Setup

**"FuelFlow would like to use iCloud" not appearing?**
- Go to Settings → FuelFlow → iCloud
- Manually enable iCloud access

**Sync not working after setup?**
- Check iCloud Storage: Settings → [Your Name] → iCloud → Manage Storage
- FuelFlow uses minimal storage (~1-5 MB for most users)
- If storage full, free up space or upgrade plan

---

## Checking Sync Status

### Current Limitations

As of November 2025, FuelFlow does not have a visible sync status indicator in the main UI. Sync happens automatically in the background.

**Coming Soon**: Sync status indicator showing:
- Last sync time
- Sync in progress
- Pending uploads/downloads
- Sync errors

### Debug Builds Only

**About Screen → CloudKit Cache** (Alpha/Beta builds):
- View cached CloudKit records
- Force manual sync
- Clear local cache (advanced)
- See last sync timestamp

### Verifying Sync Manually

**Test Method**:
1. Create unique test item on Device A (e.g., food named "Sync Test [timestamp]")
2. Wait 60 seconds
3. Check Device B for the item
4. If appears: Sync working correctly
5. If doesn't appear: See troubleshooting below

---

## Force Manual Sync

### When to Use

- Just added data on another device and want it NOW
- Suspect data is out of sync
- After resolving network issues
- Before important workout (ensure latest food library)

### How to Force Sync

**Method 1: Restart App** (Works for all users)
1. Quit FuelFlow completely (swipe up in app switcher)
2. Reopen FuelFlow
3. Automatic sync runs on launch

**Method 2: CloudKit Cache** (Debug builds only)
1. Go to Start/History/Progress screen
2. Tap hamburger menu (three lines)
3. Tap "About"
4. Tap "CloudKit Cache" (if available)
5. Tap "Force Sync" button
6. Wait for completion message

**Method 3: Toggle Airplane Mode** (Works for all users)
1. Enable Airplane Mode for 5 seconds
2. Disable Airplane Mode
3. Open FuelFlow
4. Network reconnection triggers sync

### Sync Frequency

FuelFlow syncs automatically:
- **On app launch**: Full sync of all changes
- **After data changes**: Immediate upload of new/modified data
- **Background refresh**: Every 5-10 minutes when app is active
- **Manual triggers**: When you force sync (see above)

---

## Offline Mode

### Works Without Internet

FuelFlow is designed **offline-first**, meaning most features work perfectly without internet:

**Available Offline**:
- Start/end activities
- Log food and water
- Create custom foods
- View activity history
- Edit past sessions
- View nutrition stats
- Use all tracking features
- Apple Watch tracking (syncs via Bluetooth to iPhone)

**Requires Internet**:
- Sync to iCloud (data saved locally until online)
- Weather data for current activity
- Garmin Connect integration (when enabled)
- Export to TrainingPeaks/FinalSurge (when enabled)

### Offline Workflow

1. **Go Offline**: Airplane mode, remote location, no service
2. **Track Normally**: Start activity, log nutrition, end session
3. **Data Saved Locally**: Everything stored on device
4. **Return Online**: Connect to WiFi or cellular
5. **Automatic Sync**: Opens app → background sync runs → uploads to iCloud
6. **Other Devices Get Updates**: Download changes on next sync

**Tip**: FuelFlow queues all changes made offline and uploads them in order when you reconnect. Nothing is lost.

### Airplane Mode Best Practices

**For Flights/Remote Areas**:
1. Download offline maps (if using route tracking)
2. Ensure food library is synced before going offline
3. Track activities as normal
4. Sync when you land/return to service

**Battery Saving**:
- Airplane mode saves significant battery
- Apple Watch can still track via Bluetooth to iPhone
- GPS works in airplane mode
- Just disable cellular/WiFi, keep Bluetooth on

---

## Conflict Resolution

### What Are Conflicts?

**Conflict** = Same data modified on multiple devices before sync completes.

**Example**:
1. You're offline on iPhone and log a gel at 10:00 AM
2. Also offline on Apple Watch, you log the same gel at 10:00 AM
3. Both devices come online and sync
4. FuelFlow detects duplicate logs

### Three-Way Merge Strategy

FuelFlow uses **intelligent conflict resolution** to preserve your data:

**How It Works**:
1. **Detect Conflict**: FuelFlow compares local, server, and incoming changes
2. **Determine Authority**: Uses timestamps and change tags to identify newest version
3. **Merge Data**: Combines all unique logs, preserves all nutrition data
4. **Detect Duplicates**: Flags potentially duplicate logs (same food within 60 seconds)
5. **User Review**: Notifies you of potential duplicates for manual review

### Conflict Detection

**Automatic Detection**:
- FuelFlow scans for food logs with identical:
  - Food item
  - Timestamp (within 60 seconds)
  - Quantity
- Water logs with identical:
  - Timestamp (within 60 seconds)
  - Volume

**Conflict Flags**:
Sessions with potential duplicates are flagged with:
- `hasPotentialDuplicates: true`
- `detectedAt: [timestamp]`
- Shows warning in activity detail view (coming soon)

### Reviewing Conflicts

**When Notified of Duplicates**:
1. Open flagged activity session
2. Review consumption logs
3. Look for duplicates (same item, similar time)
4. Manually delete true duplicates
5. Keep intentional duplicate entries (e.g., two gels at same aid station)

**Example Duplicate**:
```
10:23:15 AM - GU Energy Gel (Vanilla) - 25g carbs
10:23:47 AM - GU Energy Gel (Vanilla) - 25g carbs
```
Likely duplicate (32 seconds apart, same product).

**Example NOT Duplicate**:
```
10:23:15 AM - GU Energy Gel (Vanilla) - 25g carbs
10:52:30 AM - GU Energy Gel (Vanilla) - 25g carbs
```
Intentional (29 minutes apart, probably scheduled fueling).

### Preventing Conflicts

**Best Practices**:
1. **Pick One Device**: Log on iPhone OR Watch, not both
2. **Wait for Sync**: Let current session sync before switching devices
3. **Check Live Activity**: If iPhone shows Live Activity, watch session is synced
4. **Manual Review**: After ending watch sessions, review logs on iPhone

**Common Scenarios**:
- Start activity on watch → Log food on watch only
- Start activity on iPhone → Log food on iPhone only
- If switching devices mid-activity → Wait 30 seconds for sync

---

## Troubleshooting Sync Issues

### Sync Not Working

**Check iCloud Status**:
1. Go to Settings → [Your Name] → iCloud
2. Ensure iCloud Drive is ON
3. Check storage: Must have available space (even 1 MB is enough)
4. Verify signed in with same Apple ID on all devices

**Check Network**:
1. Ensure WiFi or cellular data is working
2. Open Safari, load a webpage to verify internet
3. Disable VPN if using one (CloudKit may be blocked)
4. Try different network (switch WiFi to cellular or vice versa)

**Restart Devices**:
1. Force quit FuelFlow on all devices
2. Restart iPhone: Hold Power + Volume Down → Slide to power off
3. Restart Apple Watch: Hold side button → Power Off
4. Reopen FuelFlow

**Reset Sync** (Advanced - Debug builds):
1. Go to About → CloudKit Cache
2. Tap "Clear Cache" (WARNING: Re-downloads all data from iCloud)
3. Force quit app
4. Reopen app
5. Wait 2-3 minutes for full sync

### Duplicate Sessions Appearing

**Cause**: Session created offline on multiple devices, synced separately.

**Solution**:
1. Open History screen
2. Find duplicate sessions (same time, activity, distance)
3. Compare nutrition logs:
   - If logs are identical: Delete one session completely
   - If logs differ: Merge logs manually, then delete duplicate
4. Keep the session with most complete data (GPS route, heart rate, etc.)

**Prevention**: Always check if session already exists before creating new one on second device.

### Missing Activities

**Check Filters**:
1. History screen may be filtered (by activity type, date range)
2. Tap "All Activities" to remove filters
3. Scroll down to load older sessions (lazy loading)

**Check Other Devices**:
1. Session may have been deleted on another device
2. Check Recently Deleted (if feature exists)
3. Check iCloud.com (not supported for FuelFlow currently)

**Force Sync**:
1. Quit and reopen app
2. Wait 2 minutes for full sync
3. Pull to refresh on History screen (if supported)

### Watch Not Syncing

**Check Bluetooth**:
1. iPhone Settings → Bluetooth → Ensure ON
2. Watch should show "Connected" in Watch app
3. Bring watch close to iPhone (within 10 feet)

**Check Watch App Installation**:
1. Open Watch app on iPhone
2. Scroll to FuelFlow
3. Ensure "Show App on Apple Watch" is ON
4. Re-install watch app if needed

**Verify WatchConnectivity**:
1. Start activity on watch
2. Check iPhone for Live Activity notification
3. If appears: Connectivity working
4. If doesn't appear: Restart both devices

**Manual Sync Fallback**:
- If Bluetooth fails, watch syncs via iCloud when online
- Connect watch to WiFi: Settings → WiFi on watch
- Wait 2-3 minutes for iCloud sync
- Check iPhone History for session

### Food Library Not Syncing

**Symptom**: Custom food created on iPhone missing on iPad.

**Solution**:
1. Force sync on device with missing food (restart app)
2. Wait 60 seconds
3. Check again
4. If still missing: Re-create food on problem device
5. Report issue (see below)

**Known Issue**: Very large food libraries (500+ items) may sync slowly on first install. Be patient.

### Sync Stuck "In Progress"

**Symptom**: Sync indicator shows "Syncing..." for 5+ minutes.

**Solution**:
1. Check internet connection (visit website in Safari)
2. Force quit FuelFlow
3. Wait 30 seconds
4. Reopen FuelFlow
5. If still stuck after 10 minutes: Restart device

**Advanced** (Debug builds):
1. About → CloudKit Cache
2. Check pending records count
3. If 100+ pending: May take time, be patient
4. If 0 pending but still "Syncing": Bug, report to support

### "iCloud Account Error"

**Message**: "Unable to access iCloud. Please sign in to iCloud in Settings."

**Solution**:
1. Go to Settings → [Your Name]
2. If "Sign in to iPhone" appears: Sign in with Apple ID
3. If already signed in: Sign out and sign back in
4. Go to Settings → [Your Name] → iCloud
5. Enable "iCloud Drive"
6. Restart FuelFlow

### Reporting Sync Issues

If sync issues persist after troubleshooting:

1. **Collect Information**:
   - Which devices are affected
   - What data isn't syncing (sessions, foods, etc.)
   - When issue started
   - Recent changes (new device, iOS update, etc.)

2. **Check System Status**:
   - Visit https://www.apple.com/support/systemstatus/
   - Look for iCloud issues (rare but possible)

3. **Contact Support**:
   - Email: support@fuelflow.run
   - Include: Device models, iOS versions, description
   - Screenshots of error messages

4. **Debug Logs** (If requested by support):
   - Alpha/Beta builds have enhanced logging
   - Support may ask for specific diagnostics

---

## Privacy and Data Security

### What Data Is Stored

**In iCloud (Encrypted)**:
- Activity session metadata (dates, durations, activity types)
- GPS routes and elevation data
- Nutrition logs (food consumed, water intake)
- Food library (names, nutritional values)
- User preferences (goals, units, favorites)

**NOT Stored Anywhere**:
- Your personal health data (unless you export to HealthKit)
- Payment information (handled by App Store)
- Location history outside of activities
- Device identifiers
- Usage analytics (unless you opt-in)

### Encryption

**End-to-End Encryption**:
- All FuelFlow data stored in iCloud is encrypted
- Uses your iCloud account's encryption keys
- Apple cannot read your FuelFlow data
- Only devices signed in with your Apple ID can decrypt

**In Transit**:
- All sync traffic uses HTTPS (TLS 1.3)
- CloudKit enforces encrypted connections
- No data sent over unencrypted channels

### Data Retention

**Active Data**:
- Stored indefinitely in your iCloud account
- Counts against iCloud storage quota (minimal: 1-5 MB typical)
- Remains until you delete it

**Deleted Data**:
- Removed from all devices on next sync
- Purged from CloudKit servers
- No backup or recovery after deletion (permanent)

**Account Deletion**:
- Delete FuelFlow from all devices
- Uninstall app
- Data remains in iCloud for 30 days (Apple policy)
- After 30 days: Automatically purged

### Third-Party Access

**Zero Third-Party Access**:
- FuelFlow does NOT share data with third parties
- No analytics companies
- No advertising networks
- No data brokers

**Optional Integrations** (User-initiated only):
- **HealthKit**: You choose what to export
- **Garmin Connect**: Opt-in, your credentials stored securely in keychain
- **TrainingPeaks/FinalSurge**: Opt-in, API tokens stored securely

### Privacy Controls

**What You Control**:
- Enable/disable iCloud sync (Settings → iCloud → FuelFlow)
- Delete individual activities or food items anytime
- Export your data (CSV, JSON, GPX, etc.)
- Disable integrations (HealthKit, Garmin, etc.)

**What FuelFlow Cannot Do**:
- Access your data without your iCloud credentials
- Share your data with others (no social features)
- Track your location outside of active sessions
- See your data (end-to-end encrypted via iCloud)

### Compliance

**Apple Policies**:
- Follows Apple App Store privacy guidelines
- Uses only Apple-sanctioned frameworks (CloudKit, HealthKit)
- No hidden data collection

**GDPR** (European users):
- Right to access: Export all data via app
- Right to deletion: Delete app and data
- Right to portability: Standard export formats (CSV, JSON, GPX)

---

## Sync Best Practices

### General Tips

1. **Keep Devices Updated**:
   - Use latest iOS/watchOS versions
   - Update FuelFlow regularly
   - Automatic updates recommended

2. **Maintain iCloud Storage**:
   - Check storage monthly: Settings → [Your Name] → iCloud
   - FuelFlow uses minimal space, but full storage blocks all sync
   - Consider iCloud+ if under 1 GB free

3. **Single Device for Active Session**:
   - Start/log/end on same device when possible
   - Reduces conflict chances
   - Cleaner data

4. **Sync Before Big Events**:
   - Day before race: Force sync all devices
   - Ensure latest food library available
   - Verify goals are current

5. **Review After Watch Sessions**:
   - After ending watch workout, open iPhone
   - Review nutrition logs for accuracy
   - Check for duplicates
   - Edit/annotate while fresh in mind

### Advanced Tips

**For Frequent Travelers**:
- Download food library before going offline
- Use airplane mode to save battery
- Sync when you reach WiFi (hotel, airport, etc.)

**For Multi-Device Users** (iPhone + iPad + Watch):
- Designate primary device for food library management
- Use iPhone for active tracking
- Use iPad for post-workout analysis/exports
- Avoid simultaneous edits on multiple devices

**For Privacy-Conscious Users**:
- Disable iCloud sync if preferred (app still works locally)
- Export data regularly for backup (CSV/JSON)
- Use on-device only mode (no internet connection)

**For Beta Testers**:
- Use CloudKit Cache diagnostics
- Report sync issues early
- Test sync before major workouts
- Keep backup device with stable build

---

## Additional Resources

### Related Guides
- [Activity Tracking Guide](https://fuelflow.run/ios/docs/activity-tracking/) - Start, track, and end activities
- [Nutrition Logging Guide](https://fuelflow.run/ios/docs/nutrition-logging/) - Log food and water
- [Shortcuts Integration Guide](https://fuelflow.run/ios/docs/shortcuts/) - Siri voice commands

### Support
- **Email**: support@fuelflow.run
- **Website**: https://fuelflow.run
- **Feature Requests**: support@fuelflow.run

### Technical Details
For developers interested in FuelFlow's sync architecture:
- Uses CloudKit CKSyncEngine (iOS 17+)
- Repository pattern with SessionRepository, FoodRepository, etc.
- Three-way merge conflict resolution
- WatchConnectivity for direct iPhone-Watch sync
- Offline-first with optimistic UI updates

---

**Last Updated**: November 7, 2025
**Version**: FuelFlow iOS 2.0
**Applies To**: iOS 18.0+, watchOS 11.0+

---

*Questions about sync? Email support@fuelflow.run*
