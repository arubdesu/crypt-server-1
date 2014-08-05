__[Crypt][1]__ is a system for centrally storing FileVault 2 recovery keys. It is made up of a client app, and a Django web app for storing the keys.

This Docker image contains the fully configured Crypt Django web app.

__Changes in this version__
=================

- 10.7 is no longer supported.
- Improved logging on errors.
- Improved user feedback during long operations (such as enabling FileVault).

__Client__
====
The client is written in Pyobjc, and makes use of the built in fdesetup on OS X 10.8 and higher. An example login hook is provided to see how this could be implemented in your organisation.

__Features__
=======
- If escrow fails for some reason, the recovery key is stored on disk and a Launch Daemon will attempt to escrow the key periodically.
- If the app cannot contact the server, it can optionally quit.
- If FileVault is already enabled, the app will quit.


  [1]: https://github.com/grahamgilbert/Crypt
