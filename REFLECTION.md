The path an HTTP request takes from a browser to a Github Pages site. First I look up the URL into chrome. Second, DNS my computer needs to turn the github pages site into a IP address it checks
local cache then asks a DNS resolver, which in this case looks up github.io and returns the address of the server that hosts my pages site.
Third, my browser opens a tcp connection to that ip. Fourth, HTTPS and tcp exchange certificates and establish an encrypted channel. Fifth, the browers 
sends a HTTP get request asking for the index.html. Sixth, github pages finds the static files from my repo through github and sends it back to the HTTP
Seventh, chrome reads the index.html building the page structure. Eighth, the browser finds the link tag in the index.html that points to the css file 
and img from assets and HTTP get request is sent out for those files. Ninth, Once all files are collected the browser renders them and displays them.
Tenth, once the page is built, the tcp either closes or remains open if more requests are needed like clicking the github link on the page.


HW 2 Reflection:

The difference between flex-direction: row, and flex-direction: column, is that row puts items side by side from left to right. Column stacks items on top of each other, from top to bottom. Column is useful for mobile view, and row is useful for desktop view. 

Relative units are better than fixed pixels because % is relative to the parent. In the new parts of my site I used it for navbar padding, heading size, the grid gap, and the card padding. Rem is relative to the root font size. It also respects the user's browser font size setting, so someone who has set larger text for accessibility still gets it. Vh/vw are relative to the viewport. They are useful for things like a full screen hero section. The fr is also relative. It splits the available space in the grid evenly, so the three columns resize with the screen. 
