## `sapmachine:22-jdk-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:2f8c65d18faa95c7e0233ffea4691f732dd070f226e9e58f3dc479d836cc3ea9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:22-jdk-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:616db9b880b0040811a53bbb05d8fb57b17a70cc4bf61c60c707df378b615250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243324380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23dbdbe80ad7019ed769571a594f369778d703e93f76b5d45c1cf593fec47ae3`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d37c1d5d74bda5f284248a9007a99d32fd9befc00092a90c240e9979929cf4`  
		Last Modified: Fri, 19 Jul 2024 17:59:11 GMT  
		Size: 213.6 MB (213619227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:412d7a82a40e7d84e35798e4715db33dc33bbd9b6846f1b8b53620081fb86c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af56943a2d6a071c119e827c10a38c6e4b89a989e042081a2d1a972ef1c3e06e`

```dockerfile
```

-	Layers:
	-	`sha256:8b36dc8b289646e34058fc60c62b4111f9708ecb3a98018aaa33161592c6b5ad`  
		Last Modified: Fri, 19 Jul 2024 17:59:08 GMT  
		Size: 2.5 MB (2450190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5c527e7ad99b822bfaf10d386d52c8e1444137c041c7820fcd94650a1edbd43`  
		Last Modified: Fri, 19 Jul 2024 17:59:08 GMT  
		Size: 13.0 KB (13031 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jdk-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:f3df2d23bada81bbedb966ca3000db8ec468c7a9ac2f64112479d0ffc74431d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240624375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff743f8c5fdb6a52a45dd5fe578a27a9970f74a689e017578ecf12d62ce99d98`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8be052ef5d257bce29bcdac702f21606f8f820cb3a9f5c2aaec6f245d396016`  
		Last Modified: Tue, 25 Jun 2024 23:50:20 GMT  
		Size: 211.8 MB (211781332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d8c0f6d035f697caf8b3c32f4afe7549140b9530f458449e87e8265ad9f31843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2435632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e421e567a4f6b4bb7f48eb48a79f838b7a4c272a84da0e75d0699cead6ea8d`

```dockerfile
```

-	Layers:
	-	`sha256:71e19796d1a4e20f155ce3268a5d759e9bfc39b6978145c20e150178c5a7cdcb`  
		Last Modified: Tue, 25 Jun 2024 23:50:15 GMT  
		Size: 2.4 MB (2422114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6be06ce529ab4636b640a65dbe0342b602dfde686e3da5583ffeb5b23910a09`  
		Last Modified: Tue, 25 Jun 2024 23:50:15 GMT  
		Size: 13.5 KB (13518 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jdk-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:7081ee0f27ffe1203c3b712d806ef0cc02d76a3e8e2fdcb5a04491461bccdefa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.5 MB (249502125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6484fccd61179fb63afd336c6268966efb251d1127092ff1b993ae8a43aab0c`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:875c01bc1b3e6b966440b42d40365968bfdd742c762026b5739c5d1f493510d7`  
		Last Modified: Fri, 07 Jun 2024 12:11:45 GMT  
		Size: 34.5 MB (34506029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccc34635659453a00507f117554b35de0cc6055a7e9f1d9d5e220ab8d70f5ca`  
		Last Modified: Wed, 26 Jun 2024 00:06:30 GMT  
		Size: 215.0 MB (214996096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2d25cb5bcf20de652082129a50916d0d764c5c540e749bd24e8e4c9e8380946a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2436733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d308a20845bfac96cd9a2bec22672936b0c5ec366a836cb4b1de76802a40c2b7`

```dockerfile
```

-	Layers:
	-	`sha256:86a62a74092f226e6a265fe7c9706634b645b36b0301053c2bdad1ac69b2ec3c`  
		Last Modified: Wed, 26 Jun 2024 00:06:25 GMT  
		Size: 2.4 MB (2423563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:284964b4cfb29178d90d73a1cc0ea0c68fc037d95349d76324300a54c1e0102a`  
		Last Modified: Wed, 26 Jun 2024 00:06:24 GMT  
		Size: 13.2 KB (13170 bytes)  
		MIME: application/vnd.in-toto+json
