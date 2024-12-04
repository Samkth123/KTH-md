
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

Mock helps with character mismatch, because if you print might look the same, but this shows if there is any error
- so basically send http request to mock-it or any mock framework for tests

mock-it 
- java syntax for regex
- finns nog på github
- ex: {:path "/the/path"
:http-metod "GET"}
- {:http-status 200}
- can also write with pathid: :path /the/path/:path-id
- mock response is json
- should be in logs and test enviroment

use IFn (ifunctions)


i can set mock score
- 


--