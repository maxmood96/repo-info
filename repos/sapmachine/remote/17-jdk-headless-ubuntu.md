## `sapmachine:17-jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:ef4f0607185d181c270953a1912028c79de3761d1e5091ea2e1b67cf0f5df516
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:42e563b1486226d6dd4b57a121a39b2ce430591c9aa817d6399450ea2bc8903d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228931734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9fecd6f9ce930f26bcc916ce995df34ff2d948af61f29ae4f83a068a882ac7`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:41 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:41 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Thu, 29 May 2025 06:11:31 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c861e6f8dbf7c222fac4b25b8f9f10da59dc8110ebf5d696fe8b074538a43fc`  
		Last Modified: Tue, 03 Jun 2025 04:17:48 GMT  
		Size: 199.2 MB (199216397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7c4584dca286007978c040315ed2b2bba926733d6516e8ea5b789dd9ad377645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2262467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18736dc487e899ebc0b046863a24c4ccb1e7fbc847bf6aa995fa6ef5c09622b0`

```dockerfile
```

-	Layers:
	-	`sha256:ffe15420a2576aa996c7ea45539efba2ce36a959ff0b7ff4e632281ad732d486`  
		Last Modified: Tue, 03 Jun 2025 04:17:45 GMT  
		Size: 2.3 MB (2252848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a049148b4d40fc4f61786da137b36b7ef176582397b85f2a8bbd90a24147a30c`  
		Last Modified: Tue, 03 Jun 2025 04:17:45 GMT  
		Size: 9.6 KB (9619 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:dedf984e4e10c78f2c399832af29bfac39afce714a9632f7830c74aca3f1ba8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.8 MB (226809697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cc0be1df64c9d072401ae0ecd226911a058efa3caf2f67aa9c25fe1778d2d9a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:41 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:41 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Mon, 28 Apr 2025 10:53:55 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43bc49ec3396724fa0a43c92b45dbd62ff8b489d95a1720c43b161bfc0793a7`  
		Last Modified: Mon, 05 May 2025 18:39:09 GMT  
		Size: 198.0 MB (197962821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b9e309e8fdc64ba8fb2de3cbce3c975de1a21ba4a4146627d6dbe315db2e634c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2241834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc1fce96a076aebc0817b9e4ca6df4b0cd3224d19a92140d253e3a73c59bf7a`

```dockerfile
```

-	Layers:
	-	`sha256:1f6412c534b211a2c3e96c8d9b7e30d6d9723958fa5162b5ec85bee0a3411efb`  
		Last Modified: Mon, 05 May 2025 18:39:05 GMT  
		Size: 2.2 MB (2232087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a19f9dd4a7f9ca80e6bd75555d574dda0f12ad1a349d3de66c35a96f3caf1ba1`  
		Last Modified: Mon, 05 May 2025 18:39:04 GMT  
		Size: 9.7 KB (9747 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:e04289b4453b7a5ec205303b30c5379717dfba17ed7148e7c2914aca67551907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234556519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43584f43277cd853d9b851ca96aa0a1f08c2dd5c86a8e9402142b5549d938679`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:41 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:41 GMT
ADD file:d4d363297b0bc97147d6215ececd915564f3540c035d4c68fcdd781acaf0e4e7 in / 
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd7ce82c353803b69e06046e91345d15e766766fa395e4fb8e9f652834cddb32`  
		Last Modified: Mon, 28 Apr 2025 10:54:08 GMT  
		Size: 34.3 MB (34340838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a8b25f3e9e518a3c3377b3c5a6ebac89996ce5c7fb2b98956b7de5ab12f0e8`  
		Last Modified: Mon, 05 May 2025 18:35:26 GMT  
		Size: 200.2 MB (200215681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d04110914748ef5af4d281e66200ae1021189724864f53f6ce59a37b30186f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2243221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7818fc0703ada1b5f8aa9cc07fc25cb0346a73a7d419b082137ce0e694070311`

```dockerfile
```

-	Layers:
	-	`sha256:4c5b4e6787ca3d577149ef8e5cf2ad42b18c28b3e1bd4d4e563a427b6b51d282`  
		Last Modified: Mon, 05 May 2025 18:35:21 GMT  
		Size: 2.2 MB (2233546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6165589c2e04323576448212d9131924bd2149939df31a2d65c042661bd3034`  
		Last Modified: Mon, 05 May 2025 18:35:21 GMT  
		Size: 9.7 KB (9675 bytes)  
		MIME: application/vnd.in-toto+json
