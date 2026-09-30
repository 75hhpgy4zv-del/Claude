# Plate Counter

A free calorie counter. Take a photo of your meal, and Claude estimates the calories and macros for each food on the plate. You can adjust portions before adding the meal to your daily log.

Live page: https://claude.ai/artifact/Cbq5bqSMmgiQSqhL7fwa4y (private to the owner)

## How it stays free

The page runs as a claude.ai artifact. Photo and text estimates count against your existing Claude plan's usage, so there's no subscription, API key or per-photo fee. The first estimate in each visit asks you to allow the page to use Claude.

## What it does

- **Snap a plate**: take or pick a photo and add an optional note ("fried in butter"). Claude lists each food with a portion, calories, protein, carbs, fat and a confidence level.
- **Describe it**: type what you ate ("2 eggs, toast with butter") for an estimate without a photo.
- **Quick add**: enter a number you already know, such as one from a label. This works without Claude.
- Change each item's portion (½×, 1×, 1.5×, 2×), edit its calories, or remove it before saving.
- Daily ring for calories left or over, a macro split, meals grouped by breakfast/lunch/dinner/snacks, and a 7-day chart against your goal.

## Storage

When you're signed in to Claude, meals and your goal are saved to the artifact's database under your private per-user path (`data/users/<your id>/…`), so no one else can read them, including anyone you share the page with. Only a 96 px thumbnail of each photo is kept, never the full image. If the page can't reach that database, it saves to browser storage instead.

## Accuracy

Photo-based estimates are usually within about 15–25% of the true value. Hidden fats (oil, butter, dressings) cause the biggest misses, so mention them in the note when you can.

## Editing

`index.html` is the whole app. After editing, republish it to the same artifact URL.
