## `sapmachine:jdk-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:c827c30a0586fde9a4d00cd9555f537dcdbe63af00fbedd946fe448e0919c7f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:aeb3cf604b0010b61ec44cd1e1c69b9e7ee5541a850fbb3dae4d779044a96811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261582063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9f342597d5efda2c2705d1d71616b82ed4e35f024b97f1de48ee6e33d9ad6ce`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7d795e842dafd032b165183ef13f4771f190ba73bfe4e686e631ef6ca38dee`  
		Last Modified: Tue, 03 Jun 2025 21:04:11 GMT  
		Size: 232.0 MB (232049060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cdec35dc4c65d2ff348acf9f2d6a66e9796a89c2cd32970754d81eba81b2b312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2523297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b407899ecc1c313ff02ee9b30fc74fbd338042a39c1186064489481429bed2b`

```dockerfile
```

-	Layers:
	-	`sha256:83cf5b80a7db31dba23e82bce016bc66dbc23e568151b2c1e4c4da0abf4d6f70`  
		Last Modified: Tue, 03 Jun 2025 04:17:48 GMT  
		Size: 2.5 MB (2511885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a4d3646c2809f189e95f4f68549b5161f54c28777568947d8b98e2d3c46c0bf`  
		Last Modified: Tue, 03 Jun 2025 04:17:48 GMT  
		Size: 11.4 KB (11412 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:38afa7454095a6fab8f15c5f8b15fdcc222fa906035614327ab215e01a0d98de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.3 MB (257269581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed0bfe087c86ae4f6f8e41669efb5bc731526145ef0ae664730d01fbcb14ccb`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce5535be8a471803f14edd1cfdb50a067808eb41af5df9e88d40ee2a1febbeb`  
		Last Modified: Tue, 03 Jun 2025 05:55:28 GMT  
		Size: 229.9 MB (229914000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4b7aeff2ca11a8653f9061778838abca130fb15ed52a7ce97d7f65fcd2ca65b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2523273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7339896fe49304ee331ca33131431da1ded4cee9d9ebd986d112e050c873c50e`

```dockerfile
```

-	Layers:
	-	`sha256:5af7aa862977ff456e821c9ea22104799505a8559542c2d0b1abb4ecb86cb94c`  
		Last Modified: Tue, 03 Jun 2025 05:55:23 GMT  
		Size: 2.5 MB (2511660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37d452b2e0e803f039422670a7e976c2a7a25e304571e7722c7dadf901ed03f1`  
		Last Modified: Tue, 03 Jun 2025 05:55:22 GMT  
		Size: 11.6 KB (11613 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:7a346b055c6b75e8b8a2b76d99bf788b518be5916c7f31a0432fd890f425a190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.7 MB (267692273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c397cc96cea69e60a01f441364e5b3ecfe4f6a6b4eb4db1db7f5b3b5cdf0101`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:ff7ae346164d0b3da702390fb0f6f4187ba164036794a6081fdf0f9817b59053 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b728b0b1adf8a1b191ffc8bfd1fbfbb2bc25a989db32698511ae9a36f8b82a7`  
		Last Modified: Tue, 03 Jun 2025 13:34:58 GMT  
		Size: 34.4 MB (34440357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a61eb1b625936289b693ab79b78354b8f465a40ae91d736ae7b7fb86a8771d`  
		Last Modified: Tue, 03 Jun 2025 05:50:21 GMT  
		Size: 233.3 MB (233251916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2522d6e735f048ee9e9ea56003c68cc6c0dd004f376f66ce0332d0751d350632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2525004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a48d97dfaabb9445baf6cd149d67532457c9d42eebb17d31b48c130f44325b0`

```dockerfile
```

-	Layers:
	-	`sha256:a478778cb2d56aa986f092b21fa89a4b5b448ed36f9d25528f3b43ff2263b2ce`  
		Last Modified: Tue, 03 Jun 2025 05:50:16 GMT  
		Size: 2.5 MB (2513500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c0722adf99748df1745d9c7d2c8243b9bdb3acc310fe3499fb3d3de913fbebb`  
		Last Modified: Tue, 03 Jun 2025 05:50:15 GMT  
		Size: 11.5 KB (11504 bytes)  
		MIME: application/vnd.in-toto+json
