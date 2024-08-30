<H1>KUKA Welding Program Converter</H1>

This application is designed to convert additive welding programs into KUKA-specific welding instructions. It was tested using a specific post-processor in AdaOne Adaxis software, generating a program compatible with KUKA ArcTechBasic 3.4.2 (KSS 8.6.x).

<h2>Features</h2>

**-Program Conversion:** The application converts general additive welding programs into instructions tailored for KUKA robotic systems, particularly for ArcTechBasic 3.4.2.

**-Process Handling:** It detects ;process_on markers to initiate the ARCON command and ;process_off markers for the ARCOFF command. All lines between these markers are converted into ARCSWI instructions.

**-Velocity and Weld Data Management:** The software identifies changes in velocity within the welding program and generates specific weld data entries in the .DAT file accordingly.

**-User Input:** The application allows users to input a job number, which is then automatically updated in the .DAT file.

<h2>Compatibility</h2>  

While the application was initially tested with AdaOne Adaxis software, it is designed to be adaptable and can be used with other path generation software that produces similar welding programs.

**Below is the User interface of the application.**

<p align="center">
  <img src="Docs/appUI.JPG" alt="Application Interface" width="500"/>
</p>

<h2>How to Use the App</h2>

**Generate the Program:**

-The app has been tested with AdaOne software.

-Use the POST file available in the docs folder (WAAM_PP.adxp) of this repository to generate the program in AdaAxis.

**Run the Application:**

-After generating the program in AdaAxis, run the application executable(Application\dist\KukaATBConvertor.exe).

-The application interface will resemble the image provided above.

**Input the Required Paths:**

-Enter the folder path that contains the AdaAxis-generated program in the "Source Directory" section.

-Enter the folder path where the output files should be written in the "Target Directory" section.

**Default Job Number:**

-You can set a default job number that will be used when a specific layer in AdaAxis has no job number or has a job number of 0.

-In AdaAxis, set the job number for specific layers as needed. The software will use the layer-specific job number where it is provided, and the default job number where it is not.

**Convert the Program:**

-Once all fields are filled out, click "Convert" to process the program.

**Success:**

Voilà! If everything is right, you'll have your output files ready in the specified target folder.

