# Plate Counter

A free calorie tracker. Photograph a meal and Claude estimates calories and macros for each food on the plate. Adjust anything that looks off, log it, and follow your history and trends over time.

Live page: https://claude.ai/artifact/Cbq5bqSMmgiQSqhL7fwa4y (private to the owner)

## How it stays free

The page runs as a claude.ai artifact. Photo and text estimates count against your existing Claude plan's usage, so there's no subscription, API key or per-photo fee. The first estimate in each visit asks you to allow the page to use Claude.

## Screens

The tabs are Home, Recipes, Plan, Hero and Progress. Settings opens from the gear on Home.

- **Home**: your hero's level and gold, a week strip with a progress ring for each day, calories left, protein/carbs/fats left, steps and exercise, a water counter, today's quests, a one-tap row of favorites and usuals, meals planned for the day, and the day's logged meals with photos and macros.
- **Progress**: a weekly check-in from Claude, current weight and progress toward your goal weight, day streak, a daily calorie chart (7/30/90 days) with a goal line, a weight trend chart (30 days, 90 days, 1 year or all), average macros against your goals, and lifetime totals.
- **Calendar** (inside Progress): month view where each day's ring fills toward your goal and turns red when you went over. Tap a day to see its meals.
- **Recipes**: saved recipes with a photo, calories and protein per serving, searchable by name, tag or ingredient.
- **Plan**: a week at a time. Add saved recipes or custom items (like a dinner out) to any day, see planned calories against your goal, and log a planned meal with one tap. **Plan my week** has Claude fill the days and meals you pick from your saved recipes, aiming for your calorie and protein goals; you review the plan before it's added. Planned meals for the day also show on Home.
- **Hero**: your character sheet, weekly boss, quests, achievements and the gold shop (see below).
- **Settings**: calorie and macro goals (with a 30/40/30 split helper), daily water goal, step and exercise goals, whether burned calories add to your food budget, lb or kg, goal weight.

## Recipes

Tap **Import** on the Recipes tab (or **+** › Import recipe):

- **Paste text**: copy the caption from an Instagram or TikTok post, or a recipe from a website or your notes.
- **Screenshots**: add one or more screenshots of the caption and ingredient list, for example from a multi-slide post.

The page can't open Instagram links itself, because artifact pages can't reach other websites. You can still save the link with the recipe and open the original from there.

Claude pulls out the title, servings, time, ingredients and steps, and estimates calories and macros for every ingredient. You can then edit the name, servings, time and photo, change any ingredient's calories, remove ingredients, or add ingredients (their calories are estimated automatically). From a saved recipe you can log any number of servings, add it to a day in your plan, edit it or delete it.

**Make it lighter** on a saved recipe asks Claude for a version with fewer calories, more protein, lower carbs or less sugar. It keeps the dish recognizable, recalculates every ingredient, summarizes the swaps, and saves as a new recipe next to the original.

## Grocery list

On the Plan tab, **Groceries** combines the week's planned recipes into one list, scaled to your planned servings and grouped by store section. Check items off as you shop. If you change the plan, the list offers to rebuild.

## Logging

Tap **+**:

- **Scan food**: take or pick a photo and add an optional note. Review each ingredient, change portions (½× to 2×), adjust servings, or tap **Fix results** to tell Claude what it got wrong and get a revised estimate.
- **Scan label**: photograph a nutrition facts panel and optionally say how much you had. Claude reads the printed values instead of estimating.
- **Describe food**: type what you ate.
- **Quick add**: enter calories and macros you already know. This works without Claude.
- **Favorites**: your starred meals plus anything you've logged at least twice in the last 30 days.
- **Log weight**: record a weigh-in for any date.

The photo buttons always work. If the screen you're using can't send photos to Claude, the app keeps your photo and asks you to describe the food, and Claude estimates from the description. If Claude isn't connected at all, you enter the calories yourself. **Settings › Claude connection** shows what your current screen supports.

If you close the sheet while a photo is being analyzed, the result waits on the home screen. Tap any logged meal to see its details, star it as a favorite, delete it, or log it again today. Logging from the favorites row on Home shows an Undo button for a few seconds.

## Activity, steps and watches

Artifact pages can't read Apple Health, Google Fit or a watch directly; that needs a native app. Instead, tap the Steps card on Home:

- **Import screenshot**: screenshot your activity summary in Apple Fitness or Health, Google Fit, Samsung Health, Garmin Connect, Fitbit, Oura, Whoop or Strava. Claude reads steps, active calories, exercise minutes and workouts, and you check them before saving.
- **Enter by hand**: type steps and active calories, or add workouts by type and minutes. Workout calories are estimated from standard MET values and your latest weigh-in.

In Settings you can keep your calorie budget fixed or add burned calories to it. Progress shows a daily steps chart with your goal line, plus totals for active calories and exercise minutes. The weekly check-in includes activity too.

## Hero (RPG)

- **Class**: pick Warrior, Ranger, Monk or Mage. Each earns 25% more XP and gold on two quests. Changing class later costs 100 gold.
- **Daily quests**: log 3 meals, hit your protein goal, land within 10% of your calorie budget, reach your step goal, hit your water goal, and exercise for your goal minutes. Quests track themselves; tap **Claim** when one is done, today or the next day. Claiming all six opens the daily chest.
- **Levels**: level *L* needs 50 × *L* × (*L* − 1) total XP, so each level takes a little longer than the last. Ranks go from Novice through Squire, Knight and Champion to Mythic.
- **Stats**: STR, END, VIT and WIS count the days in the last 30 that you hit protein or exercise, steps, water, and 3 logged meals.
- **Weekly boss**: a new boss every Sunday with 1,200 HP. Every XP you earn from quests that week deals one point of damage; defeat it for bonus XP and gold.
- **Achievements**: 15 milestones, including streaks, protein days, 100,000 steps in a week, workouts, recipes, bosses and levels. Each one pays out gold and XP when you claim it.
- **Shop**: spend gold on Streak Shields (cover one missed day), avatar frames, titles and auras.

## Water

Tap + or − on the Home water card. Each glass is 8 oz (250 ml when units are set to kg). Set the daily goal in Settings.

## Weekly check-in

On Progress, **Get my check-in** sends Claude a summary of your last 7 days: daily calories and macros, meal counts, water, weigh-ins and most-logged foods. It returns a one-line summary, what went well, and one or two things to try. The latest check-in is saved; tap **Refresh** for a new one.

## Storage

When you're signed in to Claude, everything is saved to the artifact's database under your private per-user path (`data/users/<your id>/…`). No one else can read it, including anyone you share the page with. Meals, weigh-ins, water, activity, hero progress, favorites, check-ins, recipes, plan entries, grocery lists and photos (meal photos resized to 360 px, recipe photos to 480 px) are stored in separate collections. If the page can't reach that database, it saves to browser storage instead.

## Accuracy

Photo-based estimates are usually within about 15–25% of the true value. Hidden fats (oil, butter, dressings) cause the biggest misses, so mention them in the note or use **Fix results**.

## Editing

`index.html` is the whole app. After editing, republish it to the same artifact URL.
