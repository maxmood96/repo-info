## `sapmachine:17-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:9cbbb1c2a0a94c39e8bcfd6205f06990a5d75138941041bfdcbab2dc76e2d7d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:7695d2143564ea8fff5be386327594ee77d5e849a812964137feb8c4ec0b2e40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.1 MB (230148496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c4d4e0c7f728e913efc66a0cdb959fbb407069d95d0c2560e424e7769bbd5e1`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:05:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.19 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:05:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 21 Apr 2026 23:05:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81422843d9a50c6fcd753786cc46a402c426f7eb91745ae6310c8ac573ca244f`  
		Last Modified: Tue, 21 Apr 2026 23:06:17 GMT  
		Size: 200.4 MB (200411998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bc533e2fcaf1f0ed61dcd1484e7812f58096a6dd34bdf8afcde96a0d9f64a389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2387938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05371b00ee7005dd43d272703abdf601bf76eb94be8ae17f691973fa346babf7`

```dockerfile
```

-	Layers:
	-	`sha256:34c53f8260e408a1f074bf1064213bf04243526fcfa13e7c13762e561a9c4a75`  
		Last Modified: Tue, 21 Apr 2026 23:06:13 GMT  
		Size: 2.4 MB (2379048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91f779c9c6abfe76891c007010dcb52601accff4c469fd22965e030d7e13812c`  
		Last Modified: Tue, 21 Apr 2026 23:06:12 GMT  
		Size: 8.9 KB (8890 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:3c3a3607670aa13fbc87fb7f48f9a1356736ed90ad02e570ef90e8041656c093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.7 MB (226720251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6b55de02db2d5c9501d773df27527066ede853297a62ee1ec154504fd9274d3`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:07:09 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.19 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:07:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 21 Apr 2026 23:07:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533a67de8b9909ccb4bdf85170094fccae62f8ead8dc205f95a6fac8c3f9c293`  
		Last Modified: Tue, 21 Apr 2026 23:07:33 GMT  
		Size: 199.1 MB (199113708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1267959f541f146217e21eefcfa7244dacb2bc8623097c2b11f7bcfb016a296c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2387714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7657816da96e493440f65b8d6026111a3a128354bb56958fb433afd5c996551f`

```dockerfile
```

-	Layers:
	-	`sha256:2385c75cb14fe4fdcf6a448e93f1563af41e5bbc0acc73799e34605109b46e82`  
		Last Modified: Tue, 21 Apr 2026 23:07:28 GMT  
		Size: 2.4 MB (2378720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:671d6d1a54b406835c40ec729ba73e442904ceeb226279f62d701077666402bf`  
		Last Modified: Tue, 21 Apr 2026 23:07:28 GMT  
		Size: 9.0 KB (8994 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:1bfc9024d9e72e9a43b7597fd7f9b8c49b7950e2e8fba31919e4cc609edde266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235705949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:710cf8d09efedafdf56809398579eae5af4897ccd5dc8ddff7d78a795ec73f44`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:37:04 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.19 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:37:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 21 Apr 2026 23:37:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb8fa202613ecf8206577372ce82f83fb97d18de557afb80a69ebf17d026ca3`  
		Last Modified: Tue, 21 Apr 2026 23:37:48 GMT  
		Size: 201.1 MB (201057551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:564897b1199a609966e5c182269bad8145f6a7097945878e00162100d61c0e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f3e18d9958c1364be7b446425383068266fc3b497904a9349e39e57bb4573c`

```dockerfile
```

-	Layers:
	-	`sha256:97c3c311c9bb0c414390c2025249b7125c68adda7cf49178491b9c285b8529f9`  
		Last Modified: Tue, 21 Apr 2026 23:37:43 GMT  
		Size: 2.4 MB (2376544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff939b45ca6fcdced5ef7e0d2874ceb3b3ef033acb996a0e489c6bb1d7dab354`  
		Last Modified: Tue, 21 Apr 2026 23:37:43 GMT  
		Size: 8.9 KB (8934 bytes)  
		MIME: application/vnd.in-toto+json
