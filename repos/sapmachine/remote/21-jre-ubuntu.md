## `sapmachine:21-jre-ubuntu`

```console
$ docker pull sapmachine@sha256:7afb428974e1e3bc6faccba2974b6495d1b475ee0a15fd1b62995ff529cfb107
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:0c18e5432a9d901ce85b5f473bde34ab440348eb7861e0dddbd820d53553bd43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89794405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3032ff410136a56d37128efc555b242df0d275bcda2a19e90ef0bac35b094bd7`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:48:01 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:48:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:48:03 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Fri, 11 Oct 2024 03:48:04 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f7d096c2281edd32633c4095cf3b33932b520dcc03e6be3dd903b64506f391`  
		Last Modified: Wed, 16 Oct 2024 18:58:46 GMT  
		Size: 60.0 MB (60044042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7de3cb58063d6cdc2317fe315ac554a88d3ec3c7c942aa088cc2d76ffa50a933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2382528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223f4dd4270965ed4674bde84e3292f47d235927fb853bd2984c6c74594075fd`

```dockerfile
```

-	Layers:
	-	`sha256:2a253fcb0142616f5cd9fb58e02d9baceb1c543b75cd7c8bb5718dd03cf96455`  
		Last Modified: Wed, 16 Oct 2024 18:58:45 GMT  
		Size: 2.4 MB (2372297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a74cc75b7637a9d7b29ddb78f66bcc5fff76a4dc3416ec00a2830b19ca61be1f`  
		Last Modified: Wed, 16 Oct 2024 18:58:44 GMT  
		Size: 10.2 KB (10231 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:c3bd4c83de223b1f6ee919599ace41d5d0225e9ee54491f16a16c962caebf103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88093595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c971dd0b02742ed544c646583943efa8566956361a0534365d1db3637a152b`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:52:53 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:52:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:52:55 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Fri, 11 Oct 2024 03:52:55 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438e354f62c1e84d26056b81f85f205b3047e1616e82327296dafeff21fc7ca6`  
		Last Modified: Wed, 16 Oct 2024 19:15:41 GMT  
		Size: 59.2 MB (59207750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2a9af84826285abbd661322fc1df31145b3e4f41078e63e862962faaa57965a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2383216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cd8f3df2658be8c504c8aaa4aedb46c80ffefadecca50cc313b41d5d88e9f39`

```dockerfile
```

-	Layers:
	-	`sha256:fcd01f3ff32c5767eb5cc3370145c001313922c685ae7dbee367a499b7778127`  
		Last Modified: Wed, 16 Oct 2024 19:15:40 GMT  
		Size: 2.4 MB (2372824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c9bad1f4b2d870d22de088f97f0f64f617ca7a53e7c0c3f6415fc5d26c29d94`  
		Last Modified: Wed, 16 Oct 2024 19:15:39 GMT  
		Size: 10.4 KB (10392 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:96be53e005e599f511740ef23d23e00bee415164223ac0e4e1aa541dfe4fac29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96139801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e34d59d87a638c7dfd575ef844ac755a9454e95b2a7764d4b072b6cef585c46d`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:51:17 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:51:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:51:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:51:17 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:51:21 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Fri, 11 Oct 2024 03:51:21 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288bfe21970586cb86b6a4a491e82f96b4c7cb72fd074ff7306dad745309a496`  
		Last Modified: Wed, 16 Oct 2024 19:28:49 GMT  
		Size: 61.8 MB (61750832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ec8b7b5c9b28ecb7000d0989f16013d162b593a8a3bcc85778401663c12c209b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd572e4b036b1e48a58fc3b79f9437852323863e12582d2db22ecd491783cf7`

```dockerfile
```

-	Layers:
	-	`sha256:f64850bbb0c970289c531116cceb979893da0ea28cb3cdea023a8bdc20aeb35d`  
		Last Modified: Wed, 16 Oct 2024 19:28:47 GMT  
		Size: 2.4 MB (2376264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc7614caba1a92cad21708cb2376f43cd06f0c7df5dd90737053b3e248463328`  
		Last Modified: Wed, 16 Oct 2024 19:28:46 GMT  
		Size: 10.3 KB (10302 bytes)  
		MIME: application/vnd.in-toto+json
