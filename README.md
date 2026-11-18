# Emberbound news

The Emberbound app downloads `announcement.json` on launch and shows it once as a popup.
Edit the file on GitHub to post a new announcement - no app build needed. Changes reach
players within about 5-10 minutes.

## Fields

| Field | Required | Notes |
|---|---|---|
| `id` | yes | Each player sees an id once. **Change it for every new announcement.** |
| `title` | yes | Short, shown in capitals. Max 40 characters. |
| `body` | yes | One or two sentences. Max 400 characters. |
| `hint` | no | Small grey line under the text. Max 200 characters. |
| `button` | no | `{ "label": "...", "url": "https://..." }`. Must be an `https://` link. Without it, the popup only has a close button. |
| `startsAt` / `endsAt` | no | ISO dates (UTC). Outside this window nothing is shown. |
| `platforms` | no | `["ios", "android"]` or just one. Omit for both. |

## Turning it off

Set `endsAt` to a past date, or replace the whole file with `{}`.

If the file is broken or a required field is missing, the app shows nothing.
