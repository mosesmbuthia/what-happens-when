## What happens when you type google.com in your browser and press Enter?

When you type google.com in your browser and press, Enter, many things are going on in the background before Google’s homepage is displayed on your screen. Sure, it happens in milliseconds, but a lot happens under the hood.

In this article, we are going to see the networking side of the process and give you a little bit of an understanding of what goes on under the hood for us to get the results that appear on our web browser.

### Brief introduction on a Browser
A browser is a software program used to locate and display information on the Internet or an intranet. Browsers are most often used to access Web pages. Most can display graphics, photographs and text; multimedia information (e.g., sound and video) may require additional software, often referred to as “plug-ins.”

You can think of it as an intermediary between you and the Internet that helps you navigate websites and interact with various online content using `URLs`.

**URL** - Universal Resourse Locator 

This is the text that you type in the browser and in our case `google.com`

Browsers are programs such as , Google Chrome, Safari, Mozzilla Firefox, Brave browser and Microsoft Edge.

## DNS Request
So, what is a DNS request? 
 A DNS(Domain Name System) is like a phonebook of the internet.

 For example, Humans use names to identify each other, or if you want to save the mobile number of your friend, instead of memorizing the whole number which might be hard to remember, we save them using simple names that can be memorized faster but the name represents the friends mobile number. 

 That same way is also how the DNS works. Web browsers communicate with the internet using IP Addresses (Internet Protocal). If a user wants to visit a page such as google.com, instead of the user memorizing the Internet Protocal Address for google.com, the DNS server does that for you. 

 It converts `google.com` from text to an IP address which is readable by the browser. That is what we call a DNS request.

 This is a process that happens in several stages as follows.

 1. After typing your URL, the browser looks into its cache to see if it has a record matching the domain name to its IP address. If it has the record, the browser uses the IP address to send a request to the server.

 2. If it can't find the IP address for the URL requested then it asks your operating system to locate the website. The first place your operating system is going to check for the address of the URL you specified is in the host file. If the URL is not found inside this file, then the OS will make a DNS request to find the IP Address of the web page.

 3. The first step is to ask the Resolver (or Internet Service Provider) server to look up its cache to see if it knows the IP Address, if the Resolver does not know then it asks the root server to ask the .COM TLD (Top Level Domain) server - if your URL ends in .net then the TLD server would be .NET and so on - the TLD server will again check in its cache to see if the requested IP Address is there. 

4. If not, then it will have at least one of the authoritative name servers associated with that URL, and after going to the Name Server, it will return the IP Address associated with your URL. All this is done in a matter of milliseconds.

5. After the OS has the IP Address and gives it to the browser, it then makes a GET (a type of HTTP Method) to the said IP Address. When the request is made the browser again makes the request to the OS which then, in turn, packs the request in the TCP traffic protocol it is then sent to the IP Address. 




