---
layout: page
title: Privacy Policy
permalink: /privacy/
---

# Privacy Policy

**Last Updated: November 22, 2025**

This Privacy Policy describes how FuelFlow ("we", "our", or "the app") collects, uses, and protects your information when you use our iOS and watchOS application.

---

## Our Commitment to Privacy

Your privacy is critically important to us. FuelFlow is designed with privacy as a core principle. We believe your nutrition and health data belongs to you, and you alone.

**Key Privacy Principles:**
- Your nutrition and activity data stays in your private iCloud account
- By default, we do not collect, store, or have access to your personal data
- Optional third-party integrations may involve temporary data transit through our servers (see "Third-Party Integrations" below)
- No third-party data sharing or selling
- No advertising or tracking
- No analytics collection about your usage

---

## Information We Collect

### Data You Provide
When using FuelFlow, you create and manage the following data:

**Nutrition Data:**
- Food items (name, carbohydrates, sodium content)
- Water intake logs
- Run session data (start time, duration, consumption logs)
- Nutrition goals (hourly targets for carbs, sodium, water)

**Usage Note:** All of this data is stored exclusively in your private iCloud account. FuelFlow does not collect, transmit, or store any of this information on our servers.

### Data We Do NOT Collect
- Personal identification information (name, email, phone number)
- Location data
- Health data beyond what you manually log
- Device information or identifiers
- Usage analytics or statistics
- Crash reports (unless you opt-in through iOS)

---

## How Your Data is Stored

### iCloud Storage
FuelFlow uses Apple's CloudKit framework to store and sync your data. This means:

- Your data is stored in **your private iCloud account**
- Apple encrypts data in transit and at rest
- We (FuelFlow) have **no access** to your iCloud data
- Only devices signed in with your Apple ID can access your data
- Your data is protected by your Apple ID password and device authentication

### Local Storage
Some data is cached locally on your device for offline functionality:
- Recent nutrition logs
- Food library items
- Active run sessions

This local data is stored securely on your device and is not accessible to other apps.

### Optional Integration Services

Some optional features (such as automatic workout import from Garmin Connect) may temporarily route data through FuelFlow servers to deliver it to your device. When you enable these features:

- **Your nutrition data** (food logs, goals, preferences) still stays exclusively in your iCloud
- **Workout data from third-party services** may transit through our servers
- **Data is encrypted** in transit and at rest
- **Data is not stored long-term** - automatically deleted within 24 hours
- **Data is not used** for analytics, advertising, or any purpose other than delivering it to you
- **You control it** - these integrations are entirely optional and can be disconnected anytime

See "Third-Party Integrations" section below for complete details.
---

## How We Use Your Data

**Short answer: We don't.**

Because your data is stored exclusively in your iCloud account, FuelFlow (the developer) never receives, accesses, or uses your data in any way. Your nutrition logs, food library, and run history remain private to you.

The app uses your data locally on your device to:
- Display your nutrition progress
- Calculate hourly consumption rates
- Generate export reports
- Sync between your iPhone and Apple Watch

---

## Data Sharing

**We do not share your data with anyone.** Period.

Your nutrition data is never:
- Sold to third parties
- Shared with advertisers
- Used for marketing purposes
- Transmitted to our servers
- Shared with other users
- Provided to data brokers

### Export Functionality
FuelFlow includes an export feature that allows **you** to share your run reports. This is entirely under your control:
- You choose what to export
- You choose who to share it with
- You initiate the export action
- Exports happen through iOS's native sharing system

---

## Third-Party Integrations

### Apple iCloud (CloudKit)
FuelFlow uses Apple's CloudKit service to sync your data across your devices. Your data is subject to [Apple's Privacy Policy](https://www.apple.com/legal/privacy/).

Key points about iCloud:
- Data is encrypted in transit and at rest
- Apple cannot access the contents of your encrypted data
- You control your iCloud data through your Apple ID settings

### Optional Workout Integrations

FuelFlow offers optional integrations with third-party fitness platforms to help you import workout data. **These integrations are entirely optional** - you can use FuelFlow without ever connecting them.

#### Client-Side Integrations (Zero-Server)

**Apple HealthKit** and **Manual File Import** (FIT, TCX, GPX files):
- All data processing happens on YOUR device
- FuelFlow servers are NOT involved
- Data goes directly from the source to your device to your iCloud
- We cannot access your data

**Example**: When you import a workout from Apple Health:
```
Apple Health → Your iPhone → Your iCloud
(FuelFlow servers never see this data)
```

#### Server-Assisted Integrations (Optional)

**Garmin Connect** (if enabled):
- ⚠️ FuelFlow servers temporarily receive workout data to forward to your device
- ⚠️ We act as a secure bridge between Garmin and your device
- ✅ Data is encrypted in transit and at rest
- ✅ Data is automatically deleted from our servers within 24 hours
- ✅ Data is NOT used for analytics, advertising, or any other purpose
- ✅ You can disconnect at any time

**Example**: When Garmin integration is enabled:
```
Garmin Connect → FuelFlow Bridge → Your iPhone → Your iCloud
                 (temporary transit only, deleted within 24 hours)
```

**Why servers are required**: Garmin's API uses "server-to-server" architecture that requires our servers to receive workout notifications. This is a technical limitation of Garmin's API design.

**What data transits our servers** (for Garmin integration):
- Workout metrics (distance, duration, heart rate, calories, etc.)
- GPS route data (if you choose to import routes)
- Activity types and timestamps

**What we DO NOT receive**:
- Your Garmin password (OAuth authentication only)
- Your nutrition logs, food library, or personal goals from FuelFlow
- Your personal information beyond what's needed for the integration

**Your control**:
- Enable or disable in Settings → Integrations
- See what data was imported and when
- Disconnect anytime (your OAuth tokens and in-transit data are immediately deleted)

#### Comparison Table

| Feature | Client-Side (HealthKit, Files) | Server-Assisted (Garmin) |
|---------|--------------------------------|--------------------------|
| FuelFlow servers involved? | ❌ No | ✅ Yes (temporary) |
| We can see workout data? | ❌ No | ⚠️ Briefly (<24 hours) |
| Long-term storage | Your iCloud only | Your iCloud only |
| Your nutrition data visible? | ❌ No | ❌ No |
| Can disconnect anytime? | ✅ Yes | ✅ Yes |

#### Alternative Options

If you prefer zero-server integrations:
- Use manual FIT file import (Settings → Import → From File)
- Use Apple HealthKit (if Garmin syncs to Apple Health)
- Export from Garmin Connect, import manually

### No Analytics, Advertising, or Tracking

FuelFlow does not integrate with:
- Analytics platforms
- Advertising networks
- Social media platforms
- Marketing or tracking services

Your data is never used for these purposes, regardless of which integrations you enable.

---

## Your Privacy Rights

### Access Your Data
All your data is accessible directly within the FuelFlow app:
- View your food library
- Review past runs
- Export nutrition reports

### Modify Your Data
You have complete control to:
- Add, edit, or delete food items
- Modify run sessions
- Adjust nutrition goals
- Update your food library

### Delete Your Data
You can delete your data at any time:

**Delete Individual Items:**
- Swipe to delete food items in your library
- Delete individual run sessions from your history

**Delete All App Data:**
1. Delete the FuelFlow app from your device
2. Go to Settings > [Your Name] > iCloud > Manage Storage
3. Find FuelFlow and delete its data

**Important:** Deleting the app or its iCloud data is permanent and cannot be undone.

---

## Data Retention

### Active Data
Your data is retained indefinitely in your iCloud account until you choose to delete it. This allows you to:
- Maintain a historical record of your runs
- Reference past nutrition strategies
- Build a comprehensive food library over time

### Deleted Data
When you delete data from FuelFlow:
- It is immediately removed from your device
- It is removed from iCloud within 24 hours
- It is permanently deleted and cannot be recovered

---

## Children's Privacy

FuelFlow is not directed to children under the age of 13 (or the applicable age of consent in your jurisdiction). We do not knowingly collect personal information from children. If you are a parent or guardian and believe your child has provided us with personal information, please contact us at [info@fuelflow.run](mailto:info@fuelflow.run).

Given that FuelFlow stores all data in the user's iCloud account and we have no access to that data, we have no way to identify users by age.

---

## International Users

FuelFlow is available worldwide. If you use FuelFlow outside the United States, please be aware that your data is stored in your iCloud account, which may be processed in any country where Apple operates data centers.

Your use of FuelFlow and the storage of your data in iCloud is subject to Apple's international data transfer practices as described in [Apple's Privacy Policy](https://www.apple.com/legal/privacy/).

---

## Security

### Our Security Measures
While we don't store your data on our servers, we take security seriously in our app design:
- Communication with iCloud uses TLS encryption
- Data is encrypted by Apple's CloudKit
- Local data is protected by iOS sandboxing
- No authentication credentials are stored in the app

### Your Security Responsibilities
To keep your data secure:
- Use a strong Apple ID password
- Enable two-factor authentication on your Apple ID
- Keep your devices updated with the latest iOS/watchOS
- Use a passcode or biometric authentication on your devices
- Don't share your devices with untrusted individuals

---

## Server Security for Optional Integrations

When you enable server-assisted integrations (such as Garmin Connect), we protect data that transits our servers with:

### Encryption
- **In transit**: HTTPS/TLS 1.3 for all communications with third-party services
- **At rest**: AES-256 encryption for any temporary storage (data waiting to be delivered to your device)

### Access Controls
- Minimal employees have access to integration infrastructure
- Access is logged and monitored
- No direct access to user data by support staff

### Data Minimization
- We only receive data necessary for the integration to function
- Data is automatically purged within 24 hours
- No long-term storage or backups

### Monitoring
- Automated alerts for unusual access patterns
- Regular security audits of integration code
- Intrusion detection systems

### Incident Response
If a security breach occurs:
1. We will immediately invalidate all authentication tokens
2. We will notify affected users within 72 hours
3. We will publish a transparent post-mortem
4. Your nutrition data in iCloud remains safe (it was never on our servers)

**Remember**: Server-assisted integrations only handle workout data from third-party services. Your nutrition logs, food library, and FuelFlow settings are always stored exclusively in your iCloud, never on our servers.

---

## Changes to This Privacy Policy

We may update this Privacy Policy from time to time to reflect changes in:
- Our app features
- Legal requirements
- Industry best practices

When we make changes:
- We will update the "Last Updated" date at the top of this policy
- Significant changes will be communicated through the app or our website
- Continued use of FuelFlow after changes constitutes acceptance of the updated policy

We encourage you to review this Privacy Policy periodically to stay informed about how we protect your information.

---

## App Store Privacy Labels

FuelFlow's App Store privacy labels accurately reflect our data practices:

**Data Not Collected:**
FuelFlow does not collect any data that is linked to you or your identity.

**Data Used to Track You:**
FuelFlow does not use data for tracking purposes.

**Data Linked to You:**
None

**Data Not Linked to You:**
None

You can review these labels in FuelFlow's App Store listing.

---

## Cookie Policy

FuelFlow does not use cookies, tracking pixels, or similar technologies. This privacy policy covers our app only, not our website (fuelflow.run), which may use standard web analytics.

---

## Contact Us

If you have questions, concerns, or requests regarding this Privacy Policy or your data privacy, please contact us:

**Email:** [info@fuelflow.run](mailto:info@fuelflow.run)

**Response Time:** We aim to respond to all privacy inquiries within 48 hours.

---

## Legal Information

### Data Controller
Tom Ralph  
FuelFlow  
Email: [info@fuelflow.run](mailto:info@fuelflow.run)

### Governing Law
This Privacy Policy is governed by the laws of the United States and the state where the developer resides, without regard to conflict of law provisions.

### Dispute Resolution
Any disputes relating to this Privacy Policy will be resolved through good faith negotiations. If negotiations fail, disputes may be submitted to binding arbitration in accordance with the laws of the applicable jurisdiction.

---

## Compliance

FuelFlow is designed to comply with:
- California Consumer Privacy Act (CCPA)
- General Data Protection Regulation (GDPR) for EU users
- Children's Online Privacy Protection Act (COPPA)
- Other applicable data protection laws

**For your core FuelFlow data** (nutrition logs, food library, goals): These provisions are handled directly by you through the app interface and your iCloud settings, as we do not collect or store this data on our servers.

**For server-assisted integrations** (such as Garmin Connect): If you enable these optional features, we process workout data as a "data processor" on your behalf. You can exercise your rights by:
- Disconnecting the integration (deletes OAuth tokens and in-transit data immediately)
- Contacting us at [info@fuelflow.run](mailto:info@fuelflow.run) to request data deletion
- Viewing import history in the app to see what data was processed

---

## Your California Privacy Rights

If you are a California resident, you have specific rights under the California Consumer Privacy Act (CCPA):

1. **Right to Know**: You can request information about data collected about you
2. **Right to Delete**: You can request deletion of your personal information
3. **Right to Opt-Out**: You can opt-out of the sale of personal information
4. **Right to Non-Discrimination**: You won't be discriminated against for exercising your rights

**Important:** Because FuelFlow stores all data exclusively in your private iCloud account and we have no access to it, these rights are exercised directly by you through the app and your iCloud settings. We do not sell personal information.

---

## European Users (GDPR)

If you are located in the European Economic Area (EEA), you have rights under the General Data Protection Regulation (GDPR):

1. **Right of Access**: Access your personal data
2. **Right to Rectification**: Correct inaccurate data
3. **Right to Erasure**: Delete your personal data
4. **Right to Restrict Processing**: Limit how data is used
5. **Right to Data Portability**: Receive your data in a portable format
6. **Right to Object**: Object to certain processing activities

**Legal Basis:** FuelFlow processes data based on your consent and our legitimate interests in providing app functionality.

Because your data is stored in your iCloud account, you can exercise these rights directly through the app interface and Apple's iCloud settings.

---

**By using FuelFlow, you acknowledge that you have read and understood this Privacy Policy.**

[Back to Home](/){: .btn .btn-secondary}
