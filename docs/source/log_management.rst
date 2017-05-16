Log management
==============

**Note 1:** All the operations described below assume that a logbook is
already open.

**Note 2:** Any modifications made to the logs are permanent. Users
should make sure they keep up-to-date backups.

Creating a new log
------------------

To create a new log, click ``New Log`` in the ``Logbook`` menu and enter
the desired name of the log in the dialog window that appears (e.g. repeater\_contacts, dx, mobile\_log).
Alternatively, use the shortcut key combination ``Ctrl + N``.

The log name must be unique (i.e. it cannot already exist in the
logbook). Furthermore, it can only be composed of alphanumeric
characters and the underscore character, and the first character in the
name must not be a number.

**Note:** When logs are stored in the database file, field/column names from
the ADIF standard are used. However, please note that only the following
subset of all the ADIF fields is considered: CALL, QSO\_DATE, TIME\_ON,
FREQ, BAND, MODE, SUBMODE, TX\_PWR, RST\_SENT, RST\_RCVD, QSL\_SENT, QSL\_RCVD,
NOTES, NAME, ADDRESS, STATE, COUNTRY, DXCC, CQZ, ITUZ, IOTA. Visit the `ADIF website <http://adif.org/>`_ for more information about these fields.

Renaming a log
--------------

To rename the currently selected log, click ``Rename Selected Log...`` in
the ``Logbook`` menu. Remember that the log's new name cannot be the
same as another log in the logbook.

Deleting a log
--------------

To delete the currently selected log, click ``Delete Selected Log`` in
the ``Logbook`` menu. As with all database operations in PyQSO, this is
permanent and cannot be undone.

Exporting a log
---------------

While PyQSO stores logbooks in SQL format, it is possible to export
individual logs in the well-known `ADIF <http://www.adif.org/>`_ and `Cabrillo <http://wwrof.org/cabrillo/>`_ formats. Select the log to export,
and click ``Export Log as ADIF...`` or ``Export Log as Cabrillo...`` in the ``Logbook`` menu.

**Note for contesters:** Cabrillo records typically require contest QSO information in the form ``CALL RST EXCH``, where ``EXCH`` denotes exchange information (e.g. a serial number or US state). No dedicated field exists in PyQSO to store exchange information so the RST fields should be used to store both the RST report *and* exchange information, separated by a space. The ``RST Sent`` field should therefore contain the RST and exchange information that you give to the other station, and the ``RST Received`` field should contain the RST and exchange information that the other station gives you. The export process asks for your callsign (this should be the callsign used during the contest) and the contest's name which can be selected from a drop-down list. If the contest name does not appear in this list, you may enter its name manually.

Importing a log
---------------

Records can be imported from an ADIF file. Upon importing,
users can choose to store the records in a new log, or append them to an
existing log in the logbook. To import, click ``Import Log...`` in the
``Logbook`` menu.

Note that all data being imported must conform to the ADIF standard, otherwise it will
be ignored.

Printing a log
--------------

Due to restrictions on the page width, only a selection of field names
will be printed: callsign, date, time, frequency, and mode.

Filtering by callsign
---------------------

Entering an expression such as ``xyz`` into the ``Filter by callsign``
box will instantly filter out all records whose callsign field does not
contain ``xyz``.

Sorting by field
----------------

To sort a log by a particular field name, left-click the column header
that contains that field name. By default, it is the ``Index`` field
that is sorted in ascending order.

