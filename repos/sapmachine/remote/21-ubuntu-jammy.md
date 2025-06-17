## `sapmachine:21-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:ef741b2cf6582cdf4dd635c4800fc820aebe8f8ecd3b8e692ade25f4af71e6ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:1d017eff8972d07ac3e12e6fcb12818d133365b8e6450debb057bf9230a531a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.3 MB (244264207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:620e28a75b32e5f0a06e6aa2c49cad4f6fe4ce0d9e225507f49ff3719c9d632a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a4750eb5e7b5f03d94bdf2700de0950f4bc5f670b2dbd6cf983302ad25e357`  
		Last Modified: Tue, 03 Jun 2025 21:05:37 GMT  
		Size: 214.7 MB (214731204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ea104fa785531c1ee8e579255c9678d5ac7f80d5b609a99f21b3ad275732a697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2532636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78094ad987c7a2c7cbfa6a2e8d0dff93673185baacbcaa1a163347024afdb664`

```dockerfile
```

-	Layers:
	-	`sha256:abaae4ec0c90e213b2a6fa62d0c11d8ef4733382b9ee5c7a1d5adbc490486aa7`  
		Last Modified: Tue, 17 Jun 2025 09:52:27 GMT  
		Size: 2.5 MB (2521191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcc3bd9148eec82cff1d8a7e0c2b708a5d7d82c7d156a23895bbe06b5a024c81`  
		Last Modified: Tue, 17 Jun 2025 09:52:28 GMT  
		Size: 11.4 KB (11445 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:74863d12aa1eeb2788c96525fee6ae057096f70ce4d52f0543b0932247edc111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240299886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7012d2deb5890362af0efe4ea557250ab2cf79d49a5d438a6fded7ce16715d35`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a89bd6a246fb4dbe439db8ef3ec46f9c9828cef0bd57ff293886efffc991b34`  
		Last Modified: Tue, 03 Jun 2025 17:58:49 GMT  
		Size: 212.9 MB (212944305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:69fbb3721668101d3e9a72d404a5a6929acb1ea6e5412086caf74b4f3e095bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2532614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a5405d857a00dadef090ee5407bb4eee0b70c86e51c2965bffdb76ff0a49d8`

```dockerfile
```

-	Layers:
	-	`sha256:154fe4cc691215188d2304f57972f1c005f3d9b312fe3d595df96927319ed408`  
		Last Modified: Tue, 03 Jun 2025 06:04:04 GMT  
		Size: 2.5 MB (2520969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e52cfcbda0e994995344375238b3e6dd3fce372d244eaa278b451ad9ebc2b044`  
		Last Modified: Tue, 03 Jun 2025 06:04:03 GMT  
		Size: 11.6 KB (11645 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c5b7459f2965249cbed4b2d1b94dc8289332f7e76d702e44437894bc17809518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 MB (250471341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e40e6f9f089f7bb8e323fe09e3ad92a19f98450dcc2cf6169be1c76e693ae2be`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:ff7ae346164d0b3da702390fb0f6f4187ba164036794a6081fdf0f9817b59053 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b728b0b1adf8a1b191ffc8bfd1fbfbb2bc25a989db32698511ae9a36f8b82a7`  
		Last Modified: Tue, 03 Jun 2025 13:34:58 GMT  
		Size: 34.4 MB (34440357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a3a2e0e4169af900918698e91edf76eb167fda9d42cc866e93c913eb0a176e`  
		Last Modified: Tue, 03 Jun 2025 06:05:45 GMT  
		Size: 216.0 MB (216030984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8ed39d836999a818202f3c2177e288d38ec16787a1609be60ad7bfc67d6241ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2534961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfca1163d07e80fc71f8d7f0d393ca3a4694898c13d0734cf8abe8c310449e8f`

```dockerfile
```

-	Layers:
	-	`sha256:24d324c3a149f623acbc25fa1addd1848c95452d378e9ac894910092100dd8b2`  
		Last Modified: Tue, 03 Jun 2025 06:05:39 GMT  
		Size: 2.5 MB (2523424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ee45bea1468f8bbc1faac1501b573bae4da347022563ccc463b6ee4c2650b69`  
		Last Modified: Tue, 03 Jun 2025 06:05:39 GMT  
		Size: 11.5 KB (11537 bytes)  
		MIME: application/vnd.in-toto+json
