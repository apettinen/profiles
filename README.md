# Profiles
Configuration profiles (.mobileconfig) for macOS

Please edit the profiles to suit your organization - i.e. change the ```my.org``` prefixes. If you feel like it, you can generate new UUIDs with https://github.com/apettinen/generateUUID

### Signing:

You can sign the profiles with the following procedure:

Find your codesigning identities:
```
security find-identity -p codesigning -v
```

Use one of the identities to sign your profile:
```
security cms -S -N "Mac Developer: MyDeveloperID (INFORMATION)" -i /path/to/MyProfile.mobileconfig -o /path/to/signed/MyProfile.mobileconfig
```
Note! Signing is not encrypting! If you need to encrypt your profiles, check for example: https://github.com/nmcspadden/ProfileSigner


#### Copyright:
2016 Tampere University of Technology

#### License:
Apache 2.0
