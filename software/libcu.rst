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

        class Lasershark : public frc::Sendable,
                           public frc::SendableHelper<Lasershark>
        {
        public:
            /**
             * Construct a new Lasershark on a given digital input channel.
             *
             * @param channel The channel to which to attach.
             */
            explicit Lasershark(int channel);

            /**
             * Construct a new Lasershark attached to a DigitalSource object.
             *
             * @param source The digital source to which to attach.
             */
            explicit Lasershark(frc::DigitalSource &source);

            /**
             * Construct a new Lasershark attached to a DigitalSource object.
             *
             * @param source The digital source to which to attach.
             */
            explicit Lasershark(frc::DigitalSource *source);

            /**
             * Construct a new Lasershark attached to a DigitalSource object.
             *
             * @param source The digital source to which to attach.
             */
            explicit Lasershark(std::shared_ptr<frc::DigitalSource> source);

            /**
             * Get the distance reported by the LiDAR sensor. See WPILib Units library guide.
             */
            units::foot_t GetDistance();
        };
        } // namespace libcu

   .. code-tab:: java

        public class Lasershark implements Sendable {

            /**
             * Construct a new Lasershark on a given digital input channel.
             *
             * @param channel The channel to which to attach.
             */
            public Lasershark(int channel);

            /**
             * Construct a new Lasershark attached to a DigitalSource object.
             *
             * @param source The digital source to which to attach.
             */
            public Lasershark(DigitalSource source);

            /**
             * Get the distance reported by the LiDAR sensor in feet.
             */
            public double getDistanceFeet();

            /**
             * Get the distance reported by the LiDAR sensor in inches.
             */
            public double getDistanceInches();

            /**
             * Get the distance reported by the LiDAR sensor in centimeters.
             */
            public double getDistanceCentimeters();

            /**
             * Get the distance reported by the LiDAR sensor in meters.
             */
            public double getDistanceMeters();
        }