# cloudbackenc-parent



This repository contains the parts of cloudbackenc as separate sub-modules as well as some settings for Intellij IDEA to make it easier to develop the project as a whole.  If you just want to edit one part (like the common package), then check out that repository instead.

Since Intellij IDEA doesn't support git submodules very well, after checking out this repository, open a terminal in the root project directory and run:

    git submodule update --init --remote
    git submodule foreach git checkout <branch>

Where \<branch\> is the branch you are checking out (e.g. master)

This will check out the submodules for you and attach them to the proper branch so you can check in changes.  Don't check in to the parent repo.  

I strongly suggest you run this before openning the project in IDEA.  Alternately, you can open the project after checkout, immediately open the terminal and run the commands, then refresh the Gradle projects.  But if you interact with IDEA, it may start removing modules that it doesn't think exist anymore.

## Description

This application is designed to allow users to encrypt files and store them using various cloud services.  The system will upload files to the cloud services that have available space according to user preferences allowing for the user to distribute files to multiple places either as a secondary backup or as a single large cloud drive.  This is similar, though not exactly the same, as the concept of Raid 0 vs Raid 1 when thinking about local drives.  It does most of this using various plugins/extensions that implement the encryption protocols as well as the cloud service file transfers.

NOTE: This software is in very early development and not meant for use at this time.  Stay tuned for further updates as alpha and beta versions are available.  This will take a while as this is an experimental project at this time.

<span style="font-size: .5em;">
Copyright (C) 2016  Irotsoma, LLC

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU Lesser General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU Lesser General Public License for more details.

You should have received a copy of the GNU Lesser General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>
</span>
