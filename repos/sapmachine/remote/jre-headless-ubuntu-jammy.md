## `sapmachine:jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:bb140d12c6264c5cdfd121d48bc5c1648adf26c37a33cbd4f4cf3cae26ab3e5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:9d0db732c27c3b63c350fd23889ad3c5bef5112deae48427842fca5c3d43352c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87130001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc024608df82a8b424a7d4a5885c5a4fa4019f4da440c38f87323e39058a23f6`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:15:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 01 Apr 2026 20:15:47 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be46259504447e12b1183d4145bb4b5ab3fc2441b3136b2ac82a0fc41a69ea33`  
		Last Modified: Wed, 01 Apr 2026 20:15:59 GMT  
		Size: 57.4 MB (57393588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:31e8bb6dae621acc2c326203a611c5950a19a7e83d32314c836b2612a7508951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2309183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b49b0b3e4175003c85ebff56976462e68d88af393d1e0ff86a5da4eadbb8f1d`

```dockerfile
```

-	Layers:
	-	`sha256:711e7c40d6929d701e1bd0611f708f4b5dfb4964c5b6d28915a2e821069c76be`  
		Last Modified: Wed, 01 Apr 2026 20:15:58 GMT  
		Size: 2.3 MB (2300343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8c6ac66eaa6f9a808a86a77084bfd60442e8f86e16d7452f5174b6594c5b0d0`  
		Last Modified: Wed, 01 Apr 2026 20:15:58 GMT  
		Size: 8.8 KB (8840 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:79e47272ffac386b97b6f2bc25af98d40b3783c54bc32e8a5677197a83ac88d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.0 MB (83973679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0258b231c60541bf70c3bf3b060b412542782a12c21e3a756c3ef71ab46719cb`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:15:28 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 01 Apr 2026 20:15:28 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8389b40122578c34e774a067db7974fd4d6a9cb9d6863ba85b2aab4ac900b7`  
		Last Modified: Wed, 01 Apr 2026 20:15:41 GMT  
		Size: 56.4 MB (56366736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7e9254f65b86f4a44aeae64a78f6e8bd180ef7f66f811c9c11b9f572346ab7b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9709ffd01a92b7efc8cefade1dcd530f1f6af5487f4e64d7c216f89117e526a1`

```dockerfile
```

-	Layers:
	-	`sha256:27ef8f65c70ec3ad58c0877ee7455c7a77c00796c22eaa60b8d5cdfe3a790110`  
		Last Modified: Wed, 01 Apr 2026 20:15:40 GMT  
		Size: 2.3 MB (2300012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0219ab232afa1e1c8932da19cfeb685df04e86b032b323f8d62710c48f7a7405`  
		Last Modified: Wed, 01 Apr 2026 20:15:39 GMT  
		Size: 8.9 KB (8944 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:fc07d6f5340f0afcfbf0a5dacc3c1a6fa41ce7387a39657c082cd2116f34b94e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92939672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00832cdc794c21bf61514f91564410f9c8eaa56d8f6a529abdf2b44883fca49f`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:11:34 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:11:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:11:34 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:11:37 GMT
ADD file:268be611d24f69c3d8e480314cd587652e4c89a6032236737057c8b64f2379da in / 
# Sun, 22 Mar 2026 18:11:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:43:50 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:43:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 01 Apr 2026 20:43:50 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8561174429b5506a38233fd26beb9b48b2e76e33b2d830a613ec8cdc1bec6c3`  
		Last Modified: Wed, 01 Apr 2026 20:44:17 GMT  
		Size: 58.3 MB (58290012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:36dccefc392f9cea8c2ace5d0a4cec151ee8e314e39f7ae92a1402532dbc1425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e185485ba01a6c6c45f0661ec161105800b7cd012b4110cecd47e53bc747521`

```dockerfile
```

-	Layers:
	-	`sha256:2c778f1182c1c2fe07b29c0d7b48cb0660ef3487f0ed673af05800f40b75586a`  
		Last Modified: Wed, 01 Apr 2026 20:44:15 GMT  
		Size: 2.3 MB (2299155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25b3005047bd84a216b1cb58d3cf3a990c74827dfa74930a176f98ef78ac15a9`  
		Last Modified: Wed, 01 Apr 2026 20:44:15 GMT  
		Size: 8.9 KB (8884 bytes)  
		MIME: application/vnd.in-toto+json
