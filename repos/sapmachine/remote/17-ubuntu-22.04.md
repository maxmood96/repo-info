## `sapmachine:17-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:1b7f8013d1801aa943007d3ba807fae827c66387fd0ff3ed859c835a175aa4e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:955ef669b371b586e824f89b783083d654fb21571ceb8ae0b5f9f3e79a95409f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.6 MB (229587470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf6fb47af3d7d7b40b02385793e76ced1d58badef5767cf87c540796829b442`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e967b91e1ccbaff7b30868c101c7b565ff044eeb6927f433410d9a839b5e0ebb`  
		Last Modified: Tue, 17 Sep 2024 01:00:52 GMT  
		Size: 200.1 MB (200051782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:66b4847184ba65c1a6d7a67529dae9568d4dfe54d24b65fb5af80866ef8fc9a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2481101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1efcc75c07464eced2d76855e367efa45190f0da7c3d5f879bc75e95d7b32aed`

```dockerfile
```

-	Layers:
	-	`sha256:5a6215b517fa8472d7ddeaadef1f87bd88a0abeb3cfc7bcc9c67da4cba7414f2`  
		Last Modified: Tue, 17 Sep 2024 01:00:50 GMT  
		Size: 2.5 MB (2471217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d35f4b8a9c197dd06810b476243d57509d66fa206720db144118391eda4cb35`  
		Last Modified: Tue, 17 Sep 2024 01:00:50 GMT  
		Size: 9.9 KB (9884 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:e042a023084dde8959464216a275ff1c9a35cd315fdb69e3199beff8cb73940e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.0 MB (225999124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d84b0af1efbebba9c81333d33053c1c8ccd63727535c5808ef60ae5fa09a874`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c014fd05bf12220dc2acf65dce219778797572296df4025bec9ac188f686651`  
		Last Modified: Tue, 17 Sep 2024 03:30:50 GMT  
		Size: 198.6 MB (198640795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:87bd9c6ae7ffa171ff71dfe0c594d1b9fa6af26b42b6f7b78580f62c6f02799c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2481178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d96a44bfb99901368884a747dc13f8d014053966318f27197ba1366f8f5688`

```dockerfile
```

-	Layers:
	-	`sha256:ae10fb2ab14ab966659d2dc583e7db5eae0752a3979fe11a832a001f89249eaa`  
		Last Modified: Tue, 17 Sep 2024 03:30:46 GMT  
		Size: 2.5 MB (2470945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55fbaa379e0e75e750684a5c74d5629f8d81e379f29831b304e271f3ffde99db`  
		Last Modified: Tue, 17 Sep 2024 03:30:46 GMT  
		Size: 10.2 KB (10233 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:15aad906188917d2b2548bea1f841e904303806186a689e42b6a4fc456a16a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.6 MB (235572970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26689dafd466162c6b1430c1de249731f926a94139665e8b2d9ac646689b8c79`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2bc761bb5a527b8846e26aa935dd08952ab95bc4b1c812db6c5ff5e339fa3b`  
		Last Modified: Tue, 17 Sep 2024 02:51:12 GMT  
		Size: 201.1 MB (201124728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7e90132c85173778b74f76c8cea1988d578c18c99fcd06b39108dca94dc20c04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2483216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a03950d4dd10541956ff316198d07e6d80e52c21644a53179031247fcac2005`

```dockerfile
```

-	Layers:
	-	`sha256:23f4abd76e969f71172d03c2b0232e1bbaed5309839685bea6901f70e62a8acc`  
		Last Modified: Tue, 17 Sep 2024 02:51:05 GMT  
		Size: 2.5 MB (2473271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03748582f2ac654eaccda8b31d7963423851b7448ce3e954f0bb5031d7509a54`  
		Last Modified: Tue, 17 Sep 2024 02:51:05 GMT  
		Size: 9.9 KB (9945 bytes)  
		MIME: application/vnd.in-toto+json
