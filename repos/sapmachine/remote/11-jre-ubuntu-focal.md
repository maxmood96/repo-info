## `sapmachine:11-jre-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:540965a993c8b12ed841df1a1558bb1e3038f9454cfe5278afb1ca021f3aa2f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:9960b64907ba484bef45fee7545c66164e0fefb897e938f001dcc2c639d3a8ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77047640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a162354f9bc42eb3c904272172253634d19d0a6a515775ea3469a1ea67576e47`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Wed, 08 Jan 2025 01:50:06 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ce6546c6d20b8feb253ab893d389de73fb1a35fe8ad140b7dd6ee4ad778769`  
		Last Modified: Wed, 16 Oct 2024 18:59:57 GMT  
		Size: 49.5 MB (49536580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0a1dd6ca848e15e738d6064b1b576ae5765af91ee8bcfbd9af674e80647002ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb94a5b16dc2271e0acb3756be6c6bb96e6b72d137daefb5e41bdd7eda71de0`

```dockerfile
```

-	Layers:
	-	`sha256:32d016365034851a5357eac9d98557162766d5f7d18222a18fdee595ee2cb9d9`  
		Last Modified: Wed, 16 Oct 2024 18:59:56 GMT  
		Size: 2.3 MB (2292354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5857927c5005658e379b2fb5ace60c77a4c6669c718ba03261930f52cec06efd`  
		Last Modified: Wed, 16 Oct 2024 18:59:56 GMT  
		Size: 8.6 KB (8601 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:0c852813d0c150e0847066ddbd200ed15a78375db30427c3bc954d4b23985e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74828594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cdcbcb60597974b29dea42fad3dd56dc3410bb62cf2eae188d4626c939075fc`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63795a5d30c242d5654f884b388dbe6d8a1c9bb3344a4842958bc574b883d5ee`  
		Last Modified: Wed, 16 Oct 2024 19:53:41 GMT  
		Size: 48.9 MB (48854766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e500781aec2273bcc11de76b8d6edab67c325356bbf5251c6b9e13259fd5a15c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a36336eec8eaf369e7603a2a18d63938c11f72b6813332d459f97e7f253caf29`

```dockerfile
```

-	Layers:
	-	`sha256:0adceef2c756cb1d20e46dc4563cea15e00af3c0a52e72b3fb840aab8e40836b`  
		Last Modified: Wed, 16 Oct 2024 19:53:40 GMT  
		Size: 2.3 MB (2292618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:688a7b2695fe96821e15b249189fc213864df681a510fc85681e48acf8a14d28`  
		Size: 8.7 KB (8703 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:7d31e7006518958d3734d13a9c2bccf1ad5df5494f1f927c916fdaa2511459db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79868990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1033b8ff62ab9156b70bf0476e29d6cb48beb95c133bd98a6f67aa9ccf18b7`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:35 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:38 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Fri, 11 Oct 2024 03:38:39 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4022e8d821c40b81496d5c22fe041731367be503a498ec693b0cae0929b3c1e3`  
		Last Modified: Wed, 16 Oct 2024 20:32:28 GMT  
		Size: 47.8 MB (47792484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bff41a9401eb32dd2d4bf2a5c28a998c7441aa5bfd75a2daeaee42b622735112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47f184a361b5cad4153a0928d88fc44250fa808600630daf7f7745f90197c2e1`

```dockerfile
```

-	Layers:
	-	`sha256:92996deea54712edc641dc916bf8cc24732e77abaf4983ccd37952942ca17a5d`  
		Last Modified: Wed, 16 Oct 2024 20:32:26 GMT  
		Size: 2.3 MB (2296125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7aa239411750d93633b78b0ad5a52c899cc89db91bcea3fd38dcbb35fe0a1e7b`  
		Last Modified: Wed, 16 Oct 2024 20:32:26 GMT  
		Size: 8.6 KB (8643 bytes)  
		MIME: application/vnd.in-toto+json
