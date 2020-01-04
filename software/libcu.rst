.. _libcu-header:

LibCu Software Library
=================================

The LibCu C++/Java software library supports Copperforge devices including the Lasershark (Cu//2A21). Both online and offline installations are supported.

LibCu follows WPILib/FRC vendor library standards and is compatible with WPILib 2020.+

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

    https://copperforge.cc/dev/files/vendordeps/LibCu-latest.json

Offline Installation
^^^^^^^^^^^^^^^^^^^^

#. Download the `latest LibCu C++/Java API <https://copperforge.cc/dev/files/artifacts/LibCu_offline_latest.zip>`_ from the following URL:

    https://copperforge.cc/dev/files/artifacts/LibCu_offline_latest.zip

#. Download and unzip the file into the ``C:\Users\Public\wpilib\2020\`` directory:

    ``C:\Users\Public\wpilib\2020\maven``

    ``C:\Users\Public\wpilib\2020\vendordeps``

#. Follow the offline installation instructions on `WPILib's FRC-Docs Adding an Offline-installed Library page <http://docs.wpilib.org/en/latest/docs/software/wpilib-overview/3rd-party-libraries.html#adding-an-offline-installed-library>`_.


API Docs
--------

.. tabs::

   .. code-tab:: c++

        namespace libcu
        {
        class Lasershark : public frc::Sendable,
                           public frc::SendableHelper<Lasershark>
        {
        public:
            explicit Lasershark(int input);
            explicit Lasershark(frc::DigitalSource &source);
            explicit Lasershark(frc::DigitalSource *source);
            explicit Lasershark(std::shared_ptr<frc::DigitalSource> source);

            units::foot_t GetDistance();
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