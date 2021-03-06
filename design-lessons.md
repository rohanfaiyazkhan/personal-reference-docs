# Design lessons

## Take as much space as you need to

Don't feel pressured to take up the whole screen. Design your component on mobile first and then expand it to add space till it feels right. Stretching out a UI layout to be very wide isn't usually convenient for our eyes to scan across.

Its best to use `width: 100%` in combination with `max-width` for this. For TailWind its `class="w-full w-max-screen-sm/md/lg"`

## You need a lot of shades of the same colors

Before I had the habit of picking a red color for danger, green color for success, and bunch of random colors from a color theme generator for the rest of my colors. While this approach works fine if you are designing a poster or a wallpaper, its not so great for designing interfaces.

Reality is that in interface design you need a lot of different shades of grey, a lot of different shades of one or two accent colors, and a few shades red for danger, yellow for warning and green for success.

You can also rotate hue to make a color seem darker or lighter. Assuming saturation and lightness are both 50%, the lightest hues are 60, 180 and 300. The darkest hues are 0, 120, 240.

## Ensure contrast between your content and background 

The color of your text/icons should contrast with your background for accessiblity reasons. Lower contrast can work for de-emphasized items but don't overdo it to the point that it is illegible.

Do not rely solely on different colors to show difference, ensure there is enough contrast between the colors so that color blind users can tell the difference. 