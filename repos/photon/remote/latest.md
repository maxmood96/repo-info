## `photon:latest`

```console
$ docker pull photon@sha256:5d9ebd735934d73465f3a83eba81e07e268b0c2be0c9489d3236aa0bcc0ccbe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:b7eb73256e917ecead459e843e917ff1be9b9270d28558f04652167e10dc9d8f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16026533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061f9e21aaf9e182aff8962e9ef3f9b342e4a26378bac0a3f2b3d6e2b4d6caa0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 13 Aug 2022 01:20:49 GMT
ADD file:7e361357e37fa126ad40f0721bf0fcebbeb16283b6d756b3709621d89f097e24 in / 
# Sat, 13 Aug 2022 01:20:49 GMT
LABEL name=Photon OS x86_64/4.0 Base Image vendor=VMware build-date=20220812
# Sat, 13 Aug 2022 01:20:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ecdb0c32fc70583e32c3851730f7686c7ffbc9e536bc68591c620924669229d7`  
		Last Modified: Sat, 13 Aug 2022 01:21:26 GMT  
		Size: 16.0 MB (16026533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:2df5c189cdd838bec758a91f45ad7ff67a6ac9a20b904dd7130b470e2510f416
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15104641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f1635f5312ecc5fbc5cf8cbc73e7545113769d59fbc40a156889d75502ba041`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 13 Aug 2022 01:46:40 GMT
ADD file:7a62dcaf94c3df7793632a1e72b14ba817fc6bd0ddd5ec7edb9844549939e71e in / 
# Sat, 13 Aug 2022 01:46:40 GMT
LABEL name=Photon OS aarch64/4.0 Base Image vendor=VMware build-date=20220812
# Sat, 13 Aug 2022 01:46:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:61e9bc6df670c4c98f4bc6660f68aa286571f1f7a673e2f8ed0e3edf0c428b0d`  
		Last Modified: Sat, 13 Aug 2022 01:47:12 GMT  
		Size: 15.1 MB (15104641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
