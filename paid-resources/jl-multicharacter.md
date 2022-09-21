---
description: Multicharacter Script For QBCore
---

# 🚶 JL Multicharacter

### Feature:

* Modern and simple UI
* Support fivem-appearance and qb-clothing ( for showing the ped )
* Developer can set player to have more slots by adding the license.
* Ped support scenario and animdict

### Dependencies:

* qb-core
* qb-spawn
* qb-apartments
* qb-weathersync
* qb-clothing or fivem-appearance

### Installation:

Just remove other multicharacter you have. and replace:

`qb-multicharacter:client:chooseChar` with `jl-multicharacter:client:chooseChar`



### Event:

Client Side:

`jl-multicharacter:client:chooseChar`

Parameter: setwelcome: boolean

Example usage:

```lua
TriggerEvent("jl-multicharacter:client:chooseChar", true)
-- true : show the message landing page (Welcome to xx Server)
```

### Changing the color:

I used svelte to build the UI so that mean you can't change everything on ui side, except for the color, I've used global variable on css, so it may make it easier.

You can use [unminify](https://www.unminify2.com/), to unminify the css. After that don't forget to [minify ](https://www.toptal.com/developers/cssminifier)it again :slight\_smile:.

After you unminify the css, you should see this:

```css
:root {
  /* Welcome Page */
  --welcome-page-bg: unset;
  --welcome-page-bg2: #d54343;
  --welcome-page-color: white;
  /* Button */
  --button-bg: rgba(255, 147, 147, 0.438);
  --button-color: white;
  --button-box-shadow: 0 0 2.5em 0 rgba(216, 105, 105, 0.616);
  --button-border: 0.5px solid rgba(255, 147, 147, 0.555);
  --button-selected: rgba(255, 147, 147, 0.603);
  --button-disabled: rgba(146, 67, 67, 0.438);
  /* Date input */
  --date-bg: rgba(255, 147, 147, 0.438);
  --date-box-shadow: 0 0 2.5em 0 rgba(216, 105, 105, 0.616);
  --date-border: 0.5px solid rgba(255, 147, 147, 0.555);
  --date-color: white;
  --date-placeholder-color: rgba(255, 255, 255, 0.527);
  /* Input number unused*/
  --input-number-bg: rgba(255, 147, 147, 0.438);
  --input-number-color: white;
  --input-number-box-shadow: 0 0 2.5em 0 rgba(216, 105, 105, 0.616);
  --input-number-border: 0.5px solid rgba(255, 147, 147, 0.555);
  /* Input Text */
  --input-text-bg: rgba(255, 147, 147, 0.438);
  --input-text-color: white;
  --input-text-box-shadow: 0 0 2.5em 0 rgba(216, 105, 105, 0.616);
  --input-text-border: 0.5px solid rgba(255, 147, 147, 0.555);
  --input-text-placeholder-color: rgba(255, 255, 255, 0.527);
  /* Create Character */
  --create-bg: rgb(37, 37, 37);
  --create-bg2: linear-gradient(
    180deg,
    rgba(37, 37, 37, 0.4906337535014006) 59%,
    rgba(138, 60, 60, 0.5186449579831933) 88%
  );
  /* Select Character */
  /* Character information */
  --char-info-bg: rgba(255, 113, 113, 0.541);
  --char-info-box-shadow: 0 0 1.2em 0 rgba(216, 105, 105, 0.616);
  --char-info-color: white;

  --select-char-button-bg: rgba(216, 105, 105, 0.616);
  --select-char-button-box-shadow: 0 0 0.5em 0 rgba(216, 105, 105, 0.616);
  --select-char-button-text-shadow: 0 0 0.225em hsl(0 0% 100% / 0.5),
    0 0 0.45em currentColor;
  --select-char-button-color: white;
  --select-char-button-disabled: rgba(128, 61, 61, 0.616);

  /* Sticky Right Side */
  --sticky-bg: rgba(255, 147, 147, 0.438);
  --sticky-box-shadow: 0 0 1em 0 rgba(216, 105, 105, 0.616);
  --sticky-color: white;
  /* Modals */
  --modals-box-bg: rgba(165, 88, 88, 0.616);
  --modals-box-color: white;
  --modals-box-box-shadow: 0 0 2.5em 0 rgba(165, 88, 88, 0.616);
  --modals-wrapper-bg: rgba(0, 0, 0, 0.493);
}
```

