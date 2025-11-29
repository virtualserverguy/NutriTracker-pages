---
layout: page
title: Food Library
permalink: /food-library/
---

# Default Food Library

This is the default food library that FuelFlow can load into your app. The app will fetch this data when you choose to pre-load common ultrarunning foods.

**Last Updated**: October 19, 2025  
**Version**: 1.0.0

---

## Energy Gels

| Food | Carbs (g) | Sodium (mg) | Serving Size |
|------|-----------|-------------|--------------|
| GU Energy Gel | 22 | 55 | 32g packet |
| Maurten Gel 100 | 25 | 37 | 40g packet |
| Spring Energy Gel | 21 | 80 | 44g packet |
| Clif Bloks | 24 | 70 | 3 chews |
| SIS Isotonic Gel | 22 | 49 | 60ml packet |
| UCAN Edge | 15 | 90 | 1 packet |

## Drinks

| Food | Carbs (g) | Sodium (mg) | Serving Size |
|------|-----------|-------------|--------------|
| Tailwind Nutrition | 25 | 303 | 200ml serving |
| Cola | 26 | 15 | 240ml cup |
| Gatorade | 14 | 110 | 240ml cup |
| Ramen Broth | 5 | 800 | 1 cup |
| Pickle Juice | 0 | 690 | 60ml shot |

## Aid Station Foods

| Food | Carbs (g) | Sodium (mg) | Serving Size |
|------|-----------|-------------|--------------|
| Potato (boiled) | 15 | 200 | small potato |
| Pretzels | 22 | 385 | 28g (about 10 pretzels) |
| Banana | 27 | 1 | 1 medium |
| PB&J Quarter | 20 | 150 | 1/4 sandwich |
| Oreo Cookies | 25 | 160 | 3 cookies |
| Watermelon | 11 | 2 | 1 cup cubed |
| Orange Slices | 13 | 0 | 1 orange |
| Avocado Toast Quarter | 15 | 200 | 1/4 slice |
| Honey Stinger Waffle | 21 | 80 | 1 waffle |

---

## Using This Library

When you first launch FuelFlow, you'll be asked if you want to load the default food library. Choosing "Yes" will import all these items into your personal food library. You can then:

- Add your own custom foods
- Edit any of these items to match your preferred brands/amounts
- Delete items you don't use
- Organize items however you like

The app fetches this data from `https://fuelflow.run/data/foods.json`.

---

## For Developers

The JSON endpoint is publicly accessible at:

```
https://fuelflow.run/data/foods.json
```

Response format:
```json
{
  "version": "1.0.0",
  "lastUpdated": "2025-10-19",
  "foods": [
    {
      "name": "GU Energy Gel",
      "carbs": 22,
      "sodium": 55,
      "servingSize": "32g packet",
      "category": "Gel"
    }
  ]
}
```

---

## Suggest Additions

Think we're missing a common ultrarunning food? Email us at [info@fuelflow.run](mailto:info@fuelflow.run) with:

- Food name
- Carbs per serving (grams)
- Sodium per serving (milligrams)  
- Serving size description
- Why it's commonly used in ultras

We regularly update this library based on community feedback.

---

[Back to Home](/){: .btn .btn-secondary}
