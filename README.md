Widget i18n Messages
========

This repository contains i18n messages for the JustNudge IBM Connections widgets.

To install the mesages follow the information on IBM Connections Wiki [here](http://www-10.lotus.com/ldd/lcwiki.nsf/xpDocViewer.xsp?lookupName=IBM+Connections+4.0+documentation#action=openDocument&res_title=Adding_custom_strings_for_widgets_and_other_specified_scenarios_ic40&content=pdcontent).

The process for installing the messages is as follows:

1. Placing the message files onto the file system.
2. Defining the messages in the LotusConnections-config.xml file.
3. Defining the messages in the profiles-config.xml file.

**NOTE:** A list of sample configuration files are included, showing their before and after appearance.  If you need assistance setting up the environment it is recommended that you download the files and diff them with each other (so that you can see the before and after) and also with your configuration.

Placing message files onto the file system
--
The files should be be placed into the following directory (example below in Linux):

    /opt/IBM/Connections/data/shared/customization/strings

**NOTE:** Only the properties files need to be placed onto the file system.  The other files describe the installation process.

Defining the messages in the LotusConnections-config.xml file
--
Place the following stanza in the "resources" section of the file:

    <widgetBundle prefix="jnmessages" name="com.justnudge.messages" />

Defining the messages in the profiles-config.xml file.
--
Modify the templateNlsBundles to include the jnmessages bundle as shown below:

    <templateNlsBundles>jnmessages</templateNlsBundles>

Javascript i18n files
==
This project includes the i18n Dojo JSON files that are using by the JustNudge commercial and open source widgets.  These sources will by default download from github when the widgets are installed or can be copied and used locally.  For further details on this see the appropriate widget documentation.