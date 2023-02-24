====================
Flashing the SD Card
====================

In some circumstances, the :abbr:`IoT (Internet of Things)` Box’s Micro SD Card may need to be
reflashed to benefit from Odoo's latest IoT image update.

Image Version from `nightly <http://nightly.odoo.com/master/iotbox/>`__:
- Odoo V15 > 21.10
- Odoo V14 > 21.06
- Odoo V13 > 20.10


Upgrade from the IoT Box homepage
=================================

Go to the :abbr:`IoT (Internet of Things)` Box homepage, and click :guilabel:`Update` (next to the
version number). If a new version of the :abbr:`IoT (Internet of Things)` Box image is available, an
:guilabel:`Upgrade` button will appear at the bottom of the page, and the :abbr:`IoT (Internet of
Things)` Box will then flash itself to the new version of the :abbr:`IoT (Internet of Things)` Box.
All of the previous configurations will be saved.

.. note::
   This process can take more than 30 minutes. Do not turn off or unplug the
   :abbr:`IoT (Internet of Things)` Box as it would leave it in an inconsistent state. This means
   that the :abbr:`IoT (Internet of Things)` Box will need to be reflashed with a new image. See
   :ref:`flash_sdcard/etcher`

.. image:: flash_sdcard/flash-upgrade.png
   :align: center
   :alt: IoT Box software upgrade in the IoT box console.

.. _flash_sdcard/etcher:

Upgrade with Etcher
===================

.. note::
   A computer is required with a Micro SD card reader/adapter in order to reflash the Micro SD.

Go to Balena's website and download `Etcher <https://www.balena.io/>`__. It's a free and open-source
utility used for burning image files. Install and launch it. Download the version specific
:abbr:`IoT (Internet of Things)` image from `nightly <http://nightly.odoo.com/master/iotbox/>`__.

Then, open *Etcher* and select :guilabel:`Flash from file`, find the image just downloaded and
extracted. Insert the :abbr:`IoT (Internet of Things)` Box Micro SD card into the computer or reader
and select it. Click on :guilabel:`Flash` and wait for the process to finish.

.. image:: flash_sdcard/etcher-app.png
   :align: center
   :alt: Balena's Etcher software dashboard.

.. note::
   An alternative software to flashing the Micro SD card with *Balena's Etcher* is *Raspberry
   Pi Imager*. Download the software `here <https://www.raspberrypi.com/software/>`__
