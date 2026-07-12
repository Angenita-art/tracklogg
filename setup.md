# TrackLog — two-site setup

Two separate, fully self-contained pages, sharing one Supabase database:

- **submit.html** — submit page (public, for logging new prints/tracks)
- **database.html** — register, search/filter, admin delete, and the photo Compare tool

Both pages already have your Supabase keys filled in and point at the same database, so an entry submitted on submit.html shows up on database.html immediately.

## Already done
- Supabase database table created
- Storage bucket `print-photos` created (public)
- Both HTML files already have your Supabase project URL and key filled in

## Still to do (optional, not required for the site to work)

### Lock deletes to just you

1. In Supabase, go to Authentication → Users → Add user → enter your own email and a password → check "Auto Confirm User" → Create.
2. Go to SQL Editor → New query → run:
