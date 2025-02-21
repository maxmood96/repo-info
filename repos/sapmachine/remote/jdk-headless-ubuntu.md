## `sapmachine:jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:affda1e2b7b9c6f955f57ae2b4a0da0cffdac063f383b800d65a717e3b079595
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:ae39d95573862c65321db8bda81301e1b25476cdf2196ebdb7e613b1defdd95e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.2 MB (251213392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0b2ad4161eeeef88264f1c629ba4fdbef4d507e4ae4a6e3b747677cee1616c`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3665cb0abca416fdba2ab3af8adf81e7b7bc108495752edd9f94d23f542890`  
		Last Modified: Tue, 04 Feb 2025 04:48:11 GMT  
		Size: 221.5 MB (221459102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:08c8b4b17ca27c380325d0dd011c1ffaf610e1aea55afa9a7c15d68f4a374384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2249266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79641d1cc371de8c7e8a2f152d13a62e7d8fdfb7b53fcfe1e23ff019e68c1d7b`

```dockerfile
```

-	Layers:
	-	`sha256:0d2322514d98ff157e62473c002d203cb8545bb41e2dc4c8d5ed1c9627b91bd3`  
		Last Modified: Tue, 04 Feb 2025 04:48:08 GMT  
		Size: 2.2 MB (2238638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39e4d028db40e41f3b3c57aa7a3036f09eda073df5a4237344d27b248e7172b2`  
		Last Modified: Tue, 04 Feb 2025 04:48:08 GMT  
		Size: 10.6 KB (10628 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:a14b857d22d0be073a638ef24fed2a23a7e3e748c7cb835bf3bc977af83c5bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.4 MB (248362248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c8e93363e15f2ddf0372100c8cd82d4e2a2ee2661ea4cb7449619dadda3d3d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032416eeecd66a785033ed75cc74b6c03e5d2910fb7e43787b4d816ef6b2835d`  
		Last Modified: Tue, 04 Feb 2025 15:18:38 GMT  
		Size: 219.5 MB (219468650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c8694612eaf71ae4f00ab3238a546810939e110d702191427fe1f350c3df5f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2249318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5641b8e128db31d950c3ebbca14294d0340198f0f4d314b958fa7a7c2c5a74f4`

```dockerfile
```

-	Layers:
	-	`sha256:9d904766dea157a4fef3c9e048144b2082b61c843c1189e5b6b91ca65250c0ff`  
		Last Modified: Tue, 04 Feb 2025 15:18:33 GMT  
		Size: 2.2 MB (2238527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4280399766346f1c9b0c6c3ab6a7710f5bcb72750fb05843a9516ffc7033fe19`  
		Last Modified: Tue, 04 Feb 2025 15:18:33 GMT  
		Size: 10.8 KB (10791 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:dc0b50a7da747dcdac064cab005a606b79338a9ddced3790e01fd5c66c641c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.8 MB (256792971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54c882f1bd86e7be61b17b2d31452d4e9510ed67093cc38f1662ad51fa0a2e5`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:16:03 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:16:07 GMT
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Mon, 27 Jan 2025 04:16:07 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb6d125283f978ab79705f4aeae2c41f68db18dc9bf1403783b3acd23361534`  
		Last Modified: Tue, 04 Feb 2025 14:22:02 GMT  
		Size: 222.4 MB (222403147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e801350ccb323c5f904763172f7bf14634c0caf718414c49c6ed448c6269560c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2250681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9974f302e481c79cdd73a596bc85026699300d2a38b5d762399d8c66c2b3a1d`

```dockerfile
```

-	Layers:
	-	`sha256:689a1ae77d9ec8096c201100cd58d7b3c6d600b6070bd47e930f868496617416`  
		Last Modified: Tue, 04 Feb 2025 14:21:56 GMT  
		Size: 2.2 MB (2239980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:301f7e1d849dc74e40c1bb7326ec41d2936466c6beff17dd83a4b1d10491d94c`  
		Last Modified: Tue, 04 Feb 2025 14:21:55 GMT  
		Size: 10.7 KB (10701 bytes)  
		MIME: application/vnd.in-toto+json
