# DMCV Sharks GU10 Soccer Information, 2023

This repository is for publication of information for my DMCV Sharks GU10 team
in fall 2023.

Private information is password protected using
[StatiCrypt](https://github.com/robinmoisson/staticrypt). Encrypted pages are in
directory [private](./private/).

## How to add a new encrypted page for the first time

1. Create a new plaintext file, say, `sample.html`, and populate its content.
2. Generate password protected, encrypted page `private/sample.html`

   ```bash
   # Use orange color 'ffa500' for Team Cheetos. Enter selected password when
   # prompted
   npx staticrypt sample.html --template-color-primary "#ffa500" -d private
   ```

   Write down or remember the selected password for accessing page content.

3. Delete the plaintext file `sample.html`. Publish only the encrypted file
   `private/sample.html`.

## How to update an encrypted page

1. Decrypt the encrypted page, say, `private/sample.html`, into a plaintext file
   `decrypted/sample.html` using the right password

   ```bash
   # Enter selected password when prompted
   npx staticrypt private/sample.html --decrypt
   ```

2. Update the plaintext file `decrypted/sample.html`

3. Re-encrypt the updated plaintext file `decrypted/sample.html` to get
   encrypted `private/sample.html`

   ```bash
   # Use orange color 'ffa500' for Team Cheetos. Enter selected password when
   # prompted
   npx staticrypt decrypted/sample.html --template-color-primary "#ffa500" -d private
   ```

4. Delete the plaintext file `decrypted/sample.html`. Publish only the encrypted
   file `private/sample.html`.
