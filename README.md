# Downloads
- Latest version of [vlc](https://www.videolan.org/vlc/)
- Latest version of [streamlink](https://github.com/streamlink/windows-builds/releases)
- Update obs studio
    - Example is using 29.1.3

# Using Streamlink
- Once you have streamlink installed, open up a command prompt
  - On Windows, you can hit `Win+r` to open a run prompt, then `cmd`
  <details>
    <summary>example</summary>

    ![](https://puu.sh/JQAld/12b39942a3.png)

  </details>

- In the command prompt, you can type `streamlink <twitch_url> best` and this should open up a new VLC window with a stream playing
  - e.g. `streamlink twitch.tv/arayalol best`
- You might see a lot of warnings, but as long as the stream is playing in the video player, I've been ignoring them without any issues.
- Make sure these command prompts stay open. If you close them, the stream will freeze/close.

# Setting up OBS Scene
## Sources
- Layout is broken up into 3 "groups"
  - All text sources (runner names, commentator names, top times, etc)
  - Main 6/4/2 person layout image
  - All VLC captures

- Use `Game Capture` with `Capture specific window` to capture a person's stream into OBS
  - Make sure the specific window for this scene is pointed at their VLC
  - Each game feed is a `Game Capture` with mode `Capture specific window`, and pointed to a VLC stream that is open.
  <details>
    <summary>example</summary>

     ![](https://puu.sh/JQAlO/ad9b1993d5.jpg)

  </details>

  - To capture the runner's timer, you can right click the VLC source, `copy`, then `paste (reference)`.
    - Also clicking on the Source, `Ctrl+C`, `Ctrl+V`
  - This will create a duplicate source that you can crop out different portions if needed.
    - If you change the `Window` of one of these duplicated sources to a different stream, it will update all of them
    - My layout ends up being 3 duplicate sources for each game feed (game feed, timer, DVs)
  - I would recommend putting these video players at full screen, 0 audio, and minimized.
    - For the one stream that you want to hear audio, raise their volume but leave everyone else muted
    - **If you end up cropping in VLC, then resizing the VLC window, the cropping will be messed up**

## Audio Sources
- I mute Desktop Audio and capture the individual audio sources directly with `Application Audio Capture (BETA)`
- One of these sources points to Discord in order to capture commentators, otherwise the stream will not be able to hear them.
- Another one is pointed to ONE VLC window. Since I only want the audio from one runner at a time to play in the stream, I use one source.
  - When I switch to a different runner, I update this source to point to the new "main" runner
- Last audio source is for your own mic.

# Switching streams
- To switch streams, you can use their existing command prompt and not need to open a new one.
- You can either close the VLC window, or hit `Ctrl+C` a few times until the stream closes
  - Identifying the correct command prompt for the right stream can be tricky, but you should be able to see the command you ran that has the stream title
  <details>
  <summary>example</summary>

  ![](https://puu.sh/JQAn5/b149a177bd.jpg)

  </details>
- Once you close the stream, you should be able to run another streamlink command to the new stream
  - e.g. `streamlink twitch.tv/redracetv best`
- After the new VLC window opens, you can find the VLC source(s) that were pointing to the old stream and update the window to point to the new VLC window
- Then you can crop the feed as needed, adjust audio as needed


# Screenshare for commentators
- To give commentators the best setup to view the restream without latency, I open a `Windowed Projector (Preview)` and full screen it
  <details>
  <summary>example</summary>

  ![](https://puu.sh/JQAmD/9adeb05536.jpg)

  </details>
- You can then screenshare the preview window in Discord
- Unfortunately the commentators won't be able to hear game audio.

# Studio Mode
- If you want to have smooth transitions, `Studio Mode` in OBS can be used to adjust the preview and change sources without having the stream see behind the secenes. Purely optional.
