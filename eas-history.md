
Doug Hanks dhanks at gmail.com
Tue Mar 28 01:24:24 EST 2006
Messages sorted by: [ date ] [ thread ] [ subject ] [ author ]
I haven't released an update to Sudosh for about a year now.  I know a
lot of people have requested a lot of features and had a lot of
questions.  I've been busy addressing those concerns and requests.
The final result is Enterprise Audit Shell (EAS).  This took me about
8 months of development time.

EAS allows organizations to centrally audit and report UNIX shell
access.  Unlike Sudosh, the audit logs are sent to a centralized
archive and reporting server.  Client server authentication and
encryption is handled by SSL.  EAS was specifically designed for
enterprise, commercial use.

I haven't setup a nice web page yet (any help appreciated), but you
may download the source and PDF documentation at:

http://download.strchr.net

List of improvements over Sudosh:

* Conforms to COBiT
* Utilized ITIL best practices
* Enterprise-view of UNIX access
* Enterprise-level audit reporting tools for Sarbanes-Oxley
* Customizable audit reports via CSS
* Embedded transactional, ACID-compliant SQL92 relational database
* Load balancing
* Disaster recovery
* SSL encryption
* SSL Public Key Infrastructure authentication
* Audit file transfers and remote command execution when used as a login shell
* Configurable default shels
* Audit logs are digitally signed for integrity
* Client and server configuration files for easy management
* Idle session timeout
* Display corporate policy before eash session

--
- Doug Hanks = dhanks(at)gmail(dot)com

