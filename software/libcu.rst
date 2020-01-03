.. _libcu-header:

LibCu Software Library
=================================

LibCu is

Installation
------------

.. warning:: LibCu is currently C++/Java only, and is not yet available for LabVIEW

Online Installation
^^^^^^^^^^^^^^^^^^^

If your development computer is connected to the internet, you should use the online method to install the LibCu C++/Java API:

#. Open your robot project in VSCode.
#. Click the WPILib icon in the top right or press Ctrl+Shift+P to open the WPILib/VS Code Command Palette.
#. Select Manage Vendor Libraries.
#. Select Install new library (online).
#. Enter the following installation URL and press Enter:

    https://copperforge.cc/dev/maven/LibCu-latest.json

Offline Installation
^^^^^^^^^^^^^^^^^^^^

#. Download and unzip the latest LibCu C++/Java API into the ``C:\Users\Public\frc2020\`` directory.
#. Follow the offline installation instructions on `WPILib's FRC-Docs Adding an Offline-installed Library page <http://docs.wpilib.org/en/latest/docs/software/wpilib-overview/3rd-party-libraries.html#adding-an-offline-installed-library>`_.


API Docs
--------

.. tabs::

   .. code-tab:: c++

        namespace libcu
        {
        class Lasershark
        {
        public:
            Lasershark(frc::DigitalSource &source);
            Lasershark(frc::DigitalSource *source);
            Lasershark(std::shared_ptr<frc::DigitalSource> source);

            double GetDistanceFeet();
            double GetDistanceInches();
            double GetDistanceCentimeters();
        };
        } // namespace libcu

   .. code-tab:: java

        package com.cuforge.libcu;

        public class Lasershark {
            public Lasershark(DigitalSource source);

            public double getDistanceFeet();
            public double getDistanceInches();
            public double getDistanceCentimeters();
        }