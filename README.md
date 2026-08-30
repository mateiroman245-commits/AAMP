AAMP

A lightweight, open-source AMP stack for Android, bringing Apache, MariaDB, and PHP together in one simple app. AAMP lets you manage your local web server environment directly from your Android device, making mobile web development easier and more accessible.

Requirements

- Android device
- AAMP
- Termux from F-Droid

Use the F-Droid version of Termux.

Installation

1. Install Termux

Install Termux from F-Droid and open it.

Give Termux access to shared storage:

termux-setup-storage

Allow the storage permission when Android asks.

2. Update Termux

Run:

pkg update && pkg upgrade

3. Install Apache, MariaDB and PHP

Run:

pkg install apache2 mariadb php

4. Prepare AAMP

Create the required directories:

mkdir -p ~/AAMP/htdocs
mkdir -p ~/AAMP/mariadb-data

5. Configure MariaDB

Initialize the MariaDB data directory using the initialization command provided by the MariaDB package installed in your Termux environment.

The MariaDB data directory used by AAMP is:

/storage/emulated/0/AAMP/mariadb-data

6. Open AAMP

Launch the AAMP Android app.

AAMP provides controls for:

- Start Apache
- Stop Apache
- Start MariaDB
- Stop MariaDB
- Start All
- Stop All

7. Website files

Place your website files in the AAMP "htdocs" directory:

AAMP/
└── htdocs/
    ├── index.php
    ├── style.css
    └── ...

Your Apache web root is:

/storage/emulated/0/AAMP/htdocs

8. PHP

PHP files placed in the "htdocs" directory can be served through Apache once PHP is configured.

9. MariaDB

MariaDB stores its databases in:

/storage/emulated/0/AAMP/mariadb-data

AAMP can start and stop the MariaDB server directly from the Android interface.

License

AAMP is licensed under the MIT License.
