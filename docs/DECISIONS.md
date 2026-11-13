# Design Decisions

## GUI Framework: tkinter
Chosen over PyQt6 because it ships with Python, has zero extra install
steps, and is sufficient for this scope. Can swap to PySide6 later
if the UI needs more polish.

## Database: SQLite
Chosen over JSON files because SQL queries (search, filter, sort) are
faster and require less custom code. The .db file is still a single
file — fully offline and portable.

## Packaging: .deb first, Flatpak second
Ubuntu/Debian is the most common Linux distro. .deb is simpler to set
up than Flatpak. Flatpak can be added after v1.0.

## Status fields: want-to-read, reading, finished
Three states cover the MVP. "Dropped" and "on-hold" are stretch goals.