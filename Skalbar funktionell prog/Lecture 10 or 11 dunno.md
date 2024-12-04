
sneak in a jar?

frontend app talks to srever and asks for http
- we dont want stateful server that responds differently to tests each time
- want something local
- need to start up application in a mode that does not call http

-- company?
använder java http

have a send api that sends java client and request osv... public interface sender

sendermock
- instead of sending extrat usfeull info
- from http point of view is
	- where want send
	- what kind of method using (patchoptions? put? get?)
	- headers we will send (cookies, auths)
	- what content have on body

--