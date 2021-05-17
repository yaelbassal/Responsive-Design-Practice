# Items to Review:

1. How to use flex-grow and flex-shrink

  Reviewed:
  https://css-tricks.com/flex-grow-is-weird/
  - "Just a quick recap: flex-grow will take the remaining space and divide it by the total amount of flex grow values. The resulting quotient is multiplied by the respective flex-grow value and the result is added to each child elements initial width."

  - "There is a property called flex-basis which defines the initial size of an element. If you use flex-basis in conjunction with flex-grow the way the widths are calculated changes."

  - "The big difference if we apply flex-basis to an element is that we don’t use its initial width in our calculation anymore, but the value of its flex-basis property."

  - flex-basis behaves like the width property. You can give your elements a defined with using flex basis.

2. Better understand rem and em - rem relative to html root element, em relative to parent element. 1 em is about 16px, the browser default size. Browser converts rem and em into pixels on the browser. User can control the size of the text, and your website will respond to their settings. For the most responsive use rem units.

  - Reviewed: https://engageinteractive.co.uk/blog/em-vs-rem-vs-px

  - use rems for sizes and spacing, using ems for media queries.

  - pixels - easy to understand but have acessibility issues. Does not adapt to user's individual preferences, for instance, if a user sets a default font size in the browser.

  - REMs - font-size of root HTML element.
  - "So how can we un-break our accessibility faux pas?
    Set the root HTML font-size as a percentage. That’s a percentage of the user’s default browser font-size.A typical method is to set the HTML font-size to 62.5%. That’s because 62.5% of 16px (typical default browser font-size) is 10px. That would still make 1.6rem = 16px. This now means that if the user’s default browser font-size is changed to, for example, 20px, 1.6rem would now equal 20px. So if your user wants bigger fonts, let them. Happy designer. Happy developer. All numbers are still easy to work with.

    The ideal scenario would be to leave the HTML font-size as 100%, but that does make the maths a little bit harder. For example, 16px is now 1rem, 20px is 1.25rem, 24px is 1.5rem etc."
  - REMs - the size always refers back to the root.
  - a css pre-processor can be very helpful in these making calculations.

  - ems - EMs perform initially in a similar fashion to REMs, until it comes to nesting. Harder to keep track of the math, can become quickly unmanageable. Media queries - use ems.
  - So the safe bet would be to write something like:

              body {
                  background: blue;
                  @media screen and (min-width: 64em) {
                      background: blue;
                  }
              }

3. vh and vw for landing page.

  - Reviewed: https://css-tricks.com/fun-viewport-units/
  - The new units – vw, vh, vmin, and vmax – work similarly to existing length units like px or em, but represent a percentage of the current browser viewport.
  - "Viewport Width (vw) – A percentage of the full viewport width. 10vw will resolve to 10% of the current viewport width, or 48px on a phone that is 480px wide. The difference between % and vw is most similar to the difference between em and rem. A % length is relative to local context (containing element) width, while a vw length is relative to the full width of the browser window."
  - "Viewport Height (vh) – A percentage of the full viewport height. 10vh will resolve to 10% of the current viewport height."
  - incorporate vmin and vmax so content remains readable while being responsive.

