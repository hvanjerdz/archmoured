# Pre-Installation

## The very first thing

This guide illustrates the installation process on a virtual machine. Every command and code snippet will be presented 
within code elements for easy identification and differentiation from regular text, such as this one:
```
This is a code element
```
This allows the reader to conveniently use the commands without ever reading all of these words (although 
it is not recommended).


### Installation image

In order to obtain acquire an installation image, it is recommended to download an ISO file via HTTP 
from one of the mirror sites listed on the [Arch Linux HTTP Direct Downloads](https://archlinux.org/download/).
It is recomended to verify the ISO signature to make sure it is [safe to use](https://www.theregister.com/2016/02/21/linux_mint_hacked_malwareinfected_isos_linked_from_official_site/).

Once the site of choice has been selected, the user is greeted with an index that contains the needed files. 

![Index of /iso/](imgs/Index_of_ISO.png)

Downloading the ISO file and one of the checksum txt files is necessary to see if the image matches the checksum.

![Matched checksum](imgs/Matched_Checksum.png)

It does! The SHA256 checksum can also be seen on the official website.

If the reader is _extra_ paranoid, the ISO PGP signature (the iso.sig file also found on the index) can be downloaded 
in the same directory and verified (assuming that [GnuPG](https://www.gnupg.org/), a libre encryption tool is already 
installed) with:

```sh
gpg --keyserver-options auto-key-retrieve --verify archlinux-version-x86_64.iso.sig
```

![Verified signature](imgs/Verified_Signature.png)

It is. It also matches the key fingerprint of the [Arch Linux Developer who signed the ISO](https://archlinux.org/people/developers/).

![Developer who signed it](imgs/Developer_who_signed_it.png)

### Installation medium preparation

Archmoured assumes that the reader already knows how to prepare an installation medium and boot from a live environment.
It could be said that it is left as an exercise.

> Protip: Use [Ventoy](https://www.ventoy.net) to get the most out of your installation media (most likely an USB drive). 

## Into the live environment

![Virtual_Console.png]()

### Boot mode verification

### Internet connection

### System clock configuration

### Disk partitioning

### Partition formatting

### Partition mounting

### Partition verification
