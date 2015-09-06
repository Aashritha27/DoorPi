****************************************************
DoorPi: VoIP Door-Intercomstation with Raspberry Pi
****************************************************

:DoorPi @ `PyPi`_: 
    |pypi_latest_version| |pypi_License|
    
    |pypi_downloads_day| |pypi_downloads_week| |pypi_downloads_month|

:DoorPi @ `GitHub`_: 

    |github_issues_open| |github_issues_all|
    
    |github_watchs| |github_stars| |github_forks|


.. contents::
    :local:
    :depth: 2
    :backlinks: none


=============
Deutsch
=============
---------------
Einf�hrung
---------------
Ziel des Projektes DoorPi ist die Steuerung einer T�rsprechanlage mittels einem Einplatiniencomputer wie dem Raspberry Pi und dem Kommunikationsprotokoll `VoIP`_.

DoorPi ist ein Event-Action basierendes System. Es gibt Komponenten die Events ausl�sen und Komponenten die aufgrund dieser Events reagieren. Dazu sollen Ereignisse (Events) wie "Dr�cken einer T�rklingel" oder "RFID Chip xyz vorgehalten" die Ausl�ser von Aktionen (Actions) wie "Anruf bei Telefon xyz", "E-Mail an xxx" oder "�ffne T�r" sein.

---------------
Event-Quellen
---------------

Um diese Events zu registrieren werden "DoorPi-Keyboards" genutzt, was z.B.:

* die GPIO-Pins
* ein PiFace 
* Dateien im Dateisystem des Pi (z.B. f�r Remote-Befehle �ber SSH)
* die serielle Schnittstelle (RDM6300 als NFC Reader)
* Webservice mit Authentifizierung
* VoIP-Telefon

sein k�nnen.

An jedes Event k�nnen beliebig viele Actions angef�gt werden, die syncron oder asyncron ausgef�hrt werden. 

-----------------
Action-Empf�nger
-----------------

Eine nicht vollst�ndige Liste der Actions ist:

* VoIP Anruf zu festgelegter Nummer starten
* VoIP Anruf zu Nummer starten, die aus einer Datei ausgelesen wird
* Anruf beenden
* E-Mail versenden
* Programm ausf�hren
* Ausgang schalten
* Status-Datei schreiben
* Werte aus IP-Symcon lesen oder zur�ck schreiben
* ...

Durch die Kombination der Events und Actions sind fast alle gew�nschten Kombinationen m�glich. 

-----------------
Beispiele
-----------------

Ein m�gliches Szenario ist:

#. Beim Druck eines Klingeltasters wird ein Anruf ausgel�st und gezielt eine Nummer angerufen (z.B. interne FritzBox Nummer \*\*613 aber auch Handynummern).
#. Der Bewohner kann mit der Au�enstelle telefonieren und auf Wunsch die T�r remote �ffnen, in dem eine definierte Taste (oder Tastenfolge) auf dem Telefon gedr�ckt wird (z.B. die Taste "#").
#. Der Bewohner vergisst das auflegen und DoorPi beendet selbst das Gespr�ch, sobald die T�r wieder geschlossen wurde.
#. DoorPi versendet eine E-Mail, dass es einen Anruf gab, jemand die T�r ge�ffnet hat und jemand ins Haus gegangen ist.

Mittlerweile gibt es auch Video-Support, so dass an der Haust�r eine Kamera installiert werden kann und das Bild auf den Innenstationen angesehen werden kann, noch bevor das Gespr�ch angenommen wird.

-----------------
Installation
-----------------

via `PyPi`_:

.. code-block:: bash

   sudo pip install doorpi &&
   sudo doorpi_cli  

via `GitHub`_:

.. code-block:: bash

   git clone https://github.com/motom001/DoorPi.git /tmp/DoorPi 
   sudo python /tmp/DoorPi/setup.py install &&
   sudo doorpi_cli  

-----------------
DoorPi Threads
-----------------

Link zu Foren mit DoorPi Threads:

:forum-raspberrypi.de: `[Haussteuerung] DoorPi (VoIP Wechselsprechanlage / T�rsprechanlage mit Video-Support) <http://www.forum-raspberrypi.de/Thread-haussteuerung-doorpi-voip-wechselsprechanlage-tuersprechanlage-mit-video-support>`_

:ip-symcon.de: `DoorPI / VoIP Door-Intercomstation with Raspberry Pi <http://www.ip-symcon.de/forum/threads/26739-DoorPI-VoIP-Door-Intercomstation-with-Raspberry-Pi>`_

=============
English
=============
---------------
Introduction
---------------

coming soon

---------------
Event-Sorces
---------------

coming soon

-----------------
Action-Receiver
-----------------

coming soon

-----------------
Examples
-----------------

coming soon

-----------------
Installation
-----------------

via `PyPi`_:

.. code-block:: bash

   sudo pip install doorpi &&
   sudo doorpi_cli  

via `GitHub`_:

.. code-block:: bash

   git clone https://github.com/motom001/DoorPi.git /tmp/DoorPi 
   sudo python /tmp/DoorPi/setup.py install &&
   sudo doorpi_cli  



.. _VoIP: https://de.wikipedia.org/wiki/IP-Telefonie
.. _PyPi: https://pypi.python.org/pypi/DoorPi
.. _GitHub: https://github.com/motom001/DoorPi

.. |pypi_License| image:: https://img.shields.io/pypi/l/DoorPi.svg
    :target: https://creativecommons.org/licenses/by-nc/4.0/
    :alt: CC BY-NC 4.0

.. |pypi_latest_version| image:: https://img.shields.io/pypi/v/DoorPi.svg?label=latest%20version
    :target: https://pypi.python.org/pypi/DoorPi
    :alt: Download

.. |pypi_downloads_day| image:: https://img.shields.io/pypi/dd/DoorPi.svg
    :target: https://pypi.python.org/pypi/DoorPi#downloads
    :alt: Downloads last day

.. |pypi_downloads_week| image:: https://img.shields.io/pypi/dw/DoorPi.svg
    :target: https://pypi.python.org/pypi/DoorPi#downloads
    :alt: Downloads last week

.. |pypi_downloads_month| image:: https://img.shields.io/pypi/dm/DoorPi.svg
    :target: https://pypi.python.org/pypi/DoorPi#downloads
    :alt: Downloads last month


.. |github_issues_open| image:: https://img.shields.io/github/issues/motom001/DoorPi.svg
    :target: https://github.com/motom001/DoorPi/issues
    :alt: open issues on github

.. |github_issues_all| image:: https://img.shields.io/github/issues-raw/badges/shields.svg
    :target: https://github.com/motom001/DoorPi/issues?utf8=%E2%9C%93&q=is%3Aissue
    :alt: all issues on github

.. |github_watchs| image:: https://img.shields.io/github/watchers/motom001/DoorPi.svg?style=social&label=watchers
    :target: https://github.com/motom001/DoorPi/watchers

.. |github_stars| image:: https://img.shields.io/github/stars/motom001/DoorPi.svg?style=social&label=stars
    :target: https://github.com/motom001/DoorPi/stargazers

.. |github_forks| image:: https://img.shields.io/github/forks/motom001/DoorPi.svg?style=social&label=forks
    :target: https://github.com/motom001/DoorPi/network
