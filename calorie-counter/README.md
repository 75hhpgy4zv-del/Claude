# Plate Counter

A free calorie tracker. Photograph a meal and Claude estimates calories and macros for each food on the plate. Adjust anything that looks off, log it, and follow your history and trends over time.

Live page: https://claude.ai/artifact/Cbq5bqSMmgiQSqhL7fwa4y (private to the owner)

## How it stays free

The page runs as a claude.ai artifact. Photo and text estimates count against your existing Claude plan's usage, so there's no subscription, API key or per-photo fee. The first estimate in each visit asks you to allow the page to use Claude.

## Screens

The tabs are Home, Recipes, Plan and Progress. Settings opens from the gear on Home.

- **Home**: week strip with a progress ring for each day, calories left, protein/carbs/fats left, and the day's meals with photos and macros.
- **Progress**: current weight and progress toward your goal weight, day streak, a daily calorie chart (7/30/90 days) with a goal line, a weight trend chart (30 days, 90 days, 1 year or all), average macros against your goals, and lifetime totals.
- **Calendar** (inside Progress): month view where each day's ring fills toward your goal and turns red when you went over. Tap a day to see its meals.
- **Recipes**: saved recipes with a photo, calories and protein per serving, searchable by name, tag or ingredient.
- **Plan**: a week at a time. Add saved recipes or custom items (like a dinner out) to any day, see planned calories against your goal, and log a planned meal with one tap. Planned meals for the day also show on Home.
- **Settings**: calorie and macro goals (with a 30/40/30 split helper), lb or kg, goal weight.

## Recipes

Tap **Import** on the Recipes tab (or **+** › Import recipe):

- **Paste text**: copy the caption from an Instagram or TikTok post, or a recipe from a website or your notes.
- **Screenshots**: add one or more screenshots of the caption and ingredient list, for example from a multi-slide post.

The page can't open Instagram links itself, because artifact pages can't reach other websites. You can still save the link with the recipe and open the original from there.

Claude pulls out the title, servings, time, ingredients and steps, and estimates calories and macros for every ingredient. You can then edit the name, servings, time and photo, change any ingredient's calories, remove ingredients, or add ingredients (their calories are estimated automatically). From a saved recipe you can log any number of servings, add it to a day in your plan, edit it or delete it.

## Grocery list

On the Plan tab, **Groceries** combines the week's planned recipes into one list, scaled to your planned servings and grouped by store section. Check items off as you shop. If you change the plan, the list offers to rebuild.

## Logging

Tap **+**:

- **Scan food**: take or pick a photo and add an optional note. Review each ingredient, change portions (½× to 2×), adjust servings, or tap **Fix results** to tell Claude what it got wrong and get a revised estimate.
- **Describe food**: type what you ate.
- **Quick add**: enter calories and macros you already know. This works without Claude.
- **Log weight**: record a weigh-in for any date.

If you close the sheet while a photo is being analyzed, the result waits on the home screen. Tap any logged meal to see its details, delete it, or log it again today.

## Storage

When you're signed in to Claude, everything is saved to the artifact's database under your private per-user path (`data/users/<your id>/…`). No one else can read it, including anyone you share the page with. Meals, weigh-ins, recipes, plan entries, grocery lists and photos (meal photos resized to 360 px, recipe photos to 480 px) are stored in separate collections. If the page can't reach that database, it saves to browser storage instead.

## Accuracy

Photo-based estimates are usually within about 15–25% of the true value. Hidden fats (oil, butter, dressings) cause the biggest misses, so mention them in the note or use **Fix results**.

## Editing

`index.html` is the whole app. After editing, republish it to the same artifact URL.
