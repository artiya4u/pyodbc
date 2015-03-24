pyodbc is a Python 2.x and 3.x module that allows you to use ODBC to connect to almost any database from Windows, Linux, OS/X, and more.

It implements the [Python Database API Specification v2.0](http://www.python.org/peps/pep-0249.html), but [additional features](Features.md) have been added to simplify database programming even more.

pyodbc is licensed using an MIT license, so it is free for commercial and personal use.  You can even use the source code in your own projects.

Installers for Windows are available here and most Linux distributions are starting to provide pre-compiled packages.  Full source code is also available.

**New to pyodbc?**  Check out the [Getting Started](GettingStarted.md) page.

# Latest Changes #

## 3.0.7 - 2013-05-19 ##

Added context manager support to Cursor

Added padding for driver bugs writing an extra byte

Cursor.executemany now accepts an iterator or generator.

Compilation improvements for FreeBSD, Cygwin, and OS/X

Use SQL\_DATA\_AT\_EXEC instead of SQL\_DATA\_LEN\_AT\_EXEC when possible for driver compatibility.

Row objects can now be pickled.

## 3.0.6 - 2012-06-25 ##

Added Cursor.commit() and Cursor.rollback().  It is now possible to use only a cursor in your code instead of keeping track of a connection and a cursor.

Added readonly keyword to connect.  If set to True, SQLSetConnectAttr SQL\_ATTR\_ACCESS\_MODE is set to SQL\_MODE\_READ\_ONLY.  This may provide better locking semantics or speed for some drivers.

Fixed an error reading SQL Server XML data types longer than 4K.

## 3.0.5 - 2012-02-23 ##

Fixed "function sequence" errors caused by prepared SQL not being cleared ("unprepared") when a catalog function is executed.

## 3.0.4 - 2012-01-13 ##

Fixed building on Python 2.5.  Other versions are not affected.

## 3.0.3 - 2011-12-28 ##

Update to build using gcc 4.6.2: A compiler warning was changed to an error in 4.6.2.

## 3.0.2 - 2011-12-26 ##

Version 3.0.2 is the first official pyodbc release that supports both Python 2 and Python 3 (3.2+).

Many updates were made for this version, particularly around Unicode support.  If you have outstanding issues from the 2.1.x line, please retest with this version.

If you are on Linux and connecting to SQL Server, you may also be interested in Microsoft's new Linux ODBC driver: http://www.microsoft.com/download/en/details.aspx?id=28160  Check your bitness - a Google search may be required ;)

If you are on Windows, there are prebuilt installers linked on the left.  Most Linux distributions include pyodbc in their packages, but you may need to build your own to ensure you are using the latest.  However, there is a 64-bit Fedora version RPM available on the [downloads](http://code.google.com/p/pyodbc/downloads/list) page.

## Earlier Releases ##

[Release Notes](http://code.google.com/p/pyodbc/wiki/ReleaseNotes)