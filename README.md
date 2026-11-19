# Satellite AI (concept)

This is a concept write-up for an AI you can use through satellite messaging, using the iPhone's satellite texting.

## The idea

During my 5 week road trip to the west coast, I went the longest I've ever gone without cell service and realized how much we rely on it nowadays.

- I went several days with very spotty service, only strong enough for messaging.
- During the trip I used the Apple satellite feature for the first time and was amazed at how strong it is.
- With a clear view of the sky, I was able to send satellite messages to my friends and family to keep them up to date on my trip.
- That got me thinking about taking advantage of the iPhone's satellite feature to create a satellite AI, so you can still ask questions when you're off-grid.

<details>
<summary>About iPhone's satellite messaging</summary>

- iPhone 14 or newer
- Recent iOS version
- Only in countries where the feature is offered
- Works when you're out of cell and Wi-Fi coverage and have a clear view of the sky
- Messages are slower than normal texts, so shorter is better

</details>

## How it works

The trick is to text a second iPhone that does have internet. We'll call it the relay phone. The iPhone that's off-grid using the satellite feature will be called the field phone. The relay phone uses an Apple Shortcuts automation to:

1. Catch the incoming message
2. Send it to an AI model
3. Send the AI reply back to the field phone

### Field phone

An iPhone with Messages via satellite (iPhone 14 or newer, on a recent iOS version, in a country where the feature is offered). When you're out of coverage, the satellite UI appears in Messages. You text the relay phone a question like any other text.

### Relay phone

Any spare iPhone that can run Shortcut automations. It needs its own Apple Account (free) so the two phones can text each other. It stays at home plugged in and on Wi-Fi. The phone doesn't need to be awake, it will detect messages in the background.

## Template Shortcut

[Get the Satellite AI Shortcut](https://www.icloud.com/shortcuts/c1e7b92d98e847148b42ebc46584f04e)

Open this link on the relay phone and tap Add Shortcut. Then change the placeholder address `test@icloud.com` to the field phone's phone number or Apple Account email.

The Ask Claude action comes from the Claude app, which must be installed and signed in on the relay phone. You can swap it for another AI action, such as Apple Intelligence's Use Model or Ask ChatGPT.

## Extra notes

- Keep replies short. Satellite messages are slow and work best when short. Add a prompt such as "Answer in under 300 characters, plain text, no formatting."
- Possible additions: commands to get realtime weather data or translations.
- Is it really free? Apple has offered satellite features free on supported iPhones for a limited period. For the AI, use Apple Intelligence's models or the free tier of the Claude or ChatGPT integrations.

*This is an experimental, unofficial setup and is not affiliated with Apple. Do not rely on it in an emergency. In an emergency, use Emergency SOS via satellite or contact emergency services directly. Satellite feature availability depends on device, iOS version, country, and carrier.*
