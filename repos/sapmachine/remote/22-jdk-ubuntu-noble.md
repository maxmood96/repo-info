## `sapmachine:22-jdk-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:b4b6e07f37eb0c47106ecf8ba3eb4df18c7f59536e696b124112789d13184198
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:22-jdk-ubuntu-noble` - linux; amd64

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

### `sapmachine:22-jdk-ubuntu-noble` - unknown; unknown

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

### `sapmachine:22-jdk-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:dbf4491578e7c5e00cb9469517852afbce890d41a01cb9433fcc6632e024cc07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.5 MB (240453998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffe29f570e4af3f1bee2a5de98e636be4e79486cd280c569608f70b5b8f9e683`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71aa85ab9ff65f99e92b615b0628854e41629b4c7a15c83606c19dc40a2d8e3b`  
		Last Modified: Fri, 19 Jul 2024 23:56:14 GMT  
		Size: 211.6 MB (211610955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c423e39d85385b211f137f541d4b17ae591d0249a22aa1c8b52a3fa866cd3242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f83ea3e809a57bcd8c0c69ed9fcacf3d6a93eca9c823acafb3377110642254`

```dockerfile
```

-	Layers:
	-	`sha256:572c869716b59e5a08bb909514f59f548d5fab4b19bdeed5d109d3036494bae7`  
		Last Modified: Fri, 19 Jul 2024 23:56:10 GMT  
		Size: 2.5 MB (2450194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cb8d3dee43be3336fca191b5bd0feb9e9ba1585546aa1d7197bb837c2c8f44b`  
		Last Modified: Fri, 19 Jul 2024 23:56:09 GMT  
		Size: 13.5 KB (13500 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jdk-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:3575a4e3fe53630954e8c7d869de61835424079a063cc2da1f29dcf7368e3efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.3 MB (249344616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b66226dacdd08734b08a27d13478e4c35acf2ee102b5673c87b318aec9015091`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:24 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:28 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Fri, 07 Jun 2024 12:00:29 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:875c01bc1b3e6b966440b42d40365968bfdd742c762026b5739c5d1f493510d7`  
		Last Modified: Fri, 07 Jun 2024 12:11:45 GMT  
		Size: 34.5 MB (34506029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1878ba9617f3d44d1f173ddafe16050cf362d0b011eaab38de6683147bd7817`  
		Last Modified: Fri, 19 Jul 2024 22:49:42 GMT  
		Size: 214.8 MB (214838587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9fa5b0311bdb83a2f393000380d5aa368fc19b369235cb57f14ab156bd4e782f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9faec38de52613ca37592d703c798277c40d7d1075b55abd5955e9cbe3409460`

```dockerfile
```

-	Layers:
	-	`sha256:a39cc4e096002fc9d1111eb1471967f70a4e76cbc83ae0760503c1752bd639b3`  
		Last Modified: Fri, 19 Jul 2024 22:49:37 GMT  
		Size: 2.5 MB (2451643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ae3f8ba6b5d59cab5bcfd1fbb5e2bf7c818c39c57e0daa4048f6dce30ac600a`  
		Last Modified: Fri, 19 Jul 2024 22:49:36 GMT  
		Size: 13.2 KB (13152 bytes)  
		MIME: application/vnd.in-toto+json
