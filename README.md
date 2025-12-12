# Account Creation
Simply input a valid email and create a password. Once you've done so, re-enter the login page, and you'll be in. 

# Installation Instructions (Local)

1. Download [Node.js v22.14.0](https://nodejs.org/en/download/releases/)
2. Download [Git](https://git-scm.com/downloads) (Select your IDE of choice in installer)'
3. Install [NPM](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm) `npm install -g npm`
3. Load up `scholarly` in your IDE 
4. Launch the terminal `CTRL + SHIFT + ~`
5. Run these following commands:
   1. `npm install` to install the dependencies
   2. `npm install astro` to install [Astro](https://docs.astro.build/en/install-and-setup/#manual-setup)
   3. `npm run dev` to start the development server
6. Open your browser and navigate to `http://localhost:4321/` to view the development site

# Supabase Recovery
Because of the nature of Supabase (they want to save money), inactive databases will be shoved into a disabled state after **90 days.** Here is the steps towards *full* database recovery:

1. Download the `.backup` file from the inactive page.
2. Ensure you have `scoop` (Windows) or `brew` for macOS. 
3. Download `supabase` and `postgresql`.
4. Delete Supabase project on both Supabase and Vercel.
5. Make new Supabase project and connect via Vercel.
6. Copy and paste `.env.local` into `.env` (only need one `SUPABASE_URL` and `SUPABASE_ANON_KEY`).
7. Add `SERVER_URL` in `.env` as `http://localhost:4321`.
8. Put `SUPABASE_URL`, `SUPABASE_ANON_KEY`, and `SERVER_URL` (Vercel domain) in GitHub secerts.
9. Run ``psql "<session pooler>" `-f "C:\path\to\your.backup"``
10. Disable e-mail confirmations in Supabase.

# Credits
- Nathan Parker ([@Azuronate](https://github.com/Azuronate)) - Backend Developer
- Megan Mann ([@ExplosiveNebula](https://github.com/ExplosiveNebula)) - Frontend Developer
- Brenden Overstreet ([@Bre-nden07](https://github.com/Bre-nden07)) - Concept Designer
