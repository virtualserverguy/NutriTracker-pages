---
layout: page
title: Shortcuts Integration Guide
permalink: /ios/docs/shortcuts/
---

# Shortcuts Integration - FuelFlow

## Overview

FuelFlow now supports **Apple Shortcuts** and **Siri voice commands**, enabling hands-free activity tracking and automation workflows. Control your nutrition tracking without touching your phone during workouts.

**Availability**: iOS 16.0+
**Status**: Beta Feature (requires opt-in)

---

## 🎯 What You Can Do

### Voice Commands

Use Siri to control FuelFlow completely hands-free:

- **"Start my workout in FuelFlow"** - Begin tracking with your last settings
- **"End my workout in FuelFlow"** - Stop current activity
- **"Log a gel in FuelFlow"** - Quick log a standard energy gel
- **"Log water in FuelFlow"** - Track hydration (500ml bottle)
- **"Check my activity status in FuelFlow"** - Get nutrition progress update

### Quick Actions

13 pre-configured shortcuts available:
1. **Quick Start** - Resume with last activity settings
2. **End Activity** - Stop current session
3. **Start Run** - Begin run with default goals
4. **Start Bike** - Begin bike ride with default goals
5. **Log Gel** - Log standard gel (25g carbs, 100mg sodium)
6. **Log Water** - Log water bottle (0.5L)
7. **Smart Start** - Time/weather-aware goal adjustments
8. **Resume Last** - Repeat your most recent workout
9. **Activity Status** - Check current progress
10. **Weekly Stats** - This week's totals
11. **Monthly Stats** - This month's totals
12. **Export** - Save last activity (text/CSV/JSON)

### Advanced Automations

Build custom workflows with these intents:

#### Activity Management
- Start activity with custom nutrition goals
- End and auto-export completed activities
- Get real-time session status
- Query recent activities

#### Nutrition Tracking
- Log specific food items from your library
- Log favorite foods
- Log custom nutrition values
- Batch log multiple items (e.g., "2 gels + 1L water")
- Log standard portions (gel, water bottle, water cup)

#### Food Library
- Add new food items
- Toggle favorites
- Query food library
- Delete food items

#### Statistics & History
- All-time totals (activities, distance, duration, nutrition)
- Weekly summaries
- Monthly summaries
- Recent activities list
- Personal records

#### Export
- Export to text, CSV, or JSON
- Save to iCloud Drive automatically
- Integration with Files app

---

## 🚀 Getting Started

### 1. Enable Shortcuts Integration

1. Open FuelFlow
2. Go to **Settings** (gear icon)
3. Tap **Optional Features**
4. Enable **"Shortcuts Integration"**

### 2. Add Shortcuts to Siri

**Method A: From Shortcuts App**
1. Open **Shortcuts** app
2. Go to **Gallery** tab
3. Search "FuelFlow"
4. Tap a shortcut → **Add Shortcut**
5. Tap ⓘ → **Add to Siri** → Record custom phrase

**Method B: From Settings**
1. Open **Settings** → **Siri & Search**
2. Tap **All Shortcuts**
3. Find FuelFlow shortcuts
4. Tap **+** → Record custom phrase

### 3. Creating Product-Specific Shortcuts

**You can create shortcuts for YOUR specific nutrition products!**

Instead of generic "log a gel", create:
- **"Log a SiS Beta Fuel"** → Your specific gel
- **"Log a Maurten 320"** → Your drink mix
- **"Log a Honey Stinger"** → Your favorite flavor
- **"Track my GU"** → Your race day gel
- **"Log Tailwind"** → Your hydration mix

**How to Create**:

1. **Add Product to Food Library**
   - FuelFlow → Food Library → Add Food
   - Name: "SiS Beta Fuel"
   - Carbs: 40g, Sodium: 200mg
   - Category: Gel

2. **Create Custom Shortcut**
   - Open Shortcuts app
   - Tap **+** (new shortcut)
   - Add Action → Search "FuelFlow"
   - Choose "Log Fuel"
   - Tap "Food Item" → Select "SiS Beta Fuel"
   - Tap ⓘ → Rename to "Log SiS Beta Fuel"

3. **Add to Siri**
   - Tap shortcut → ⓘ → "Add to Siri"
   - Record: "Log a SiS Beta Fuel"
   - Done!

Now say: **"Hey Siri, log a SiS Beta Fuel"** 🎉

**Pro Tip**: Create one for each product you commonly use:
- Race day gel
- Training gel
- Hydration mix
- Recovery drink
- Energy chews

### 4. Suggested Voice Phrases

#### Starting Activities
- "Start my long run"
- "Begin my workout"
- "I'm going for a ride"

#### Logging Nutrition (Generic)
- "Log fuel"
- "I just had a gel"
- "Track my water"

#### Logging Specific Products (After Creating Custom Shortcuts)
- "Log a SiS Beta Fuel"
- "Log a Maurten 320"
- "Log my race gel"
- "Track my Tailwind"
- "Log a Honey Stinger"

#### Getting Updates
- "How's my nutrition?"
- "Check my progress"
- "What are my stats?"

#### Ending Activities
- "Done running"
- "Finish workout"
- "End my activity"

---

## 📱 Usage Examples

### Example 1: Long Run Workflow

**Shortcut**: "Start Long Run"
```
1. Smart Start Activity (Run)
   → Adjusts goals based on weekend/time of day
2. Wait 30 minutes
3. Send notification "Time for first gel!"
```

**During Run (Voice)**:
- "Hey Siri, log a gel" (every 30-40 min)
- "Hey Siri, log water" (at aid stations)
- "Hey Siri, check my activity status" (progress update)

**After Run (Automatic)**:
- End activity → Auto-export to iCloud/TrainingPeaks

### Example 2: Quick Fuel Check

**Shortcut**: "Fuel Status"
```
Get Session Status
→ Show notification with:
  - Duration
  - Carbs: 45g / 60g (75%)
  - Sodium: 400mg / 500mg (80%)
  - Water: 0.8L / 1.0L (80%)
```

### Example 3: Post-Run Stats

**Shortcut**: "This Week's Training"
```
Get Weekly Stats
→ Show notification:
  - 5 activities
  - 65km total
  - 8 hours
  - 720g carbs consumed
```

### Example 4: Aid Station Quick Log

**Shortcut**: "Aid Station"
```
1. Log Energy Gel
2. Log Water Bottle (0.5L)
→ Batch logged in <2 seconds
```

---

## 🔧 Advanced Automation Ideas

### Location-Based Triggers

**When arriving at running trail**:
1. Ask to start activity
2. Set notification reminder for first gel at 30 min
3. Enable "Keep Screen On"

**When leaving gym**:
1. Prompt to end activity
2. Export to TrainingPeaks
3. Log recovery drink

### Time-Based Triggers

**Every Saturday 7:00 AM** (long run day):
1. Smart Start Run (weekend goals)
2. Open FuelFlow
3. Start Live Activity

**After workout ends**:
1. Wait 5 minutes
2. Ask "How do you feel?" → Log RPE
3. Export session
4. Send summary to coach via email

### Apple Watch Integration

**Watch Face Complication**:
- Tap to quick start activity
- Show current session time
- Display nutrition progress

### Focus Mode Integration

**"Workout" Focus**:
- Auto-start last activity type
- Silence non-urgent notifications
- Keep FuelFlow on screen

---

## 🎨 Control Center Widget (iOS 18+)

Add quick toggle to Control Center:
1. Settings → Control Center
2. Add **"FuelFlow Activity"** widget
3. Tap to start/stop activity with last settings

Shows:
- ○ Start (when inactive)
- ● Active (during workout)

---

## 🧪 Smart Features

### Time-of-Day Adjustments

**Morning Runs (5am-9am)**:
- 10% lower water goal (less heat/sweat)
- Standard carb/sodium goals

**Afternoon/Evening (12pm-6pm)**:
- 20% higher water goal (heat/sweat)
- 10% higher sodium goal (electrolyte loss)

### Weekend Detection

**Weekend Long Runs**:
- 10% higher carb goal (longer duration)
- 10% higher sodium goal (extended effort)
- Suggested by Smart Start intent

### History-Based Defaults

**Resume Last Activity**:
- Uses exact goals from previous session
- Repeats activity type
- Perfect for consistent training routines

---

## 📊 Shortcut Return Values

For building custom automations:

### Get Session Status Returns:
```json
{
  "isActive": true,
  "activityType": "Run",
  "durationMinutes": 87,
  "carbsConsumed": 75,
  "carbsGoal": 90,
  "sodiumConsumed": 450,
  "sodiumGoal": 500,
  "waterConsumed": 1.2,
  "waterGoal": 1.5
}
```

### Get Statistics Returns:
```json
{
  "totalActivities": 42,
  "totalDistance": 387.5,
  "totalDuration": 151200,
  "totalCarbs": 4200,
  "totalSodium": 32000,
  "totalWater": 45.5
}
```

Use these values in conditional logic, notifications, or charts.

---

## 🔐 Privacy & Permissions

### What Shortcuts Can Access:
✅ Start/stop activities
✅ Log nutrition data
✅ View activity history
✅ Query statistics
✅ Export your data

### What Shortcuts CANNOT Access:
❌ Other apps' data
❌ Contacts or messages
❌ Location (except what you manually log)
❌ Photos or camera
❌ Microphone (except Siri voice)

**All data stays local** to FuelFlow and iCloud (if you use CloudKit sync).

---

## 🐛 Troubleshooting

### "No Active Session" Error
**Cause**: Trying to log nutrition without starting an activity
**Fix**: Run "Quick Start" or "Start Run" shortcut first

### "Feature Disabled" Error
**Cause**: Shortcuts Integration is turned off
**Fix**: Settings → Optional Features → Enable "Shortcuts Integration"

### Siri Doesn't Recognize Commands
**Cause**: Shortcut not added to Siri
**Fix**: Open Shortcuts app → Tap shortcut → ⓘ → Add to Siri

### Shortcut Runs But Nothing Happens
**Cause**: FuelFlow may be terminating in background
**Fix**:
1. Settings → FuelFlow → Background App Refresh (ON)
2. Or set shortcut to open FuelFlow first

### "Session Already Active" Error
**Cause**: Can't start new activity while one is running
**Fix**: End current activity first

---

## 💡 Tips & Best Practices

1. **Create Activity-Specific Shortcuts**
   - "Saturday Long Run" with higher goals
   - "Easy Recovery Run" with lower goals
   - "Race Day" with max goals

2. **Combine with Reminders**
   - Set recurring reminders to trigger shortcuts
   - "Every 30 minutes during workout → Log fuel"

3. **Use Notification Actions**
   - Shortcuts can show interactive notifications
   - Tap to log gel/water without opening app

4. **Build Morning Routine**
   - Check last week's stats while coffee brews
   - Review personal records
   - Set up for today's workout

5. **Post-Workout Automation**
   - Auto-export to cloud storage
   - Send summary to training log
   - Log in workout journal

6. **Share with Training Partners**
   - Export shortcuts to share workflows
   - Standardize team logging practices

---

## 📚 Technical Details

### Supported Intent Types

**Core Intents**:
- `StartActivityIntent` - Begin tracking
- `EndActivityIntent` - Stop tracking
- `GetSessionStatusIntent` - Query progress
- `LogFuelIntent` - Log food/gel/drink
- `LogWaterIntent` - Log hydration
- `ExportSessionIntent` - Save data

**Food Library**:
- `AddFoodItemIntent`
- `ToggleFavoriteFoodIntent`
- `DeleteFoodItemIntent`
- `GetFoodLibraryIntent`
- `GetFavoriteFoodsIntent`

**Statistics**:
- `GetStatisticsIntent`
- `GetWeeklyStatsIntent`
- `GetMonthlyStatsIntent`
- `GetRecentActivitiesIntent`

**Automations**:
- `PreWorkoutRoutineIntent`
- `PostWorkoutRoutineIntent`
- `SmartStartActivityIntent`
- `ResumeLastActivityIntent`
- `BatchLogNutritionIntent`

**Quick Actions**:
- `QuickStartActivityIntent`
- `StartRunIntent`
- `StartBikeIntent`
- `LogGelIntent`
- `LogWaterBottleIntent`
- `LogWaterCupIntent`
- `LogFavoriteFuelIntent`
- `LogCustomFuelIntent`

### App Shortcuts

13 suggested phrases automatically appear in:
- Siri suggestions
- Spotlight search
- Shortcuts app Gallery
- Long-press app icon

No setup required - just enable the feature!

---

## 🎓 Learning Resources

### Apple Documentation
- [Intro to Shortcuts](https://support.apple.com/guide/shortcuts/welcome)
- [Use Siri with Shortcuts](https://support.apple.com/guide/shortcuts/run-shortcuts-with-siri-apd5ba077760)
- [Automate Shortcuts](https://support.apple.com/guide/shortcuts/run-shortcuts-based-on-time-or-location-apd602971e63)

### Community Shortcuts
Visit [r/shortcuts](https://reddit.com/r/shortcuts) to:
- Share your FuelFlow automations
- Get inspiration from others
- Request custom shortcuts

---

## 🚧 Known Limitations

1. **Export formats limited** - Share Sheet/Email require opening app
2. **Background execution** - iOS may terminate app after 30s
3. **Live Activity control** - Cannot start/stop Live Activity via shortcuts
4. **Weather integration** - Cannot trigger weather-based adjustments
5. **HealthKit sync** - Must sync manually, not automatic via shortcuts

These may be addressed in future updates.

---

## 🔮 Coming Soon

Planned enhancements:
- Focus Filter integration (show/hide activities by type)
- Weather-aware goal suggestions
- Training plan integration
- Coach sharing shortcuts
- Real-time pacing alerts
- Race day automation workflows

---

## 📝 Feedback

Found a bug or have a feature request?
1. Open FuelFlow
2. Settings → Help & Support
3. "Report Issue" or "Request Feature"

Or email: [support@fuelflow.run](mailto:support@fuelflow.run)

---

## 📄 Version History

### v1.0 (2025-11-06)
- Initial release
- 25+ intents supported
- 13 suggested shortcuts
- Smart time/day adjustments
- Comprehensive statistics queries
- Full export support

---

**Last Updated**: November 6, 2025
**Feature Status**: Beta
**Minimum iOS**: 16.0
**Requires**: FuelFlow with APP_INTENTS_ENABLED build

---

*Happy training! 🏃‍♂️💨*
