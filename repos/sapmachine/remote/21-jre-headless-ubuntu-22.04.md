## `sapmachine:21-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:74e4e224cc04464b394809a9511852cdd66c44f268579aa2b985a13922134c08
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:250fc8b5dd95c50d740fa86cd6ed8db32752155aabaf86caf321828592469633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.0 MB (88040887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d9f7656bd3658733485af9a680fdbb7a2a0267aa96889f515d1faa93f80551`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:13 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 27 Jan 2025 13:39:13 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec6ad6d664187334b46f9cde0a2eb1fe08f4734afddb26a98155f5ec32c22030`  
		Last Modified: Wed, 09 Apr 2025 01:21:13 GMT  
		Size: 58.5 MB (58508522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e3a6df94dc162c5ac55adea7d1252c2754bcbec053f47abf6a7805714e1629f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a741edf980fddb04b2bb349e3552c03950ec6cce0073ed9c6991d7cf87f6fe`

```dockerfile
```

-	Layers:
	-	`sha256:6f885f064da00ab5b0a1579865a8a2151c417d35a5bb4077ada3e99c6a449587`  
		Last Modified: Wed, 09 Apr 2025 01:21:08 GMT  
		Size: 2.2 MB (2166930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c45390f3810dbd718122d9bb908885200a6bbfe4615198ff7b2c2de3a48ac86`  
		Last Modified: Wed, 09 Apr 2025 01:21:08 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:cc9e4dd641f01fe46125e391604e75d2aeeab4b1bef886e8dc6a9927a2b0bbaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85009911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b6d81503446d00daca346200d3394702529025a19995adfb5d94696f235b11`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed4dda4098158ad53d503d5fc678d0eb1c847fda6e0c09c5ac47415652b9c0b`  
		Last Modified: Tue, 04 Feb 2025 15:32:43 GMT  
		Size: 57.7 MB (57651729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:13255da756eb5d6fcb06f7f0a8a90738062ed51c49dadc36342c0c565f743058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0d26d7fdf693afa5e6969a210b9df9787fe1979e0240091bdd82f18c517df89`

```dockerfile
```

-	Layers:
	-	`sha256:c55ec80933f1c4beec5dc40f289fa8869693ae9fa0b564011bc32905e0d3e10f`  
		Last Modified: Tue, 04 Feb 2025 15:32:42 GMT  
		Size: 2.2 MB (2166538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67fe6d70b4002ebb46cb6d3919181c4ed31d8fdd7722d921a2b7520f4fa704a2`  
		Last Modified: Tue, 04 Feb 2025 15:32:41 GMT  
		Size: 9.8 KB (9755 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b3d22ac64745d5bdea06363f2ad52e461a32c6cfa0648db7754562c029c9c7ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94353768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53f2f79e9c5a57a94f6df061cccc54063edebb274996b059fd52430372d1961f`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:49 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:54 GMT
ADD file:378a1f28ba6d12429f01a1e40af6c7964a243df3db0827fc9d3841a0e7e3730d in / 
# Sun, 26 Jan 2025 05:31:54 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:703356817cce0c2e3da6d57ebab57c3f97a187e707e48187655f5c46ac9bbe4e`  
		Last Modified: Tue, 04 Feb 2025 14:46:52 GMT  
		Size: 59.9 MB (59905833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3bddc7599f84f33c58e731100b77b9f0e14a2acd5a1588b3d2f84e1c21459809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2180448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef79c26022f500c582022531c726ac916e4f06a3576cdeab9eb2fee86add420`

```dockerfile
```

-	Layers:
	-	`sha256:4c4cc8c85530e91cb9c793d2a6395016b4ae383eb130ec70ef50d7c3b8bb33c3`  
		Last Modified: Tue, 04 Feb 2025 14:46:50 GMT  
		Size: 2.2 MB (2170765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25124436a7dba229844d98d804d125c66315984fb7ce8380845b36725ebedf54`  
		Last Modified: Tue, 04 Feb 2025 14:46:49 GMT  
		Size: 9.7 KB (9683 bytes)  
		MIME: application/vnd.in-toto+json
