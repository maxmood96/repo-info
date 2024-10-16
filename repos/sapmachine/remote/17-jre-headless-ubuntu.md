## `sapmachine:17-jre-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:54a87dd9f94ab092d7898b80d823a99b6835e8cec7d57bf1a1e3fc63d31ef195
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:12c8ab085638dce0c1955d09101c05aab246db63d887a52cf92c752e7e26091d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82683840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c3dd5cf0fa3783834f86eddf4e1d0635e4fab813d3c6ccba4d937bbdd802b13`
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
# Wed, 16 Oct 2024 12:49:12 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc571f0a94f69dc954dbc68a0e2dc8718f8a08f26642bb168b4253600f37c1a`  
		Last Modified: Wed, 16 Oct 2024 19:00:00 GMT  
		Size: 52.9 MB (52933477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:33303e4c7735cb763a70819deeebcddc8055900daa8b26927b31d2332f736e2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2143364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9c5adf0ddb201e348995c86003ab38e786440149296f443f92026792c6f927`

```dockerfile
```

-	Layers:
	-	`sha256:a4f51a853e77db7fde741b1a8adfc941836f959d0d437fed91dbe75e8facf4f4`  
		Last Modified: Wed, 16 Oct 2024 18:59:59 GMT  
		Size: 2.1 MB (2133962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9f7734136610834ec5549cf3ac331e21a2c3ca5d654f5990dd57d3afb550f66`  
		Last Modified: Wed, 16 Oct 2024 18:59:58 GMT  
		Size: 9.4 KB (9402 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ea518883ae4e50b137545ecc4876497fc7b4d036dd0ef52da468bd967b7d2bb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.2 MB (81248132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf6add0f519efc38e93f9e3750adeb5f107665c289d947cb9fc14484152686f`
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
# Wed, 16 Oct 2024 12:49:12 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682e249b09db673ff43871ac5da3c2b69ba32d09fb962a096dbad2edbba0ce7f`  
		Last Modified: Wed, 16 Oct 2024 19:31:08 GMT  
		Size: 52.4 MB (52362287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ce32a9272ddc5a52de4fba9d0a85a4d26e7e232029bdb65412baac1656b2e57c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2143968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74c2ec160ff3754a7ba7c6c458552ba52d0557fcca46207664012428b5f897a9`

```dockerfile
```

-	Layers:
	-	`sha256:1210fa88e7feb95c6861ac00218bc5c40350eb6a398b912d94a1441461782aa4`  
		Last Modified: Wed, 16 Oct 2024 19:31:07 GMT  
		Size: 2.1 MB (2134444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de33a09ed6c19b1750cb3eb873f049131b530626f7f75b02639f22354dbcdafd`  
		Last Modified: Wed, 16 Oct 2024 19:31:07 GMT  
		Size: 9.5 KB (9524 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:d9e535cc5cfdda58087756376f01a11378556ede97fd9444055b728da1f3c99c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88715754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a721cf8c972fb81d074b377d2199f49b89993086a455910a6ea66c790a6a24e1`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342ae7ccf7127672004426cbbfe6aebe9a768491bd2d610eed7cb3f1a752aec9`  
		Last Modified: Wed, 16 Oct 2024 03:01:17 GMT  
		Size: 54.3 MB (54326785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f886f9da64872683bbae64241336966fa7c4418babe3125b2189b456bc5392fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2140654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c6897e211f4ea19d147220aa08eb65940b24335a631720ad753285ad3b209a7`

```dockerfile
```

-	Layers:
	-	`sha256:e2f9a22a0b368a11956ce29b3c4e182d801c9a7e6a2a27d818297cf35a765aac`  
		Last Modified: Wed, 16 Oct 2024 03:01:15 GMT  
		Size: 2.1 MB (2131202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f8e9635da33d37d6a2d5a57e1131310e660f9b007bdf71807cb4b5908778ff0`  
		Last Modified: Wed, 16 Oct 2024 03:01:15 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.in-toto+json
