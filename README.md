KUKA Welding Program Converter

This application is designed to convert additive welding programs into KUKA-specific welding instructions. It was tested using a specific post-processor in AdaOne Adaxis software, generating a program compatible with KUKA ArcTechBasic 3.4.2 (KSS 8.6.x).

Features

1.Program Conversion: The application converts general additive welding programs into instructions tailored for KUKA robotic systems, particularly for ArcTechBasic 3.4.2.

2.Process Handling: It detects ;process_on markers to initiate the ARCON command and ;process_off markers for the ARCOFF command. All lines between these markers are converted into ARCSWI instructions.

3.Velocity and Weld Data Management: The software identifies changes in velocity within the welding program and generates specific weld data entries in the .DAT file accordingly.

4.User Input: The application allows users to input a job number, which is then automatically updated in the .DAT file.

Compatibility

While the application was initially tested with AdaOne Adaxis software, it is designed to be adaptable and can be used with other path generation software that produces similar welding programs.

Below is the User interface of the application. 
![User INterface](Docs/appUI.JPG)

