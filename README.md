# Mobile_Architect_and_Programming
Inventory App

#Briefly summarize the requirements and goals of the app you developed. What user needs was this app designed to address?**

I built a simple inventory app that lets someone log in, view items in a clean table, add new items, edit quantities, and track changes. When any item drops below a set amount, the app raises an alert and, if allowed, can send a text message. The goal was to make routine stock checks fast and clear, reduce mistakes, and keep a record of what changed and when.

#What screens and features were necessary to support user needs and produce a user-centered UI for the app? How did your UI designs keep users in mind? Why were your designs successful?**

The app includes a sign in screen, an inventory screen with a three-column list for name, location, and quantity, a small form to add items, an edit dialog to change quantity or delete an item, an alerts screen, an activity screen that logs adds and edits, and a profile screen with sign out. I kept labels short, aligned column headers with their data, and placed the main action as a single floating button. New items appear at the top so people can confirm what they just added. Editing opens in a small dialog so the user stays in context. Low stock warnings show immediately and are also saved to the alerts list. These choices cut down on extra taps and make it easy to scan, which is why the design works well.

#How did you approach the process of coding your app? What techniques or strategies did you use? How could those techniques or strategies be applied in the future?**

I coded in small steps and wired each screen as soon as the layout was ready. I kept data and screen logic separate by using a view model and observable lists so the list refreshed itself when items changed. The inventory table used a recycler view with a custom row and a compact adapter. Dialogs handled add and edit, with simple input checks for empty fields and non-numeric values. I also added a small rule that stops repeat alerts once the same item is already flagged, and clears that flag when the quantity is raised again. These habits—small increments, clear separation, and automatic refresh—are useful on any app because they make fixes safer and features easier to add.

#How did you test to ensure your code was functional? Why is this process important, and what did it reveal?**

I ran the app on a phone emulator with different screen sizes and tried common tasks: signing in, adding items, editing quantities, deleting, and signing out. I checked edge cases like blank input, very large numbers, and denied permissions. I also tested the alert rule by moving quantities above and below the limit to be sure alerts show once and then stop when stock is healthy again. This found small issues such as misaligned headers, a button that blocked input, and a case where the list did not refresh. Fixing those made the app feel steady and predictable.

#Consider the full app design and development process from initial planning to finalization. Where did you have to innovate to overcome a challenge?**

Two places needed extra thought. First, the low stock rule. It was not enough to show a warning when a quantity dropped. I added a way to remember which items had already warned so the user would not see the same popup again until the quantity rose above the limit and dropped again later. Second, the permission flow for alerts. I made the request appear after sign in and also gave the user a clear place in the alerts tab to grant it again if they changed their mind. Both changes reduced friction and matched how people actually use the app.

#In what specific component of your mobile app were you particularly successful in demonstrating your knowledge, skills, and experience?**

The inventory list and its edit flow show the best of my work. The table is easy to scan, the headers line up with the data, and each row has a small edit control that opens a focused dialog. From there, changing quantity or deleting an item takes one step, and the list updates in place. Tying that to the activity log and the low stock rule gives the user clear feedback and a reliable record of what happened.
