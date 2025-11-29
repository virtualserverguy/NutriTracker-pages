# FuelFlow Documentation Roadmap

**Last Updated**: November 7, 2025
**Status**: Planning Document

---

## ✅ Completed Documentation

### Phase 1 - Core User Guides (5 guides - COMPLETE)

1. **Shortcuts Integration** (`/ios/docs/shortcuts.md`) - ✅ Published
   - 25+ App Intents with examples
   - Voice command reference
   - Product-specific shortcut creation
   - Advanced automation workflows
   - Troubleshooting

2. **Activity Tracking & GPS** (`/ios/docs/activity-tracking.md`) - ✅ Published
   - GPS route mapping & elevation
   - Heart rate monitoring
   - Live Activity features
   - Nutrition goal recommendations
   - Multi-sport activity management

3. **Nutrition Logging & Food Library** (`/ios/docs/nutrition-logging.md`) - ✅ Published
   - Food library management
   - Logging strategies (short/long/ultra)
   - Favorites system
   - Voice logging integration
   - Real-world examples by sport

4. **Export & Sharing** (`/ios/docs/export.md`) - ✅ Published
   - CSV & PDF export formats
   - Importing FIT/GPX/TCX files
   - HealthKit export integration
   - Sharing workflows
   - Privacy & data ownership

5. **Sync & iCloud** (`/ios/docs/sync.md`) - ✅ Published
   - CloudKit sync architecture
   - iPhone/Watch/iPad sync
   - Offline mode capabilities
   - Conflict resolution
   - Troubleshooting

---

## 📋 Planned Documentation

### Phase 2 - Essential User Guides (HIGH PRIORITY)

#### 1. HealthKit Integration Guide
**File**: `/pub/ios/docs/healthkit.md`
**Estimated Length**: 400-500 lines
**Priority**: HIGH
**Reason**: Frequently asked about, critical for training log integration

**Contents**:
- Overview of HealthKit integration
- What FuelFlow writes to Health app:
  - Workouts (activity type, duration, distance)
  - Active Energy (calories)
  - Heart Rate (avg, min, max)
  - Route data (GPS)
  - Nutrition data (carbs, sodium, water) - optional
- Granting permissions step-by-step
- Importing workouts from HealthKit
  - Past workout import flow
  - Selecting workouts to import
  - What data transfers
- Managing HealthKit permissions
  - Revoking/changing permissions
  - Privacy implications
  - What Apple can/cannot see
- Troubleshooting:
  - "HealthKit not syncing"
  - Missing workouts
  - Duplicate workouts
  - Permission errors
- Use cases:
  - Centralized training log
  - Third-party app integration (Strava, Garmin Connect)
  - Health metrics analysis

---

#### 2. Privacy & Data Guide
**File**: `/pub/ios/docs/privacy.md`
**Estimated Length**: 400-500 lines
**Priority**: HIGH
**Reason**: App Store requirement, user trust, GDPR compliance

**Contents**:
- What data FuelFlow collects:
  - Activity sessions (GPS, HR, duration, nutrition)
  - Food library (personal database)
  - User preferences (units, goals)
  - Device info (for debugging)
  - Analytics (opt-in only)
- Where data is stored:
  - iCloud CloudKit (encrypted)
  - Local device (encrypted at rest)
  - No third-party servers
- What FuelFlow does NOT collect:
  - Contacts, messages, photos
  - Other apps' data
  - Browsing history
  - Financial information
- How to control your data:
  - Analytics opt-out (Settings → Privacy & Analytics)
  - Deleting activities
  - Clearing food library
  - Full data export
  - Account deletion
- Privacy & third parties:
  - Apple's role (CloudKit provider only)
  - No data sold to advertisers
  - No tracking across apps/websites
- GDPR & compliance:
  - Right to access data (export feature)
  - Right to deletion
  - Data portability (CSV/PDF export)
  - EU user protections
- Security measures:
  - End-to-end encryption (CloudKit)
  - Two-factor authentication (Apple ID)
  - No password storage (uses Apple ID)

---

#### 3. Update Existing: Getting Started Guide
**File**: `/pub/docs/getting-started.md` (UPDATE EXISTING)
**Estimated Work**: 2-3 hours
**Priority**: MEDIUM-HIGH
**Reason**: Currently references iOS 17/watchOS 10, needs iOS 18 update

**Updates Needed**:
- Change requirements to iOS 18.0+, watchOS 11.0+
- Update Apple Watch to Series 5 or later
- Update screenshots/references to new UI (if changed)
- Add link to new iOS docs: `/ios/docs/`
- Update fuelflow.app → fuelflow.run
- Add note about Live Activity (iOS 16+ feature)
- Update sync section to reference new `/ios/docs/sync/`

---

### Phase 3 - Feature Deep Dives (MEDIUM PRIORITY)

#### 4. Live Activity Deep Dive
**File**: `/pub/ios/docs/live-activity.md`
**Estimated Length**: 350-400 lines
**Priority**: MEDIUM
**Reason**: Cool iOS 16+ feature, good for marketing

**Contents**:
- What is Live Activity?
  - Lock Screen widgets
  - Dynamic Island (iPhone 14 Pro+)
  - StandBy Mode (iOS 17+)
- How it works in FuelFlow:
  - Auto-starts with activity
  - Shows real-time nutrition progress
  - Updates without unlocking phone
- Display modes:
  - Compact (Lock Screen)
  - Expanded (Dynamic Island tap)
  - Minimal (ongoing indicator)
  - StandBy (full-screen when charging)
- Customization options:
  - Enable/disable (Settings → Optional Features)
  - What data shows (carbs, sodium, water, HR)
  - Update frequency
- Tips & tricks:
  - Long-press to end activity
  - Tap to open full app
  - StandBy Mode for indoor training
- Troubleshooting:
  - Live Activity not appearing
  - Stuck/not updating
  - Battery impact
- Device compatibility:
  - Lock Screen: iPhone with iOS 16+
  - Dynamic Island: iPhone 14 Pro, 15 Pro, 16 Pro
  - StandBy: iPhone with iOS 17+

---

#### 5. Heart Rate Zones & Training
**File**: `/pub/ios/docs/heart-rate-zones.md`
**Estimated Length**: 400-450 lines
**Priority**: MEDIUM
**Reason**: Training optimization, popular feature request

**Contents**:
- Understanding heart rate zones:
  - Zone 1: Recovery (<60% max HR)
  - Zone 2: Aerobic (60-70%)
  - Zone 3: Tempo (70-80%)
  - Zone 4: Threshold (80-90%)
  - Zone 5: Max effort (>90%)
- Setting your max heart rate:
  - Age-based formula (220 - age)
  - Measured max (field test)
  - Lab-tested max
- Viewing HR data during activity:
  - Current HR
  - Average HR
  - Max HR
  - Time in zones
- Post-activity analysis:
  - HR graph over time
  - Zone distribution
  - HR vs. pace correlation
- Training strategies:
  - Zone 2 base building
  - Zone 4 threshold work
  - Recovery monitoring
- Supported devices:
  - Apple Watch
  - Bluetooth HR monitors (chest straps, armbands)
  - HealthKit-compatible devices
- Troubleshooting:
  - HR not showing
  - Inaccurate readings
  - Watch fit/placement

---

### Phase 4 - Specialized Topics (LOW PRIORITY)

#### 6. Multi-Sport & Triathlon Guide
**File**: `/pub/ios/docs/triathlon.md`
**Estimated Length**: 300-350 lines
**Priority**: LOW (future feature)
**Reason**: Currently single-activity tracking, plan for multi-sport mode

**Contents** (when feature available):
- Triathlon mode overview
- Swim → Bike → Run segments
- Transition tracking
- Nutrition strategy per segment
- Equipment changes
- Race day checklist

---

#### 7. Race Day Preparation
**File**: `/pub/ios/docs/race-day.md`
**Estimated Length**: 300-350 lines
**Priority**: LOW
**Reason**: Nice-to-have, could be blog post instead

**Contents**:
- Week before:
  - Test nutrition products
  - Set up food library
  - Create race-specific shortcuts
- Day before:
  - Charge all devices
  - Download offline maps (future)
  - Review goal pacing
- Morning of:
  - Pre-race checklist
  - Device setup
  - Nutrition plan review
- During race:
  - Pacing strategy
  - Aid station planning
  - When to check stats (vs. stay focused)
- After race:
  - Save and export data
  - Review performance
  - Post-race analysis

---

#### 8. Consolidated Troubleshooting Guide
**File**: `/pub/ios/docs/troubleshooting.md`
**Estimated Length**: 500-600 lines
**Priority**: LOW (content exists in individual guides)
**Reason**: Consolidate all troubleshooting sections from other guides

**Contents**:
- GPS & Location Issues
- Heart Rate Problems
- Sync Issues (iCloud, Watch, HealthKit)
- Export Errors
- Food Library Not Syncing
- Live Activity Not Working
- Shortcuts/Siri Issues
- Battery Drain
- App Crashes
- Data Recovery

---

### Phase 5 - Beta/Alpha Features (DOCUMENT WHEN RELEASED)

#### 9. Sweat Profiles Guide (Alpha Only)
**File**: `/pub/ios/docs/sweat-profiles.md`
**Estimated Length**: 450-500 lines
**Priority**: ALPHA ONLY (behind feature flag)
**Flag**: `AppConfiguration.enableSweatPredictions`
**Reason**: Alpha feature, limited availability

**Contents**:
- What are sweat profiles?
- Creating your first profile:
  - Weigh-in before activity
  - Record fluid consumed
  - Weigh-in after activity
- Understanding sweat rate:
  - Liters per hour
  - Environmental factors (temp, humidity)
  - Intensity impact
- Sodium concentration:
  - Light/moderate/heavy sweater
  - Heat acclimation
- Personalized recommendations:
  - Hydration goals
  - Sodium goals
  - Adjustment by conditions
- Building accurate profiles:
  - Multiple sessions needed
  - Different conditions
  - Sport-specific rates
- Troubleshooting:
  - Inaccurate predictions
  - Missing data

---

#### 10. Third-Party Integrations (Future)
**File**: `/pub/ios/docs/integrations.md`
**Priority**: FUTURE (not yet implemented)

**Contents** (when available):
- Garmin Connect (Alpha)
- TrainingPeaks Export (Alpha)
- FinalSurge Export (Alpha)
- Strava integration
- Wahoo/Zwift integration

---

## 📊 Documentation Metrics

### Current Status
- **Published**: 5 comprehensive guides (2,912 lines)
- **Planned High Priority**: 3 guides (~1,200-1,500 lines)
- **Planned Medium Priority**: 2 guides (~750-850 lines)
- **Planned Low Priority**: 3 guides (~1,100-1,350 lines)
- **Future/Beta**: 2 guides (~950-1,000 lines)

### Coverage
- ✅ **Core Features**: 100% covered
- ✅ **Advanced Features**: 80% covered (Shortcuts, Export, Sync)
- 🟡 **Integration**: 60% covered (HealthKit needs dedicated guide)
- 🟡 **Troubleshooting**: 70% covered (distributed across guides)
- 🔴 **Privacy/Security**: 40% covered (needs dedicated guide)

---

## 🎯 Recommended Next Steps

### Immediate (Next Release)
1. **Create HealthKit Integration Guide** - User demand, App Store importance
2. **Create Privacy & Data Guide** - Compliance, trust building
3. **Update getting-started.md** - iOS 18 requirements

### Short Term (Within 2-3 months)
4. **Create Live Activity Deep Dive** - Marketing value, iOS 18 showcase
5. **Create Heart Rate Zones Guide** - Training optimization, popular request

### Long Term (6+ months or when features ship)
6. **Multi-Sport Guide** - When triathlon mode implemented
7. **Sweat Profiles Guide** - When leaving Alpha
8. **Third-Party Integrations** - When public APIs launched

---

## 📝 Documentation Standards

All new docs should follow:
- **Jekyll format** with proper YAML front matter
- **Requirements**: iOS 18.0+, watchOS 11.0+, Apple Watch Series 5+
- **Domain**: fuelflow.run (not fuelflow.app)
- **Tone**: Professional, helpful, concise
- **Examples**: Practical, real-world scenarios
- **Cross-links**: Reference related guides
- **Last Updated**: Date stamp at bottom
- **Support**: Link to support@fuelflow.run

---

## 🔗 Related Files

- **In-App Help**: `/FuelFlow/Help/ContextualHelpButton.swift` (short summaries)
- **Help Topics Proposal**: `/docs/HELP_TOPICS_PROPOSAL.md` (48 proposed topics)
- **Help Architecture**: `/docs/HELP_SYSTEM_ARCHITECTURE.md` (technical design)
- **Shortcuts Guide Source**: `/docs/SHORTCUTS_INTEGRATION.md` (3,500+ word original)

---

**Maintained By**: Development Team
**Review Frequency**: Quarterly (or when major features ship)
**Contact**: support@fuelflow.run
