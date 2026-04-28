# ActivityBridge

Sync your activities from Strava to Suunto.

## The problem

Many endurance athletes use multiple devices: a Garmin head unit on the bike, a Suunto watch on the trail, sometimes a phone for indoor sessions. Strava aggregates everything because every device pushes there. Suunto receives only what is recorded on a Suunto. Result: training load, recovery and progression metrics in the Suunto app and on the watch are missing data.

## What ActivityBridge does

ActivityBridge is a small open-source service that watches your Strava feed and pushes any activity not originally recorded by a Suunto device into your Suunto account. Your Suunto app and watch then see the full picture.

## Status

In development. Suunto API access requested. Code being built in public.

## How it works

1. Listens to Strava webhooks (or polls on a schedule as a fallback).
2. Filters out activities that originated from Suunto, to avoid loops.
3. Reconstructs a FIT file from the Strava activity streams (GPS, heart rate, power, cadence).
4. Uploads the FIT to Suunto via the Suunto Cloud API (Workouts endpoint).

## Tech stack

- Cloudflare Workers (serverless, free tier)
- TypeScript
- Strava API and Suunto Workouts API
- OAuth2 on both sides

## Privacy

See [PRIVACY.md](PRIVACY.md). Short version: only OAuth tokens and activity IDs are stored, encrypted at rest. Activity data is processed in memory and discarded. Nothing is shared with third parties.

## Roadmap

- [x] Project setup, identity, license
- [ ] Suunto API access approval
- [ ] Strava OAuth flow
- [ ] Suunto OAuth flow
- [ ] FIT reconstruction from Strava streams
- [ ] Webhook handler with deduplication and loop prevention
- [ ] Self-host documentation
- [ ] Hosted free instance for non-technical users

## License

MIT. See [LICENSE](LICENSE).

## Author

Adrien Rivoallan, [@adrivoa](https://github.com/adrivoa).
