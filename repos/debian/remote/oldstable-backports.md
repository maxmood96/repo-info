## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:7bdb113b5f94869a34ace3854d8651797c46c687ff65b7a6329446a6ddde6dff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:eac24cc9c013eeab615bbdf49e8b49c62d23a967ec3b3ad3d80689f9af006c04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53739367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e498bc081728719c3bd8b10e13906059ce32e43aa38d1ab2b59a67d192edec86`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'oldstable' '@1733097600'
# Mon, 02 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d0d23b67f8dcc8b3d84fba837834db43d499365c3d1e8fc4b37d70dd2d8748b0`  
		Last Modified: Tue, 03 Dec 2024 01:27:23 GMT  
		Size: 53.7 MB (53739143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38616613a7231ea17ed9261719b55b90305c08a293f1e105319189e645cc2654`  
		Last Modified: Tue, 03 Dec 2024 02:13:40 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e5a48e5b028cb0218a06aad4a72581a54fd2aad32136604ab3cf056014e23257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3927864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c0fd605db2171d428ed546f57450fab89258793306af105bfe10388d53ac94`

```dockerfile
```

-	Layers:
	-	`sha256:496827099a9fa3024c59f0cc4551703b18b34d50f2effb3b96ed4d7df4853da3`  
		Last Modified: Tue, 03 Dec 2024 02:13:40 GMT  
		Size: 3.9 MB (3922011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc132f6acf9ca69e63fe94c14a47697414aa0a51ac564bbf7492507b4f5a9fd7`  
		Last Modified: Tue, 03 Dec 2024 02:13:40 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:6846b1dbc299a13118de5f4fda83a91542f36dab778fd389ee30288f1b78051a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49025242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82127e9de7e8e51af4e56915f862980b8438b2fa5de188e82eb34c9df19e3dbf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'oldstable' '@1733097600'
# Mon, 02 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:dee7f7f62627a074bdb63dacdb2be9fb45000e1cd161e46523c3b644527bf144`  
		Last Modified: Tue, 03 Dec 2024 01:29:12 GMT  
		Size: 49.0 MB (49025018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2676f3afae1526c4d2b831241628e21293682593051649fc3cf714797acbf461`  
		Last Modified: Tue, 03 Dec 2024 02:19:24 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:500606826e3d83af7676f2b5114ca2a21e60532ced5e8fb3adf25930d77a2b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3929476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd7833a8f1ba4e0e7bc8e1bf8217bae7064cbca0b2e57495782b39460ed3749e`

```dockerfile
```

-	Layers:
	-	`sha256:b7f983c8fe689a7450d02f34bf6b65f64cf2ecb7ed7b998edeb597ed78647eb7`  
		Last Modified: Tue, 03 Dec 2024 02:19:25 GMT  
		Size: 3.9 MB (3923571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc6c57e1f9b8097a6dec66e49df0f7e3ad50f84b17287ca2d83c32f2fdd93292`  
		Last Modified: Tue, 03 Dec 2024 02:19:24 GMT  
		Size: 5.9 KB (5905 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:ecdd797afaa8ae82a427f70f329722903145627905ecc0e56a3ec90e23bb8434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52246216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbaf8c8f22e963b188ed32a70bccb971a873ae87ddc05b9becd438e9a78983d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'oldstable' '@1733097600'
# Mon, 02 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:84fdf4c4d7112b3143ac709934811c1b1e8c98ce16bf4f8db393626781a6d647`  
		Last Modified: Tue, 03 Dec 2024 01:30:53 GMT  
		Size: 52.2 MB (52245995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8c4207d082aafb7682cb0744f1e0224fe568660290dafb01d23be29c371021`  
		Last Modified: Tue, 03 Dec 2024 02:18:46 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d6b4a3b8abebff2607c36e7becf266058b3be9d4dc1ba13e0760b08a526581e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3927510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d564ec48b97f613e411a4749cbf32eebdfceaff695290b653b8b55ed6e3b218`

```dockerfile
```

-	Layers:
	-	`sha256:9166ac56c1fa439ac550f5b7a92ddcd465230afb0b65bc4fc0f385eaab9af740`  
		Last Modified: Tue, 03 Dec 2024 02:18:46 GMT  
		Size: 3.9 MB (3921589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c538d4ef2fc9338a7b260fdcd4f86215957a6ca0192be5fc0ba241700640748`  
		Last Modified: Tue, 03 Dec 2024 02:18:46 GMT  
		Size: 5.9 KB (5921 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:092d47b2ffd877b458e17492bf1b0dc7ea86de736a549a435045c1be3a5a1b9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54676499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09481da947b91de0645d6f1bb2093dba9171b42edaac09ca8c9681bbd234f34`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'oldstable' '@1733097600'
# Mon, 02 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d6e904da6e711c933ffd8761aff5a77bfd051532b3d191b30efee6e5183d05ad`  
		Last Modified: Tue, 03 Dec 2024 01:27:14 GMT  
		Size: 54.7 MB (54676274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3cebb89faf6a44703e2cd85c0996c4cc671447016a1950d54ab639b6b3ec53e`  
		Last Modified: Tue, 03 Dec 2024 02:14:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:36c8a6e503a9adbee8a8fdc554a85c00b1b0ee47289ed1570d5ca8fcb2436e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3924352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d9b5763d90a28b7e5d15aad47338b14fcd71b509efb167b78e1df6d41a38e1`

```dockerfile
```

-	Layers:
	-	`sha256:9a485923cb565c2793fd5e2a4719a4a8dda694dbfc88c5a8fb84b28b9c2e98b7`  
		Last Modified: Tue, 03 Dec 2024 02:14:08 GMT  
		Size: 3.9 MB (3918516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e0955a6d2eea53acc434a631d6ed42defaeadaf5c62f083d3b46a16e9b25c13`  
		Last Modified: Tue, 03 Dec 2024 02:14:07 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.in-toto+json
