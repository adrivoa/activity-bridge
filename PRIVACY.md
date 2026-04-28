# Privacy Policy

Last updated: April 2026

ActivityBridge is a free open-source service that synchronises sport activities from Strava to Suunto on behalf of the user who connects both accounts. This policy explains what data ActivityBridge handles and how.

## What data ActivityBridge handles

To do its job, ActivityBridge stores:

- Strava and Suunto OAuth access and refresh tokens, encrypted at rest.
- The IDs of activities that have already been synced, to avoid duplicates.
- Minimal sync logs (timestamp, activity ID, success or failure status), retained for 30 days.

## What data ActivityBridge does NOT store

- No name, email, or profile information beyond the minimum required by OAuth.
- No GPS coordinates, no heart rate, no power, no cadence, no other sensor data. Activity streams are fetched from Strava, transformed in memory into a FIT file, uploaded to Suunto, and discarded.
- No payment data. ActivityBridge is free.

## What data ActivityBridge shares

Nothing. ActivityBridge does not share any data with third parties beyond the strict transit between Strava and Suunto required to perform the sync requested by the user.

## Revoking access

Access can be revoked at any time:

- Strava: https://www.strava.com/settings/apps
- Suunto: from the connected apps section of your Suunto account.

When access is revoked, ActivityBridge stops syncing immediately, and the corresponding tokens and sync history are deleted within 7 days.

## Contact

For any privacy question or data deletion request, open an issue on the project repository or email adrien.rivoallan@gmail.com.
