---
layout: page
title: Activity Tracking & GPS Guide
permalink: /ios/docs/activity-tracking/
---

# Activity Tracking & GPS Guide

Master FuelFlow's activity tracking features for real-time nutrition monitoring during runs, rides, and endurance activities.

---

## Overview

FuelFlow tracks your activities with:
- **GPS route mapping** with elevation profiles
- **Heart rate monitoring** (from Apple Watch or Bluetooth sensors)
- **Real-time nutrition tracking** (carbs, sodium, water)
- **Live Activity** on your Lock Screen (iOS 16+)
- **Automatic HealthKit sync**

---

## Starting an Activity

### On iPhone

1. Open FuelFlow
2. Tap **Start Activity** (+ button)
3. Choose your **sport type**:
   - Run (Road, Trail, Track)
   - Cycle (Road, Mountain, Gravel)
   - Swim
   - Hike
   - Triathlon
   - Other endurance sports
4. Set your **nutrition goals**:
   - **Carbs**: 30-150g/hour (see [Nutrition Goals](#nutrition-goals))
   - **Sodium**: 300-3000mg/hour
   - **Water**: 400ml-1L+/hour
5. Optional: Set **route details**:
   - Distance estimate
   - Expected duration
   - Surface type (road, trail, track)
6. Tap **Start**

**GPS tracking begins immediately.**

### On Apple Watch

1. Open FuelFlow on your watch
2. Tap **Start Activity**
3. Rotate **Digital Crown** to select sport
4. Adjust **nutrition goals** with Digital Crown
5. Tap **Start**

The activity **instantly syncs to your iPhone** via Bluetooth - no internet required!

---

## During Your Activity

### Live Metrics

FuelFlow displays real-time stats:

**Nutrition Progress**:
- Carbs consumed vs. goal (per hour)
- Sodium intake vs. goal (per hour)
- Water intake vs. goal (per hour)
- **Color-coded indicators**:
  - 🟢 Green: On target (80-120% of goal)
  - 🟡 Yellow: Slightly off (60-80% or 120-150%)
  - 🔴 Red: Needs attention (<60% or >150%)

**Activity Metrics**:
- Elapsed time
- Distance (GPS-based)
- Current pace/speed
- Heart rate (if available)
- Elevation gain

### Lock Screen Live Activity (iOS 16+)

Your nutrition stats appear on your Lock Screen:
- Glanceable progress bars
- Current carbs/sodium/water intake
- Elapsed time and distance
- **Dynamic Island** (iPhone 14 Pro+): Tap to expand full stats

**Enable**: Settings → Optional Features → Live Activity

---

## GPS & Route Tracking

### How GPS Works

FuelFlow uses your iPhone's GPS to:
- Track your route on a map
- Calculate distance and pace
- Record elevation changes
- Create shareable route maps

**Accuracy depends on**:
- Clear view of sky (trees/buildings reduce accuracy)
- GPS signal strength
- Device location (phone in pocket/armband works best)

### Granting Location Permission

**First Time**:
1. FuelFlow will ask for location access
2. Choose **"While Using the App"**

**To Check/Change**:
- Settings → Privacy & Security → Location Services → FuelFlow
- Recommended: **"While Using"** (saves battery vs "Always")

**Tip**: You don't need "Always" permission - FuelFlow only tracks while the activity is active.

### Viewing Your Route

**During Activity**:
- iPhone: Swipe to Map tab
- Watch: Not available (battery saving)

**After Activity**:
- Activity Detail screen → Route Map
- Shows your path with nutrition log markers
- Elevation profile with climb/descent totals

### Troubleshooting GPS

**No route data / "GPS unavailable"**:
- Check location permission (Settings → FuelFlow)
- Ensure you're outdoors with clear sky view
- Give GPS 30-60 seconds to acquire signal at start
- Indoor activities (treadmill/trainer) won't have route data

**Inaccurate distance**:
- Poor GPS signal (buildings, dense trees)
- Watch left on charger (using iPhone GPS only)
- Calibrate by running a known distance

---

## Heart Rate Monitoring

### Supported Devices

FuelFlow reads heart rate from:
- **Apple Watch** (automatic, if worn)
- **Bluetooth HR monitors** (chest straps, armbands)
- **HealthKit-compatible devices**

### Viewing Heart Rate

**During Activity**:
- iPhone: Main stats screen
- Watch: Raise wrist to see current HR
- Live Activity: Swipe for HR widget (if available)

**After Activity**:
- Activity Detail → Heart Rate graph
- Average HR, Max HR, Time in zones

### HR Zone Tracking

FuelFlow calculates time spent in heart rate zones:
- **Zone 1**: Recovery (<60% max HR)
- **Zone 2**: Aerobic (60-70% max HR)
- **Zone 3**: Tempo (70-80% max HR)
- **Zone 4**: Threshold (80-90% max HR)
- **Zone 5**: Max effort (>90% max HR)

**Set your max HR**:
- Settings → Profile → Max Heart Rate
- Default: 220 - (your age)
- Or use measured max from recent hard effort

---

## Nutrition Goals

### Understanding Hourly Goals

FuelFlow displays nutrition **per hour**, not total for the activity. This helps you:
- Maintain consistent fueling rate
- Avoid under/over-fueling as duration increases
- Adjust intake based on intensity

### Recommended Ranges

**Carbohydrates (Energy)**:
- Light effort: 30-40g/hour
- Moderate effort: 40-60g/hour
- Hard effort: 60-90g/hour
- **Ultra endurance**: 90-150g/hour (trained gut required)

**Sodium (Electrolytes)**:
- Light effort: 300-500mg/hour
- Moderate effort: 500-800mg/hour
- Hard effort: 800-1500mg/hour
- **Heavy sweaters/heat**: 1500-3000mg/hour

**Water (Hydration)**:
- Cool conditions: 400-600ml/hour
- Moderate conditions: 600-800ml/hour
- Warm conditions: 800ml-1L/hour
- **Hot/humid**: 1L+/hour

**Important**: Most athletes absorb 800-1000ml/hour max. Match your sweat rate without over-drinking.

### Setting Default Goals

**Per-Sport Defaults**:
1. Activity tab → Menu (☰) → **Default Goals**
2. Choose sport type
3. Set carbs, sodium, water goals
4. These apply automatically when starting that sport

**Example**:
- Long runs: 60g carbs, 800mg sodium, 800ml water
- Easy rides: 40g carbs, 500mg sodium, 500ml water

---

## Activity Types & Customization

### Available Sports

FuelFlow supports 20+ activity types:
- **Run**: Road, Trail, Track, Treadmill
- **Cycle**: Road, Mountain, Gravel, Indoor
- **Swim**: Pool, Open Water
- **Triathlon**
- **Hike**
- **Ski/Snowboard**
- **Row**
- **Walk**
- **Other**

### Managing Activity Types

**Enable/Disable Sports**:
1. Activity tab → Menu (☰) → **Manage Activities**
2. Toggle sports on/off
3. Disabled sports don't appear in start menu

**Reorder Sports**:
- Drag to rearrange
- Your most-used sports appear first

**Set Watch Default**:
- Choose the sport that appears first on Apple Watch
- Quick start without scrolling

---

## Logging Nutrition During Activity

### Quick Logging

**From iPhone**:
1. Tap **Log Food** or **Log Water**
2. Select item from library or enter custom
3. Confirm

**From Apple Watch**:
1. Tap food item from quick list
2. Or tap **Water** → Choose amount
3. Done (syncs to iPhone instantly)

**Tip**: Add frequently-used items to Favorites for faster access.

### Logging at Specific Times

Each nutrition log is timestamped. You'll see:
- "30 minutes" - Logged 30 min into activity
- "1:15" - Logged at 1 hour 15 minutes

This helps you:
- Review fueling strategy post-activity
- See nutrition markers on route map
- Analyze what worked (or didn't)

---

## Ending an Activity

### How to End

**iPhone**:
- Tap **End Activity** button
- Or: Swipe down → End Activity

**Apple Watch**:
- Swipe right → **End**
- Or: Force Touch → **End Activity**

**Confirmation**:
- Review session summary
- Save or Discard

### What Happens When You End

1. **GPS tracking stops**
2. **Final stats calculated** (distance, pace, HR)
3. **Route map generated** (if GPS data available)
4. **Activity saved** to History
5. **HealthKit sync** (if enabled)
6. **iCloud sync** (to all your devices)

### Celebration Screen

After saving, you'll see:
- Total distance and time
- Nutrition consumed (carbs, sodium, water)
- % of goals achieved
- Quick share option

---

## Live Activity Features (iOS 16+)

### What is Live Activity?

Live Activity shows your nutrition stats on:
- **Lock Screen** - Always visible when locked
- **Dynamic Island** (iPhone 14 Pro+) - Tap to expand
- **StandBy Mode** (iOS 17+) - Full-screen when charging

### What You See

**Compact (Lock Screen)**:
- Current carbs, sodium, water (compact)
- Elapsed time
- Tap to open app

**Expanded (Dynamic Island)**:
- Full progress bars with percentages
- Distance and pace
- Heart rate (if available)

**Minimal (Dynamic Island - Ongoing)**:
- Tiny fuel/water icons
- Activity time

### Enabling/Disabling

**To Enable**:
1. Settings → Optional Features
2. Toggle **Live Activity** ON

**To Disable Mid-Activity**:
- Long-press Live Activity → **End**
- Or: Disable in Settings

**Note**: Live Activity auto-ends when you end the session.

---

## Offline & Airplane Mode

### What Works Offline

✅ **Full GPS tracking**
✅ **Nutrition logging**
✅ **Apple Watch sync** (Bluetooth only)
✅ **Heart rate monitoring**
✅ **Route recording**
✅ **All calculations**

### What Requires Internet

❌ Weather data (uses last-known if offline)
❌ iCloud sync (waits until online)
❌ Map tile downloads (shows blank map)

**Tip**: FuelFlow is designed for offline use. Perfect for trail runs and remote rides!

---

## HealthKit Integration

### What Syncs to Apple Health

FuelFlow automatically logs:
- **Workouts** (activity type, duration, distance)
- **Active Energy** (calories burned)
- **Heart Rate** (avg, min, max)
- **Route** (GPS data as workout route)
- **Nutrition data** (carbs, sodium, water) *(optional)*

### Enabling HealthKit Sync

1. Settings → Optional Features → **HealthKit Integration**
2. Grant permissions when prompted
3. Choose what to sync

**Privacy**: You control what FuelFlow writes to Health app.

### Importing from HealthKit

**Import Past Workouts**:
1. Activity tab → Menu (☰) → **Import from HealthKit**
2. Select workout(s) to import
3. FuelFlow creates activity with route/HR data
4. Add nutrition logs retroactively

---

## Advanced Features

### Intervals & Laps

**Auto Lap Detection** (from FIT file imports):
- FuelFlow preserves lap markers
- View splits in Activity Detail

**Manual Intervals** (future feature):
- Planned: Manual lap button during activity
- View nutrition per interval

### Multi-Sport Activities (Triathlon)

**Triathlon Mode** (future feature):
- Currently: Log as single "Triathlon" activity
- Planned: Separate swim/bike/run segments with transitions

### Pause/Resume (future feature)

Currently: Activity runs continuously until you end it
Planned: Pause button to stop GPS/timer temporarily

---

## Troubleshooting

### Activity Won't Start

**Check**:
- Location permission granted
- Not already in active session (end previous first)
- iPhone not in Low Power Mode (limits GPS)

### GPS Track is Jagged/Inaccurate

**Causes**:
- Poor GPS signal (buildings, trees)
- Phone in bag/deep pocket
- Watch left behind

**Fix**:
- Keep phone/watch on you
- Give GPS 30-60s to lock signal before starting
- Avoid starting indoors

### Heart Rate Not Showing

**Check**:
- Apple Watch worn snugly on wrist
- Or Bluetooth HR sensor paired and charged
- HealthKit permission granted

### Watch and iPhone Out of Sync

**If watch shows activity but iPhone doesn't**:
1. Ensure Bluetooth enabled on both
2. Keep devices close together (< 10 meters)
3. If still stuck: End on watch, should sync within seconds

**Persistent sync issues**:
- Settings → iCloud → Force Sync
- Or: Restart both devices

### Battery Drain During Long Activities

**Tips to Extend Battery**:
- Lower screen brightness
- Disable Live Activity
- Use Airplane Mode (GPS still works!)
- Carry portable charger for ultra events

---

## Tips & Best Practices

### Before Your Activity

1. **Charge devices** (phone >50%, watch >30%)
2. **Check location permission** (should be "While Using")
3. **Load food library** with today's fuel
4. **Set realistic goals** based on effort/conditions

### During Your Activity

1. **Log as you consume** (don't wait until end)
2. **Glance at Live Activity** instead of unlocking phone
3. **Trust your gut** over strict goal adherence
4. **Use voice logging** (Shortcuts) when hands are full

### After Your Activity

1. **Review nutrition timing** on route map
2. **Note what worked** (add to favorites)
3. **Adjust default goals** based on learnings
4. **Sync to HealthKit** for complete training log

---

## Related Guides

- [Nutrition Logging & Food Library](/ios/docs/nutrition-logging/) - Manage your fuel database
- [Apple Watch Guide](/docs/apple-watch/) - Watch-specific features
- [Shortcuts Integration](/ios/docs/shortcuts/) - Hands-free voice control
- [Export & Sharing](/ios/docs/export/) - Save and share your data
- [Sync & iCloud](/ios/docs/sync/) - Keep data across devices

---

## Feedback & Support

Questions or issues?
- Email: [support@fuelflow.run](mailto:support@fuelflow.run)
- In-app: Settings → Help & Support

---

**Last Updated**: November 7, 2025
**App Version**: 1.0+
**Requirements**: iOS 18.0+, watchOS 11.0+ (Apple Watch Series 5 or later)

---

*Track smarter, fuel better! 🏃‍♂️⚡*
