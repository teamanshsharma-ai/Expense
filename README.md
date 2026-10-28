# Ledger – Personal Expense Tracker

No server, no account, no API keys. Everything runs in your browser.

## Use it
1. Unzip, then double-click index.html. It opens in your browser and works offline.
2. Optional: put the folder on any static host (Netlify Drop, GitHub Pages) to open it on your phone.

## Your data
- Saved automatically in this browser on this device (localStorage). Other browsers, devices and private windows start empty.
- Profile → Download backup saves a .json file. Restore backup loads it on any device. Do this regularly, because clearing browser data erases the app's data.

## How numbers work
- Remaining balance = income - expenses. Savings rate = (income - expenses) / income.
- Recurring items count on their start date and on every repeat date up to today.
- Budgets apply from the month you set them until you change them.


## Custom expense category icons
- The 16 expense-category tiles use the supplied transparent 3D PNG icons in `assets/icons/3d/`.
- The icon mapping is defined in `index.html` in `CAT_ASSETS`.
- This remains a static browser app; open `index.html` as described above. Keep the `assets` folder beside it.
