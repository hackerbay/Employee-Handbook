---
layout: markdown_page
title: PGP Process
---

# Install GPG Keychain and import PGP keypair

On a Mac, download and install the [GPG Keychain](https://gpgtools.org) application.
Download the keypair file from the Support vault. It's attached to the
'security@gitlab.com PGP Keypair' item.
Open the GPG Keychain application and import the keypair file. It will ask for
a password. Use the password saved on the vault item.

Now you will be able to encrypt, decrypt, and share the public key with others.

# Share the public key

Users that wish to report a possible security issue may request our PGP public
key by sending an email to 'security@gitlab.com'. Right-click on the key in the
GPG Keychain application and click 'Export'. Ensure the dialog box does not have
'Include secret key in exported file' checked. Save the exported file and send
it to the requestor.

![GPG Keychain Export](/images/support/pgp/gpg_keychain_export.png)

# Decrypt text and files

If the encrypted data comes to the security email as text, decrypting is very
easy. Copy the entire block of encrypted text, right-click, go to 'Services',
then 'OpenPGP: Decrypt Selection to New Window'. After a few seconds a new
window will appear with the decrypted text.

![Decrypt text](/images/support/pgp/decrypt_text.png)

If the encrypted data comes as an attachment, start by downloading the file to
your workstation. Navigate to the file in your Finder. Right-click the file,
go to 'Services', and choose 'OpenPGP: Decrypt File'. The decrypted file will
be placed in the same directory as the encrypted file. It may have a different
name, though.

![Decrypt file](/images/support/pgp/decrypt_file.png)
