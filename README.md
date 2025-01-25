# What is this for
A minimal OXWU Docker image ready to run on Raspberry Pi with 64-bit CPU & 64-bit operating system (e.g., Pi 4 with Ubuntu) under **headless mode** (i.e., without display, keyboard & mouse).

# How to
1. Update settings under `oxwu-desktop/oxwu-configs/settings.json`, especially `townID`.
   - One method to discover the `settings.json` fits you the best:
      1. Start this project with default `settings.json`.
      2. Access to the virutal desktop as the tutorial below.
      3. Pick your favority configurations on the OXWU's UI.
      4. Copy the generated `settings.json` out, which locates under `/home/oxwu-announcer/.config/oxwu/`.
   - The other method to discover your `townID`, please refer [https://hub.docker.com/r/jscat/oxwu](https://hub.docker.com/r/jscat/oxwu).
2. Update field `VNC_PW` in `docker-compose.yml`.
3. `sudo docker compose build && sudo docker compose up -d`
4. Naigate with a webb-browser to `<IP>:6901` with username=`kasm_user` passward=`<password set in step 2>`