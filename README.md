# Text-Adventure.ai

AI Powered Text Adventure Game Engine

## OpenSource Version

It is coming soon. 
We are revising security and usability features as well as adding documentation.

For the moment, please enjoy https://text-adventure.ai

## Screenshots

<p float="left">
  <img src=public/Screenshots/AIdventure_36.png width=160>
  <img src=public/Screenshots/AIdventure_1.png width=160>
  <img src=public/Screenshots/AIdventure_24.png width=160>
  <img src=public/Screenshots/AIdventure_2.png width=160>
  <img src=public/Screenshots/AIdventure_11.png width=160>
</p>
<p float="left">
  <img src=public/Screenshots/AIdventure_13.png width=160>
  <img src=public/Screenshots/AIdventure_45.png width=160>
  <img src=public/Screenshots/AIdventure_40.png width=160>
  <img src=public/Screenshots/AIdventure_43.png width=160>
  <img src=public/Screenshots/AIdventure_8.png width=160>
</p>
<p float="left">
  <img src=public/Screenshots/AIdventure_22.png width=160>
  <img src=public/Screenshots/AIdventure_41.png width=160>
  <img src=public/Screenshots/AIdventure_15.png width=160>
  <img src=public/Screenshots/AIdventure_10.png width=160>
  <img src=public/Screenshots/AIdventure_20.png width=160>
</p>
<p float="left">
  <img src=public/Screenshots/AIdventure_21.png width=160>
  <img src=public/Screenshots/AIdventure_34.png width=160>
  <img src=public/Screenshots/AIdventure_23.png width=160>
  <img src=public/Screenshots/AIdventure_29.png width=160>
  <img src=public/Screenshots/AIdventure_30.png width=160>
<p float="left">
  <img src=public/Screenshots/AIdventure_14.png width=160>
  <img src=public/Screenshots/AIdventure_32.png width=160>
  <img src=public/Screenshots/AIdventure_35.png width=160>
  <img src=public/Screenshots/AIdventure_38.png width=160>
  <img src=public/Screenshots/AIdventure_27.png width=160>
</p>

<!-- <img src=public/Screenshots/AIdventure_37.png width=160> -->

## Project setup

You need either:

- OpenAI API key
  or
- Local LLM that accepts OpenAI-like API requests (I use LMSTudio with Llama3 locally)
- Supabase Server (I use the docker self-hosted version)

## Optional features

- Stable Diffusion Image Generation or Dall-E3 Image Generation
- ElevenLabs voiceover and/or sound effects generation (requires ElevenLabs API key)

## Local Environment

- If you are running this on a non-https server, for dall-e-3 you will need to run the serverless function server.
- You also need to run this server to receive streamed audio from ElevenLabs

```bash
cd helper-server
npm i
node server.mjs
```

- Add these to your `/etc/hosts` file

```bash
127.0.0.1 text-adventure.example.com
127.0.0.1 studio.text-adventure.example.com
127.0.0.1 data.text-adventure.example.com
127.0.0.1 node.text-adventure.example.com
127.0.0.1 proxy.text-adventure.example.com
```

## For a hosted version with OAuth

```yaml
# Replace with your actual supabase domain
GOTRUE_EXTERNAL_GITHUB_ENABLED: 'true'
GOTRUE_EXTERNAL_GITHUB_CLIENT_ID: ''
GOTRUE_EXTERNAL_GITHUB_SECRET: ''
GOTRUE_EXTERNAL_GITHUB_REDIRECT_URI: 'https://data.text-adventure.example.com/auth/v1/callback'

# Replace with your actual supabase domain
GOTRUE_EXTERNAL_DISCORD_ENABLED: 'true'
GOTRUE_EXTERNAL_DISCORD_CLIENT_ID: ''
GOTRUE_EXTERNAL_DISCORD_SECRET: ''
GOTRUE_EXTERNAL_DISCORD_REDIRECT_URI: 'https://data.text-adventure.example.com/auth/v1/callback'

# Replace with your actual supabase domain
GOTRUE_EXTERNAL_TWITTER_ENABLED: 'true'
GOTRUE_EXTERNAL_TWITTER_CLIENT_ID: ''
GOTRUE_EXTERNAL_TWITTER_SECRET: ''
GOTRUE_EXTERNAL_TWITTER_REDIRECT_URI: 'https://data.text-adventure.example.com/auth/v1/callback'
```

## How to run

Import `schema.sql` into your supabase database (via studio's SQL editor)

## Todo

- [x] Allow Dall-E3 image generation
- [x] Audio streaming via wss
- [ ] Autoplay story
- [ ] Customization of prompt
- [ ] Model change for Stable Diffusion
- [ ] LORA settings for Stable Diffusion
- [~] Function calls
- [ ] Add many more features

## Credits

Made by | <a href="https://knowmad.online"><img src=public/knowmad_white.png width=120></a> |

## License

You can use this for both personal and commercial projects but you must credit and link to the [original repository](https://github.com/knowmad-online/aidventure).

Reselling is prohibited.
