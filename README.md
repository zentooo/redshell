# redshell

redshells is interactive shell and shortcut tools for Redmine.

This tool is mainly for executing *batch* request to Redmine. For example:

* create related tickets for the specified ticket at once
* set version for multiple tickets

and so on.

Generic query condition support is annoying and we do not want to do try-and-error on command line tool, so issue filtering strategy is implemented by only two ways:

* specify all issue\_ids
* specify query\_id, which of created custom query on redmine

That's it.

## Required libraries

Install these libraries with pip or easy\_install.

* argparse
* python-redmine
* ipython

## Authorization

Set environment veriables below:

* REDMINE\_URL
 * Your redmine base url (e.g. http://redmine.com/)
* REDMINE\_API\_TOKEN
 * Get it on redmine's user setting page. example: http://redmine.com/my/account)

## Function

* redshell projects
 * show projects

* redshell add\_related\_tickets --target\_issue\_id $issue\_id --query\_id $query\_id
* redshell add\_related\_tickets --target\_issue\_id $issue\_id --issue\_ids $issue\_id\_1, $issue\_iid\_2, ...
 * create related tickets at once
