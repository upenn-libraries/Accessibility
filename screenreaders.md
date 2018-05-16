# All About Screen Readers

## Software recommendations
| Name | Operating System | Price | Details |
|:--------------:|:----------------:|-------------|-----------|
| VoiceOver (VO) | Mac | Free, native to Mac. | Requires no installation and comes with a built-in tutorial. A beginner-friendly, low-barrier screen reader if you have a Mac. |
| NVDA | Windows | Free, open-source. | Must be downloaded and installed from the [NVDA website](https://www.nvaccess.org/download/).  |
| JAWS | Windows | Not Free. | You (or your organization) must purchase a license in order to use JAWS, even for testing purposes. JAWS is more popular, but it'll cost ya. |

To learn more about the latest screenreader user demographics, check out [WebAIM's biannual surveys](https://webaim.org/projects/screenreadersurvey7/).

## How many screen readers should I test with?
[WebAIM's Screenreader Q&A](https://webaim.org/articles/screenreader_testing/) contains an in-depth discussion of this issue, but in short: *Consistently* testing with one or two popular screen readers should generally be enough. Testing with both VoiceOver and a Windows screen reader (either JAWS or NVDA) is an excellent goal. Since all screen readers differ, more is always nice, but the more important thing is to make sure your website adheres to standard guidelines & accessible design practices.

**Consistent, recurrent testing with *one* screen reader is vastly superior to inconsistent, sporadic testing in multiple screen readers.**

## How to start using VoiceOver
On your Mac, go to System Preferences > Accessibility > VoiceOver. There, you can enable VoiceOver. (You can also hit Command + F5 to toggle VO on and off.)
When you first enable VoiceOver, it will give you the option to use its tutorial. The tutorial is a great way to walk through the basics.

### Online guides:
Penn State has a helpful beginner-level cheatsheet of VoiceOver commands: http://accessibility.psu.edu/screenreaders/voiceover/

This site has an extensive list of commands, and links to Apple's color-coded keyboard charts: http://lab.dotjay.com/notes/voiceover-commands/

WebAIM also has a useful introduction to testing with VoiceOver: https://webaim.org/articles/voiceover/

### Super short list of commands:
*Note: "VO" stands for "Control + Option". This combination used in the majority of VoiceOver commands, so this shorthand notation is common in online documentation & guides.*

| Keyboard Command | Result |
|------------------|--------|
| Command + F5 | Turn on/off |
| VO + A  | Read all |
| Control  | Pause |
| Tab | Skips to major page elements (links, form items, etc). Works regardless of whether or not you have VoiceOver on. |
| VO + Left/Right Arrow Keys | Hop from element to element. |
| VO + U  | [Rotor menu](http://accessibility.psu.edu/screenreaders/voiceover/#rotor) (useful way to navigate the page outline by heading tags, links, page landmarks, etc). Use left & right arrows to navigate between menus. Up/down/enter to select an item. Escape to exit. |
| VO + V | VoiceOver settings. Use left & right arrows to navigate between menus. Up/down to change val. Escape to exit. |
| VO + Command + Right Arrow | Voice settings (speed, pitch, style, etc). Use left & right arrows to navigate between menus. Up/down to change val. |
