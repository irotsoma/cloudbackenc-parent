# cloudbackenc

This application is designed to allow users to encrypt files and store them using various cloud services.  The system will upload files to the cloud services that have available space according to user preferences allowing for the user to distribute files to multiple places either as a secondary backup or as a single large cloud drive.  This is similar, though not exactly the same, as the concept of Raid 0 vs Raid 1 when thinking about local drives.  It does most of this using various plugins/extensions that implement the encryption protocols as well as the cloud service file transfers.

The current architecture uses a central controller application that does most of the work and should be deployed on a server. This application connects to cloud services, encrypts/decrypts files, versions files, maintains users, etc. This application uses extensions for accessing various cloud services and to enable third party encryption libraries to be used for encryption.

The second primary application is the file controller. This application will run in the background on each individual workstation or other system that needs to back up files. Optionally, this could be run on the central controller server if files are shared to that server. The application includes a web front end for modifying user settings on the central controller as well as selecting which files need to be backed up. Additionally, a background process will monitor the file locations specified and request that the central controller create a new version when a monitored file changes.

A common library is also present which contains any shared code as well as interfaces and data types shared across applications. Other repositories are for extensions for cloud service access and encryption libraries.

NOTE: This software is in early development and not meant for use at this time except as an example for using Kotlin with Spring Boot and various other technologies.  Stay tuned for further updates as alpha and beta versions are available. Alpha version should be available in late 2019.


##### Copyright (C) 2016-2019  Irotsoma, LLC

##### This program is free software: you can redistribute it and/or modify it under the terms of the GNU Lesser General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

##### This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU Lesser General Public License for more details.

##### You should have received a copy of the GNU Lesser General Public License along with this program.  If not, see <http://www.gnu.org/licenses/>

###### <img src="./images/jetbrains-variant-4.png" height="40px" width="60px"/> Special thanks to JetBrains for donating products used in the development of this product.
