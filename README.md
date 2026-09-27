# NYC Rules for You

A desktop app that shows which New York City and New York State laws apply to you, which ones already passed and start
later, and which bills and proposed agency rules would change them: each in plain language, with the official text it
rests on. Everything runs on your computer; your answers never leave it.

## Data releases

The [`data` release](https://github.com/JorickvdHoeven/nyc-rules/releases/tag/data) holds the app's data. If you let
the app go online, it checks this release for newer laws, bills and links and downloads only what changed:

| file | what |
|---|---|
| `manifest.json` | the current data version and its files, with sizes and SHA-256 checksums |
| `manifest.json.sig` | Ed25519 signature of `manifest.json`; the app ignores data without the publisher's signature |
| `core-*.duckdb.gz` | plain-language rules, bill records and texts, votes and links (changes with every update) |
| `bills-*.duckdb.gz` | the text of every tracked bill, with its search index |
| `laws-*.duckdb.gz` | the text of every law section, with its search index (changes rarely) |

Sources: the NYC Charter, Administrative Code and Rules (American Legal Publishing), New York State laws and bills
(NYS Senate Open Legislation), City Council legislation and votes (Legistar), the City Record, mayoral executive orders,
the NYC Codes, Rules and Regulations (NYCRR), the US Code and the eCFR.

This is an unofficial guide, not legal advice. Check the official text linked on each rule.
