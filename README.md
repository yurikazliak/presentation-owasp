# presentation-owasp
https://yurikazliak.github.io/presentation-owasp/    

(slide 1)    
My name is Yuri, and i'd like to tell about Open Web Application Security Project, or OWASP.    
(slide 2)    
This is a free from commercial pressure and not affilated whith any technology company organization.    
Almost everyone assotiated whith organization is volunteer.    
The OWASP most known project whith biggest feedback is :    
(slide 3)    
OWASP Top 10 is regulary-updated report. It consists of the top biggest Web Application Security Risks.   
Primary aim is to educate developers, designers, architects, managers, and organizations about most	common and most important web application security weaknesses.    
According to risk rating metodology,     
(Slide OWASP Risk rating metology)    
The OWASP calculate final score of risk, and ranked them, depending on this score:    
(slide risks table)    
So, Lets talk about each point in detail.    
(slide A1)    
First risk is injection.     
If a website, app, or device incorporates user input within a command, an attacker can insert a “payload” command directly into said input. If that input is not verified, an attacker then “injects” and runs their own commands.     
Why it is possible?    
(slide A1 - 2)    
Because on client side ther is bad filters to validate or sanitise input data, or bad implementation of query parametrisation.    
How to prevent?    
(slide A1 - 3)    
Blacklist of specified symbols - when user can type only letters in login field, for example. Whitelist of accepting input. Encoding 'bad' caracters, after they have been submitted. Using parameterised query.    
Next risk is     
(slide A2)    
Broken Authentication.    
Big class of vulnerability covers any weaknesses in authontification/session management.    
(slide A2 - 2)    
It happens when developers allow users to have weak or well-known passwords, like password123, or weak password recovery, or allowed long sessions, or not change session ID. Also here is all kind of automated attacks, like brute-forces.    
How to prevent?    
(slide A2 - 3)    
2 factor autontification, password validaton for strong passwords, Blacklist IP, strong session ID    
Next.    
(slide A3)    
Sensitive Data Exposure    
This vulnerability is when a web application fails to sufficiently protect sensitive data — namely personally identifiable information    
(slide A3 - 2)    
Happens when data is transmitted in clear text, or data is stored in clear text on server side, or used default/weak cryptographic keys.    
Prevent?    
(slide A3 - 3)    
Identify all data which could be considered ‘sensitive’. Note where and how it is stored, as well as if and how it is transferred. Do not store sensitive data which is no longer needed. Use tokenisation.    
Next    
(slide A4)    
XML External Entities (XXE)    
XML is a data format used to describe different data elements. XML also uses “entities” to help define related data, but entities can access remote or local content.    
(slide A4 - 2)    
An attacker sends malicious data lookup values asking the site, device, or app to request and display data from a local file. If a developer uses a common or default filename in a common location, an attacker’s job is easy.    
Prevent    
(slide A4 - 3)    
Write security-conscious code, avoid serialisation of sensitive data, use JSON instead od XML.    
Next    
(slide A5)    
Broken Access Control.    
Access control, or authorization, is how web apps let different users access different content, data, or functions. When it’s broken,or mistakenly misconfigured, attacker can access more than you should be able to.    
Prevent
(slide A5 - 2)    
There is one simple rule to keep in mind when managing access control: unless the resources must be publicly accessible, deny users from accessing them.    
(slide A6)    
Security Misconfiguration.    
This can include insecure default configurations, incomplete configurations, default usernames/passwords kept for administrative    tools/hardware, misconfigured HTTP headers or exposed error messages which guide attackers in their search for vulnerabilities.    
Prevent    
(slide A6 - 2)    
Take a minimalist approach to your web app — if a feature, framework or function is not required, remove it.    
Ensure that all available updates and patches are applied as soon as possible.       
Next    
(slide A7)    
Cross-Site Scripting (XSS)    
One of the better-known vulnerabilities.     
Put simply, Cross-Site Scripting allows an attacker to execute script(s) in a victim’s browser.    
This can be used to hijack user sessions (by getting cookies, session ID’s and so on), alter the contents of a web page or redirect a user to an evil site.    
(slide A7 - 2)    
There are 3 types of XSS: two commons and one lesser-known.    
(slide A7 - 3)    
Happens when the web app or API stores user input which is unsanitised, unescaped, unvalidated or fails to be encoded.     
prevent    
(slide A7 - 4)     
Employ a combination of validating, filtering, encoding and escaping methods to prevent untrusted user input from executing on the web app.     
Next     
(slide A8)    
Insecure Deserialisation   
Deserialisation: transforming serialised data from a file, stream or network socket into an object.    
Fundamentally, an application is likely vulnerable to this type of attack if it deserialises untrusted or tampered data inputted from a malicious source.     
prevent    
(slide A8 - 2)     
the only safe architectural pattern is not to accept serialised objects from untrusted sources or to use serialisation mediums that only permit primitive data types    
Next, my favorite:     
(slide A9)     
Using Components with Known Vulnerabilities.     
Nothing to add or to subtract.     
(slide A9 - 2)    
Update components, or remove them, if they not updatable, or already not used in project.    
Last, my favorite, part two.    
(slide A10)    
Insufficient Logging & Monitoring.     
When important events such as logins, login attempts, and significant transactions are not logged.    
Warnings and errors generate inadequate log messages, or no generate then at all.    
(slide A10 - 2)    
All important events, warnings, errors, suspicious activities must be logged!    
(slide "thank you")    
So, thats all i want to talk about, thank you for watching!    