# Lisk Core Troubleshooting
 
## Overview

### Setup
- **[Binary]** [A process is already listening on port 5432](#a-process-is-already-listening-on-port-5432-binary)
- **[Source]** [error: role "lisk" does not exist](#role-lisk-does-not-exist-source)
- **[Source]** [Nothing shown in console after starting Lisk Core](#nothing-shown-in-console-after-starting-lisk-core-source)

### Administration
- [Enable forging: delegate not found](#enable-forging-delegate-not-found)
- [Enable forging: Invalid password and public key combination](#enable-forging-invalid-password-and-public-key-combination)

## Setup

### A process is already listening on port 5432 (Binary)

#### Problem:
After running `installLisk.sh`, the installation script is aborted with the following output:
```
Error: A process is already listening on port 5432
PostgreSQL by default listens on 127.0.0.1:5432 and attempting to run two instances at the same time will result in this installation failing
To proceed anyway, use the -i flag to ignore the warning.
```
PostgreSQL is already installed on your system and listening to the PostgreSQL default port 5432.
This can happen e.g. when a second Lisk Core node is installed on the same server.

#### Solution 1:
If postgreSQL has been installed globally on the system, disable it:
```bash
sudo systemctl stop postgresql
sudo systemctl disable postgresql
```
Possible data inside of databases remains stored in this case.

#### Solution 2:
If postgreSQL has been installed globally on the system and the data in it is not needed anymore, simply remove the already installed postgreSQL by running the following command:
```bash
sudo apt-get --purge remove postgresql postgresql-doc postgresql-common
```

### Role "lisk" does not exist (Source)

#### Problem:
Starting the Lisk node fails with error: 
```
error: role "lisk" does not exist
```
Lisk Core expects a Postgres user called "lisk" exists on the system and has the rights to create a database.
This user is specified in `config.json`.
If the user is not present on the system, the above error will be thrown.

#### Solution 1: create lisk user (recommended)
Create a Postgres user with name "lisk" and grant it the right to create databases.
```bash
  sudo -u postgres createuser --createdb lisk
```

#### Solution 2: change `db.user` from "lisk" to custom username

Edit [`config.json`](configuration.md) and replace the value "lisk" in `db.user` with an alternative Postgres username on the system, that has the right to create databases.

### Nothing shown in the console after starting Lisk Core (Source)

#### Problem: 
After installing from Source and starting Lisk Core with `npm start`, no are logs visible in the console.
This is, in fact, an expected behavior, as the default console logging value in the config is `none`, which means no logs are shown in the console after starting the process.

#### Solution: 
To verify, that your installation works as expected, you can change the`consoleLogLevel` to `error`, `info` or `debug`.
Alternatively, you can check the log files located in `logs/`, which are on `info` logging level by default.

## Administration

### Enable forging: Delegate not found
#### Problem:
When trying to activate forging on your node, it answers with `Delegate with publicKey: xyz not found`
#### Solution 1: Node still syncing
Check the current height of your Node and compare it with the Height in Explorer.
If your Nodes' height is significantly lower than the height shown in the Explorer, it means your Node is still syncing/downloading the Lisk Blockchain. At this time, enabling forging might fail, because the Delegate registration has not been downloaded, yet.
To solve it, just wait until your Node is fully synced.
#### Solution 2: Missing data in config
Check your `config.json` in section `forging.delegates`.
If you want to enable forging for a particular delegate on your node, you need to store an object with the delegates' public key and encrypted passphrase in that section as described in the [configuration](configuration.md#forging) section.

### Enable forging: Invalid password and public key combination
#### Problem:
When trying to activate forging on a node like described in section [Enable/Disable forging](configuration.md#enable-disable-forging), it responds with: `{"message":"\"Invalid password and public key combination\""}`.
#### Solution:
As the message states, the provided combination of your delegates publicKey and the password don't seem to be valid. Please ensure, both properties are set to the correct values, especially that you don't use the original passphrase of your account with that command.

We further explain the chosen naming to avoid confusion:
- **Passphrase** is always referring to your 12-word long mnemonic passphrase that was created at the same time as your Lisk ID. You should always keep this secure and private! For communication with the API, the passphrase is not passed in plaintext. Instead, the password is passed so you use it to encrypt your passphrase and the encrypted passphrase is stored in your [config](configuration.md).
- **Password** is always referring to the secret word/s you use to encrypt your passphrase symmetrically like described in the [Forging section](configuration.md#forging).

Should you have any further queries please reach out to one of the team or the Lisk community on [Lisk Chat](https://lisk.chat/home)
