# Review-a-QGIS-Plugin-For-Development-QGIS-Plugin

![image](https://github.com/GMT-456-GIS-Programming/final-project-SametToptas/assets/92017600/b81fcb04-2e04-4bae-b568-53d50ea8baa3)

**GMT 456 – GIS Programming**

**2023 – 24 Fall**

**FINAL Project**

**Assoc. Prof. Dr. Berk ANBAROĞLU**

**Due date; Sunday, 21 January 2023, 11:59 PM**

**Abdulsamet TOPTAŞ -21905024**

# CONTENT

**1- About qgis2web (REVIEW)**

**2- Document Review**

**3- Python Code Analysis**

**4- Tests**

**5- Experimental Setup**

**6- Bug**


# 1- About qgis2web (REVIEW)

The plugin I will be reviewing is "qgis2web," which I haven't used before but aim to learn as part of this project. I believe it would be more meaningful to learn a plugin that I haven't used before, especially for the purposes of my thesis and individual projects, as opposed to revisiting one I am already familiar with. This way, I can both acquire knowledge about a new plugin and analyze the process of creating and coding it.

The plugin under review is a QGIS plugin called "qgis2web." The qgis2web extension in QGIS is a tool used to convert QGIS projects into web maps. With this plugin, you can transform your QGIS projects into various web map formats and platforms. Using qgis2web, you can export your project to an OpenLayers or Leaflet web map. It replicates as many aspects of the project as possible, including layers, extent, and styles (including categorized and graduated ones). No server-side software is required.

**Features of the plugin;**

**1 - Different Output Formats:** qgis2web supports various output formats compatible with popular web map libraries such as Leaflet, OpenLayers, and Google Maps. This allows you to convert your project into a web map compatible with the desired map library.

**2 - Layer Support:** You can transfer layers, labels, symbols, and popup information from your QGIS project to the web map while preserving their configurations.

**3 - Map Settings:** qgis2web enables customization of map styles and configuration of map elements. You can edit features like colors, transparency, and layer visibility.

**4 - Map Interactivity:** Add interactive features to your map, including thematic coloring, queries, search functionality, and zoom capabilities.

**5 - Easy Web Integration:** Share the created web map easily or integrate it into your own website with straightforward methods.

**6 - Map Transformation:** qgis2web allows you to transform a QGIS project into an HTML, CSS, and JavaScript-based web map, facilitating the sharing of your created maps on the web.

**7 - Various Map Types:** The plugin supports different map types, including Open Street Map, Esri World Street Map, Google Maps, Leaflet, OpenLayers, and other supported map libraries.

**8 - Layer Support:** Integrate different layers, themes, and interactive elements from your QGIS project into the web map while maintaining their configurations.

**9 - Responsive Design:** The created web map features a responsive design suitable for mobile devices and various screen sizes.

**10 - Customization Options:** qgis2web offers various options for customizing the appearance and behavior of the created web map. You can customize features ranging from colors to popup information.

# 2- Document Review

**First of all, if I examine the documentation of the plugin,**

![image](https://github.com/GMT-456-GIS-Programming/final-project-SametToptas/assets/92017600/19fcdc43-bcb5-4c35-a504-e313e6012d9b)


**__init__.py:** This file initializes the Python package. Typically, it contains settings and definitions for the package's initial configuration.

**CODE_OF_CONDUCT.md:** This file contains the code of conduct, outlining the behavioral rules and community guidelines for the project.

**configparams.py:** This file includes information related to configuration parameters, likely containing settings, configuration parameters, and similar information used in the project.

**CONTRIBUTING.md:** The file provides guidance and contribution rules for developers interested in contributing to the project. It explains how contributions can be made and how code should be submitted.

**exp2js.py:** This file likely involves a script or function related to "export to JavaScript," potentially transforming something related to QGIS into JavaScript.

**exporter.py:** This file may be related to a data export function, containing functions to transform project data into another format.

**feedbackDialog.py:** This file likely contains a Python script for a feedback dialog or window that handles feedback from users.

**helpFile:** This file may contain the general help documentation for the project, providing guidance and explanations on how to use the project for users.

**ISSUE_TEMPLATE:** This file includes templates to be filled out when creating new issues on the GitHub repository, specifying basic information users need to provide when creating an issue.

**leafletFileScripts:** This folder may contain scripts used to process and manage Leaflet map files. Leaflet is a JavaScript library commonly used to create interactive maps.

**leafletLayerScripts:** This folder may contain scripts used to process and manage layers in Leaflet maps. Layers correspond to data layers displayed on the map.

**leafletScriptStrings:** This folder may contain strings used in Leaflet map creation processes. These strings often include descriptions, labels, or other text-based elements displayed on the map.

**leafletStyleScripts:** This folder may contain scripts used to determine the style of elements (layers, markers, etc.) in Leaflet maps. It includes features such as colors, line styles, fill styles, and other visual attributes.

**leafletWriter.py:** This file may contain the Python script responsible for generating map files in the Leaflet format.

**LICENSE:** This file outlines the terms and license under which the project is available, providing information on how others can use and distribute the project.

**maindialog.py:** This file typically contains the Python script for the main window or main dialog box, managing the basic components of the user interface.

**Makefile:** This file may contain a Makefile script used to automate project compilation and configuration processes.

**metadata:** This file may contain metadata information about the project, including basic details, version numbers, authors, and other relevant information.

**olFileScripts:** This folder may contain scripts used to create and process OpenLayers map files. OpenLayers is a JavaScript library commonly used to create interactive maps.

**olLayerScripts:** This folder may contain scripts used to manage, edit, and create layers in OpenLayers maps.

**olScriptStrings:** This folder may contain strings used in creating OpenLayers maps, often including descriptions, labels, or other text-based elements.

**olStyleScripts:** This folder may contain scripts used to determine the style of elements (layers, markers, lines, etc.) in OpenLayers maps.

**olwriter.py:** This file may contain the Python script responsible for generating map files in the OpenLayers format.

**package:** This directory represents the Python package and contains the modules of the project. These modules may include functions, classes, and other elements used in different sections of the project.

**qgis2web:** This directory contains the essential files for the qgis2web plugin, which is used to convert QGIS map projects into web maps using Python scripts.

**qgis2webAlgorithm:** This directory may contain qgis2web algorithms, which process and transform QGIS data into web maps.

**qgis2webProvider:** This directory may contain qgis2web data providers, dealing with how to access QGIS data and integrate it into a web map.

**README:** This file typically contains general information about the project, usage guidelines, and information about contributing to the project.

**resources:** This directory contains general resource files for the project, often including images, icons, and other media elements.

**resources.qrc:** This file is a Qt Resource Collection file, defining the project's resource files.

**ui_feedback_dialog.py:** This file contains the Python code for a feedback dialog created using PyQt5.

**ui_feedback_dialog.ui:** This file contains the XML representation of the feedback dialog designed using tools like PyQt5 Designer or Qt Creator.

**ui_ftp_configuration.py:** This file contains the Python code for an FTP configuration window created using PyQt5.

**ui_ftp_configuration.ui:** This file contains the XML representation of the FTP configuration window designed using tools like PyQt5 Designer or Qt Creator.

**ui_maindialog.py:** This file contains the Python code for the main dialog box created using PyQt5.

**ui_maindialog.ui:** This file contains the XML representation of the main dialog box designed using tools like PyQt5 Designer or Qt Creator.

**utils:** This directory contains utility tools and functions, likely serving as a module with helper functions.

**writer:** This directory contains the writer module used for creating map files.

**writerRegistry:** This may be a registry that records writer modules.

**xmltodict:** This directory contains a library for converting XML files to Python dictionaries.

**icons:** This folder contains icons used in the project, often associated with buttons, tools, or other graphical elements in the user interface.

**leaflet:** This folder contains files specific to the Leaflet map library, a JavaScript library used to create web maps.

**openlayers:** This folder contains files specific to the OpenLayers map library, a JavaScript library used to create interactive maps.

**templates:** This folder contains files related to user interface or map templates. These files determine the design and content of the webpage, typically using HTML or other template types.

**webfonts:** This folder contains files related to web fonts used in the project. If custom fonts are used on the webpage, these files are often located in this folder.

**z_old:** This folder is often used to store old or unused files. It is commonly used to retain old files when updates or edits are made to the project.

These folders usually contain files for different components of the project, such as its configuration and user interface. For example, the "icons" folder may contain icon files, while the "templates" folder may contain HTML files that determine the design of the web page. The "leaflet" and "openlayers" folders contain files for the map libraries used.

**If I examine the codes in the main documents that make up the plugin;**

There are many documents that make up the qgis2web plugin, but here I will talk about the five main lines that make up the plugin and analyze the codes contained in these documents.

**1 - qgis2web:** The Python module in the main directory with this name contains the main codes of the qgis1web plugin. This module usually contains main pieces of code, such as initializing the plugin, creating the main window, and defining basic functions.

**2 - maindialog.py:** Contains Python code related to the main dialog. The main dialog is a core part of the user interface and is often used for map creation options and other settings.

**3 - writer.py:** Contains the Python script that creates map files. This file creates files suitable for the selected map format (Leaflet, OpenLayers, etc.), based on the QGIS project.

**4 - exporter.py:** Contains Python code for exporting map data. This file interacts with other modules in the QGIS project that process data and create map files.

**5 - utils:** Contains a module containing utility tools. These files usually contain auxiliary functions and tools used in the project.

The qgis2web plugin enables the conversion of map projects created within QGIS into web pages when these files come together. The main dialog box allows users to configure options during this conversion process. The Writer module determines how the map will appear on the webpage by generating files compatible with the selected map format. The Exporter module accesses the data in the QGIS project to create map files and ensures the proper integration of these files.

# 3- Python Code Analysis

## qgis2web.py Analysis

![image](https://github.com/GMT-456-GIS-Programming/final-project-SametToptas/assets/92017600/cec0faa1-aa99-4fea-9abf-6fb4bfb128b7)

**from qgis.PyQt.QtCore import Qt:** Imports the Qt module from the PyQt library.
**from qgis.PyQt.QtWidgets import QAction:** Imports the QAction class to be used in QGIS.
**from qgis.PyQt.QtGui import QIcon:** Imports the QIcon class.
**from qgis.core import QgsApplication:** Imports the QgsApplication class.
**import sip:** Imports the SIP module.
**import os:** Imports the OS module.


**Class Method:**

**class Qgis2Web(object)::** A class named Qgis2Web is created. This class provides management of the Qgis2Web plugin within QGIS.

**init Method:**

**def __init__(self, iface)::** Initializer method of the class. The iface (interface) parameter is an object that provides access to the QGIS interface.
**self.provider = qgis2webProvider():** A provider object named qgis2webProvider is created and assigned to the self.provider variable.
**self.iface = iface:** The iface variable is assigned, which provides access to the QGIS interface.
**self.dlg = None:** A variable is created to hold the dialog window and is initially assigned to None.

**initGui Method:**

**def initGui(self)::** This is the method that performs the settings that must be initially added to the QGIS plugin's interface.
**QgsApplication.processingRegistry().addProvider(self.provider):** The created provider object is added to the Processing module.
**icon = os.path.join(os.path.dirname(__file__), "icons", "qgis2web.png"):** Specifies the file path of the plugin icon.
**self.action = QAction(QIcon(icon), u"Create web map", self.iface.mainWindow()):** The QAction object is created. This action represents an option called "Create web map" in the QGIS interface.
**self.action.triggered.connect(self.run):** Calls the self.run method if the action is triggered.
**self.iface.addPluginToWebMenu(u"&qgis2web", self.action):** Adds the plugin to the QGIS menu.
**self.iface.addToolBarIcon(self.action):** Adds the add-on icon to the QGIS interface.

**unload Method:**

**def unload(self)::** This is the method that performs the cleaning operations that need to be done in case the plugin is uninstalled.
**QgsApplication.processingRegistry().removeProvider(self.provider):** Removes the provider object from the Processing module.
**self.iface.removePluginWebMenu(u"&qgis2web", self.action):** Removes the plugin from the QGIS menu.
**self.iface.removeToolBarIcon(self.action):** Removes the plugin icon from the QGIS interface.

**run Method:**

**def run(self)::** This is the method called when the plugin is run.
**if not self.dlg or sip.isdeleted(self.dlg)::** If the dialog window (self.dlg) has not been created before or delete it

These Python codes establish the fundamental structure for the "qgis2web" plugin, designed to work within QGIS. The plugin aims to convert QGIS projects into web maps.

The initializer method (init) configures the basic settings of the plugin, particularly providing access to the QGIS interface. The "initGui" method integrates the plugin into the QGIS interface. Cleanup procedures for when the plugin is unloaded are encapsulated in the "unload" method. The "run" method is invoked when the plugin is initiated, presenting the user with a dialog box offering the option to create a web map.

The plugin collaborates with the QGIS Processing module to manage map creation processes and interacts with the QGIS interface using the PyQt library. The "qgis2webProvider" class facilitates the integration of the plugin with the Processing module, encompassing its core functionality. It also works in conjunction with other modules handling the plugin icon and user interface configurations.


## qgis2webAlgorithm.py Analysis

**qgis2webAlgorithm Class:** This class represents a fundamental algorithm class that interacts with the QGIS Processing module. Methods like "createInstance," "group," and "groupId" define essential properties of the algorithm.

**exportProject Class:** This class contains an algorithm for converting a QGIS project into a web map. The "initAlgorithm" and "processAlgorithm" methods specify the input parameters and processing steps of the algorithm.

**exportLayer, exportVector, exportRaster Classes:** These classes comprise customized algorithms for converting different types of layers (vector, raster) into a web map. The "initAlgorithm" and "processAlgorithm" methods of each class define processes specific to the corresponding layer type.

The overall purpose of the code is to provide the necessary algorithms and processes for converting QGIS project data into a web map. These algorithms are designed to work appropriately for different types of data layers (vector, raster).

## ui_maindialog.py Analysis

The ui_maindialog code contains the Python implementation code of a PyQt5-based UI file that defines a user interface (UI) for the "qgis2web" plugin. This code contains PyQt5 UI code that forms the interface of the main window of the qgis2web plugin, which aims to convert QGIS projects into web maps.

First of all, this part is the interface creation part in general. I can explain a few notable features by looking at the general structure of the code;

**Tab Widget and Tabs:** The code creates a tab interface using the QTabWidget class in PyQt5. QTabWidget is used to switch between tabs. Each tab represents a specific section (Export, Settings, Help).

**Layouts and Components:** A number of component layouts have been created using different layout classes (e.g. QHBoxLayout, QVBoxLayout) and components (e.g. QTreeWidget, QRadioButton, QPushButton) in PyQt5.

**Translation and Styling:** Some functions are defined to use PyQt5's language translation and styling features (for example, _translate and setStyleSheet). This is used to set the language properties and appearance of the user interface.

## exporter.py Analysis

![image](https://github.com/GMT-456-GIS-Programming/final-project-SametToptas/assets/92017600/5f8f0c3c-6812-47c1-9bd2-5b106283345c)
![image](https://github.com/GMT-456-GIS-Programming/final-project-SametToptas/assets/92017600/5b8e688d-6d62-4414-935b-ea3b5cd4668c)
![image](https://github.com/GMT-456-GIS-Programming/final-project-SametToptas/assets/92017600/c5b8e92f-70bc-48fe-9fa5-e4c16c2a4217)
![image](https://github.com/GMT-456-GIS-Programming/final-project-SametToptas/assets/92017600/5aef477a-b10f-4006-a578-56b4f27550ed)
![image](https://github.com/GMT-456-GIS-Programming/final-project-SametToptas/assets/92017600/965038df-7300-4b7e-96bf-93cb02d4edbf)
![image](https://github.com/GMT-456-GIS-Programming/final-project-SametToptas/assets/92017600/d7458fe3-3de8-4f17-905d-0a2df24ad3f0)
![image](https://github.com/GMT-456-GIS-Programming/final-project-SametToptas/assets/92017600/42ee7f12-c24a-48c4-9c97-ca78bf49b32f)
![image](https://github.com/GMT-456-GIS-Programming/final-project-SametToptas/assets/92017600/8fd6175f-8aaf-4bc2-8d0f-4a0e6b7aa7e4)
![image](https://github.com/GMT-456-GIS-Programming/final-project-SametToptas/assets/92017600/86c74767-e2e2-4925-8257-caf1003a3f3b)


**Modules and Libraries:** The code uses the QGIS Python API (qgis.core) and the PyQt library. It also imports classes and functions from other parts of the plugin (utils, feedbackDialog, ui_ftp_configuration).

**Exporter Classes:** The Exporter class is a base class that represents general web map export functionality. Below this class, there are two special export classes designed for different targets: FolderExporter and FtpExporter. The first saves the map in a folder, while the second uploads the map to an FTP server.

**FTP Configuration Dialog:** The FtpConfigurationDialog class represents a window in which the user can specify FTP connection settings.

**ExporterRegistry:** The ExporterRegistry class manages the available export options. This class contains all export classes and can create an export class using settings saved in the project. It can also write the settings saved in the project to an export class.

**Exporter Factory and Configuration Dialogs:** The code contains factory methods (createFromProject) and corresponding configuration dialogs (configure) for different export types.

**FTP Export Functionality:** The FtpExporter class contains the functionality to upload files to the FTP server. It receives connection information from the user and uploads the files to the server.

**Other Helper Functions:** newTempFolder is a helper function used to create temporary folder.

This python code includes web map export functionality used to export and save data to different destinations (e.g. folder, FTP server) when creating a web map. The overall task of the code is to manage the web map creation process and export data to different destinations.

**Exporter Class:**

**__init__(self):** The base class's initializer method does not perform any special initialization.

**type(cls):** Class method that determines the type of the class.

**name(cls):** Class method that returns the user-friendly name of the class.

**configure(self):** Method that opens a window or dialog for configuring the export. This method must be implemented by subclasses.

**exportDirectory(self):** Method that returns the directory where the export files will be saved. Must be implemented by subclasses.

**postProcess(self, results, feedback=None):** Method called after the HTML output is created and written to exportDirectory. Relevant subclasses can perform the final operations of the export by implementing this method.

**destinationUrl(self):** Method that returns the URL of the results of the export, either on the local file system or in a remote location.

**writeToProject(self):** Method that writes Exporter's settings to the QGIS project.

**readFromProject(self):** Method that reads the Exporter's settings from the QGIS project.

**FolderExporter Class:**

**__init__(self):** Calls the initializer method of the Exporter class and initializes the folder and export_file variables.

**type(cls):** Class method that determines the type of 'folder'.

**name(cls):** Class method that returns the name 'Export to folder'.

**configure(self, parent_widget=None):** Method that opens a directory selection window for configuring the export.

**postProcess(self, results, feedback=None):** Implements the postProcess method of the Exporter class and returns the value it returns.

**destinationUrl(self):** Method that returns the URL of the results of the export, either on the local file system or in a remote location.

**writeToProject(self):** Implements the writeToProject method of the Exporter class.

**FtpExporter Class:**

**__init__(self):** Calls the initializer method of the Exporter class and initializes FTP-related settings.

**type(cls):** Class method that determines the type of 'ftp'.

**name(cls):** Class method that returns the name 'Export to FTP site'.

**configure(self, parent_widget=None):** Method that opens a window for configuring FTP connection settings.

**exportDirectory(self):** Method that creates a temporary folder and returns the path of this folder.

**postProcess(self, results, feedback=None):** Method that performs the necessary operations to upload files to the FTP server.

**destinationUrl(self):** Method that returns the URL of the results of the export on a remote FTP server.

**writeToProject(self):** Implements the writeToProject method of the Exporter class.

## qgis2webProvider.py Analysis

![image](https://github.com/GMT-456-GIS-Programming/final-project-SametToptas/assets/92017600/95c77e49-8631-4f6a-a881-cb49039f88b0)
![image](https://github.com/GMT-456-GIS-Programming/final-project-SametToptas/assets/92017600/06711136-df79-42ca-9d4c-4c21845fd9c2)


**Module and Class Imports:**

**from qgis.core import QgsProcessingProvider:** This line imports a provider of the QGIS Processing Framework. Processing Framework is used to automate workflows and combine algorithms within QGIS.

**from .qgis2webAlgorithm import exportProject, exportVector, exportRaster:** This line imports the basic algorithms of the QGIS2Web plugin. These algorithms are used to convert map projects, vector data, and raster data into web maps.

**Module Information:**

__author__, __date__, __copyright__, __revision__: This section contains general information about the module and plugin. For example, the plugin's author, date, copyright information and revision (version) information are included.

**qgis2webProvider Class:**

**__init__(self):** It is the initializer method of the class. This method uses the activate variable to check if the provider is active. Currently, this variable is left inactive.

**unload(self):** Defines the provider's unload function. This method must implement the unload functionality of the provider. However, it is currently left inactive.

**id(self):** This is the method that returns the name of the provider (toolbox group name). QGIS Processing Framework groups algorithms using this name.

**name(self):** This is the method that returns the full name of the provider. This name appears as the fully qualified name of the provider in QGIS Processing Framework.

**icon(self):** This is the method that returns the icon of the provider. Currently, a default icon is used.

**load(self):** This is the method called when loading the provider. This method is used by the Processing Framework to update the provider's algorithms and populate the list. Here it updates the list of algorithms by calling the refreshAlgorithms method.

**loadAlgorithms(self):** This is the method that creates and fills the list of algorithms. This method is constantly called by the Processing Framework and updates the list of algorithms.

**Algorithms:**

**exportProject, exportVector, exportRaster:** These algorithms implement the core functionality of the QGIS2Web plugin. Each performs a specific task. For example, exportProject converts the project file, exportVector converts vector data, and exportRaster converts raster data into web maps. These algorithms can be recognized by the Processing Framework and made available in the QGIS Processing window.


These codes contain a provider class that manages the interaction of the qgis2web plug-in with the Processing Framework. This provider provides the list of algorithms recognized by the Processing Framework and makes these algorithms available in the QGIS Processing window.

## writer.py Analysis

![image](https://github.com/GMT-456-GIS-Programming/final-project-SametToptas/assets/92017600/fb1123a1-83ac-47b7-b3ea-d3627df9050b)
![image](https://github.com/GMT-456-GIS-Programming/final-project-SametToptas/assets/92017600/edcc0e4b-e234-4a96-a363-dc5978b40cfe)

The Writer class provides a basic structure for creating the HTML, JavaScript, and other necessary assets of the web map. It also manages the configuration for the generated map.

**WriterResult Class:**

**The WriterResult** class is used to store the results of a write operation.

**index_file:** Represents the main file (usually index.html) of the created web map.

**older:** Specifies the folder where the map is created.

**files:** Contains a list of other files used to create the relevant map.

**Writer Class:**

**__init__(self):** It is the initializer method of the base Writer class. This method creates the basic variables and structures needed to write a web map.

**type(cls):** It is a class method and returns a unique string representing an author's type.

**name(cls):** It is a class method and returns a user-friendly author name.

**write(self, iface, dest_folder, feedback=None):** This method provides the basic functionality for creating a web map. The QGIS interface (iface) takes parameters such as destination folder (dest_folder) and feedback. The implementation of this method can be extended to create a customized web map.

These codes provide the basic functionality of a Writer class and how the results of the writing operation are stored. The qgis2web plugin extends this basic Writer class and performs writing operations suitable for different output formats. This can produce output suitable for different map engines, for example Leaflet, OpenLayers, or Mapbox GL.

## utils.py Analysis

This utils.py file is a Python module that contains various helper functions of the qgis2web plugin. The task of the code includes functions to retrieve data and style information from QGIS projects when creating a web map, export this data in the appropriate format and convert it if necessary.

Below I would like to explain some important functions included in this utils.py file:

**tempFolder:** Creates the folder where temporary files will be stored or references it if available.

**getUsedFields:** Gets the used fields from a layer.

**writeTmpLayer:** Writes a layer as a temporary layer, transforming it when necessary.

**exportLayers:** Exports layers (for example, vector data as JSON or raster data as PNG).

**exportVector:** Exports a vector layer (for example, in GeoJSON format).

**exportRaster:** Exports a raster layer (for example, in PNG format).

**is25d:** Checks whether a layer has 2.5D properties (height information).

**safeName:** Safeguards a name as a URL or filename.

**replaceInTemplate:** Replaces certain values within a template.

**exportImages:** Exports images in a layer's area.

**handleHiddenField:** Controls the visibility of a field and hides it if necessary.

**getRGBAColor:** Creates the RGBA color value.

**boilType:** Simplify the data type of the field (bool, int, str, date, datetime, time, real).

**returnFilterValues:** Obtains filter values for a specific field from a layer.

These functions include helper functions used in various stages of the qgis2web plugin. In particular, it is used to export vector and raster data, process color and style information, create temporary files, and perform other common tasks.

# 4- Tests

![image](https://github.com/GMT-456-GIS-Programming/final-project-SametToptas/assets/92017600/2acaa3dd-665b-4d4b-89c2-d955e3ec09c1)

**__init__.py:**
This file specifies the start of a Python package. The presence of a file with this name in a directory marks this directory as a package in Python.

**qgis_interface.py:**
This file tests the capabilities of interacting with QGIS via the QGIS Python API. It can perform operations on QGIS API elements, such as the QgisInterface class, and check that these operations are working correctly.

**test_init.py:**
This file contains tests for starting the plugin. It usually checks the basic functionality of the plugin.

**test_qgis_environment.py:**
This file tests the QGIS Python environment. That is, it checks whether the plugin works compatible with QGIS.

**test_qgis2web_dialog.py:**
This file contains tests related to the user interface (dialog) of the qgis2web plugin. It checks whether dialogs are rendered correctly and how user input is interacted with.

**test_qgis2web_exporters.py:**
This file checks whether qgis2web creates map output formats (exporters) correctly.

**test_qgis2web_writerRegistry.py:**
This file tests whether qgis2web correctly manages a structure called Writer Registry. Writer Registry determines how it handles the output of a particular data type.

**test_qgis2web_writers.py:**
This file tests how qgis2web will handle various data types. For example, vector data, raster data or style files.

**test_resources.py:**
This file checks whether the resources used when using the plugin are handled correctly. These resources are usually icons, style files and similar files.

**utilities.py:**
This file usually contains various helper functions of the plugin. These functions provide general functions used in different parts of the code and may require testing of this file.

Each of these files is intended to test different aspects of the qgis2web plugin, improving the quality of the code and detecting errors. Testing ensures that the plugin is resilient to future changes and provides the expected functionality.

**The test_qgis2web_writers.py file** tests the main target of the qgis2web plugin. This file tests how various data types (e.g. vector data, raster data, style files) are handled. This is used to ensure the basic functionality of the plugin and to check whether it handles different types of data correctly. The tests performed in this file are intended to evaluate the overall performance and accuracy of qgis2web.

Therefore, if I examine the important test commands in the test_qgis2web_writers.py file in detail;

**The function test101_Leaflet_raster_crs** checks how a raster layer is transferred to a Leaflet map with its original coordinate reference system (CRS). This test examines the style applied to a specific raster layer, whether the map projection is configured correctly, and if the output aligns with the expected control output. Additionally, the test verifies whether the exported raster file is in the expected location.

If errors occur in this test, first ensure that the relevant map writing classes are up to date and that the project is configured correctly. Also, confirm that dependencies like Leaflet or OpenLayers are installed correctly.

On the other hand, **the function test102_Leaflet_interactive** examines how a layer is interactively displayed on a Leaflet map. This test evaluates the style applied to a specific layer, whether the map projection is configured correctly, and if the output aligns with the expected control output.

If issues arise in these tests, first check that the map writing classes and the project are properly configured. Also, ensure that map libraries like Leaflet or OpenLayers are up to date and installed correctly. To identify the source of errors, carefully review the test outputs and, if necessary, focus on resolving the problem by examining relevant documentation or source code.

# 5- Experimental Setup

First of all, I would like to answer the questions of how to download the qgis2web plugin and how to use it by making a tutorial.

Step 1: Install qgis2web Plugin

**1-** Open your QGIS program.

**2-** Go to "Plugins" -> "Manage and Install Plugins" from the menu bar.

**3-** Switch to the "Installed" tab and find and activate the "qgis2web" plugin.

Step 2: Preparing Your Map Project

**4-** Open the map you are working on in the QGIS project.

**5-** Edit and stylize your map. Set your properties such as layers, symbols, and labels.

Step 3: Using qgis2web Plugin

**6-** Go to the "Web" tab from the menu bar.

**7-** Click "qgis2web" option.

**8-** qgis2web window will open. In this window, you have options to convert your map to various web formats.

**9-** Select the output format from the "Format" section (for example, Leaflet, OpenLayers, etc.).

**10-** In the "Map" section, you can customize the general appearance of your map. Select the tools and set the starting position of the map.

**11-** In the "Data" section, determine the data tables and layers that the converted map will contain.

**12-** In the "Appearance" section, customize the appearance of the map (color schemes, symbols, etc.).

**13-** Start the conversion process by clicking the "Export" button.

Step 4: Review and Share the Converted Map

**14-** After the conversion process is completed, open the output folder.

**15-** Check your map by opening the relevant HTML file (for example, index.html) with a web browser.

**16-** The converted map can be hosted on a local server or your web server. Depending on the need, you can upload the files to a web server to share the map.

I downloaded this plugin;


![image](https://github.com/GMT-456-GIS-Programming/final-project-SametToptas/assets/92017600/260084ca-fee1-4860-b15b-bc4d81e27aa4)


I started designing a web map with this plugin;


![image](https://github.com/GMT-456-GIS-Programming/final-project-SametToptas/assets/92017600/3ad1c302-29fd-4e1e-9d12-52afd02efbbe)


I turned a map of Turkey, where each city is represented by a central point, into a web map using the qgis2web plugin.


![image](https://github.com/GMT-456-GIS-Programming/final-project-SametToptas/assets/92017600/11b01876-aa7a-428b-900b-1595aeae08d3)


Thanks to this plugin, I can leave a mark when the name of the city I want is entered using the search option on the side.

![image](https://github.com/GMT-456-GIS-Programming/final-project-SametToptas/assets/92017600/e3c18268-91c6-4aea-96e6-fc655f694e7e)

## 6- Bug

QGIS image with same region and same scale;

![image](https://github.com/GMT-456-GIS-Programming/final-project-SametToptas/assets/92017600/cab0b33b-17e6-4ceb-bbda-1fcdc74ed204)

Image designed from qgis2web with the same region and the same scale;

![image](https://github.com/GMT-456-GIS-Programming/final-project-SametToptas/assets/92017600/e195a6d4-dcd9-4478-b0c8-abd840f92efa)

As a plugin bug, there was a problem in the previous version that it could not distinguish between line thickness and line types (dashed - solid confusion). However, this problem was resolved by the authorities while the final project was under construction. However, there is still an ongoing problem that has not been detected before.

As seen in both images shared above, I drew a line on the Turkey map I created from QGIS and adjusted its thickness and saturation. I adjusted the line I drew to coincide with the center points of some provinces.

Now, when I examine these two images, the line I drew in QGIS appears to be saturated and its color more dominant, and **the point representing the center of the provinces is not visible.** However, in the web image designed with qgis2web, the line color is lighter and not saturated. **Additionally, points representing the center within the provinces appear.**
