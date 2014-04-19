# [fit] Web Accessibility
## [fit] What, why, and how
### [fit] Mike Schneider, BarCampRoc, April 2014
### @MikeASchneider

![filtered](https://farm5.staticflickr.com/4012/4610457832_744c0d4122_o.jpg)

---

# Outline
1. What is Web accessibility?
2. Why bother?
3. Principles of the accessible Web?
4. Specific disabilities
5. How to make your site accessible
6. Busting myths of the accessible Web
7. Screenreader demo

---

# What is Web accessibility?

> The inclusive practice of making websites usable by people of all abilities and disabilities

- Web accessibility is about *removing barriers to access*

---

# Why bother?
- Moral/social reasons
- Financial reasons
- Legal reasons

^
Moral reasons:
The Web: Potential for unprecedented access to information and interaction for disabled people
Financial reasons:
Don't want to lose the business or attention of disabled users
Legal reasons:
USA's American Rehabilitation Act and ADA, UK's Disability Discrimination Act, etc. Consult a lawyer!

---

# Principles of the accessible Web
- Perceivable
- Operable
- Understandable
- Robust

^
Perceivable (sight, hearing, touch, transformability)
Operable (input, interaction, timing, error recovery)
Understandable (meaning, functionality)
Robust (functional across past and future tech, according to spec)

---

# What sort of disabilities?
- Deafness
- Blindness
- Colorblindness
- Motor disabilities
- Seizure disorders

---

# [fit] Let's talk specifics about these disabilities.

---

# Deafness

- Transcripts and captions for all embedded audio/video
- All audio cues should be accompanied by a visual cue

- Side benefits!
  - SEO
  - Hearing users who prefer not to use speakers

---

# Colorblindness

- Color should never be the only means of conveying info
- Use a colorblindness simulator

---

# Motor disabilities

- Ensure that your site can be used without a mouse
- Mistakes are likely - always ask for confirmation, make it easy to undo

---

# Seizure disorders

- Strobing, flickering, flashing may cause dizziness, nausea, seizures
- Avoid strobes, flickers, and flashes or provide a clear and concise warning
- Some laws prohibit flickers > 2 per second

---

# Blindness

---

# How do blind people use the Web?

- Perception: Screenreaders
- Operation: Keyboard-only
- Understanding: Information presented linearly

---

# General tips in developing for the blind:

- Always provide a keyboard alternative to mouse/touch
- Provide descriptive text when necessary
- Don't repeat yourself

---

# How screenreaders can be used
- Navigate linearly down the page
- Skip through heading tags to desired section
- Skim through a list of all links (context removed)

---

# Limitations of screenreaders

- Can't "describe" images (duh)
- Context that's obvious to a seeing user may be unclear
- Tip: When necessary, use  offscreen descriptive text

---

# Semantic HTML helps everybody

HTML should reinforce the meaning of your content

# Would a user understand the page if they were reading your unrendered HTML?

---

# Offscreen text example

```html
<!-- html -->
<span class="offscreen">Friends attending this event:</span>
<ul>
  <li><img src="01.jpg" alt="Mike Schneider" /></li>
  <li><img src="02.jpg" alt="Dave Thomas" /></li>
  <li><img src="03.jpg" alt="Anthony Mitchell" /></li>
</ul>
```

```css
/* css */
/* make this invisible, don't let it take up space */
.offscreen {
  font-size: 0;
  position: absolute;
  display: inline-block;
  height: 0;
  width: 0;
}
/* screenreaders ignore text that is 'display: none' or 'visibility:hidden' */
```
---

# Aria roles

```html
<h2 id="nav-heading">Navigation</h2>
<ul class="navbar" role="navigation" aria-labelledby="nav-heading">
  <li><a href="about.html">About</a></li>
  <li><a href="contact.html">Contact</a></li>
  <li><a href="developers.html">Developers</a></li>
</ul>
```

---

# [fit] Web accessibility myths

---

# Myth: Adding title text to links helps screenreaders
## FALSE: Title text is only ever visible to hearing users as a tooltip

---

# Myth: Most blind people use special text-only browsers like Lynx
## FALSE: Most blind people use Firefox or Internet Explorer with a screenreader (with JS and CSS)

---

# Myth: Every image needs an alt attribute
## TRUE… but don't repeat yourself. Use a blank attribute (alt="") if necessary.

---

# Myth: Accessible websites are ugly
## Only if you make them ugly! (duh)

---

# [fit] Screenreader demo
## [fit] OS X Voiceover: Press ⌘+F5 to activate

---

# Conclusion
## Web accessibility *isn't that hard*
## Keep disabled users in the back of your mind
## A little bit of research goes a long way

---

# Resources

- WebAIM.org - WebAIM: Web Accessibility In Mind
- w3.org/TR/wai-aria/ - W3C: Web Accessibility Initiative - Accessible Rich Internet Applications

## Slides powered by Deckset http://decksetapp.com

---

# Thanks / Questions
## [fit] Mike Schneider / @MikeASchneider
## [fit] Software engineer, Brand Networks
