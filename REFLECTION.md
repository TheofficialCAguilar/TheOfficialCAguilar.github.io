The path an HTTP request takes from a browser to a Github Pages site. First I look up the URL into chrome. Second, DNS my computer needs to turn the github pages site into a IP address it checks
local cache then asks a DNS resolver, which in this case looks up github.io and returns the address of the server that hosts my pages site.
Third, my browser opens a tcp connection to that ip. Fourth, HTTPS and tcp exchange certificates and establish an encrypted channel. Fifth, the browers 
sends a HTTP get request asking for the index.html. Sixth, github pages finds the static files from my repo through github and sends it back to the HTTP
Seventh, chrome reads the index.html building the page structure. Eighth, the browser finds the link tag in the index.html that points to the css file 
and img from assets and HTTP get request is sent out for those files. Ninth, Once all files are collected the browser renders them and displays them.
Tenth, once the page is built, the tcp either closes or remains open if more requests are needed like clicking the github link on the page.
