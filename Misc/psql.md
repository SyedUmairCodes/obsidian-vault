The psql command is the command-line interface that ships with every
installation of PostgreSQL. While you can certainly use a graphical user
interface to connect and interact with the databases, a basic knowledge of
psql is mandatory in order to administer a PostgreSQL cluster. In fact, a
specific psql version is shipped with every release of PostgreSQL;
therefore, it is the most up-to-date client speaking the same language (i.e.,
protocol) of the cluster. Moreover, the client is lightweight and useful even
in emergency situations when a GUI is not available.

psql accepts several options to connect to a database, mainly the following:
-d : The database name
-U : The username
-h : The host (either an IPv4 or IPv6 address or a hostname)
If no option is specified, psql assumes your operating system user is trying
to connect to a database with the same name, and a database user with a
name that matches the operating system on a local connection. 

This means that the current operating system user ( postgres ) has required
psql to connect to a database named postgres via the PostgreSQL user
named postgres on the local machine. Explicitly, the connection could
have been requested as follows:
The first thing to note is that once a connection has been established, the
command prompt changes: psql reports the database to which the user has
been connected ( postgres ) and a sign to indicate they are a superuser ( # ).

In the case that the user is not a database administrator, a > sign is placed at the end of the prompt.
If you need to connect to a database that is named differently by your
operating system username, you need to specify it:

Similarly, if you need to connect to a database that does not correspond to
your operating username with a PostgreSQL user that is different from your
operating system username, you have to explicitly pass both parameters to
psql :

To quit from psql and close the connection to the database, you have to
type \q or quit and press Enter (you can also press CTRL + D to exit on
any Unix and Linux machines):

Once you are connected to a database via psql , you can issue any statement
you like. Statements must be terminated by a semicolon, indicating that the
next Enter key will execute the statement. The following is an example
where the Enter key has been emphasized:

Another way to execute the statement is to issue a \g command, again
followed by <ENTER> . This is useful when connecting via a terminal
emulator that has keys remapped:

Until you end a statement with a semicolon or \g , psql will keep the
content you are typing in the query buffer, so you can also edit multiple
lines of text as follows:

Note how the psql command prompt has changed on the lines following
the first one: the difference is there to remind you that you are editing a
multi-line statement and psql has not (yet) found a statement terminator
(either a semicolon or the \g ).
One useful feature of the psql query buffer is the capability to edit the
content of the query buffer in an external editor. If you issue the \e
command, your favorite editor will pop up with the content of the last-
edited query. You can then edit and refine your SQL statement as much as
you want, and once you exit the editor, psql will read what you have
produced and execute it. The editor to use is chosen with the EDITOR
operating system environment variable.

It is also possible to execute all the statements included in a file or edit a
file before executing it. As an example, assume the test.sql file has the
following content:

The file has three very simple SQL statements. In order to execute the
whole file at once, you can use the \i special command followed by the
name of the file:

As you can see, the client has executed, one after the other, every statement
within the file. If you need to edit the file without leaving psql , you can
issue \e test.sql to open your favorite editor, make changes, and come
back to the psql connection.

Every command specific to psql starts with a backslash character ( \ ). It is
possible to get some help with SQL statements and PostgreSQL commands
via the special \h command, after which you can specify the specific
statement you want help for

If you need help with the psql commands, you can issue a \? command There are also a lot of introspection commands, such as, for example, \d to
list all user-defined tables. These special commands are, under the hood, a
way to execute queries against the PostgreSQL system catalogs, which are,
in turn, registries about all objects that live in a database. The introspection commands will be shown later in the book and are useful as shortcuts to get an idea of which objects are defined in the current database.

