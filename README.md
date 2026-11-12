# TVU Go creator code walkthrough overlay

A 1920x1080 transparent HTML overlay for OBS. When it's triggered, it walks viewers through signing up and using a creator's code, using the real app screens with highlights. It runs about 62 seconds.

The steps are:
1. Intro card with the code
2. Sign up
3. Tap "Have a promo code?"
4. Type the code and tap Apply
5. Tap Claim
6. iPhone: paste the code and tap Redeem
7. Android: redeem in Google Play
8. All set
9. Outro card

## URL options
- `?code=GOCASH` sets the creator's code. It appears on the cards and inside the app screenshots.
- `&side=left` puts the panel on the left. The default is right.
- `&scale=0.8` shrinks the panel.
- `&every=15` replays automatically every 15 minutes.
- `&loop=1` plays forever, for testing.
- `&step=5` freezes on one step, for previews.

## OBS setup
1. Add a Browser source at 1920x1080 and point it at the hosted URL. You can also tick "Local file" and pick index.html.
2. Tick "Shutdown source when not visible" and "Refresh browser when scene becomes active".
3. Hide the source. To trigger the walkthrough, show it with a hotkey, a Stream Deck button, or a chat command.

Each time the source becomes visible, the walkthrough plays once and then slides away.

## Examples
- index.html?code=GOCASH
- index.html?code=GOKEEM
