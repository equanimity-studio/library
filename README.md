# library

A personal book library where you can add books, mark them read or unread, and remove them. Built for [The Odin Project](https://www.theodinproject.com/) curriculum.

**Live demo:** https://equanimity-studio.github.io/library/

Built with HTML, CSS and vanilla JavaScript.

## Features

- An "Add Book" button opens a pop-up form for title, author, page count and read status
- Each book appears as a card with its details
- A button on each card toggles between Read and Not Read
- A Remove button deletes the book's card
- Clicking outside the form closes it

## What I learned

- **Object constructors and prototypes**, then **rewriting the same code with a `class`**. I did the rewrite on a separate `lib-class` branch and merged it into `main` once it worked.
- **Storing objects in an array** and building the page from that array
- **Handling form submission**: stopping the default page reload, reading input values and checking for empty fields
- **Closing the pop-up on an outside click** with `Element.contains()`
- **CSS Grid** for the card layout, and styling with box shadows and a Google Font

## Looking back: what I'd do differently

- **Keep the data and the page in sync.** The Read/Not Read button changes only the button; the book object's `read` value never changes. The button should update the data, and the card should be re-drawn from it.
- **Use real booleans.** Read status is stored as the strings `"yes"`/`"no"`; `isRead: true/false` would be simpler.
- **Give each book an ID.** Removing a book matches on its title, so removing one book also removes any other book with the same title.
- **Add event listeners once.** `openForm()` adds a new click listener every time the form opens, so the listeners pile up. The listener should be set up once, when the page loads.
- **Keep JavaScript out of the HTML.** The button uses an inline `onclick` attribute; using `addEventListener` in the script keeps all the behavior in one place.
