# YMD — Your Music Distributor — Launch Ready

This package is a deployable static web application for YMD. It connects to the existing YMD Supabase project using the publishable client key and uses Supabase Auth plus the deployed `ymd-health` and `dsp-sandbox` Edge Functions.

## Deploy

### Vercel
1. Upload this folder to a Git repository or import the folder into Vercel.
2. Vercel detects the static site automatically.
3. Deploy as production.

Vite/static sites can also be deployed through the Vercel CLI.

### Netlify
Upload the folder as a static site.

## Important

- The included Supabase publishable key is intended for browser use; never add a Supabase secret/service-role key to this site.
- DSP delivery buttons are explicitly sandbox/simulated. They do NOT deliver to real Spotify, Apple Music or YouTube Music.
- Real distribution requires an authorized downstream distribution partner/DSP relationship, credentials, commercial agreement, exact DDEX profile, and production worker configuration.
- The existing Supabase project already contains the YMD control-plane tables and RLS configuration.

## Production next step

Connect the artist-facing app to an authorized distribution partner and replace the sandbox adapter with the partner's authenticated API/SFTP/DDEX workflow. Keep the existing sandbox until end-to-end production certification is complete.
